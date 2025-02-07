# Audio-Network-Devices Unity Project

## Description
This Unity project focuses on the integration of audio processing, networking, and device-related features. The objective was to implement an interactive application incorporating:

- 3D audio
- Real-time sound acquisition
- Multiplayer functionality
- Webcam integration
- Extended Reality (XR) support

## Implemented Features

### Splash Screen
- A two-second stereoscopic splash screen enabled by XR mode.
- Displays the authors' images along with the Unity logo.

### Menu System
- A startup menu allowing users to select between Host and Client modes.
- Utilizes `NetworkManager` to establish and manage multiplayer connections.

### Player System
- **Character model:** \"Samurai Rojo\" (sourced from the Unity Asset Store).
- **Movement mechanics:** Implemented using `CharacterController`.
- **Sword interactions:** Used for object interactions within the scene.

### 3D Audio
- Sword sound effects triggered during attack actions.
- Moving sphere emits a 3D sound effect.
- **Game mechanics:**
  - Sphere disappears when hit, increasing the player's score.
  - The sphere stops respawning once a player reaches three points.

### Microphone - Real-Time Audio Capture
- A cube with a microphone texture representing audio recording functionality.
- Players can start or stop recording by pressing 'M' or interacting with the cube.
- Recorded audio is stored as `recording.wav`.

### Networking and Multiplayer
- Implemented using **NetCode for Unity**.
- Each player has a distinct avatar.
- Synchronization of game actions, player movements, and scoring.
- **Known issue:** Some elements, such as sphere disappearance, are not correctly updated for non-host players.

### Devices and Platforms
- **Mirror Wall:** Implements a reflection effect within the game environment.
- **Webcam Wall:** Displays a live feed from the local player's webcam.
  - **Limitation:** If two players are using the same device, only one can access the default webcam.
- **VR Mode:** Provides a simulated VR experience without requiring a headset, toggled using the 'V' key.
  - **Known issue:** XR mode may not function properly when multiple players are active.
  - **Solution:** The XR Interaction Toolkit and Device Simulator were utilized to test and refine VR functionality.

### Game Logic and Score Tracking
- **GameController:** Manages the game state, including score tracking and game-over conditions.
- **Sphere Respawn Mechanism:**
  - The sphere respawns at a new position upon being hit.
  - If a player reaches three points, the sphere ceases to respawn.
- **Known issue:**
  - Score tracking is accurate, but some object state updates are not fully synchronized for non-host players.

### Audio Controller
- A singleton `AudioController` manages audio playback.
- Plays a sound effect when the sphere is struck.
- Ensures centralized and consistent audio management across the application.

### Linux Executable
- The project includes a compiled **Linux-compatible executable** for deployment and testing.

## Installation and Configuration

### Requirements
- **Unity:** 2022.3.45f1
- **Modules:** XR Interaction Toolkit, NetCode for Unity
- **Optional:** Microphone and Webcam for enhanced functionality

### Running the Project
1. Clone the repository or extract the provided ZIP file.
2. Open the project in Unity.
3. Set the main scene as the Startup Scene.
4. Execute the game as either a Host or Client.

## Challenges and Issues

### Networking Synchronization
- Some objects do not update correctly for client players.
- The sphere disappearance logic is not fully synchronized for non-host players.

### Webcam Access
- Only one player per device can utilize the default webcam.

### VR Mode Compatibility
- XR mode may malfunction when multiple players are active simultaneously.
- Implemented the **XR Device Simulator** to facilitate testing without a physical headset.

## Conclusion
This project provided hands-on experience with advanced Unity functionalities, including audio processing, multiplayer networking, and device integration.

### Key challenges involved:
- Maintaining network synchronization
- Optimizing XR compatibility
- Managing webcam access for multiple users

Despite these complexities, the project successfully demonstrates fundamental **Audio/Network/Devices functionalities** and offers a foundation for further refinement and enhancement.

## Contact
- **Lorenzo Severini** - [GitHub](https://github.com/lorenzo-severini)
- **David Zipperstein** - [GitHub](https://github.com/david-z2812)

## License
This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.
