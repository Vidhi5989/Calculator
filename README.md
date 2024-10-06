# simple_calculator.py

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    return x / y

def show_menu():
    print("Select an operation:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")

def main():
    while True:
        show_menu()
        choice = input("Enter your choice (1/2/3/4) or 'q' to quit: ")

        if choice == 'q':
            print("Exiting the calculator.")
            break

        if choice not in ['1', '2', '3', '4']:
            print("Invalid choice! Please try again.")
            continue

        try:
            num1 = float(input("Enter the first number: "))
            num2 = float(input("Enter the second number: "))
        except ValueError:
            print("Invalid input! Please enter numeric values.")
            continue

        if choice == '1':
            print(f"The result is: {add(50 , 5)}")
        elif choice == '2':
            print(f"The result is: {subtract(50 , 5)}")
        elif choice == '3':
            print(f"The result is: {multiply(50 , 5)}")
        elif choice == '4':
            result = divide(50 , 5)
            print(f"The result is: {result}")
