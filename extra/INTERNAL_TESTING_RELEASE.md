# Internal Testing Release Documentation for Fillup App

## Signed App Bundle (AAB) File Location

The signed Android App Bundle (AAB) file is located at:
```
build/app/outputs/bundle/release/app-release.aab
```

This file is generated after building the app with Flutter's release configuration.

## Building the Signed AAB

### Prerequisites
- Flutter SDK installed and configured
- Android SDK with necessary tools
- Keystore configured for release signing

### Build Steps

1. **Set up signing configuration** (if not already done):
   - Copy `android/key.properties.template` to `android/key.properties`
   - Fill in your keystore details:
     ```
     storeFile=path/to/your/keystore.jks
     storePassword=your_keystore_password
     keyAlias=fillup_key
     keyPassword=your_key_password
     ```

2. **Build the app bundle**:
   ```bash
   flutter build appbundle --release
   ```

3. **Verify the build**:
   - Check that `build/app/outputs/bundle/release/app-release.aab` exists
   - The file should be signed with your release keystore

## App Information for Google Play Console

- **App Name**: Fillup
- **Package Name**: com.fillup.fillup
- **Version**: 1.0.0+1
- **Description**: A fuel tracking app for monitoring fuel spends and efficiency
- **Minimum SDK**: As defined in `android/app/build.gradle` (flutter.minSdkVersion)
- **Target SDK**: 36

## Publishing Internal Testing Release

### Prerequisites
- Google Play Console account with developer access
- App created in Google Play Console (if not already)
- Signed AAB file ready
- List of tester email addresses (up to 100)

### Steps to Publish

1. **Access Google Play Console**:
   - Go to [play.google.com/console](https://play.google.com/console)
   - Select your app or create a new one

2. **Navigate to Internal Testing**:
   - In the left menu, go to **Testing > Internal testing**
   - Click **Create new release**

3. **Upload the AAB**:
   - Click **Upload** and select the `app-release.aab` file
   - Wait for Google to process the bundle

4. **Configure Release Details**:
   - **Release name**: e.g., "Internal Testing v1.0.0"
   - **Release notes**: Describe what's new or being tested
     ```
     Initial internal testing release of Fillup app.
     Features:
     - Fuel entry tracking
     - Vehicle management
     - Reports and analytics
     - Data export functionality
     ```

5. **Set Up Testers**:
   - Scroll to **Testers** section
   - Create a new tester list or use existing one
   - Add tester emails (comma-separated, up to 100)
   - Alternatively, use a Google Group for easier management

6. **Review and Rollout**:
   - Review all information
   - Click **Start rollout to internal testing**
   - Confirm the rollout

### Tester Management

- **Adding Testers**: Go to Internal testing > Testers tab
- **Email Notifications**: Google automatically sends opt-in links to testers
- **Tester Limits**: Up to 100 testers per list
- **Feedback**: Testers can provide feedback through the testing app

### Important Notes

- Internal testing releases are not visible on the Play Store
- Testers need to opt-in via the email link
- You can have multiple internal testing releases
- Changes to app details (description, screenshots) are not required for internal testing
- The app must be properly signed with a release keystore

### Troubleshooting

- **AAB upload fails**: Ensure the file is properly signed and not corrupted
- **Testers can't install**: Check that they've opted-in and have compatible devices
- **Build issues**: Run `flutter doctor` to check Flutter/Android setup

### Next Steps After Internal Testing

- Gather feedback from testers
- Fix any reported issues
- Prepare for beta testing or production release
- Update store listing with proper descriptions, screenshots, and privacy policy