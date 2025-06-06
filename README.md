# Flash-Cards

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/username/flashcard-pro.svg)](https://github.com/username/flashcard-pro/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/username/flashcard-pro.svg)](https://github.com/username/flashcard-pro/network)
[![GitHub issues](https://img.shields.io/github/issues/username/flashcard-pro.svg)](https://github.com/username/flashcard-pro/issues)

> A modern, interactive flashcard application designed to enhance learning through spaced repetition and active recall techniques.

## 🚀 Features

- **Spaced Repetition Algorithm**: Optimizes review timing based on your performance
- **Multiple Study Modes**: Flashcards, quiz mode, and self-assessment
- **Deck Management**: Create, edit, and organize flashcard decks by subject
- **Progress Tracking**: Visual analytics and performance statistics
- **Import/Export**: Support for CSV, JSON, and Anki deck formats
- **Offline Support**: Study anywhere without an internet connection
- **Cross-Platform**: Available on web, mobile, and desktop

## 📋 Table of Contents

- [Installation](#installation)
- [Quick Start](#quick-start)
- [Usage](#usage)
- [Features](#features-in-detail)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)


![Flashcard Demo](./assets/demo.gif)

## 🛠️ Installation

### Prerequisites

- HTML CSS JS
- npm or yarn
- Git

### Local Development

```bash
# Clone the repository
git clone https://github.com/username/Flash-Cards.git

# Navigate to project directory
cd Flash-Cards

# Install dependencies
npm install

# Start development server
npm run dev
```

### Production Build

```bash
# Build for production
npm run build

# Start production server
npm start
```

## 🚀 Quick Start

### Creating Your First Deck

```javascript
// Example: Creating a new flashcard deck
const deck = {
  name: "Spanish Vocabulary",
  description: "Basic Spanish words and phrases",
  cards: [
    {
      front: "Hola",
      back: "Hello",
      tags: ["greetings", "basic"]
    },
    {
      front: "Gracias",
      back: "Thank you",
      tags: ["courtesy", "basic"]
    }
  ]
};

// Add deck to your collection
addDeck(deck);
```

### Starting a Study Session

```javascript
// Begin studying a deck
const studySession = new StudySession('spanish-vocabulary', {
  mode: 'spaced-repetition',
  maxCards: 20,
  shuffled: true
});

studySession.start();
```

## 📚 Usage

### Basic Operations

**Creating Flashcards**
1. Click "New Deck" to create a collection
2. Add cards with front/back content
3. Optionally add tags, images, or audio
4. Save your deck

**Studying**
1. Select a deck from your library
2. Choose study mode (flashcards, quiz, or mixed)
3. Review cards and rate your confidence
4. Track your progress over time

### Advanced Features

**Spaced Repetition**
The app uses a modified SM-2 algorithm to optimize review intervals:
- New cards: Reviewed frequently
- Easy cards: Longer intervals between reviews
- Difficult cards: More frequent review sessions

**Import/Export**
```bash
# Import from CSV
npm run import -- --file vocabulary.csv --deck "My Deck"

# Export to JSON
npm run export -- --deck "My Deck" --format json
```

## 🎨 Features in Detail

### Study Modes
- **Flashcard Mode**: Traditional front-to-back card review
- **Quiz Mode**: Multiple choice and fill-in-the-blank questions
- **Self-Assessment**: Rate your own knowledge confidence

### Analytics Dashboard
- Study streaks and session history
- Performance metrics by deck and tag
- Visual progress charts and heatmaps
- Retention rate analysis

### Customization
- Dark/light theme support
- Adjustable fonts and card layouts
- Custom study session parameters
- Personalized spaced repetition settings

## 🔧 Configuration

Create a `config.json` file in the root directory:

```json
{
  "database": {
    "type": "sqlite",
    "path": "./data/flashcards.db"
  },
  "spaced_repetition": {
    "algorithm": "sm2",
    "initial_interval": 1,
    "graduation_interval": 4
  },
  "ui": {
    "theme": "auto",
    "animations": true,
    "sounds": false
  }
}
```

## 📱 Supported Platforms

- **Web**: Modern browsers (Chrome, Firefox, Safari, Edge)
- **Mobile**: iOS 12+, Android 8+
- **Desktop**: Windows 10+, macOS 10.14+, Linux

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Setup

```bash
# Fork and clone the repository
git clone https://github.com/your-username/flashcard-pro.git

# Create a feature branch
git checkout -b feature/amazing-feature

# Make your changes and commit
git commit -m "Add amazing feature"

# Push and create a pull request
git push origin feature/amazing-feature
```

### Running Tests

```bash
# Run unit tests
npm test

# Run integration tests
npm run test:integration

# Run all tests with coverage
npm run test:coverage
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Anki](https://apps.ankiweb.net/) for spaced repetition inspiration
- [SuperMemo](https://supermemo.com/) for the SM-2 algorithm
- Our amazing community of contributors


Made with ❤️ by [Your Name](https://github.com/Sameer21)
