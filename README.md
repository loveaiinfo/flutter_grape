# grape

Create project
```bash
flutter create --org info.loveai --project-name grape --platforms android,ios flutter_grape
```

Create keystore
```bash
keytool -genkey -v -keystore grape.keystore -alias grape -keyalg RSA -keysize 2048 -validity 10240
base64 -i grape.keystore -o keystore-base64.txt
java -jar pepk.jar --keystore=grape.keystore --alias=grape --output=output.zip --include-cert --rsa-aes-encryption --encryption-key-path=encryption_public_key.pem
```

Build Android App
```bash
flutter build apk --debug --target-platform=android-arm64
flutter build ipa --no-codesign
```

## Getting Started

## References
- [Flutter: Build and Deploy Android apps using GitHub Actions](https://tbrgroup.software/flutter-build-and-deploy-android-apps-using-github-actions/)
- [Flutter CI/CD using GitHub Actions](https://blog.logrocket.com/flutter-ci-cd-using-github-actions/)
- [Deploy your Flutter app to Google Play with Github Actions](https://medium.com/lodgify-technology-blog/deploy-your-flutter-app-to-google-play-with-github-actions-f13a11c4492e)
- [Automating Flutter Builds with GitHub Actions: A Step-by-Step Guide](https://medium.com/@colonal/automating-flutter-builds-and-releases-with-github-actions-77ccf4a1ccdd)
- https://github.com/marketplace/actions/flutter-action
- [Build and release an iOS app](https://docs.flutter.dev/deployment/ios)
