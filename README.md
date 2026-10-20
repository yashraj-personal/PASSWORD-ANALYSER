# CyberGuard - Advanced Password Security Analyzer

A comprehensive password strength checker developed by **Parag Patel** that evaluates passwords based on length, complexity, character types, and common vulnerabilities.

## 👨‍💻 Developer
**Parag Patel** - Cyber Security Student & Python Developer  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/parag-patel-9593742a7)

## Features

### 🔍 Comprehensive Analysis
- **Length Validation**: Checks minimum and recommended password lengths
- **Character Type Analysis**: Evaluates presence of uppercase, lowercase, digits, and special characters
- **Complexity Scoring**: Detects patterns, repetitions, and common weaknesses
- **Entropy Calculation**: Measures password randomness and unpredictability
- **Pattern Detection**: Identifies common passwords, keyboard patterns, and sequential sequences

### 📊 Scoring System
The checker uses a 100-point scoring system based on:
- **Length (30 points)**: Minimum 8 chars, bonus for 12+ chars
- **Character Types (40 points)**: 10 points each for uppercase, lowercase, digits, special chars
- **Complexity (30 points)**: Pattern detection, repetition analysis
- **Security Patterns (20 points)**: Common password detection
- **Entropy (20 points)**: Character diversity and randomness

### 🎯 Strength Levels
- **Very Strong (80-100 points)**: Excellent security
- **Strong (60-79 points)**: Good security
- **Moderate (40-59 points)**: Acceptable but could be better
- **Weak (20-39 points)**: Poor security
- **Very Weak (0-19 points)**: Extremely vulnerable

## Usage

### 🌐 Web Version (Recommended)
Launch the web-based password checker with a beautiful UI:

```bash
python server.py
```
Then open http://localhost:8000 in your browser.

**Features:**
- Real-time password analysis as you type
- Visual strength meter with color coding
- Interactive analysis cards
- Responsive design for mobile/desktop
- Example passwords to try
- Modern, user-friendly interface

### 💻 Command Line Versions

**Interactive Mode:**
```bash
python password_checker.py
```

**Demo Mode:**
```bash
python demo.py
```

**Programmatic Usage:**
```python
from password_checker import PasswordStrengthChecker

checker = PasswordStrengthChecker()
result = checker.check_password_strength("MyP@ssw0rd123!")

print(f"Strength: {result['strength_level']}")
print(f"Score: {result['score']}/100")
print(f"Is Strong: {result['is_strong']}")
```

## Example Output

```
Password Analysis:
Strength Level: Strong
Score: 75/100
Length: 12 characters
Strong Password: Yes

Detailed Analysis:
  Length: PASS (30 points)
  Character_types: PASS (40 points)
  Complexity: PASS (25 points)
  Patterns: PASS (20 points)
  Entropy: PASS (20 points)

Suggestions for improvement:
  - Consider using at least 12 characters
  - Include special characters (!@#$%^&*)
```

## Security Features

### Pattern Detection
- **Common Passwords**: Checks against a list of frequently used passwords
- **Sequential Patterns**: Detects "123", "abc", "qwe" patterns
- **Keyboard Patterns**: Identifies "qwerty", "asdf" sequences
- **Character Substitutions**: Flags common substitutions like "0" for "O"

### Complexity Analysis
- **Repetition Detection**: Identifies excessive character repetition
- **Personal Information**: Warns against using personal data
- **Entropy Calculation**: Measures password unpredictability

## Requirements

- Python 3.6+
- No external dependencies (uses only standard library)

## Files

- `index.html`: Web-based password checker with modern UI
- `server.py`: HTTP server for local/network access
- `password_checker.py`: Command-line password checker implementation
- `demo.py`: Command-line demonstration script with examples
- `README.md`: This documentation

## Contributing

Feel free to enhance the checker by:
- Adding more pattern detection rules
- Improving entropy calculations
- Adding support for different languages
- Creating a GUI interface
- Adding password generation features

## License

This project is open source and available under the MIT License.
