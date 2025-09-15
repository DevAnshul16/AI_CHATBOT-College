# 🎓 GCET Connect - AI-Powered College Assistant

**An intelligent Android chatbot application designed specifically for Galgotias College of Engineering and Technology (GCET) students.**

[![Android](https://img.shields.io/badge/Platform-Android-green.svg?style=flat)](https://www.android.com/)
[![Kotlin](https://img.shields.io/badge/Language-Kotlin-purple.svg?style=flat)](https://kotlinlang.org/)
[![API](https://img.shields.io/badge/API-24%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=24)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-blue.svg?style=flat)](https://developer.android.com/jetpack/compose)

## 📱 Demo

🎥 **Working Demo**: [Watch the app in action](https://drive.google.com/file/d/1DoOvtGeavTUvZP_EJ0KnL3zcxUFVHwwT/view?usp=drive_link)

## ✨ Features

### 🧠 Smart AI Assistant
- **Powered by Google Gemini Pro API** for intelligent responses
- **College-specific knowledge base** with 100+ predefined queries
- **Context-aware responses** tailored for GCET students
- **Fallback to AI** for queries not in the knowledge base

### 🎨 Modern UI/UX
- **Built with Jetpack Compose** for native Android experience
- **Material Design 3** components and theming
- **Smooth animations** using Lottie and Compose animations
- **Interactive suggestion chips** for quick queries
- **Typing indicators** and loading animations
- **Professional splash screen** with college branding

### 💾 Data Management
- **Room Database** for local message persistence
- **Chat history** preservation across app sessions
- **MVVM Architecture** for clean code separation

### 🔒 Content Safety
- **Intelligent query filtering** to ensure appropriate responses
- **Educational focus** with professional tone
- **Restricted to college-related topics**

## 🏗️ Technical Architecture

### **Architecture Pattern**
- **MVVM (Model-View-ViewModel)** for separation of concerns
- **Repository Pattern** for data management
- **Dependency Injection** with manual injection

### **Tech Stack**
| Component | Technology |
|-----------|------------|
| **Language** | Kotlin |
| **UI Framework** | Jetpack Compose |
| **Architecture** | MVVM + Repository Pattern |
| **Database** | Room (SQLite) |
| **AI Integration** | Google Gemini Pro API |
| **Animations** | Lottie + Compose Animations |
| **Navigation** | Navigation Compose |
| **Async Operations** | Kotlin Coroutines |

### **Project Structure**
```
app/src/main/java/com/example/collegebot/
├── data/                     # Data layer
│   ├── ChatDatabase.kt      # Room database configuration
│   ├── MessageDao.kt        # Data access object
│   └── MessageEntity.kt     # Database entity
├── ui/theme/                 # UI theming
│   ├── Color.kt
│   ├── Theme.kt
│   └── Type.kt
├── ChatViewModel.kt          # Business logic
├── ChatPage.kt              # Main chat interface
├── SplashScreen.kt          # App splash screen
├── CustomQueries.kt         # Predefined Q&A database
├── Constants.kt             # Configuration constants
├── MessageModel.kt          # Message data model
└── MainActivity.kt          # Entry point
```

## 📋 Key Features in Detail

### 🎯 Smart Query Matching
- **Fuzzy string matching** algorithm for query recognition
- **Keyword-based similarity** scoring
- **Levenshtein distance** calculation for optimal matches
- **70%+ similarity threshold** for custom responses

### 📚 Comprehensive Knowledge Base
Covers essential student queries including:
- 📅 **Academic Calendar** - Semester dates, exam schedules
- 🏫 **Campus Information** - Department locations, facilities
- 📖 **Academic Resources** - Study materials, previous papers
- 🚌 **Transportation** - Bus services, routes
- 🏠 **Hostel Information** - Facilities, admission process
- 🎯 **Placements** - Training cell, company visits
- 📝 **Assignments** - Submission process, formats
- 🏃 **Sports & Clubs** - Activities, joining procedures

### 🎨 UI Components
- **Animated Text Input** with shimmering border effects
- **Message Bubbles** with user/bot differentiation
- **Suggestion Chips** for quick query access
- **Floating Animations** for enhanced visual appeal
- **Responsive Design** for various screen sizes

## 🚀 Getting Started

### Prerequisites
- **Android Studio** Arctic Fox (2020.3.1) or later
- **Kotlin** 1.8.0 or later
- **Android SDK** API level 24 (Android 7.0) or higher
- **Google Gemini API Key**

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/AI_CHATBOT-College.git
   cd AI_CHATBOT-College
   ```

2. **Open in Android Studio**
   - Import the project into Android Studio
   - Wait for Gradle sync to complete

3. **Configure API Key**
   - Open `app/src/main/java/com/example/collegebot/Constant.kt`
   - Replace the API key with your Google Gemini API key:
   ```kotlin
   object Constants {
       val apiKey = "YOUR_GEMINI_API_KEY_HERE"
   }
   ```

4. **Build and Run**
   - Connect your Android device or start an emulator
   - Click "Run" or use `Ctrl+R` to build and install

### 🔑 Getting Gemini API Key
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Sign in with your Google account
3. Create a new API key
4. Copy and paste it into the Constants file

## 📱 Usage Guide

### **Starting a Conversation**
1. Launch the app and enjoy the animated splash screen
2. On the welcome screen, either:
   - Type your question in the input field
   - Tap on suggested quick action chips
3. The chat interface will appear with your conversation

### **Interactive Features**
- **Quick Suggestions**: Tap the up/down arrow to show/hide suggestion chips
- **Typing Indicators**: See "Typing..." when the bot is processing
- **Message History**: Your conversations are saved locally
- **Back Navigation**: Return to welcome screen anytime

### **Sample Queries**
- "What are the college timings?"
- "Where is the CSE department?"
- "How to apply for hostel?"
- "Tell me about placement cell"
- "What clubs are available?"

## 🔧 Configuration

### **Customizing Responses**
Edit `CustomQueries.kt` to add/modify predefined responses:
```kotlin
val customQueries = mapOf(
    "Your question" to "Your custom response",
    // Add more Q&A pairs here
)
```

### **Theming**
Modify colors and typography in the `ui/theme/` package:
- `Color.kt` - Define color palette
- `Theme.kt` - Configure Material Design theme
- `Type.kt` - Set typography styles

## 🏢 College Integration

**Designed specifically for Galgotias College of Engineering and Technology (GCET)**
- Campus-specific information and locations
- Department details and faculty information
- Official procedures and contact details
- Academic calendar and examination schedules
- Transportation and hostel services

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### **Development Guidelines**
- Follow **Kotlin coding conventions**
- Use **meaningful commit messages**
- Add **comments** for complex logic
- **Test** thoroughly before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Developer

**Created with ❤️ for GCET students**

---



---

**Made with ❤️ using Android & Kotlin** | **Powered by Google Gemini AI**
