Here's a detailed outline of the file structure and components for the VoiceClone app using Expo:

```
VoiceClone/
├── App.js
├── app.json
├── package.json
├── assets/
│   ├── images/
│   │   ├── logo.png
│   │   └── user-avatar.png
│   └── fonts/
│       ├── Roboto-Regular.ttf
│       └── Roboto-Bold.ttf
├── src/
│   ├── components/
│   │   ├── VoiceRecording/
│   │   │   ├── RecordButton.js
│   │   │   ├── RecordingList.js
│   │   │   └── RecordingItem.js
│   │   ├── VoiceCloning/
│   │   │   ├── CloningProgress.js
│   │   │   ├── CloningResult.js
│   │   │   └── VoicePreview.js
│   │   ├── BookLibrary/
│   │   │   ├── BookList.js
│   │   │   ├── BookItem.js
│   │   │   └── BookReader.js
│   │   ├── MessageRecording/
│   │   │   ├── MessageForm.js
│   │   │   ├── MessageList.js
│   │   │   └── MessageItem.js
│   │   ├── VoiceDiary/
│   │   │   ├── DiaryList.js
│   │   │   ├── DiaryItem.js
│   │   │   └── DiaryRecorder.js
│   │   ├── Playlists/
│   │   │   ├── PlaylistList.js
│   │   │   ├── PlaylistItem.js
│   │   │   └── PlaylistPlayer.js
│   │   ├── Sharing/
│   │   │   ├── ShareButton.js
│   │   │   └── SharingOptions.js
│   │   ├── UI/
│   │   │   ├── Button.js
│   │   │   ├── Input.js
│   │   │   ├── Text.js
│   │   │   └── Icon.js
│   │   └── index.js
│   ├── screens/
│   │   ├── HomeScreen.js
│   │   ├── ProfileScreen.js
│   │   ├── RecordingScreen.js
│   │   ├── CloningScreen.js
│   │   ├── BookLibraryScreen.js
│   │   ├── MessageRecordingScreen.js
│   │   ├── VoiceDiaryScreen.js
│   │   ├── PlaylistsScreen.js
│   │   └── SettingsScreen.js
│   ├── navigation/
│   │   └── AppNavigator.js
│   ├── services/
│   │   ├── authService.js
│   │   ├── voiceService.js
│   │   ├── storageService.js
│   │   └── sharingService.js
│   ├── config/
│   │   ├── firebase.js
│   │   └── google-cloud.js
│   ├── utils/
│   │   ├── colors.js
│   │   └── constants.js
│   └── App.js
├── .gitignore
├── .expo/
│   ├── packager-info.json
│   └── settings.json
└── README.md
```

Here's a breakdown of the main files and components:

- `App.js`: The entry point of the application where the main component is rendered.
- `app.json`: The configuration file for the Expo app.
- `package.json`: The file containing project dependencies and scripts.
- `assets/`: The directory for storing static assets such as images and fonts.
  - `images/`: Contains images used in the app (e.g., logo, user avatar).
  - `fonts/`: Contains custom fonts used in the app (e.g., Roboto).
