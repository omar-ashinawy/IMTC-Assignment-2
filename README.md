# UBC Courtyard VR Experience

A virtual reality exploration of the UBC-O (University of British Columbia - Okanagan) courtyard environment, featuring interactive locomotion and university-branded visual elements.

---

## 📋 Project Overview

This VR experience allows users to freely explore the UBC-O courtyard using intuitive VR interactions. The project leverages Unity's XR Interaction Toolkit to provide a comfortable and immersive virtual environment with UBC-themed customizations.

---

## ✨ Key Features

### 1. 🚀 Teleportation System
- **Strategically Placed Teleportation Areas**: Multiple teleport points positioned throughout the courtyard enable smooth navigation across the entire environment
- **Coverage**: Teleportation areas are distributed to provide access to all major courtyard locations including:
  - Main pathways
  - Building entrances
  - Courtyard center
  - Viewing areas
  - Key landmarks
- **Intuitive Controls**: Activate teleportation via controller input and aim at any teleport area to instantly travel

### 2. 🎨 UBC-Branded Visual Design
- **Custom Color Scheme**: All interactive elements feature official **UBC Blue** (`RGB(0, 33, 69)`) branding
  - Teleportation areas highlighted in UBC Blue
  - Climbing zones marked with UBC Blue indicators
  - Visual consistency throughout the experience
- **Enhanced Visibility**: Color-coded interaction zones make it immediately clear which areas are interactive
- **Professional Aesthetic**: University branding creates a cohesive, polished experience

### 3. 💬 Welcome Interface
- **Floating UI Message**: A world-space canvas displays a welcoming message to orient new users
- **User Onboarding**: Provides context and instructions upon entering the VR experience
- **Non-Intrusive Design**: Positioned to inform without blocking the view of the courtyard

---

## 🎮 Controls

### VR Controller Layout

| Action | Input |
|--------|-------|
| **Teleport** | Aim + Release |
| **Grab Objects** | Grip Button |
| **Activate/Use** | Trigger Button |
| **Climb** | Grip Button (when near climbing surface) |


---

## 🗺️ Scene Layout

```
UBCO_Courtyard_Scene
├── Directional Light
├── Environment
│   ├── snil?tn
│   ├── UBCOcourtyard
│   ├── Deers
│   ├── Info
│   └── Ground
├── XR Interaction Manager
├── XR Origin (XR Rig)
│   ├── Camera Offset
│   │   ├── Main Camera
│   │   ├── Gaze Interactor
│   │   ├── Gaze Stabilized
│   │   ├── Left Controller
│   │   ├── Left Controller Teleport Stabilized Origin
│   │   ├── Right Controller
│   │   └── Right Controller Teleport Stabilized Origin
│   └── Locomotion
├── Far Grab Samples
├── Teleportation Environment
├── UI Sample
├── Poke Interactions Sample
├── Interactables Sample
└── Climb Sample
```

---

## 🚀 Setup Instructions

### Running the Experience

1. **Open the Project**
   ```
   File → Open Project → Select UBC_Courtyard_VR folder
   ```

2. **Load the Scene**
   ```
   Navigate to: Assets/Scenes/UBCO_Courtyard_Scene.unity
   Double-click to open
   ```
### First-Time Setup

If this is your first time opening the project:

1. **Configure XR Settings**
   - Edit → Project Settings → XR Plug-in Management
   - Enable your target platform (Quest/OpenXR/etc.)

2. **Verify Input Actions**
   - Check that XRI Default Input Actions are enabled
   - Located in: Assets/Samples/XR Interaction Toolkit/[version]/Starter Assets/

3. **Build Settings**
   - Ensure the courtyard scene is added to "Scenes in Build"
   - Set platform to Android (Quest) or Windows (PC VR)

---

## 🎨 Customization Details

### UBC Blue Color Values
```
Standard RGB: RGB(0, 33, 69)
Hex Code: #002145
```

### Modified Elements
- **Climbing Surface Indicators**: UBC Blue highlight overlay
- **Welcome UI**: Canvas positioned at eye level with UBC branding

### Material Assignments
All interactive zones use materials located in:
```
Assets/Materials/UBC_Branded/
├── UBC_Blue_Teleport.mat
├── UBC_Blue_Climb.mat
└── UBC_Blue_UI.mat
```

---

### Interaction Layers
```
Layer Configuration:
- Layer 8: Teleport
- Layer 9: Interactable
- Layer 10: Climbable
- Layer 11: UI
```

