# Screen Capture

<p align="center">
  <img src="doc/images/screencapture.jpg" alt="Screen Capture Application" width="800"/>
</p>

<p align="center">
  <strong>English</strong> | <a href="README_RU.md">Русский</a>
</p>

## 📝 Description

**Screen Capture** is a cross-platform Qt 6 application for real-time screen and window capture. The application demonstrates the use of Qt Multimedia API, including `QScreenCapture` and `QWindowCapture`, to create an interactive preview of captured content.

### ✨ Key Features

- 🖥️ **Screen Capture** — select and capture any available screen
- 🪟 **Window Capture** — capture specific application windows
- 📺 **Real-time Preview** — instant display of captured video
- 🎯 **Simple Interface** — intuitive controls with source selection and start/stop buttons
- 🔄 **Dynamic Updates** — refresh list of available windows
- ⚠️ **Error Handling** — informative messages when problems occur
- 📱 **Android Support** — special configuration for mobile devices

## 🛠️ Technologies

- **Qt 6** (Qt 5 also supported)
  - Qt Widgets — graphical interface
  - Qt Multimedia — video capture and processing
  - Qt Multimedia Widgets — video display widget
- **C++17** — language standard
- **CMake** — build system (qmake also supported)

## 📋 Requirements

### Minimum Requirements

- Qt 6.x or Qt 5.x (with Widgets, Multimedia, MultimediaWidgets modules)
- CMake 3.16 or higher (or qmake)
- C++17 compatible compiler
  - GCC 7+ / Clang 5+ / MSVC 2017+

### Platforms

- ✅ Windows 10/11
- ✅ macOS 10.14+
- ✅ Linux (X11/Wayland)
- ✅ Android (with additional permissions)
- ✅ iOS (with FFmpeg libraries)

## 🚀 Build and Installation

### Building with CMake

```bash
# Clone the repository
git clone https://github.com/sile350/QtScreenCapture.git
cd screencapture

# Create build directory
mkdir build
cd build

# Configure project
cmake ..

# Build
cmake --build .

# Run
./screencapture  # Linux/macOS
# or
screencapture.exe  # Windows
```

### Building with qmake

```bash
# Clone the repository
git clone https://github.com/sile350/QtScreenCapture.git
cd screencapture

# Configure and build
qmake screencapture.pro
make  # Linux/macOS
# or
nmake  # Windows with MSVC
# or
mingw32-make  # Windows with MinGW
```

### Building for Android

```bash
# Use Qt Creator with configured Android SDK/NDK
# or command line with qt-cmake
qt-cmake -DCMAKE_TOOLCHAIN_FILE=<path_to_android_toolchain> ..
cmake --build .
```

## 📖 Usage

1. **Launch the application** — a window with two panels will open
2. **Select capture source:**
   - Choose a screen from the **"Select screen to capture"** list
   - Or choose a window from the **"Select window to capture"** list
3. **Start capture** — click the "Start capture" button
4. **Preview** — captured video will appear in the right panel
5. **Stop capture** — click the "Stop capture" button

### 💡 Tips

- To refresh the window list, use the context menu (right-click) on the window list
- Switching between screen and window happens automatically when selecting
- If a window becomes unavailable, the application will offer to refresh the list

## 🏗️ Project Architecture

```
screencapture/
├── main.cpp                      # Application entry point
├── screencapturepreview.h/cpp    # Main UI and capture logic class
├── screenlistmodel.h/cpp         # Screen list model
├── windowlistmodel.h/cpp         # Window list model
├── CMakeLists.txt                # CMake configuration
├── screencapture.pro             # qmake configuration
├── android/
│   └── AndroidManifest.xml       # Android manifest
├── doc/
│   ├── images/                   # Application screenshots
│   └── src/                      # Qt documentation
└── Info.plist.in                 # macOS configuration

```

### Key Components

- **ScreenCapturePreview** — main widget managing interface and capture
- **QScreenCapture** — Qt class for screen capture
- **QWindowCapture** — Qt class for window capture
- **QMediaCaptureSession** — capture session linking source with output
- **QVideoWidget** — widget for displaying video stream
- **ScreenListModel** — model for displaying available screens
- **WindowListModel** — model for displaying available windows

## 🤝 Contributing

We welcome any contributions to the project! Please refer to [CONTRIBUTING.md](CONTRIBUTING.md) for detailed information.

### How to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is distributed under the BSD-3-Clause License. See [LICENSE](LICENSE) for details.

Parts of the code are based on official Qt examples and licensed under:
- BSD-3-Clause License
- Qt Commercial License

## 🙏 Acknowledgments

- [Qt Project](https://www.qt.io/) — for the excellent framework and examples
- Qt Community — for support and documentation

## 📞 Contacts

- **Issues:** [GitHub Issues](https://github.com/yourusername/screencapture/issues)
- **Discussions:** [GitHub Discussions](https://github.com/yourusername/screencapture/discussions)

## 🗺️ Roadmap

- [ ] Add saving captured video to file
- [ ] Audio capture support
- [ ] Quality and resolution settings
- [ ] Hotkeys for control
- [ ] Selected area capture
- [ ] Annotations and drawing over capture

---

<p align="center">
  Made with ❤️ using Qt
</p>
