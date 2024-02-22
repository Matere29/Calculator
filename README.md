# Calculator App

This is a simple calculator app implemented in JavaScript. It allows users to perform basic arithmetic operations such as addition, subtraction, multiplication, and division.

## Usage

To use the calculator, open the `index.html` file in your web browser. You can interact with the calculator by clicking on the number buttons, operation buttons, and control buttons.

## Features

- **Basic Operations**: Addition, subtraction, multiplication, and division.
- **Clear**: Clears the current input and previous operation.
- **Delete**: Removes the last digit entered.
- **Error Handling**: Prevents invalid inputs, such as multiple decimal points.

## How to Use

1. **Number Buttons**: Click on the number buttons to input numbers.
2. **Operation Buttons**: Click on the operation buttons to choose the desired operation.
3. **Equals Button**: Click on the equals button to perform the calculation.
4. **Clear Button (AC)**: Clears the entire calculation.
5. **Delete Button (DEL)**: Deletes the last digit entered.

## Code Overview

The calculator functionality is implemented using a JavaScript class named `Calculator`. The class has methods to handle basic operations, clear, delete, and update the display. The HTML elements are selected, and event listeners are attached to handle user interactions.

## Example Code

```javascript
const calculator = new Calculator(previousOperandTextElement, currentOperandTextElement);

numberButtons.forEach(button => {
    button.addEventListener('click', () => {
        calculator.appendNumber(button.innerText);
        calculator.updateDisplay();
    });
});

operationButtons.forEach(button => {
    button.addEventListener('click', () => {
        calculator.chooseOperation(button.innerText);
        calculator.updateDisplay();
    });
});

equalsButton.addEventListener('click', () => {
    calculator.compute();
    calculator.updateDisplay();
});

allClearButton.addEventListener('click', () => {
    calculator.clear();
    calculator.updateDisplay();
});

deleteButton.addEventListener('click', () => {
    calculator.delete();
    calculator.updateDisplay();
});
