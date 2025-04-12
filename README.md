# Bio Guardian App

The **Bio Guardian App** is an Android application built with Kotlin and Jetpack Compose. It follows a modular architecture and leverages modern Android development practices, including Material Design 3, Hilt for dependency injection, and Gradle for build management. This README is designed to be fully integrated in your IDE for a smooth development experience.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [How to Build and Run](#how-to-build-and-run)
- [Key Components](#key-components)
  - [Fonts](#fonts)
  - [Permissions](#permissions)
  - [Dependency Injection](#dependency-injection)
  - [ProGuard](#proguard)
- [Testing](#testing)
- [Dependency Management](#dependency-management)
- [Team Members](#team-members)
- [License](#license)
- [Contributing](#contributing)
- [Issues](#issues)
- [🛠️ Build](#-build)

---

## Overview

The **Bio Guardian App** combines modern UI development techniques with a robust Android architecture. It is carefully designed to be scalable, maintainable, and efficient, making use of industry-standard development practices.

## Features

- **Jetpack Compose**: Implements a modern declarative UI approach.
- **Material Design 3**: Ensures a cohesive, intuitive, and visually appealing design.
- **Dependency Injection (Hilt)**: Supports clean architecture and ease of testing.
- **Custom Fonts**: Integrates Montserrat and Roboto fonts to enhance readability.
- **Permissions Management**: Handles essential permissions like CAMERA and STORAGE.
- **ProGuard**: Configured for release builds to optimize and secure the app.

## Project Structure

```plaintext
.
├── .idea/                   # IDE-specific configuration files
├── app/                     # Main Android application module
│   ├── build.gradle.kts     # Gradle build script for the app module
│   ├── proguard-rules.pro   # ProGuard rules for release builds
│   └── src/                 # Source code for the app module
│       ├── androidTest/     # Instrumented tests
│       ├── main/            # Main application code
│       └── test/            # Unit tests
├── gradle/                  # Gradle wrapper and dependency versions
│   ├── libs.versions.toml   # Centralized dependency version management
│   └── wrapper/             # Gradle wrapper files
├── build.gradle.kts         # Root Gradle build script
├── gradle.properties        # Gradle configuration properties
├── settings.gradle.kts      # Gradle settings file
├── Readme.md                # Project documentation
```

## Prerequisites
- *Android Studio*: Latest stable version
- *JDK*: Version 17 or higher
- *Gradle*: Managed via the Gradle wrapper included in the repository

## How to Build and Run
1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd Bio-Guardian-App
   ```
   
2. Open the project in Android Studio.
3. Sync the Gradle files when prompted.
4. Run the application on an emulator or a physical device.

## From the Command Line
Alternatively, you can build the project using Gradle:
```bash
./gradlew assembleDebug
```

## Key Components
This section provides details on the main components of the project:

### Fonts
Custom fonts are defined in Type.kt:
- Montserrat: Available in Medium, SemiBold, and Bold weights.
- Roboto: Available in Regular weight.

Usage: The fonts are applied throughout the application to maintain visual consistency.

## Permissions
The application requests the following permissions as defined in AndroidManifest.xml:
- **INTERNET**
- **READ_EXTERNAL_STORAGE**
- **WRITE_EXTERNAL_STORAGE**
- **CAMERA**

Usage: These permissions enable features such as photo capture and accessing device storage.

## Dependency Injection
The app utilizes Hilt for dependency injection:
- Annotate the application class with @HiltAndroidApp.
- Define necessary modules to provide required dependencies.

Usage: Hilt simplifies dependency management and testing throughout the app.

## ProGuard
ProGuard configuration is provided in proguard-rules.pro:
- Optimizes bytecode.
- Obfuscates the code to protect against reverse-engineering.

Usage: Ensure ProGuard runs during release builds to improve performance and security.

## Testing
- **Unit Tests**: Located in app/src/test/java/.
- **Instrumented Tests**: Located in app/src/androidTest/java/.

## Run tests using the following Gradle commands:
```bash
./gradlew test          # Run unit tests
./gradlew connectedTest # Run instrumented tests
```

## Dependency Management
Dependencies are maintained centrally using the libs.versions.toml file located in the gradle/ directory, ensuring consistency across the project.

## Team Members
- Shubhansu Kumar Singh - 12104991
- Satyam Thakur - 12114830
- Rishabh Deo Singh - 12116007
- Joshita Pachar - 12116639

## License
This project is licensed under the MIT License. Please update this section if a different license applies.

## Contributing
We welcome contributions! To contribute:
1. **Fork the repository**.
2. **Create a new branch** for your feature or bugfix.
3. **Submit a pull request** with a detailed description of your changes.

## Issues
If you encounter any issues, please report them in the Issues section of this repository.

## 🛠️ Build
To build the project, use the following command in the project root directory:
``` bash
./gradlew assembleDebug
```
Alternatively, if you need to build specific modules (like the frontend or backend), navigate to the corresponding directory and run:
```bash
npm run build
```

