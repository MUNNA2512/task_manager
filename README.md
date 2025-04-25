# Task Manager - Premium Edition

A beautiful task management app with a premium dark theme to help you organize your life efficiently.

## Download

You can find the latest release files in the `release-files` directory:

- **Debug APK**: [TaskManager-v1.0.0-debug.apk](release-files/TaskManager-v1.0.0-debug.apk) - For testing and development
- **Release AAB**: [TaskManager-v1.0.0.aab](release-files/TaskManager-v1.0.0.aab) - For Google Play Store submission

To install the debug APK directly on your Android device:
1. Download the APK file to your device
2. Enable "Install from unknown sources" in your device settings
3. Open the APK file and follow the installation instructions

## Screenshots

<div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
    <img src="screenshots/screenshot1.png" width="200" alt="Home Screen"/>
    <img src="screenshots/screenshot2.png" width="200" alt="Task Detail"/>
    <img src="screenshots/screenshot3.png" width="200" alt="Filter Tasks"/>
    <img src="screenshots/screenshot4.png" width="200" alt="Dark Theme"/>
</div>

## Features

- **Beautiful Premium Dark Theme** - Elegant purple and teal color scheme
- **Task Organization**
  - Create, edit, and delete tasks
  - Mark tasks as completed with a simple checkbox
  - Set priority levels (Low, Medium, High)
  - Categorize tasks (Personal, Work, Shopping)
  - Set due dates and reminders
- **Advanced Filtering**
  - Filter by status (All, Active, Completed)
  - Filter by priority (High, Medium, Low)
  - Filter by category (Personal, Work, Shopping)
  - Filter for today's tasks or overdue tasks
- **Smart Sorting**
  - Sort by date added
  - Sort by due date
  - Sort by priority
  - Sort alphabetically
- **Search Functionality** - Quickly find tasks with the search bar
- **Task Statistics** - View total, completed, and pending task counts
- **Export Feature** - Export your tasks for backup
- **Notifications** - Get reminders for tasks due soon

## Tech Stack

- **Language:** Java
- **Architecture:** Single Activity with RecyclerView
- **Database:** Room Persistence Library
- **UI Components:** Material Design Components
- **Notifications:** Android Notification System

## Setup Instructions

1. Clone the repository:
```
git clone https://github.com/MUNNA2512/task_manager.git
```

2. Open the project in Android Studio

3. Build the project:
```
./gradlew build
```

4. Run on a device or emulator:
```
./gradlew installDebug
```

## Creating a Release Build

To create your own signed release build:

1. Create a keystore file for signing:
```
keytool -genkey -v -keystore release-key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias release
```

2. Update the `app/build.gradle` file with your keystore information:
```gradle
signingConfigs {
    release {
        storeFile file('path/to/release-key.jks')
        storePassword 'your-store-password'
        keyAlias 'release'
        keyPassword 'your-key-password'
    }
}
```

3. Build the release APK:
```
./gradlew assembleRelease
```

4. Build the release App Bundle for Google Play:
```
./gradlew bundleRelease
```

## Publishing to Google Play Store

To publish your app to the Google Play Store:

1. Create a Google Play Developer account at [play.google.com/apps/publish](https://play.google.com/apps/publish)
2. Pay the one-time registration fee ($25 USD)
3. Create a new application and fill in all the required metadata
4. Upload your AAB file (TaskManager-v1.0.0.aab)
5. Add screenshots, feature graphic, and app descriptions
6. Set up pricing and distribution
7. Submit for review

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

Created by Munna Kumar - feel free to connect!

Instagram: [@coding_dev25](https://www.instagram.com/coding_dev25) 