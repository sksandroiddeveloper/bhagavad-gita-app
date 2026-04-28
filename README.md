<div align="center">

<!-- Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=FF6B1A&height=200&section=header&text=श्रीमद्भगवद्गीता&fontSize=52&fontColor=FFF5E1&fontAlignY=38&desc=Bhagavad%20Gita%20App&descAlignY=58&descSize=22&descColor=FFB730" width="100%"/>

<br/>

<p>
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white"/>
  <img src="https://img.shields.io/badge/Platform-Android%20%7C%20Web-FF6B1A?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-FFB730?style=for-the-badge"/>
</p>

<p>
  <img src="https://img.shields.io/github/stars/sksandroiddeveloper/bhagavad-gita-app?style=social"/>
  <img src="https://img.shields.io/github/forks/sksandroiddeveloper/bhagavad-gita-app?style=social"/>
</p>

<br/>

> *"यदा यदा हि धर्मस्य ग्लानिर्भवति भारत।*  
> *अभ्युत्थानमधर्मस्य तदात्मानं सृजाम्यहम्॥"*  
> — **Bhagavad Gita, Chapter 4, Verse 7**

<br/>

**A beautifully designed Flutter app to read all 700 verses of the Bhagavad Gita — with explanations in both Hindi and English.**

<br/>

</div>

---

## ✨ Features

| Feature | Description |
|---|---|
| 📖 **18 Chapters** | Complete chapter index with verse counts and yoga names |
| 🕉️ **700 Verses** | Every shlok in original Sanskrit (Devanagari script) |
| 🔤 **Transliteration** | Roman-script phonetic guide for each verse |
| 🇮🇳 **Hindi Explanation** | Translation & commentary by Swami Tejomayananda & Swami Ramsukhdas |
| 🇬🇧 **English Explanation** | Translation & commentary by Swami Sivananda & Shri Purohit Swami |
| 🎚️ **Verse Slider** | Jump instantly to any verse within a chapter |
| 🔢 **Verse Grid Picker** | Bottom sheet grid to select any verse number |
| ✨ **Smooth Animations** | Powered by `flutter_animate` — staggered reveals, shimmer loaders |
| 📱 **Cross Platform** | Runs on Android & Flutter Web (Chrome) |

---

## 📸 Screenshots

<div align="center">

| Splash Screen | Home — Chapters | Shlok Reader |
|:---:|:---:|:---:|
| Animated OM intro | 18-chapter gradient grid | Sanskrit + dual-language tabs |

</div>

> *Deep saffron & sacred-night dark theme with authentic Devanagari typography.*

---

## 🏗️ Project Structure

```
gita_app/
├── lib/
│   ├── main.dart                   # App entry point
│   ├── app_theme.dart              # Colors, gradients, fonts, ThemeData
│   ├── models/
│   │   └── slok_model.dart         # SlokModel & ChapterModel
│   ├── services/
│   │   └── gita_api_service.dart   # REST API calls
│   ├── screens/
│   │   ├── splash_screen.dart      # Animated OM splash
│   │   ├── home_screen.dart        # Chapter grid
│   │   └── slok_detail_screen.dart # Verse reader
│   └── widgets/
│       ├── explanation_card.dart   # Expandable Hindi/English card
│       └── language_tab.dart       # Language switcher tab
├── web/
│   └── index.html                  # Flutter web entry
├── android/
│   └── app/src/main/
│       └── AndroidManifest.xml     # Internet permission
└── pubspec.yaml
```

---

## 🌐 API

This app uses the free & open-source **[Vedic Scriptures API](https://vedicscriptures.github.io)**:

```
GET https://vedicscriptures.github.io/slok/{chapter}/{verse}
GET https://vedicscriptures.github.io/chapters
GET https://vedicscriptures.github.io/chapter/{chapter}
```

**Example response for `/slok/1/1`:**
```json
{
  "chapter": 1,
  "verse": 1,
  "slok": "धृतराष्ट्र उवाच | धर्मक्षेत्रे कुरुक्षेत्रे...",
  "transliteration": "dhṛtarāṣṭra uvāca...",
  "tej": { "ht": "हिन्दी अनुवाद..." },
  "siva": { "et": "English translation..." }
}
```

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK `>=3.0.0` → [Install Flutter](https://flutter.dev/docs/get-started/install)
- Android Studio / VS Code
- Chrome (for web)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/sksandroiddeveloper/bhagavad-gita-app.git
cd bhagavad-gita-app

# 2. Install dependencies
flutter pub get

# 3. Run on Flutter Web
flutter run -d chrome

# 4. Run on Android Emulator
flutter run -d emulator-5554

# 5. Build release APK
flutter build apk --release

# 6. Build for Web
flutter build web --release
```

---

## 📦 Dependencies

```yaml
dependencies:
  flutter_animate: ^4.3.0      # Animations & transitions
  google_fonts: ^6.1.0         # Playfair Display, Crimson Text, Cinzel, Noto Serif Devanagari
  http: ^1.1.0                 # API calls
  shimmer: ^3.0.0              # Loading placeholders
  provider: ^6.1.1             # State management
  shared_preferences: ^2.2.2   # Local storage
  cached_network_image: ^3.3.0 # Image caching
```

---

## 🎨 Design System

<div align="center">

| Token | Value | Use |
|---|---|---|
| `background` | `#0D0A1A` | App background |
| `saffron` | `#FF6B1A` | Primary accent |
| `gold` | `#FFB730` | Secondary accent |
| `cream` | `#FFF5E1` | Sanskrit text |
| `card` | `#1E1838` | Card surfaces |
| Display font | **Playfair Display** | Headings |
| Sanskrit font | **Noto Serif Devanagari** | Shlok text |
| Body font | **Crimson Text** | Explanations |
| Label font | **Cinzel** | Badges & labels |

</div>

---

## 🛣️ Roadmap

- [ ] 🔖 Bookmarks — save favourite verses
- [ ] 🔍 Search across all 700 verses
- [ ] 🔊 Audio recitation for each shlok
- [ ] 🌙 Light theme option
- [ ] 📤 Share verse as image card
- [ ] 🌐 More languages (Bengali, Tamil, Telugu)
- [ ] 📴 Offline mode with local database

---

## 🤝 Contributing

Contributions are always welcome!

```bash
# Fork the repo, then:
git checkout -b feature/your-feature
git commit -m "Add: your feature description"
git push origin feature/your-feature
# Open a Pull Request
```

Please make sure to follow the existing code style and add comments where necessary.

---

## 📄 License

```
MIT License — Copyright (c) 2024 SK Android Developer

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software to deal in the Software without restriction.
```

---

## 🙏 Acknowledgements

- **[Vedic Scriptures API](https://github.com/vedicscriptures)** — for the open Bhagavad Gita dataset
- **Swami Sivananda**, **Swami Tejomayananda**, **Shri Purohit Swami**, **Swami Ramsukhdas** — for their timeless commentaries
- **Flutter & Dart** teams at Google

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=FF6B1A&height=120&section=footer" width="100%"/>

*Made with ❤️ and devotion · ॥ हरे कृष्ण ॥*

**[⭐ Star this repo](https://github.com/sksandroiddeveloper/bhagavad-gita-app) if you found it useful!**

</div>
