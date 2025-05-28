# dart-assignment-wk1

# DART-WEEK-ONE-assignment

void main() {
  // === Data Types Implementation ===

  // Define and initialize variables
  int age = 20;
  double height = 5.9;
  String name = "Channelle";
  bool isStudent = true;
  List<int> numbersList = [3, 8, 12, 104, 7];

  print("Int: $age");
  print("Double: $height");
  print("String: $name");
  print("Bool: $isStudent");
  print("List: $numbersList");

  // Type conversion examples
  print(convertStringToInt("123")); // 123
  print(convertStringToDouble("12.34")); // 12.34
  print(convertIntToString(456)); // "456"
  print(convertIntToDouble(789)); // 789.0

  // Call conversion display function
  convertAndDisplay("42");

  // === Control Flow ===

  // If-Else Statements
  checkNumberSign(-5);
  checkVotingEligibility(17);

  // Switch Case for Days
  printDayOfWeek(3);

  // Loops
  print("For loop:");
  forLoopExample();

  print("While loop:");
  whileLoopExample();

  print("Do-while loop:");
  doWhileLoopExample();

  // === Combining Data Types and Control Flow ===

  List<int> complexNumbers = [2, 15, 200, 0, 9];
  complexDataFlow(complexNumbers);
}

// === Type Conversion Functions ===

int convertStringToInt(String value) {
  return int.parse(value);
}

double convertStringToDouble(String value) {
  return double.parse(value);
}

String convertIntToString(int value) {
  return value.toString();
}

double convertIntToDouble(int value) {
  return value.toDouble();
}

void convertAndDisplay(String input) {
  int intValue = convertStringToInt(input);
  double doubleValue = convertStringToDouble(input);
  print("String to Int: $intValue");
  print("String to Double: $doubleValue");
}

// === Control Flow Functions ===

void checkNumberSign(int number) {
  if (number > 0) {
    print("The number is positive.");
  } else if (number < 0) {
    print("The number is negative.");
  } else {
    print("The number is zero.");
  }
}

void checkVotingEligibility(int age) {
  if (age >= 18) {
    print("You are eligible to vote.");
  } else {
    print("You are not eligible to vote.");
  }
}

void printDayOfWeek(int dayNumber) {
  switch (dayNumber) {
    case 1:
      print("Monday");
      break;
    case 2:
      print("Tuesday");
      break;
    case 3:
      print("Wednesday");
      break;
    case 4:
      print("Thursday");
      break;
    case 5:
      print("Friday");
      break;
    case 6:
      print("Saturday");
      break;
    case 7:
      print("Sunday");
      break;
    default:
      print("Invalid day number");
  }
}

void forLoopExample() {
  for (int i = 1; i <= 10; i++) {
    print(i);
  }
}

void whileLoopExample() {
  int i = 10;
  while (i >= 1) {
    print(i);
    i--;
  }
}

void doWhileLoopExample() {
  int i = 1;
  do {
    print(i);
    i++;
  } while (i <= 5);
}

// === Complex Data Flow Function ===

void complexDataFlow(List<int> numbers) {
  for (int number in numbers) {
    print("Number: $number");

    // Even or odd
    if (number % 2 == 0) {
      print("Even");
    } else {
      print("Odd");
    }

    // Size category using switch
    switch (true) {
      case true when (number >= 1 && number <= 10):
        print("Category: Small");
        break;
      case true when (number >= 11 && number <= 100):
        print("Category: Medium");
        break;
      case true when (number > 100):
        print("Category: Large");
        break;
      default:
        print("Category: Undefined");
    }

    print("---");
  }
}
