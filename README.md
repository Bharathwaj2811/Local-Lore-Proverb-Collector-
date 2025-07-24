# 📚 Local Lore & Proverb Collector

A beautiful, multilingual web application for collecting and preserving cultural proverbs, sayings, and folklore from around the world. Built with React, TypeScript, and Tailwind CSS.

![Local Lore Collector](https://images.pexels.com/photos/1370298/pexels-photo-1370298.jpeg?auto=compress&cs=tinysrgb&w=1200)

## ✨ Features

### 🌍 Core Functionality
- **Multilingual Support**: Full Unicode support for proverbs in any language
- **Offline-First**: All data stored locally in browser for privacy and offline access
- **Rich Metadata**: Capture contributor, region/origin, and meaning alongside each proverb
- **Smart Search**: Search across proverbs, languages, contributors, and meanings
- **Language Filtering**: Filter collection by specific languages
- **Export Options**: Download your collection as JSON or CSV

### 🎨 Design & UX
- **Modern Interface**: Clean, card-based design with smooth animations
- **Responsive Layout**: Optimized for mobile, tablet, and desktop
- **Cultural Aesthetics**: Warm color palette inspired by traditional storytelling
- **Accessibility**: High contrast ratios and keyboard navigation support
- **Real-time Stats**: Track collection growth with live statistics

### 🔧 Technical Features
- **TypeScript**: Full type safety throughout the application
- **Local Storage**: Persistent data without external dependencies
- **Component Architecture**: Modular, reusable React components
- **Performance Optimized**: Lazy loading and efficient rendering
- **Browser Compatible**: Works across all modern browsers

## 🚀 Getting Started

### Prerequisites
- Node.js 16+ 
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/local-lore-collector.git
   cd local-lore-collector
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:5173` to start collecting proverbs!

### Build for Production
```bash
npm run build
npm run preview
```

## 📖 Usage Guide

### Adding Proverbs

1. **Enter the Proverb**: Type or paste the proverb in its original language
2. **Select Language**: Choose from 25+ supported languages including:
   - Telugu (తెలుగు)
   - Hindi (हिन्दी) 
   - Tamil (தமிழ்)
   - Arabic (العربية)
   - Chinese (中文)
   - And many more...

3. **Add Context** (Optional):
   - **Contributor**: Your name or leave anonymous
   - **Region/Origin**: Where the proverb comes from
   - **Meaning**: Explanation of the proverb's significance

4. **Submit**: Click "Add to Collection" to save

### Managing Your Collection

- **Search**: Use the search bar to find specific proverbs or filter by any text
- **Filter by Language**: Use the dropdown to show only proverbs from specific languages
- **View Stats**: Monitor your collection growth with real-time statistics
- **Export Data**: Download your entire collection as JSON or CSV for backup

### Data Export Formats

**JSON Export Example:**
```json
[
  {
    "id": "uuid-here",
    "proverb": "చీకటిలో దీపం వెలిగించినట్లు",
    "language": "Telugu",
    "contributor": "Rama Devi",
    "region": "Andhra Pradesh",
    "meaning": "Like lighting a lamp in darkness - bringing hope in difficult times",
    "timestamp": "2025-01-24T15:30:00.000Z"
  }
]
```

**CSV Export**: Includes all fields in a spreadsheet-friendly format for analysis.

## 🏗️ Architecture

### Project Structure
```
src/
├── components/           # Reusable UI components
│   ├── Header.tsx       # Application header
│   ├── ProverbForm.tsx  # Form for adding new proverbs
│   ├── ProverbCard.tsx  # Individual proverb display
│   ├── ProverbList.tsx  # Collection view with search/filter
│   ├── ExportButtons.tsx # Data export functionality
│   └── Stats.tsx        # Collection statistics
├── data/
│   └── languages.ts     # Supported languages configuration
├── types/
│   └── index.ts         # TypeScript type definitions
├── utils/
│   └── storage.ts       # Local storage operations
└── App.tsx              # Main application component
```

### Key Components

**ProverbEntry Interface:**
```typescript
interface ProverbEntry {
  id: string;           // Unique identifier
  proverb: string;      // The actual proverb text
  language: string;     // Language name
  timestamp: string;    // ISO timestamp
  contributor?: string; // Optional contributor name
  region?: string;      // Optional region/origin
  meaning?: string;     // Optional explanation
}
```

**Storage System:**
- Uses browser's `localStorage` for persistence
- Automatic save on every addition
- JSON serialization with error handling
- Export functionality for data portability

## 🌐 Language Support

Currently supports 25+ languages including:

| Language | Native Name | Code |
|----------|-------------|------|
| English | English | en |
| Telugu | తెలుగు | te |
| Hindi | हिन्दी | hi |
| Tamil | தமிழ் | ta |
| Arabic | العربية | ar |
| Chinese | 中文 | zh |
| Japanese | 日本語 | ja |
| Spanish | Español | es |
| French | Français | fr |
| ... and many more | | |

### Adding New Languages

To add support for additional languages, update `src/data/languages.ts`:

```typescript
export const LANGUAGES: LanguageOption[] = [
  // ... existing languages
  { 
    code: 'new-lang', 
    name: 'Language Name', 
    nativeName: 'Native Script Name' 
  },
];
```

## 🎨 Customization

### Color Scheme
The application uses a warm, cultural color palette:
- **Primary**: Amber/Orange gradients (`from-amber-500 to-orange-600`)
- **Secondary**: Blue/Indigo (`from-blue-500 to-indigo-600`)
- **Accent**: Green, Purple, Red for various UI elements
- **Neutral**: Gray tones for text and backgrounds

### Styling
Built with Tailwind CSS for easy customization:
- Modify `tailwind.config.js` for theme changes
- Component styles use Tailwind utility classes
- Responsive breakpoints: `sm:`, `md:`, `lg:`, `xl:`

## 🔒 Privacy & Security

- **Local-Only Storage**: All data stays in your browser
- **No External Calls**: No data sent to external servers
- **GDPR Compliant**: Users control their own data
- **Offline Capable**: Works without internet connection
- **Export/Import**: Users can backup and restore their data

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### Bug Reports
1. Check existing issues first
2. Provide detailed reproduction steps
3. Include browser and OS information

### Feature Requests
1. Search existing feature requests
2. Clearly describe the proposed functionality
3. Explain the use case and benefits

### Code Contributions
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes following the existing code style
4. Add tests if applicable
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Use functional components with hooks
- Maintain responsive design principles
- Add proper error handling
- Update documentation for new features

## 📋 Roadmap

### Version 2.0 (Planned)
- [ ] **Audio Recording**: Record pronunciations of proverbs
- [ ] **Translation Integration**: Automatic translation using AI models
- [ ] **OCR Support**: Extract text from handwritten proverbs
- [ ] **Community Sharing**: Share collections with others
- [ ] **Advanced Search**: Full-text search with highlighting
- [ ] **Categories/Tags**: Organize proverbs by themes
- [ ] **Print Formatting**: Beautiful print layouts

### Future Enhancements
- [ ] **Mobile App**: React Native version
- [ ] **Collaboration**: Multi-user editing
- [ ] **Visualization**: Data charts and insights
- [ ] **Integration**: Import from external sources
- [ ] **AI Enhancement**: Meaning suggestions and cultural context

## 🐛 Known Issues

- Large collections (1000+ entries) may experience slight performance degradation
- Mobile keyboard may cover input fields on some devices
- Safari sometimes requires refresh for proper font rendering

## 🔧 Troubleshooting

### Common Issues

**Data Not Saving:**
- Check if browser has sufficient storage space
- Ensure JavaScript is enabled
- Try clearing browser cache and refreshing

**Display Issues:**
- Update to a modern browser version
- Disable browser extensions that might interfere
- Check if dark mode extensions are affecting styles

**Export Not Working:**
- Ensure pop-up blockers aren't preventing downloads
- Check browser download settings
- Try using a different browser

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Cultural Inspiration**: Traditional storytellers and wisdom keepers worldwide
- **Technical Stack**: React, TypeScript, Tailwind CSS, and Vite teams
- **Icons**: Lucide React for beautiful, consistent iconography
- **Community**: Contributors and users preserving cultural heritage

## 📧 Contact & Support

- **GitHub Issues**: [Report bugs or request features](https://github.com/your-username/local-lore-collector/issues)
- **Discussions**: [Community discussions](https://github.com/your-username/local-lore-collector/discussions)
- **Email**: your-email@example.com

---

**Start preserving cultural wisdom today!** 🌟

Every proverb collected helps preserve the rich tapestry of human wisdom for future generations. Whether it's a saying from your grandmother, a regional idiom, or traditional folklore, your contribution matters.

*"The tongue weighs practically nothing, but so few people can hold it."* - Anonymous