# Blind-Tracking-Guide-BTG-
An AI-powered Android accessibility app that helps visually impaired users navigate their surroundings using voice assistance, object detection, pedestrian navigation, and emergency SOS features.
# Blind Tracking Guide (BTG) ♿

**An AI-powered Android assistant designed to support independent and safer navigation for visually impaired people.**

Blind Tracking Guide (BTG) is an Android application built with Kotlin and Jetpack Compose. It aims to help visually impaired users understand their surroundings, navigate pedestrian routes, interact with a voice assistant, and access safety-related features through a mobile device.

## ✨ Features

- **AI-Powered Object Detection** — Identify objects in the user's surroundings using on-device machine learning.
- **Voice Assistance** — Support hands-free interaction through voice commands and audio feedback.
- **Pedestrian Navigation** — Provide location-aware navigation and walking-route support.
- **Emergency SOS** — Support emergency events and configured safety contacts.
- **Live Location Sharing** — Enable location synchronization for caregiver awareness.
- **Nearby Places** — Help users discover nearby locations and points of interest.
- **Safe Zones and Geofencing** — Support location-based safety features.
- **Detection History** — Maintain records of previous detection events.
- **Local Data Storage** — Store application data using Room.
- **Cloud Integration** — Integrate remote services for authentication, synchronization, and real-time location-related data.

*Note: Feature availability depends on the device, permissions, backend configuration, network connectivity, and the current implementation.*

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Kotlin |
| UI Development | Jetpack Compose, Material 3 |
| Architecture | MVVM, Repository Pattern, Clean Architecture principles |
| Dependency Injection | Dagger Hilt |
| Local Database | Room, SQLite |
| Cloud Services | Firebase, Supabase-related integrations |
| AI and Computer Vision | TensorFlow Lite, MediaPipe, Google ML Kit |
| Networking | Retrofit, OkHttp, Kotlin Coroutines |
| Maps and Navigation | MapLibre, OpenStreetMap, GraphHopper integration |
| Background Tasks | WorkManager, Android foreground services |
| Build System | Gradle with Kotlin DSL |

## 🏗️ Project Structure

```text
app/src/main/java/com/blindtracking/guide/
├── ai/
│   ├── audio/
│   ├── live/
│   └── model/
├── data/
│   ├── local/
│   │   ├── dao/
│   │   ├── entity/
│   │   └── migration/
│   ├── remote/
│   ├── repository/
│   └── routing/
├── device/
├── di/
├── domain/
├── services/
└── ui/
    ├── camera/
    ├── emergency/
    ├── history/
    ├── navigation/
    ├── screens/
    └── theme/
```

## ⚙️ Prerequisites

Before building the project, install:

- Android Studio with a compatible Android SDK.
- JDK 17.
- Android SDK Platform 34.
- Android SDK Build Tools and platform tools.
- A physical Android device or emulator running Android 8.0 (API 26) or later.
- Required credentials and configuration for the cloud services and AI integrations you intend to use.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/blind-tracking-guide.git
cd blind-tracking-guide/bgt-main
```

Replace `YOUR_USERNAME` and the repository name with your actual GitHub details.

### 2. Configure local credentials

Configure the required services before building:

- Add your Firebase configuration through a locally maintained `google-services.json`.
- Supply your Gemini API key through a secure local configuration or the `GEMINI_API_KEY` environment variable.
- Configure any required Supabase, routing, or other service credentials according to the implementation.
- Keep signing keys, passwords, API secrets, and private configuration files out of version control.

For local development, the project reads `gemini.api.key` from `local.properties` or falls back to the `GEMINI_API_KEY` environment variable.

**Security:** A key included in an Android application can potentially be extracted. Production applications should use appropriate API restrictions and a secure backend where necessary.

### 3. Open in Android Studio

1. Open the `bgt-main` project directory.
2. Allow Gradle to synchronize dependencies.
3. Install any missing SDK components.
4. Connect an Android device or launch an emulator.

### 4. Build the application

On Windows:

```powershell
.\gradlew.bat assembleDebug
```

On macOS or Linux:

```bash
chmod +x gradlew
./gradlew assembleDebug
```

If the build succeeds, the debug APK is normally generated at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

### 5. Run and test

Launch the application from Android Studio and grant only the permissions required for the features you want to test, such as camera, microphone, location, and notifications.

Verify that the relevant backend services and API credentials are configured before testing cloud-dependent functionality.

## 🔐 Privacy and Safety

BTG may process camera input, audio, location information, and emergency-contact data to support its intended functionality.

- Request permissions transparently and only when needed.
- Protect API credentials and signing keys.
- Configure database access rules and authentication appropriately.
- Test emergency workflows and location sharing carefully.
- Do not rely on the application as the sole means of emergency communication or personal safety.

## 🗺️ Roadmap

Potential areas for further development include:

- Improving real-time object detection and spoken scene descriptions.
- Enhancing voice interaction and accessibility.
- Improving pedestrian route guidance and obstacle awareness.
- Strengthening caregiver synchronization and emergency workflows.
- Expanding automated testing and device compatibility.
- Improving privacy controls and secure credential management.

## 🤝 Contributing

Contributions, bug reports, and feature suggestions are welcome.

1. Fork this repository.
2. Create a feature branch.
3. Make and test your changes.
4. Commit your changes with a descriptive message.
5. Open a pull request explaining the changes.

## 📄 License

No license has been specified in this README. Add a suitable open-source license before inviting others to reuse, modify, or distribute the project.

## 👨‍💻 Author

**Rajakarthikeyan V**

GitHub: [YOUR_GITHUB_PROFILE](https://github.com/YOUR_USERNAME)

---

*Blind Tracking Guide — using mobile technology to support accessibility, independence, and safer navigation.*
