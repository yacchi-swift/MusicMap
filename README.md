# MusicMap 🎵📍

**Your music listening journey, mapped and private.**

MusicMap is an iOS app that lets you log the songs you're listening to along with your location, creating a beautiful visual diary of your musical experiences across different places and times.

![App Icon](README_logo.png)

## 🔒 Privacy First

**Your data belongs to you. Period.**

- ✅ **100% Local Storage** - All your music logs are stored exclusively on your device using UserDefaults
- ✅ **No External Servers** - Zero data transmission to any external servers or services
- ✅ **No iCloud Sync** - Your data never leaves your device, not even to your own iCloud
- ✅ **No Third-Party Libraries** - Built entirely with Apple's native frameworks
- ✅ **No Analytics or Tracking** - We don't collect, analyze, or share any of your information

**I will never sell your data.** This app is built with respect for your privacy and your right to keep your listening habits personal.

## ✨ Features

### 📱 Core Functionality
- **Instant Logging** - Capture your current song and location with a single tap
- **Smart Music Integration** - Works with Apple Music's system player
- **Beautiful Maps** - See all your logged locations on an interactive map
- **Time-Based Colors** - Markers change color based on the sun's position at that time and place
- **Solar Time Tracking** - Accurate sunrise/sunset calculations for each location

### 🎨 Visual Design
- **Solar Color Coding** - Each log is colored based on actual sunrise/sunset times:
  - 🌃 Deep Night - Deep blue
  - 🌅 Before Sunrise - Lightening blue
  - 🌄 Sunrise - Blue to orange transition
  - ☀️ Day - Bright yellow-orange
  - 🌆 Before Sunset - Deepening orange
  - 🌇 Sunset - Orange to blue transition
  - 🌙 Night - Transitioning to deep blue

- **Location-Aware Solar Times** - Colors reflect the actual light conditions at that specific location and time
- **Smart Marker Filtering** - Prevents overlapping markers on the map (minimum 5m spacing)

### 🗺️ Views
- **List View** - Chronological list of all your music logs with swipe-to-delete
- **Map View** - Interactive map showing all your logged locations
- **Detail View** - Full information for each log with ability to replay the song
- **Solar Time Legend** - Helpful guide explaining the color-coding system

## 📋 Requirements

- iOS 18.0 or later
- Location Services permission
- Apple Music (for playing songs)

## 🛠️ Technical Details

Built with modern iOS development practices:
- **SwiftUI** - Modern declarative UI framework
- **@Observable** - New iOS 17+ observation framework
- **CoreLocation** - Precise location tracking
- **MapKit** - Beautiful native maps
- **MediaPlayer** - Apple Music integration

### Architecture
- `LocationLogger.swift` - Core location and data management
- `MusicLog.swift` - Data model for music logs
- `ContentView.swift` - Main tab view and list interface
- `MapView.swift` - Interactive map with solar time colors
- `DetailView.swift` - Individual log details and playback
- `MusicMapApp.swift` - App entry point

## 🎯 How It Works

1. **Play Music** - Start playing a song in Apple Music
2. **Log Location** - Tap the "Log Current Location" button
3. **View on Map** - Switch to the Map tab to see your logged locations
4. **Explore Details** - Tap any marker or list item to see full details
5. **Replay Songs** - Tap the play button in detail view to replay songs from your library

## 🔐 Permissions

MusicMap requires:
- **Location** (When In Use) - To log your current location
- **Media Library** (Optional) - To replay songs from your Apple Music library

All permissions are requested only when needed and clearly explained.

## 📊 Data Storage

All data is stored locally using:
- **UserDefaults** - Simple, secure, local-only storage
- **JSON Encoding** - Efficient data serialization
- **No Cloud Sync** - Your data stays on your device

Data includes:
- Song name and artist
- Location coordinates (latitude/longitude)
- Timestamp
- Unique identifier

## 🗺️ Solar Time Calculation

The app calculates precise sunrise and sunset times for each logged location using:
- Solar declination based on day of year
- Hour angle calculations
- Latitude-based adjustments
- Timezone conversions
- Smooth color transitions during twilight periods

This ensures that colors accurately represent whether it was light or dark at that specific place and time.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 🙏 Acknowledgments

Built with Apple's native frameworks:
- SwiftUI
- CoreLocation
- MapKit
- MediaPlayer

## ⚠️ Disclaimer

This app accesses Apple Music's system player. It does not have access to Apple Music's streaming catalog directly - songs must be in your library or you can use the app to open Apple Music to search for songs.

---

**Made with ❤️ for music lovers who value their privacy**

*Your listening habits are personal. This app ensures they stay that way.*
