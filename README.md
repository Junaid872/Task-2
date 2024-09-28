def simple_calculator():
    print("Simple Calculator")
    print("Available operations:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")

    # Get user input for the numbers and the operation
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
    except ValueError:
        print("Invalid input. Please enter numeric values.")
        return

    operation = input("Enter the operation (+, -, *, /): ")

    # Perform the calculation and display the result
    if operation == '+':
        result = num1 + num2
        print(f"The result of {num1} + {num2} is {result}.")
    elif operation == '-':
        result = num1 - num2
        print(f"The result of {num1} - {num2} is {result}.")
    elif operation == '*':
        result = num1 * num2
        print(f"The result of {num1} * {num2} is {result}.")
    elif operation == '/':
        if num2 == 0:
            print("Error: Division by zero is not allowed.")
        else:
            result = num1 / num2
            print(f"The result of {num1} / {num2} is {result}.")
    else:
        print("Invalid operation. Please choose one of the following: +, -, *, /.")

# Run the calculator
if _name_ == "_main_":
    simple_calculator()