- `src/`: The main directory for the application source code.
  - `components/`: Contains reusable components used throughout the app.
    - `VoiceRecording/`: Components related to voice recording functionality.
      - `RecordButton.js`: The button component for starting and stopping voice recording.
      - `RecordingList.js`: Renders the list of voice recordings.
      - `RecordingItem.js`: Renders an individual voice recording item.
    - `VoiceCloning/`: Components related to voice cloning functionality.
      - `CloningProgress.js`: Displays the progress of the voice cloning process.
      - `CloningResult.js`: Displays the result of the voice cloning process.
      - `VoicePreview.js`: Allows users to preview their cloned voice.
    - `BookLibrary/`: Components related to the book library feature.
      - `BookList.js`: Renders the list of books available for reading.
      - `BookItem.js`: Renders an individual book item.
      - `BookReader.js`: Provides the interface for reading a book using the cloned voice.
    - `MessageRecording/`: Components related to recording messages for loved ones.
      - `MessageForm.js`: The form component for recording a message.
      - `MessageList.js`: Renders the list of recorded messages.
      - `MessageItem.js`: Renders an individual message item.
    - `VoiceDiary/`: Components related to the voice diary feature.
      - `DiaryList.js`: Renders the list of voice diary entries.
      - `DiaryItem.js`: Renders an individual voice diary entry.
      - `DiaryRecorder.js`: Provides the interface for recording a voice diary entry.
    - `Playlists/`: Components related to the playlists feature.
      - `PlaylistList.js`: Renders the list of playlists.
      - `PlaylistItem.js`: Renders an individual playlist item.
      - `PlaylistPlayer.js`: Provides the interface for playing a playlist using the cloned voice.
    - `Sharing/`: Components related to sharing functionality.
      - `ShareButton.js`: The button component for sharing recordings.
      - `SharingOptions.js`: Provides options for sharing recordings (e.g., email, social media).
    - `UI/`: Contains reusable UI components.
      - `Button.js`: Renders a custom button component.
      - `Input.js`: Renders a custom input component.
      - `Text.js`: Renders a custom text component.
      - `Icon.js`: Renders custom icons used in the app.
    - `index.js`: Exports all the components for easy importing.
  - `screens/`: Contains the main screens of the app.
    - `HomeScreen.js`: The home screen of the app displaying the main features and options.
    - `ProfileScreen.js`: Allows users to view and edit their profile information.
    - `RecordingScreen.js`: Provides the interface for recording voice samples for cloning.
    - `CloningScreen.js`: Displays the progress and result of the voice cloning process.
    - `BookLibraryScreen.js`: Displays the list of books available for reading using the cloned voice.
    - `MessageRecordingScreen.js`: Allows users to record messages for their loved ones.
    - `VoiceDiaryScreen.js`: Provides the interface for recording and managing voice diary entries.
    - `PlaylistsScreen.js`: Displays the list of playlists and allows users to play them.
    - `SettingsScreen.js`: Allows users to adjust app settings and preferences.
  - `navigation/`: Contains the navigation setup for the app.
    - `AppNavigator.js`: Defines the main navigation flow of the app.
  - `services/`: Contains the services for interacting with external APIs and services.
    - `authService.js`: Handles user authentication and authorization.
    - `voiceService.js`: Interacts with the Google Cloud Text-to-Speech API for voice cloning.
    - `storageService.js`: Handles data storage and retrieval using Firebase Firestore.
    - `sharingService.js`: Handles sharing functionality for recordings.
  - `config/`: Contains configuration files for external services.
    - `firebase.js`: Configuration for Firebase services.
    - `google-cloud.js`: Configuration for Google Cloud Text-to-Speech API.
  - `utils/`: Contains utility functions and constants used throughout the app.
    - `colors.js`: Defines the color palette used in the app.
    - `constants.js`: Defines constant values used in the app.
  - `App.js`: The main component that sets up the app navigation and screens.
- `.gitignore`: Specifies files and directories to be ignored by Git.
- `.expo/`: Contains Expo-related configuration files.
- `README.md`: Provides information and instructions about the project.

To set up the project with Expo, follow these steps:

1. Install Expo CLI globally: `npm install -g expo-cli`
2. Initialize a new Expo project: `expo init VoiceClone`
3. Choose the "blank" template when prompted.
4. Navigate to the project directory: `cd VoiceClone`
5. Create the necessary directories and files as outlined in the file structure above.
6. Implement the components, screens, and navigation according to the app's requirements.
7. Set up Firebase and Google Cloud Text-to-Speech API and add the configuration files.
8. Implement user authentication, data storage, and sharing functionality.
9. Test the app using Expo's development server: `expo start`
10. Follow the Expo CLI instructions to run the app on an emulator/simulator or physical device.

Remember to handle edge cases, error scenarios, and loading states throughout the app. Implement proper state management using React hooks, context, or libraries like Redux or MobX.

Regularly test the app on different devices and platforms to ensure compatibility and a smooth user experience. Optimize performance by implementing lazy loading, caching, and efficient data fetching strategies.

Follow Expo's documentation and best practices for building and deploying your app. Consider implementing push notifications, analytics, and crash reporting to enhance the app's functionality and gather user insights.

Finally, ensure that the app follows accessibility guidelines and provides a user-friendly interface for all users, including those with disabilities.