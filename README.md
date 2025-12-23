# 📊 Product Quote Builder

A professional, feature-rich Flutter application for creating, managing, and previewing product quotations with real-time calculations and beautiful UI.

![Flutter](https://img.shields.io/badge/Flutter-3.0+-02569B?style=for-the-badge&logo=flutter)
![Dart](https://img.shields.io/badge/Dart-3.0+-0175C2?style=for-the-badge&logo=dart)


## ✨ Features

### Core Functionality
- ✅ **Dynamic Line Items** - Add/remove multiple products or services
- 🧮 **Real-time Calculations** - Automatic subtotal, tax, and grand total computation
- 📱 **Responsive Design** - Adapts seamlessly to mobile, tablet, and desktop
- 🎨 **Beautiful UI** - Modern gradient design with smooth animations
- 📄 **Professional Preview** - Print-ready quote layout
- 💾 **Local Storage** - Save quotes for later (ready to implement)

### Advanced Features
- 🔄 **Tax Modes** - Tax-inclusive or tax-exclusive calculations
- 💰 **Multi-Currency** - Support for USD, EUR, GBP, INR, AUD
- 📊 **Status Tracking** - Draft, Sent, Accepted status management
- 🎯 **Form Validation** - Input validation and error handling
- 📈 **Per-item Calculations** - Individual discounts and tax rates
- 🖨️ **Export Ready** - Print and share functionality

## 📸 Screenshots

### Quote Builder Form
![Quote Form](screenshots/bill.jpg)

### Professional Preview
![Quote Preview](screenshots/quote_preview.png)

## 🚀 Getting Started

### Prerequisites

- **Flutter SDK**: 3.0 or higher
- **Dart SDK**: 3.0 or higher
- **IDE**: VS Code, Android Studio, or IntelliJ IDEA
- **Device**: iOS Simulator, Android Emulator, or Physical Device

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/quote_builder_app.git
   cd quote_builder_app
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   # For mobile/emulator
   flutter run
   
   # For web
   flutter run -d chrome
   
   # For specific device
   flutter run -d <device_id>
   ```

4. **Build for production**
   ```bash
   # Android
   flutter build apk --release
   
   # iOS
   flutter build ios --release
   
   # Web
   flutter build web
   ```

## 📦 Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  cupertino_icons: ^1.0.6
  intl: ^0.18.0              # Currency and date formatting

dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^3.0.0
```

## 🏗️ Project Structure

```
lib/
├── main.dart                    # Entry point
├── models/                      # Data models
├── screens/                     # UI screens
├── widgets/                     # Reusable widgets
├── utils/                       # Utilities
├── theme/                       # Theme config
└── enums/                       # Enumerations
```

See [ARCHITECTURE.md](docs/ARCHITECTURE.md) for detailed structure.

## 💡 Usage

### Creating a Quote

1. **Enter Client Information**
   - Client name (required)
   - Client address
   - Reference/Quote number

2. **Configure Settings**
   - Select tax mode (inclusive/exclusive)
   - Choose currency
   - Set quote status

3. **Add Line Items**
   - Click "Add Item" to add products/services
   - Enter product name, quantity, rate
   - Add optional discount and tax percentage
   - Remove items with the delete button

4. **Review Calculations**
   - View real-time item totals
   - Check subtotal, tax, and grand total

5. **Preview & Save**
   - Click "Preview Quote" for professional layout
   - Save or share the quote

### Formula Used

```
Item Total = ((Rate - Discount) × Quantity) + Tax
Tax Amount = Subtotal × (Tax% / 100)
Grand Total = Σ(All Item Totals)
```

## 🎨 Customization

### Colors & Gradients

Modify `lib/theme/app_colors.dart` and `app_gradients.dart`:

```dart
// Example gradient customization
static const primaryGradient = LinearGradient(
  colors: [Colors.blue.shade600, Colors.purple.shade600],
);
```

### Currency Support

Add new currencies in `lib/utils/currency_formatter.dart`:

```dart
case 'JPY':
  return '¥';
case 'CNY':
  return '¥';
```

### Business Logic

Modify calculation formulas in `lib/models/line_item.dart`:

```dart
double get itemTotal {
  // Your custom calculation logic
}
```

## 🧪 Testing

Run tests with:

```bash
# Run all tests
flutter test

# Run with coverage
flutter test --coverage

# Run specific test
flutter test test/models/line_item_test.dart
```

## 📱 Platform Support

| Platform | Status | Notes |
|----------|--------|-------|
| Android  | ✅ Supported | API 21+ |
| iOS      | ✅ Supported | iOS 12+ |
| Web      | ✅ Supported | Chrome, Firefox, Safari |
| Windows  | 🟡 Experimental | Requires testing |
| macOS    | 🟡 Experimental | Requires testing |
| Linux    | 🟡 Experimental | Requires testing |

## 🔧 Troubleshooting

### Common Issues

**Issue**: Overflow errors on small screens
```bash
Solution: The app uses responsive design with horizontal scrolling for tables
```

**Issue**: Dependencies not installing
```bash
flutter clean
flutter pub get
```

**Issue**: Hot reload not working
```bash
Press 'R' for hot restart instead of 'r' for hot reload
```

## 🛣️ Roadmap

- [ ] PDF Export functionality
- [ ] Email quote directly from app
- [ ] Cloud sync with Firebase
- [ ] Multiple templates
- [ ] Dark mode support
- [ ] Invoice conversion
- [ ] Payment tracking
- [ ] Client database
- [ ] Analytics dashboard
- [ ] Multi-language support

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct.

## 📝 Code Style

This project follows the official [Dart Style Guide](https://dart.dev/guides/language/effective-dart/style).

Run the linter:
```bash
flutter analyze
```

Format code:
```bash
dart format lib/

## 👨‍💻 Author

Alok Pandey
- GitHub: [@ap737147-stack](https://github.com/ap737147-stack)
- LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)
- Email: ap737147@gmail.com

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- Community plugins and packages
- Design inspiration from modern B2B tools
- Icons from [Flutter Icons](https://api.flutter.dev/flutter/material/Icons-class.html)

## 📞 Support

For support, email support@example.com or open an issue in the repository.

## ⭐ Show Your Support

Give a ⭐️ if this project helped you!

---

**Made with ❤️ using Flutter**
