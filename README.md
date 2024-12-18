# Google Sign-In Integration with Firebase Authentication

This project demonstrates Google Sign-In integration using Firebase Authentication in an Android application with Jetpack Compose. It includes sign-in and sign-out functionality with proper UI handling.

## Features

- Google Sign-In using Firebase Authentication
- Sign-in and sign-out functionality
- Jetpack Compose UI

## Prerequisites

- Android Studio Ladybug | 2024.2.1 Patch 3
- Firebase project with `google-services.json` configured
- Google Play Services

## Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/Shriram2005/GoogleSignIn.git
    cd GoogleSignIn
    ```

2. Open the project in Android Studio.

3. Add `google-services.json` to the `app` directory.

4. Sync the project with Gradle files.

## Configuration

1. Add necessary permissions in `AndroidManifest.xml`:
    ```xml
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.GET_ACCOUNTS" />
    <uses-permission android:name="android.permission.USE_CREDENTIALS" />
    ```

2. Add metadata for Google Play Services in `AndroidManifest.xml`:
    ```xml
    <meta-data
        android:name="com.google.android.gms.version"
        android:value="@integer/google_play_services_version" />
    ```

3. Ensure the following dependencies are added in `app/build.gradle.kts`:
    ```kotlin
    dependencies {
        implementation(libs.firebase.auth)
        implementation(libs.play.services.auth)
        implementation(libs.androidx.credentials)
        implementation(libs.ui)
        implementation(libs.material3)
    }
    ```

## Usage

1. Initialize `GoogleAuthClient` in `MainActivity.kt`:
    ```kotlin
    val googleAuthClient = GoogleAuthClient(this)
    ```

2. Implement sign-in and sign-out logic in `GoogleAuthClient.kt`.

3. Update UI in `MainActivity.kt` to handle sign-in and sign-out actions.

## Running the Project

1. Build and run the project on an Android device or emulator.

2. Test the Google Sign-In functionality by clicking the "Sign In With Google" button.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
