# ==============================================================================
# STUDENT REFLECTION
# Using a library is more practical because it provides pre-tested, optimized 
# functions like math.sqrt() and math.pow(), saving time and reducing code complexity. 
# Instead of writing complex algorithms from scratch to calculate square roots and 
# exponents, I could focus entirely on implementing the distance formula correctly.
# Without the math library, building an accurate square root function would require 
# many extra lines of iterative math logic, making the code harder to read and debug.
# ==============================================================================def calculate_distance(x1: float, y1: float, x2: float, y2: float) -> float:
    """Calculate the Euclidean distance between two 2D points."""
    return math.hypot(x2 - x1, y2 - y1)

def main() -> None:
    # 1. Ask the user for input using explicit type conversions
    try:
        x1 = float(input("Enter x1: "))
        y1 = float(input("Enter y1: "))
        x2 = float(input("Enter x2: "))
        y2 = float(input("Enter y2: "))
    except ValueError:
        print("Error: Please enter valid numerical values.")
        return

    # 2. Compute the final Euclidean distance using the helper function
    distance = calculate_distance(x1, y1, x2, y2)

    # 3. Display the result formatted to 2 decimal places
    print(f"\nThe distance between the two points is: {distance:.2f}")

if __name__ == "__main__":
    main()
