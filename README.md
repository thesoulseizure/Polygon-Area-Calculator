# Polygon Area Calculator

## Overview
This project implements a Polygon Area Calculator using object-oriented programming in Python. It includes two classes: `Rectangle` and `Square`, where `Square` is a subclass of `Rectangle`. The calculator can compute various properties of rectangles and squares, including area, perimeter, diagonal length, and visual representation.

## Features
- **Rectangle Class**:
  - Initialize with width and height
  - Methods: set_width, set_height, get_area, get_perimeter, get_diagonal, get_picture, get_amount_inside
  - String representation: `Rectangle(width=x, height=y)`
- **Square Class**:
  - Subclass of Rectangle
  - Initialize with a single side length
  - Additional method: set_side
  - Overrides set_width and set_height to maintain equal sides
  - String representation: `Square(side=x)`
- **Functionality**:
  - Calculate area (width * height)
  - Calculate perimeter (2 * width + 2 * height)
  - Calculate diagonal length using Pythagorean theorem
  - Generate a string-based picture using '*' characters
  - Determine how many times one shape can fit inside another
  - Handle edge cases (e.g., shapes too large for picture representation)

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/thesoulseizure/polygon-area-calculator.git
   ```
2. Navigate to the project directory:
   ```bash
   cd polygon-area-calculator
   ```
3. Ensure Python 3.x is installed:
   ```bash
   python --version
   ```

## Usage
Here's an example of how to use the classes:

```python
# Create a rectangle
rect = Rectangle(10, 5)
print(rect.get_area())  # Output: 50
rect.set_height(3)
print(rect.get_perimeter())  # Output: 26
print(rect)  # Output: Rectangle(width=10, height=3)
print(rect.get_picture())  # Output: **********\n**********\n**********\n

# Create a square
sq = Square(9)
print(sq.get_area())  # Output: 81
sq.set_side(4)
print(sq.get_diagonal())  # Output: 5.656854249492381
print(sq)  # Output: Square(side=4)
print(sq.get_picture())  # Output: ****\n****\n****\n****\n

# Check how many squares fit in a rectangle
rect.set_height(8)
rect.set_width(16)
print(rect.get_amount_inside(sq))  # Output: 8
```

## Testing
The code has been tested to meet the following requirements:
1. Square is a subclass of Rectangle
2. Square and Rectangle are distinct classes
3. Square objects are instances of both Square and Rectangle
4. Correct string representations for Rectangle and Square
5. Accurate calculations for area, perimeter, and diagonal
6. Proper picture representation with '*' characters
7. Correct handling of shapes too large for picture (>50)
8. Accurate counting of shapes fitting inside another

To run tests, you can use the example code above in a Python environment. Open the browser console (F12) to see verbose test output if running in a compatible environment.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes. Ensure that your code follows the existing style and passes all tests.
