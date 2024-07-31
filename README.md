# Basic Calculator Application

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyQt5](https://img.shields.io/badge/PyQt5-5.15.4-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Description

This is a basic calculator application built using PyQt5. It includes functionality for basic arithmetic operations and can be operated using both on-screen buttons and keyboard input. This project demonstrates a simple GUI application with event handling in Python.

## Features

- Basic arithmetic operations: addition, subtraction, multiplication, and division.
- Clear and backspace functionalities.
- Keyboard input for calculator operations.
- User-friendly graphical interface.

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

2. **UI Setup**: The `Ui_Form` class contains the setup for the UI. It defines all the buttons and the input field.

    ```python
    class Ui_Form(object):
        def setupUi(self, Form):
            Form.setObjectName("Form")
            Form.resize(400, 300)
            self.lineEdit = QtWidgets.QLineEdit(Form)
            self.lineEdit.setGeometry(QtCore.QRect(10, 10, 381, 41))
            self.lineEdit.setObjectName("lineEdit")
            ...
    ```

3. **Button Initialization**: Each button is initialized with a specific geometry and text label. 

    ```python
    self.pushButton = QtWidgets.QPushButton(Form, text="7")
    self.pushButton.setGeometry(QtCore.QRect(10, 60, 61, 51))
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

---

> **Stickers:**
> 
> ![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
> ![PyQt5](https://img.shields.io/badge/PyQt5-5.15.4-green)
> ![License](https://img.shields.io/badge/License-MIT-yellow)

