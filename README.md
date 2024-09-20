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
```

## Getting Started

## References
- [Flutter: Build and Deploy Android apps using GitHub Actions](https://tbrgroup.software/flutter-build-and-deploy-android-apps-using-github-actions/)
