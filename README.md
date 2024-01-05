# Tic Tac Toe

### a. Basic Information

**Project Name** - Tic Tac Toe

**Participants**: Ayush Bhardwaj (2021A7PS2634G, f20212634@goa.bits-pilani.ac.in) - Naman Agarwal (2021A7PS2668G, f20212668@goa.bits-pilani.ac.in)

### b. Overview of the Application and Its Current State

The application is designed to simulate a Tic Tac Toe game, supporting both single-player and two-player modes. It operates on a device and integrates with Firebase to store game data. Currently, there are no reported bugs in the app.

### c. Summary of Completed Tasks and Methods Used

**Task 1: Development of Sign-in Screen**
- Established connection with Firebase and enabled user data management.
- Enabled user login with email and password, with access to view active games in the database.

**Task 2: Single-Player Mode Implementation**
- Post-login, users can opt for a single-player game where the computer makes random moves after the player.

**Task 3: Two-Player Mode Development**
- Implemented a two-player game option post-login, creating new game entries in the database.
- Players interact with a tracked tic tac toe grid.

**Task 4: Enhancing Accessibility**
- Utilized TalkBack service for accessibility testing, ensuring audible guidance and screen element identification.
- Employed Accessibility Scanner, identifying issues like text contrast, image color contrast, and lack of speakable text. These were addressed, particularly by adjusting `android:textColor`.

### d. Testing Strategy and Outcomes

To host and run a Java Android app with Firebase authentication and a real-time database, follow these steps:

1. *Firebase Setup:*
    - Go to the [Firebase Console](https://console.firebase.google.com/).
    - Create a new Firebase project or select an existing one.
    - Add your Android app to the project:
        - Click on the Android icon to add an app.
        - Enter your app's package name (found in your Android project's `AndroidManifest.xml` file).
        - Download the `google-services.json` file and place it in your app module's directory (usually `app/`).

2. *Android Studio Configuration:*
    - Open your project in Android Studio.
    - Add Firebase SDK to your project:
        - Add the classpath in your project level `build.gradle`:
        ```
          gradle
          buildscript {
          dependencies {
          // Add this line
          classpath 'com.google.gms:google-services:4.3.10' // use the latest version
          }
          }

        ```
     - Add the apply plugin line at the bottom of your app-level `build.gradle`:
    ```
       gradle
       apply plugin: 'com.google.gms.google-services'
   ```

     - Add dependencies for Firebase Authentication and Realtime Database:
   ```
       gradle
       dependencies {
         // Add these lines
         implementation 'com.google.firebase:firebase-auth:21.0.1' // use the latest version
         implementation 'com.google.firebase:firebase-database:20.0.3' // use the latest version
       }
      ```



### e. Testing Strategy and Outcomes

- Adopted a test-driven development approach, focusing on edge cases.
- Conducted instrumented/UI tests and regularly updated test cases.
- Executed monkey stress-testing with 10000 iterations, confirming stability and handling of edge cases without crashes.

### f. Time Investment for Completion

- Coding, Testing, and Accessibility Fixing: 19 hours.
- Documentation Preparation: 1 hour.
- **Total Duration**: 20 hours.

### g. Assignment Difficulty Assessment

On a scale from 1 to 10, the assignment's difficulty is rated at **9.5**.