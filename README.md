# Calculator Application

## Overview of the Project
A simple yet elegant desktop calculator application built with Python and Tkinter. This lightweight calculator provides a clean graphical user interface for performing basic arithmetic operations. Designed with simplicity in mind, it offers all essential calculation features without unnecessary complexity, making it perfect for quick mathematical computations in daily use.

## Features
 **Core Functionality**
- Basic arithmetic operations (Addition, Subtraction, Multiplication, Division)
- Decimal number support for precise calculations
- Real-time expression display
- Instant calculation results

 **User Interface**
- Clean and modern GUI design
- Large, easy-to-read display screen
- Responsive button grid layout
- Professional styling with consistent fonts and spacing

 **User Experience**
- Clear All (C) button to reset calculations
- Delete (DEL) button to remove last entered character
- Error handling for invalid operations
- Division by zero protection
- Continuous calculations (result becomes the starting point for next operation)

## Technologies/Tools Used
- **Python 3.x**: Core programming language
- **Tkinter**: Python's standard GUI library for creating the graphical interface
- **ttk (Themed Tkinter)**: Modern widget styling for enhanced appearance
- **Object-Oriented Programming**: Clean code architecture using classes

## Steps to Install & Run the Project

### Prerequisites
- Python 3.x installed on your system
- Tkinter (usually comes pre-installed with Python)

### Installation Steps

1. **Clone the repository or download the source code**
   ```bash
   git clone https://github.com/yourusername/calculator-app.git
   cd calculator-app
   ```
   OR download the `calculator.py` file directly

2. **Verify Python installation**
   ```bash
   python --version
   ```
   or
   ```bash
   python3 --version
   ```

3. **Run the application**
   ```bash
   python calculator.py
   ```
   or
   ```bash
   python3 calculator.py
   ```

### Alternative: Direct Execution
Simply double-click the `calculator.py` file if Python is properly configured on your system.

## Instructions for Testing

### Basic Operation Testing
1. **Number Input Test**
   - Click numbers 0-9 to verify they appear in the display
   - Test multi-digit numbers (e.g., click 1, 2, 3 to display "123")

2. **Arithmetic Operations**
   - **Addition**: Enter "5 + 3" and press "=" → Should display "8"
   - **Subtraction**: Enter "10 - 4" and press "=" → Should display "6"
   - **Multiplication**: Enter "6 * 7" and press "=" → Should display "42"
   - **Division**: Enter "15 / 3" and press "=" → Should display "5"

3. **Decimal Operations**
   - Enter "3.5 + 2.5" and press "=" → Should display "6.0"
   - Enter "10.5 / 2" and press "=" → Should display "5.25"

### Error Handling Testing
1. **Division by Zero**
   - Enter "5 / 0" and press "=" → Should display "Error"
   
2. **Invalid Expressions**
   - Enter "5 + + 3" and press "=" → Should display "Error"
   - Enter "* 5" and press "=" → Should display "Error"

### Control Button Testing
1. **Clear Function**
   - Enter any expression
   - Press "C" → Display should be empty
   
2. **Delete Function**
   - Enter "1234"
   - Press "DEL" → Should display "123"
   - Press "DEL" again → Should display "12"

### Chain Calculation Testing
1. Enter "5 + 3" and press "=" → Displays "8"
2. Enter "+ 2" and press "=" → Should display "10"
3. Verify that the previous result is used as the starting value

### Edge Cases
- Test very long expressions to verify display formatting
- Test multiple decimal points (should calculate based on valid Python syntax)
- Test negative results (e.g., "3 - 5" = "-2")
- Test operations with zero (e.g., "0 * 100" = "0")

## Troubleshooting
- If the application doesn't start, ensure Python is properly installed
- If GUI appears broken, verify Tkinter installation: `python -m tkinter`
- For font issues, the application will fall back to system defaults if Helvetica is unavailable
