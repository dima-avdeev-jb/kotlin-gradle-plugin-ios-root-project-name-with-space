### Issue with Kotlin Gradle plugin for iOS

When in settings.gradle:
```Kotlin
rootProject.name = "Contains Space"
```
error occurs:
```bash
e: Could not find "Contains" in [/Users/dim/Desktop/github/dima-avdeev-jb/kotlin-gradle-plugin-ios-root-project-name-with-space, /Users/dim/.konan/klib, /Users/dim/.konan/kotlin-native-prebuilt-macos-aarch64-1.8.20/klib/common, /Users/dim/.konan/kotlin-native-prebuilt-macos-aarch64-1.8.20/klib/platform/ios_simulator_arm64]
```

All fine with: `rootProject.name = "NoSpace"`

To reproduce:
`./gradlew :module1:linkPodDebugFrameworkIosSimulatorArm64`
