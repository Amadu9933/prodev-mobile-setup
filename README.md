# ProDev Mobile Setup

A comprehensive mobile development setup using React Native and Expo, configured for professional development workflows.

## 📱 Project Overview

This project is a React Native mobile application built with Expo SDK 53, featuring:

- TypeScript for type safety
- Expo Router for file-based navigation
- Tab-based navigation structure
- Modern React Native components and hooks
- Cross-platform development (iOS, Android, Web)

## 🚀 Quick Start

### Prerequisites

Before setting up this project, ensure you have the following installed:

1. **Node.js** (v18 or higher)

   - Download from [nodejs.org](https://nodejs.org/)
   - Verify installation: `node --version`

2. **npm or yarn** (comes with Node.js)

   - Verify installation: `npm --version`

3. **Expo CLI** (optional but recommended)

   ```bash
   npm install -g @expo/cli
   ```

4. **Mobile Development Tools** (choose based on your target platform):
   - **For Android**: Android Studio with Android SDK
   - **For iOS**: Xcode (macOS only)
   - **For testing**: Expo Go app on your mobile device

### Installation Steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/Amadu9933/prodev-mobile-setup.git
   cd prodev-mobile-setup/mobile-development-setup
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Start the development server**

   ```bash
   npm start
   # or
   npx expo start
   ```

4. **Run on specific platforms**

   ```bash
   # Android
   npm run android

   # iOS
   npm run ios

   # Web
   npm run web
   ```

## 📁 Project Structure

```
mobile-development-setup/
├── app/                     # Main application code (file-based routing)
│   ├── (tabs)/             # Tab navigation group
│   │   ├── _layout.tsx     # Tab layout configuration
│   │   ├── index.tsx       # Home tab
│   │   └── explore.tsx     # Explore tab
│   ├── _layout.tsx         # Root layout
│   └── +not-found.tsx     # 404 page
├── assets/                 # Static assets
│   ├── fonts/             # Custom fonts
│   └── images/            # Images and icons
├── components/            # Reusable UI components
│   ├── ui/               # Platform-specific UI components
│   └── *.tsx             # Shared components
├── constants/            # App constants and configuration
├── hooks/               # Custom React hooks
└── scripts/            # Build and utility scripts
```

## 🛠️ Development Workflow

### Available Scripts

- `npm start` - Start the Expo development server
- `npm run android` - Run on Android emulator/device
- `npm run ios` - Run on iOS simulator/device
- `npm run web` - Run in web browser
- `npm run lint` - Run ESLint code linting
- `npm run reset-project` - Reset to blank project structure

### Code Quality

The project includes:

- **TypeScript** for static type checking
- **ESLint** with Expo configuration for code linting
- **File-based routing** with Expo Router
- **Component organization** following React Native best practices

## 🔧 Setup Challenges & Solutions

### Common Setup Issues

#### 1. Node.js Version Compatibility

**Challenge**: Expo requires Node.js v18 or higher
**Solution**:

- Update Node.js to the latest LTS version
- Use `node --version` to verify your version
- Consider using nvm (Node Version Manager) for version management

#### 2. Metro Bundler Cache Issues

**Challenge**: Stale cache causing build errors
**Solution**:

```bash
# Clear Metro cache
npx expo start --clear

# Or clear npm cache
npm start -- --reset-cache
```

#### 3. Android Emulator Setup

**Challenge**: Android emulator not detected
**Solution**:

- Ensure Android Studio is properly installed
- Set up Android SDK and AVD (Android Virtual Device)
- Add Android SDK to your PATH environment variable
- Verify with `adb devices`

#### 4. iOS Simulator Issues (macOS only)

**Challenge**: iOS simulator not launching
**Solution**:

- Ensure Xcode is installed and updated
- Accept Xcode license: `sudo xcodebuild -license accept`
- Open Xcode and install additional components if prompted

#### 5. Dependency Installation Errors

**Challenge**: npm install fails with permission or network errors
**Solution**:

```bash
# Clear npm cache
npm cache clean --force

# Delete node_modules and reinstall
rm -rf node_modules package-lock.json
npm install

# Use yarn as alternative
npm install -g yarn
yarn install
```

### Platform-Specific Setup

#### Windows Development

- Install Android Studio for Android development
- Enable Windows Subsystem for Linux (WSL) for better terminal experience
- Use Windows PowerShell or Command Prompt for running commands

#### macOS Development

- Full iOS and Android development support
- Xcode for iOS development
- Android Studio for Android development

#### Linux Development

- Android development only (no iOS support)
- Ensure proper Android SDK configuration

## 📱 Testing Your Setup

### 1. Basic Functionality Test

Run the development server and verify:

- App loads without errors
- Navigation between tabs works
- Hot reload functions properly

### 2. Platform Testing

Test on different platforms:

- **Mobile**: Use Expo Go app to scan QR code
- **Android**: Test on emulator or physical device
- **iOS**: Test on simulator or physical device (macOS only)
- **Web**: Test in browser

### 3. Code Quality Check

```bash
# Run linting
npm run lint

# Check TypeScript compilation
npx tsc --noEmit
```

## 🐛 Troubleshooting

### Metro Bundler Issues

```bash
# Reset Metro cache
npx expo start --clear

# Kill all Metro processes
npx expo start --reset-cache
```

### Port Conflicts

```bash
# Start on different port
npx expo start --port 8082
```

### Package Issues

```bash
# Reinstall dependencies
rm -rf node_modules package-lock.json
npm install
```

### Expo CLI Issues

```bash
# Update Expo CLI
npm install -g @expo/cli@latest

# Check Expo version
npx expo --version
```

## 📚 Learning Resources

- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/)
- [Expo Router Guide](https://docs.expo.dev/router/introduction/)
- [TypeScript React Native Guide](https://reactnative.dev/docs/typescript)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Open a pull request

## 📝 Development Notes

### Setup Progress Tracking

- ✅ Initial Expo project setup
- ✅ TypeScript configuration
- ✅ ESLint configuration
- ✅ Tab navigation implementation
- ✅ Component structure organization
- ✅ Asset management setup

### Next Steps

- [ ] Add state management (Redux/Zustand)
- [ ] Implement API integration
- [ ] Add testing framework (Jest/React Native Testing Library)
- [ ] Set up CI/CD pipeline
- [ ] Add more UI components
- [ ] Implement push notifications

## 📄 License

This project is part of the ALX Professional Development program.

---

**Last Updated**: July 22, 2025
