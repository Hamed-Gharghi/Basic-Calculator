# Basic Calculator Application

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyQt5](https://img.shields.io/badge/PyQt5-5.15.4-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Description

This is a basic calculator application built using PyQt5. It includes functionality for basic arithmetic operations and can be operated using both on-screen buttons and keyboard input. This project demonstrates a simple GUI application with event handling in Python. The UI now supports a dark theme for a modern look and reduced eye strain. An application icon is also included.

## Features

- Basic arithmetic operations: addition, subtraction, multiplication, and division.
- Clear and backspace functionalities.
- Keyboard input for calculator operations.
- User-friendly graphical interface with dark theme.
- Application icon for a polished look.

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/Basic-Calculator.git
   ```
2. Change to the project directory:
   ```sh
   cd Basic-Calculator
   ```
3. Install the required packages:
   ```sh
   pip install PyQt5
   ```

## Usage

1. Run the Python script:
   ```sh
   python Basic-Calculator.py
   ```

2. Use the on-screen buttons or the keyboard to perform calculations.

### Keyboard Shortcuts

- `0-9`: Enter numbers
- `+`: Addition
- `-`: Subtraction
- `*`: Multiplication
- `/`: Division
- `(`: Open parenthesis
- `)`: Close parenthesis
- `.`: Decimal point
- `Enter`: Calculate result
- `Backspace`: Remove last character
- `ESC`: Clear input

## How It Works

### Code Explanation

The `Basic-Calculator.py` script is the main Python file for this application. It uses the PyQt5 library to create the GUI. Here is a brief explanation of the code:

1. **Importing Libraries**: The code starts by importing the necessary modules from PyQt5.

    ```python
    from PyQt5 import QtCore, QtGui, QtWidgets
    ```

2. **UI Setup**: The `Ui_Form` class contains the setup for the UI. It defines all the buttons and the input field, and now includes a dark theme and an application icon.

    ```python
    class Ui_Form(object):
        def setupUi(self, Form):
            Form.setObjectName("Form")
            Form.resize(400, 300)
            self.setWindowIcon(QtGui.QIcon('icon.png'))  # Set application icon
            self.setStyleSheet("background-color: #2e2e2e; color: #f0f0f0;")  # Dark theme

            self.lineEdit = QtWidgets.QLineEdit(Form)
            self.lineEdit.setGeometry(QtCore.QRect(10, 10, 381, 41))
            self.lineEdit.setObjectName("lineEdit")
            self.lineEdit.setStyleSheet("background-color: #1e1e1e; color: #ffffff;")
            ...
    ```

3. **Button Initialization**: Each button is initialized with a specific geometry and text label, and styled for the dark theme.

    ```python
    self.pushButton = QtWidgets.QPushButton(Form, text="7")
    self.pushButton.setGeometry(QtCore.QRect(10, 60, 61, 51))
    self.pushButton.setStyleSheet("background-color: #3e3e3e; color: #ffffff;")
    ```

4. **Connecting Buttons to Methods**: Each button is connected to a method that handles its functionality.

    ```python
    self.pushButton.clicked.connect(lambda: self.button_clicked("7"))
    ```

5. **Button Click Handler**: The `button_clicked` method updates the input field with the button's text.

    ```python
    def button_clicked(self, text):
        current_text = self.lineEdit.text()
        self.lineEdit.setText(current_text + text)
    ```

6. **Calculation and Clear Functions**: The `calculate` method evaluates the expression in the input field, while the `clear` method resets it.

    ```python
    def calculate(self):
        try:
            result = eval(self.lineEdit.text())
            self.lineEdit.setText(str(result))
        except Exception as e:
            self.lineEdit.setText("Error")

    def clear(self):
        self.lineEdit.setText("")
    ```

7. **Keyboard Input Handling**: The `keyPressEvent` method allows the user to use the keyboard for input.

    ```python
    def keyPressEvent(self, event):
        key = event.key()
        ...
    ```

### UI and EXE Files

- **UI File**: The user interface is defined within the Python script itself using PyQt5 widgets and layouts.
- **EXE File**: The executable file (`Basic-Calculator.exe`) allows users to run the application without needing to install Python or the required libraries.

## Files

- `Basic-Calculator.py`: The main Python script for the application.
- `icon.png`: The icon file for the application.
- `Basic-Calculator.exe`: The executable file for the application (if provided).

## Author

**Hamed Gharghi**

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- PyQt5 Documentation: [https://www.riverbankcomputing.com/static/Docs/PyQt5/](https://www.riverbankcomputing.com/static/Docs/PyQt5/)

## Tags

- `Python`
- `PyQt5`
- `Calculator`
- `GUI`
- `Basic Arithmetic`
- `Keyboard Input`
- `Event Handling`
- `Open Source`
- `MIT License`
- `Dark Theme`
- `Icon`

---

> **Stickers:**
> 
> ![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
> ![PyQt5](https://img.shields.io/badge/PyQt5-5.15.4-green)
> ![License](https://img.shields.io/badge/License-MIT-yellow)

