



# Atomic Racers — C++ Arcade Racing Game
> Arcade racing game developed in C++ using custom engine architecture, Bullet Physics, FMOD spatial audio, and an ECS framework.

![Game Banner or Demo GIF](https://img.itch.zone/aW1nLzIyMDg5MTk5LnBuZw==/original/naZJlA.png) <!-- Añade un GIF o captura del juego aquí -->

## 🏎️ Core Technical Highlights
* **Physics & Vehicle Dynamics:** Custom vehicle controller and arcade physics integration using **Bullet Physics**.
* **Event Architecture:** Decoupled Event System built on the **Observer Pattern** (`EventDispatcher` / `EventManager`) integrated into an ECS framework.
* **Audio Engine:** Complete 3D spatial sound architecture using **FMOD**.
* **Memory & Performance:** Low-level C++ development with minimal external dependencies.

---

## 🛠️ Systems & Software Architecture

### 🚗 Arcade Vehicle Dynamics & Physics (Bullet Physics)
Handles vehicle input, raycast suspension, wheel friction, and rigid body dynamics.
* **Systems:** [`VehicleSystem.cpp`](src/system/VehicleSystem.hpp) | [`VehicleSystem.cpp`](src/system/VehicleSystem.cpp) | [`VehicleInputSystem.hpp`](src/system/VehicleInputSystem.hpp) | [`VehicleInputSystem.cpp`](src/system/VehicleInputSystem.cpp)
* **Components:** [`VehicleComponent.hpp`](src/components/VehicleComponent.hpp) | [`VehicleComponent.cpp`](src/components/VehicleComponent.cpp)

### 🔄 Event System (Observer Pattern)
Provides asynchronous and decoupled event dispatching across gameplay and engine subsystems via an Event Manager and Event Components.
* **Core Logic:** [`eventDispatcher.cpp`](src/events/eventDispatcher.cpp) | [`EventManager.hpp`](src/man/EventManager.hpp)
* **Systems & Components:** [`EventSystem.hpp`](src/system/EventSystem.hpp) | [`EventSystem.cpp`](src/system/EventSystem.cpp) | [`EventComponent.hpp`](src/components/EventComponent.hpp) | [`EventComponent.cpp`](src/components/EventComponent.hpp)
* **Types:** [`EventTypes.hpp`](src/util/EventTypes.hpp) | [`EventTypes.hpp`](src/components/EventComponent.cpp)


### 🔊 Audio Architecture (FMOD)
Abstracted audio engine interface managing real-time 3D spatial audio, background music, and sound effects.
* **Engine Core:** [`ISound.hpp`](src/engine/ISound.hpp) | [`FmodSoundEngine.cpp`](src/engine/FmodSoundEngine.cpp)
* **Systems & Components:** [`SoundSystem.hpp`](src/system/SoundSystem.hpp) | [`SoundSystem.cpp`](src/system/SoundSystem.cpp) | [`SoundComponent.hpp`](src/components/SoundComponent.hpp) | [`SoundComponent.cpp`](src/components/SoundComponent.cpp)

---

## 🚀 Key Learning Outcomes & Engine Design
* Implementation of custom **ECS (Entity Component System)** architecture.
* Real-time spatial audio processing integrated with gameplay physics states.
* Event-driven programming to minimize system dependencies and improve cache efficiency.

---

# empiric_team_abp24
[ABPCE24] Proyecto de Videojuegos del grupo Empiric Team de ABP 2024/25

## 💻 Tech Stack & Dependencies
* **Language:** C++17
* **Physics Engine:** Bullet Physics
* **Audio Engine:** FMOD Studio SDK
