## Programming Fundamentals in Swift
- [Swift Basics](#swift-basics)
  - [Swift Variable Examples](#swift-variable-examples)
  - [String Operations and Manipulation](#string-operations-and-manipulation)
  - [Control Flow](#control-flow)
  - [Loops](#loops)
  - [Loop Control with Conditional Statements](#loop-control-with-conditional-statements)
  - [Simple Authentication System Example](#simple-authentication-system-example)
  - [Array Usage in Swift](#array-usage-in-swift)
  - [Swift Tuple and Validation Examples](#swift-tuple-and-validation-examples)
  - [Swift Dictionary Example](#swift-dictionary-example)
  - [Swift Function Example](#swift-function-example)
  - [Different Usages of Functions](#different-usages-of-functions)
  - [Usages of Functions with inout Parameters](#usages-of-functions-with-inout-parameters)
  - [Closures](#closures)
  - [Swift Closure Example](#swift-closure-example)
  - [Swift Completion Handler Usage](#swift-completion-handler-usage)
  - [Different Closure Usage](#different-closure-usage)
  - [Struct](#struct)
  - [Class](#class)
  - [Class Example: Virtual Food Order System](#class-example-virtual-food-order-system)
- [SwiftUI Basics](#swiftui-basics)
  - [State And Binding](#state-and-binding)
  - [Observable And Observed](#observable-and-observed)
  - [State And Event Handling](#state-and-event-handling)
  - [Views Within Views](#views-within-views)
  - [Controls Cheat Sheet](#controls-cheat-sheet)
  - [Frame And Layouts](#frame-and-layouts)
  - [Hierarchical Navigation](#hierarchical-navigation)
  - [Tabbed Navigation](#tabbed-navigation)
  - [ScrollView and List](#scrollview-and-list)
  - [Gestures](#gestures)
- [Advanced Programming in Swift](#advanced-programming-in-swift)
  - [Enum](#enum)
  - [Sets](#sets)
  - [Access-level Modifiers](#access-level-modifiers)
  - [Typecasting](#typecasting)
  - [Polymorphism](#polymorphism)
  - [Protocol](#protocol)
  - [Optional Protocol](#optional-protocol)
  - [Property and newValue](#property-and-newvalue)
  - [didSet](#didset)
  - [Delegate](#delegate)
  - [Error Handling](#error-handling)
  - [Functional programming](#functional-programming)
  - [Test](#test)
- [Working With Data](#working-with-data)
  - [URL](#url)
  - [HTTP Request](#http-request)
  - [JSON](#json)
  - [JSON Decoding](#json-decoding)
  - [Core Data](#core-data)


####  Swift Variable Examples

```swift
//// This code uses variables to display weather temperatures.

let today = "Wednesday"
let currentTemperature = 80
print("Welcome to a new day!")

print("The temperature on \(today) is \(currentTemperature)°F")
var morningTemperature = 70
print("The temperature on \(today) morning is \(morningTemperature)°F")
morningTemperature  =  85
print("The temperature on \(today) evening is \(morningTemperature)°F")
let averageTemperature = 78
morningTemperature = averageTemperature
print("The average temperature this week is \(morningTemperature)°F")


```
#### Usage of Variables and Type Casting



```swift
///// the usage of variables and type casting in a game scenario.
//// Demonstrating Game Scores and Averages

let currentPlayer = "John"
var totalScore = 0

let currentLevelScore = 10
totalScore += currentLevelScore

print("\(currentPlayer) obtained a score of \(totalScore)")

var currentLevelBonus = 10.0
currentLevelBonus = 20
print("The bonus score for this level is \(currentLevelBonus).")

// Type casting
totalScore += Int(currentLevelBonus)

print("The final score for \(currentPlayer) is \(totalScore).")

let lowestLevelScore = 50
let highestLevelScore = 99
let totalLevels = 10
let levelScoreDifference = highestLevelScore - lowestLevelScore
let averageLevelScore = levelScoreDifference / totalLevels

print("The average score for each level is \(averageLevelScore).")

let averageScoreDouble = Double(levelScoreDifference) / Double(totalLevels)
print("The average score for each level is \(averageScoreDouble).")


```


#### String Operations and Manipulation


###### Time and Day Information

```swift

let today = "Tuesday"
print("Today is \(today)")
let currentHour = "8"
let currentMinutes = "45"
let timePeriod = "AM"

var currentTime = currentHour + ":" + currentMinutes + " " + timePeriod
print("It is \(currentTime)")
print("It is \(currentTime) on \(today)")

let timeZone = "EST"
currentTime += " \(timeZone)"
print("It is \(currentTime)")
print("It is \(currentTime) on \(today)")

let shortToday = today.prefix(3)

print("Today is \(shortToday)")
print("It is \(currentTime) on \(shortToday)")

print("The abbreviation has \(shortToday.count) characters.")

```

#### Control Flow 


```swift

let isLoggedIn = true
if isLoggedIn {
    print("You are currently logged in. Enjoy your personalized experience!")
} else {
    print("Please log in to access your account.")
}

let userAge = 25
let legalDrinkingAge = 21
if userAge >= legalDrinkingAge {
    print("You are legally allowed to purchase alcohol.")
} else {
    print("Sorry, you must be at least 21 years old to purchase alcohol.")
}

let userCountry = "USA"
if userCountry == "USA" {
    print("You are currently browsing the US version of the website.")
} else {
    print("You are currently browsing the international version of the website.")
}

let isPremiumMember = true
if isPremiumMember {
    print("Thank you for being a premium member. Enjoy exclusive benefits and content!")
} else {
    print("Upgrade to a premium membership to access premium features.")
}

let userRole = "Admin"
switch userRole {
    case "Admin":
        print("You have administrative privileges. Manage the system with care.")
    case "User":
        print("You are a regular user. Enjoy using the platform!")
    default:
        print("Your role is not recognized. Contact support for assistance.")
}


```


#### Loops

```swift
// For loop to roll a dice 6 times
for _ in 1...6 {
    let dice = Int.random(in: 1...6)
    print("Roll a \(dice).")
}

// While loop to roll two dice until they show the same value
var firstDice = Int.random(in: 1...6)
var secondDice = Int.random(in: 1...6)

while firstDice != secondDice {
    firstDice = Int.random(in: 1...6)
    secondDice = Int.random(in: 1...6)
}

print("You rolled a double \(firstDice).")

// Repeat-While loop to roll two dice until they show the same value
var thirdDice = 0
var fourthDice = 0

repeat {
    thirdDice = Int.random(in: 1...6)
    fourthDice = Int.random(in: 1...6)
} while thirdDice != fourthDice

print("You rolled a double \(thirdDice).")

```


#### Loop Control with Conditional Statements

```swift

let totalLevels = 12
let unlockedLevels = 6
let bonusLevel = 4

for currentLevel in 1...totalLevels {
    if currentLevel == bonusLevel {
        print("Skip bonus level \(bonusLevel).")
        continue
    }
    
    print("Play level \(currentLevel).")
    
    if currentLevel == unlockedLevels {
        let lockedLevels = totalLevels - unlockedLevels
        print("You have played all \(unlockedLevels) unlocked levels. Purchase the full game to play the remaining \(lockedLevels) levels.")
        break
    }
}


```


#### Simple Authentication System Example

```swift

let savedPassword = "password123"
var enteredPassword = "password123"

if enteredPassword == savedPassword {
    print("Authentication successful. Welcome!")
} else {
    print("Invalid password. Try again.")
}

enteredPassword = "hello"

if enteredPassword == savedPassword {
    print("Authentication successful. Welcome!")
} else {
    print("Invalid password. Try again.")
}

let newPassword = "newPassword"
let confirmPassword = "newPassword"

if newPassword == confirmPassword {
    print("Password has been successfully changed.")
} else {
    print("Password and confirmation do not match. Please try again.")
}

let pinCode = "1234"
let enteredPin = "4321"

if enteredPin == pinCode {
    print("Authentication successful. Welcome!")
} else {
    print("Invalid PIN. Try again.")
}


```

#### Array Usage in Swift

```swift

// Students and Their Grades

var studentGrades: [String: Int] = [:]

// Add grades for students
studentGrades["Alice"] = 90
studentGrades["Bob"] = 78
studentGrades["Charlie"] = 85

// Print the grades of all students
print("Grades of Students:")
for (name, grade) in studentGrades {
    print("\(name): \(grade)")
}

// Update a student's grade
let studentToUpdate = "Bob"
let newGrade = 85
if let oldGrade = studentGrades.updateValue(newGrade, forKey: studentToUpdate) {
    print("\(studentToUpdate)'s grade has been updated from \(oldGrade) to \(newGrade).")
} else {
    print("\(studentToUpdate) is not found in the list of students.")
}

// Print the updated grades
print("Updated Grades:")
for (name, grade) in studentGrades {
    print("\(name): \(grade)")
}

// Remove a student from the list
let studentToRemove = "Charlie"
if let removedGrade = studentGrades.removeValue(forKey: studentToRemove) {
    print("\(studentToRemove) has been removed from the list. Their grade was \(removedGrade).")
} else {
    print("\(studentToRemove) is not found in the list of students.")
}

// Check if the list is empty
if studentGrades.isEmpty {
    print("The list of students and grades is empty.")
} else {
    print("There are \(studentGrades.count) students in the list.")
}


```


#### Swift Tuple and Validation Examples

```swift

let userInfo = ("JohnDoe", 1234)
if userInfo.0 == "" || userInfo.1 < 0 {
  print("Invalid credentials!")
} else {
  print("The username is \(userInfo.0) and the password is \(userInfo.1).")
}

let fullUserInfo = (username: "AliceSmith", password: 5678)
if fullUserInfo.username == "" || fullUserInfo.password < 0 {
  print("Invalid credentials!")
} else {
  print("The username is \(fullUserInfo.username) and the password is \(fullUserInfo.password).")
}

```


#### Swift Dictionary Example

```swift


// Foods and their calorie values
let foodCalories = [
    "Apple": 52,
    "Banana": 89,
    "Orange": 62,
    "Grapes": 67,
    "Strawberries": 32,
]

// Finding the highest and lowest calorie foods
var highestCalorieFood = ""
var lowestCalorieFood = ""
var highestCalories = Int.min
var lowestCalories = Int.max

for (food, calories) in foodCalories {
    if calories > highestCalories {
        highestCalories = calories
        highestCalorieFood = food
    }
    if calories < lowestCalories {
        lowestCalories = calories
        lowestCalorieFood = food
    }
}

// Printing the results
print("Highest calorie food: \(highestCalorieFood), \(highestCalories) calories.")
print("Lowest calorie food: \(lowestCalorieFood), \(lowestCalories) calories.")

```


#### Swift Function Example

```swift

// Function to calculate total calories from an array of meal calories
func calculateTotalCalories(mealCalories: [Int]) -> Int {
  var totalCalories = 0
  for calories in mealCalories {
    totalCalories += calories
  }
  return totalCalories
}

// Daily meal calories
let breakfastCalories = 350
let lunchCalories = 550
let dinnerCalories = 700

// Calculate total calories for the day
let mealCalories = [breakfastCalories, lunchCalories, dinnerCalories]
let totalCalories = calculateTotalCalories(mealCalories: mealCalories)

print("Total calories for the day: \(totalCalories)")

```


####  Different Usages of Functions 
####
###### Swift function examples with different parameter scenarios 
###### Example 1: Function with Underscore (_) for Parameter Names
###### In this example, the "_" symbol for parameters indicates that we do not need to use the parameter names "fn" and "sn" when calling the function. We can call the function as follows:

```swift

func hiThere(_ fn: String, _ sn: String) {
  let fullname = fn + " " + sn
  print("Hi there \(fullname)")
}
```
###### Example 2: Function with External Parameter Names
###### In this example, the function uses external parameter names "firstname" and "surname," which must be used when calling the function:

```swift
func hiThere(firstname fn: String, surname sn: String) {
  let fullname = fn + " " + sn
  print("Hi there \(fullname)")
}
```
###### Example 3: Function with Default Parameter Values
###### In this example, the "score" parameter has a default value of 0, which means we can call the function with or without providing a value for "score"

```swift
func display(_ s1: String, _ s2: String, score: Int = 0) {
  let name_score = s1 + " " + s2 + " " + String(score)
  print("Hello \(name_score)")
}

```

#### Usages of Functions with inout Parameters

```swift

/// Incrementing Points with inout Parameter

var playerPoints = 0

func incrementPoints(_ points: inout Int, by amount: Int = 100) {
  points += amount
}

incrementPoints(&playerPoints)
print("Player points: \(playerPoints)")

incrementPoints(&playerPoints)
print("Player points: \(playerPoints)")

incrementPoints(&playerPoints)
print("Player points: \(playerPoints)")

incrementPoints(&playerPoints, by: 300)
print("Player points: \(playerPoints)")

incrementPoints(&playerPoints, by: 50)
print("Player points: \(playerPoints)")



```


#### Closures 
###### Closures in Swift are self-contained blocks of code that can be assigned to variables or passed as arguments to functions. They are similar to functions but have a more concise syntax. Here's how closures are defined:

```swift

// Function:
func functionName(argument list) -> ReturnType {
    Execute some code
}

// Closure:
{ (argument list) -> ReturnType in
    Execute some code
}
```
###### Closures are useful for tasks that require a block of code to be executed, such as sorting arrays, filtering data, or performing operations on collections. They can be particularly handy in scenarios where you need to define a short, inline piece of functionality without creating a separate function.
######
######
###### Example 1
######
```swift


// Using a closure to find the maximum of two numbers
let maximum = { (num1: Int, num2: Int) -> Int in
    return num1 > num2 ? num1 : num2
}
print(maximum(1, 6)) // Output: 6
```

######
###### Example 2
######

```swift

let letters = ["B", "D", "A", "C"]
// Sorting an array of strings using a closure
let myCollection = letters.sorted(by: { (string1: String, string2: String) -> Bool in
    return string1 < string2
})
print(myCollection) // Output: ["A", "B", "D", "C"]

// The same sorting operation with a shorter closure syntax
let myCollection2 = letters.sorted(by: { $0 < $1 })
print(myCollection2)  // Output: ["A", "B", "D", "C"]

```


#### Swift Closure Example 
######
###### In this example, the variable waterBottles represents the amount of water bottles in a water dispenser, not gold bars. We have defined a closure named fillWaterDispenser. This closure takes an inout Int parameter called bottles, which means it can modify the value of bottles in its scope.
######

```swift

var waterBottles = 0
let fillWaterDispenser = { (bottles: inout Int) in
  bottles += 100 //ml
}
fillWaterDispenser(&waterBottles)
print(waterBottles)
```


#### Swift Completion Handler Usage 
###### Drinking Water Example

```swift

var waterBottle = 1000 // We have 1000 ml (1L) water in the bottle

func drinkTenMLWater(from bottles: inout Int, completion: (Int) -> Void) {
bottles -= 10
completion(bottles)
}

print("You have (waterBottle) ml water in the bottle.")

drinkTenMLWater(from: &waterBottle) { remainingWater in
print("You drank ten ml of water.")
print("You have (remainingWater) ml of water left.")
}


```


#### Different Closure Usage 


###### Example 1: Basic Usage of Closure


```swift

let sayHello = {
    print("Merhaba!")
}

sayHello() // Çıktı: Merhaba!
```
###### Example 2: Closure with Parameters and Return Value

```swift

let multiply = { (a: Int, b: Int) -> Int in
    return a * b
}

let result = multiply(5, 3)
print(result) // Çıktı: 15
```

###### Example 3: Passing a Closure as a Parameter to Another Function

```swift

func performOperation(a: Int, b: Int, operation: (Int, Int) -> Int) {
    let result = operation(a, b)
    print("Sonuç: \(result)")
}

let addition = { (a: Int, b: Int) -> Int in
    return a + b
}

performOperation(a: 5, b: 3, operation: addition) // Çıktı: Sonuç: 8

```

###### Example 4: Closure Expression Shorthand

```swift

let numbers = [1, 2, 3, 4, 5]
let squaredNumbers = numbers.map { $0 * $0 }
print(squaredNumbers) // Çıktı: [1, 4, 9, 16, 25]

```

###### https://docs.swift.org/swift-book/documentation/the-swift-programming-language/closures/



#### Struct
 

```swift


struct Vehicle {
    var color: String
    var name: String
    var topSpeed: Int
    var mileage: Int
    
    func drive() {
        print("\(color) \(name) can drive at a maximum speed of \(topSpeed)!")
    }
}

var newVehicle = Vehicle(color: "blue", name: "Car 1", topSpeed: 100, mileage: 5000)
newVehicle.drive()
print("The color of the vehicle is \(newVehicle.color).")
```


###### Explanation of "mutating" Keyword
###### The `mutating` keyword is used in a structure or class method to allow the method to modify the properties of the structure or class. By default, a method in a structure or class is not allowed to modify the properties; it can only read them. However, by marking a method with the `mutating` keyword, you can enable the method to modify the properties.
######
###### Example 1: Using the "mutating" keyword in a structure

```swift
struct Point {
    var x: Int
    var y: Int

    mutating func moveByX(_ deltaX: Int, y deltaY: Int) {
        x += deltaX
        y += deltaY
    }
}

var point = Point(x: 10, y: 20)
point.moveByX(5, y: 10)
print(point) // Output: Point(x: 15, y: 30)

```

###### Example 2: Using the "mutating" keyword in a structure

```swift

struct TableReservation {
    var name: String
    var tableNumber: Int

    mutating func updateBooking(updatedName: String) {
        name = updatedName
    }
}

var johnBooking = TableReservation(name: "John", tableNumber: 1)
print(johnBooking)
johnBooking.updateBooking(updatedName: "Maria")
print(johnBooking)

```


#### Class
 

```swift

class LocalFile {
  let name: String
  let fileExtension: String

  init(name: String, fileExtension: String) {
    self.name = name
    self.fileExtension = fileExtension
  }

  var fullFileName: String {
    return name + "." + fileExtension
  }
}

let file = LocalFile(name: "image", fileExtension: "png")
print(file.fullFileName)


```


#### Class Example: Virtual Food Order System
###### Virtual Food Order System
###### A virtual system that allows users to order meals and track calorie intake for breakfast, lunch, and dinner.

```swift

class VirtualFoodOrderSystem {
    var selectedMeal = ""
    var isOrdering = true

    func welcomeUser() {
        print("Welcome to your virtual food order system.")
    }

    func selectMealType() {
        print("What type of meal would you like to order?")
        print("1. Breakfast")
        print("2. Lunch")
        print("3. Dinner")
    }

    func orderMeal(mealNumber: Int) {
        print("You have selected option \(mealNumber).")
        switch mealNumber {
        case 1:
            selectedMeal = "Breakfast"
        case 2:
            selectedMeal = "Lunch"
        case 3:
            selectedMeal = "Dinner"
        default:
            print("Invalid input: \(mealNumber)")
            return
        }
        print("You are ordering \(selectedMeal).")
    }

    func addCalories(calorieCount: Int) {
        print("You've added \(calorieCount) calories to your \(selectedMeal) meal.")
    }

    func checkTotalCalories(calorieCount: inout Int) {
        print("Total calories in your meals: \(calorieCount)")
    }
}

struct MealCalories {
    var breakfastCalories = 0
    var lunchCalories = 0
    var dinnerCalories = 0

    var totalCalories: Int {
        breakfastCalories + lunchCalories + dinnerCalories
    }

    mutating func addCalories(for mealType: String, calories: Int) {
        switch mealType {
        case "Breakfast":
            breakfastCalories += calories
            print("Added \(calories) calories to breakfast.")
        case "Lunch":
            lunchCalories += calories
            print("Added \(calories) calories to lunch.")
        case "Dinner":
            dinnerCalories += calories
            print("Added \(calories) calories to dinner.")
        default:
            break
        }
    }
}

let virtualFoodOrderSystem = VirtualFoodOrderSystem()
virtualFoodOrderSystem.welcomeUser()

repeat {
    virtualFoodOrderSystem.selectMealType()
    let mealNumber = Int.random(in: 1...4)
    virtualFoodOrderSystem.orderMeal(mealNumber: mealNumber)
} while virtualFoodOrderSystem.selectedMeal == ""

var totalCaloriesInMeals = 0

repeat {
    print("What would you like to do?")
    print("1. Check total calories in meals")
    print("2. Add calories to selected meal")
    print("3. Exit the food order system")
    let option = Int.random(in: 1...4)
    print("Selected option: \(option).")
    switch option {
    case 1:
        virtualFoodOrderSystem.checkTotalCalories(calorieCount: &totalCaloriesInMeals)
    case 2:
        let calorieCount = Int.random(in: 200...800)
        virtualFoodOrderSystem.addCalories(calorieCount: calorieCount)
        MealCalories().addCalories(for: virtualFoodOrderSystem.selectedMeal, calories: calorieCount)
    case 3:
        virtualFoodOrderSystem.isOrdering = false
        print("Exiting the food order system.")
    default:
        break
    }
} while virtualFoodOrderSystem.isOrdering


```



## SwiftUI Basics

#### State and Binding

######      State and Binding are known as property wrappers and are used with interface elements to control data display.
######      State and Binding work in pairs, inside SwiftUI views, in the form @State and @Binding. All SwiftUI views are structures, also known as structs. Once initialized, structs don't allow their internal variables to change. @State elements remove this restriction, allowing variables to be stored outside the structure itself in an area that can be changed. As a plus, they serve as control variables.

######      @Binding, on the other hand, is used to create variables that receive values from @State variables and are connected to them in a way that any change to a @Binding variable will change the bind @State variable.


```swift
// ContentView is a SwiftUI view that holds the state variable changeColor.
// When changeColor is true, it displays the ColorChangeView.
struct ContentView: View {
    @State var changeColor = true
    
    var body: some View {
        VStack {
            if changeColor {
                // ColorChangeView is a subview that receives the @Binding property colorBinding,
                // which is connected to the changeColor state variable.
                ColorChangeView(colorBinding: $changeColor) // When colorBinding changes, changeColor will change too.
            }
        }
    }
}

// ColorChangeView is a SwiftUI view that changes the color of an image based on the value of colorBinding.
// It also provides a button to toggle the value of colorBinding.

struct ColorChangeView: View {
    @Binding var colorBinding: Bool
    
    var body: some View {
        VStack {
            // An image with systemName "swift" is displayed, and its color is determined by the value of colorBinding.
            Image(systemName: "swift")
                .resizable()
                .frame(width: 100, height: 100)
                .foregroundColor(colorBinding ? .red : .blue) // In this line, the color will be changed.
            
            // A button labeled "Toggle Color" is provided.
            // When pressed, it will toggle the value of colorBinding, thereby changing the color of the image.
            Button(action: {
                colorBinding.toggle() // The colorBinding value will change when the button is pressed.
            }, label: {
                Text("Toggle Color")
                    .font(.title2)
            })
        }
    }
}

```

#### Observable and Observed


######      @ObservedObject and @Published are often used together in SwiftUI to achieve reactivity and data binding.  @ObservedObject is used to mark a property in a SwiftUI view that holds an ObservableObject. It allows the view to observe changes in the properties of that ObservableObject, triggering UI updates when changes occur.
######
######     On the other hand, @Published is a property wrapper used inside an ObservableObject. When applied to a property in a class or a structure, it automatically sends notifications to its observers whenever the property value changes. This enables SwiftUI views observing the @ObservedObject to update their UI when @Published properties change.  Together, @ObservedObject and @Published enable reactive data flow in SwiftUI, allowing views to automatically respond to changes in the underlying data and keeping the user interface synchronized with the data state.

```swift

import SwiftUI
import Combine

class ControlViewModel: ObservableObject {
    @Published var isLogoVisible = true // This is the controlling variable that can be observed by SwiftUI views.
}

struct ContentView: View {
    @ObservedObject var viewModel = ControlViewModel() // Create an instance of ControlViewModel to observe changes in isLogoVisible.

    var body: some View {
        VStack {
            if viewModel.isLogoVisible {
                ColorChangeView(viewModel: viewModel)
            }
        }
    }
}

struct ColorChangeView: View {
    @ObservedObject var viewModel: ControlViewModel // Receive the observed view model.

    var body: some View {
        VStack {
            Image(systemName: "swift")
                .resizable()
                .frame(width: 100, height: 100)
                .foregroundColor(viewModel.isLogoVisible ? .red : .blue)

            Button(action: {
                viewModel.isLogoVisible.toggle() // Toggle the value of isLogoVisible from the view model.
            }, label: {
                Text("Toggle Logo Visibility")
                    .font(.title2)
            })
        }
    }
}
```

####  State and Event Handling
 

```swift
import SwiftUI

struct SearchUserForm: View { 
    @State var userName:String = "" 
    var body: some View {  
        Form {
            TextField("Type User Name", 
                text:$userName, 
                onEditingChanged: { status in 
                    print(status) 
                }) 
            .onSubmit({ 
                print("searching..") 
            }) 
            .onChange(of: userName, perform: { newValue in 
                print(newValue)
            }) 

        }
        .padding() 
    } 
} 

```

####  Frame and Layouts

###### Layout direction
###### Each stack lays out views in only one direction. 

###### HStack  :    Horizontal display of child views, from leading to trailing.

###### VStack  :    Vertical display of child views, from top to bottom.

###### ZStack  :    Spatial display of child views that stacks them from the bottom to the top. Child views that are higher in the stack are displayed over lower children.

<div style="text-align:center;">
  <img width="500" alt="Screenshot" src="https://github.com/rabiaabdioglu/SwiftBasics/assets/75799790/c45516e8-f7d4-4065-845d-c56d9a3a839c">
</div>

```swift

struct ContentView: View {
    var body: some View {
        VStack (alignment: .leading, spacing: 20) {
            Image(systemName: "globe")
                .imageScale(.large)
                .foregroundColor(.accentColor)
                .frame(width: 300, alignment: .top)

            
            // Show a text with a pink background in a fixed frame
            Text("Hello, world!")
                .background(Color.pink)
                .frame(width: 200, height: 50)
            Spacer()

            HStack {
                // Add spacing to push "One" and "Three" to the sides
                Spacer()
                Text("One")
                Text("Two")
                Text("Three")
                Spacer()
            }
            .frame(width: 300, alignment: .center)
            .background(Color.blue)
            Spacer()

        }
        .background(Color.yellow) // Set the background color of the VStack
        .padding() // Apply padding around the VStack
    }
}



```
###### Simple example with ZStack

```swiftstruct MainView: View {
    var body: some View {
        NavigationView {
            ZStack {
                HStack(spacing: 8) {
                    Text("Pink").scaledToFit().frame(
                        width: 100, height: 100, alignment: .center)
                    VStack(spacing: 10) {
                        Text("Yellow").font(.title)
                        Text("List  For VStack ").font(.title3)
                            .multilineTextAlignment(.center)
                    }// :- VStack
                    .padding()
                    .frame(width: 300)
                    .background(Color.yellow)
                }  // :- HStack
                .padding()
                .frame(width: 400)
                .background(Color.pink)
            }  // :- ZStack
            .frame(width: 500)
            .background(Color.orange)
        }
    }
}
```
####  Controls Cheat Sheet


######  Some of the most commonly used controls include Button, Toggle, Stepper, Slider, ProgressView, DatePicker and Label. 


```swift
  struct ControlView: View {
    @State private var valueForStepper = 1
    @State private var isShowingToggle = true
    @State private var sizeForSlider: CGFloat = 0.1
    @State private var selectedColor = "Red"
    @State private var selectedDate = Date()
    let colors = ["Red", "Blue", "Green", "Yellow"]

    var dateClosedRange: ClosedRange<Date> {
        let min = Calendar.current.date(byAdding: .day, value: -1, to: Date())!
        let max = Calendar.current.date(byAdding: .day, value: 1, to: Date())!
        return min...max
    }
    
    var body: some View {
        NavigationView {
            VStack (spacing: 30) {
                Label("Logo", systemImage: "book")
                    .labelStyle(.titleAndIcon)
                
             

                Button(role: .destructive) {
                    print("cancel button clicked")
                } label: {
                    HStack {
                        Image(systemName: "arrowshape.turn.up.left")
                        Text("")
                    }
                }


                Toggle(isOn: $isShowingToggle) {
                    Text("Hello World")
                }

                
                HStack {
                    Text("Number of books: \(valueForStepper)")
                    Stepper("", value: $valueForStepper, in: 1...20)
                }


                HStack {
                    VStack {
                        Text("Changable Text").font(.system(size: sizeForSlider * 50))
                        Slider(value: $sizeForSlider)
                    }
                    .padding()
                }
                
                Form {
                    Section {
                        DatePicker(
                            selection: $selectedDate,
                            in: dateClosedRange,
                            displayedComponents: .date,
                            label: { Text("Due Date") }
                        )
                    }
                }
                
                
                Picker("Color", selection: $selectedColor) {
                    ForEach(colors, id: \.self) { color in
                        Text(color)
                    }
                }
                .pickerStyle(.segmented)
                Text("You selected: \(selectedColor)")

            }
            .padding(30)
        }
    }
}



```
######  Preview of above codes 

<div style="text-align:center;">
  <img height="500" alt="Screenshot" src="https://github.com/rabiaabdioglu/SwiftBasics/assets/75799790/83c17ddc-1506-49eb-8259-6b114a626e68">
</div>
```


######  Simple Date Picker and Button Usage


```swift

struct Birthday: View {

    @State var BirthDay = Date()

    var body: some View {
        Form {
            HStack {
                DatePicker(
                    selection: $BirthDay, in: Date()...,
                    displayedComponents: [.date, .hourAndMinute]
                ) {}
                Button(action: { print("do something!") }) {
                    HStack {
                        Image(systemName: "arrow.right.circle")
                        Text("Done")
                    }
                }.padding(20)
            }
            Text("Selected Date: \(BirthDay.formatted(date: .long, time: .complete))")
        }
    }
}



```

####  Views Within Views


```swift


struct ChildView: View {

    @Binding var showBook :Bool
    var body: some View {
        VStack(spacing: 30) {
            if showBook {
                Image(systemName: "book.fill")
                    .foregroundColor(.green)
            }
            else{
                Image(systemName: "book.closed")
                    .foregroundColor(.green)
            }
            Button( action: {
                showBook.toggle()
            },label:{
                Text(showBook ? "Close Book" : "Open Book")
            })
            
        }
    }
}

struct ParentView: View {

    @State var showBook = true
    var body: some View {
    
            ChildView(showBook: $showBook)
    }
}




```
####  Hierarchical Navigation

###### Hierarchical navigation in SwiftUI allows users to move through different levels of content using NavigationView and NavigationLink. With NavigationView, you can create a stack of views, and NavigationLink defines the links to other views. SwiftUI handles the navigation, providing a back button to go back to the previous view.


```swift

struct ContentView: View {
    var body: some View {
        var elements = ["Page1", "Page2"]
        let colors = [Color.pink, Color.orange]
        
            NavigationView {
                VStack {
                    Text("Select page:")
                        .font(.title)
                    
                    ForEach(elements.indices, id: \.self) { index in
                        NavigationLink(destination: Text(elements[index]).font(.title).foregroundColor(colors[index])) {
                            Text(elements[index])
                                .font(.title)
                                .foregroundColor(colors[index])
                        }
                    }
                }
                .navigationTitle("Hierarchical navigation")
                .navigationBarTitleDisplayMode(.inline)
            }
        }}
```

####    Tabbed Navigation

###### Tabbed navigation organizes app content into multiple tabs, enabling users to switch between sections easily. In SwiftUI, you can implement it using TabView, presenting a tab bar at the bottom for navigation between different views associated with each tab.

```swift

struct ContentView: View {
    var body: some View {
        TabView{
            Text("Home Page")
                .font(.title)
                .tabItem({
                    Label("Home",systemImage: "house")
                })
            Text("Profile")
                .font(.title)
                .tabItem({
                    Label("Profile",systemImage: "person")
                })
        }
    }
}
```

#### ScrollView and List


###### Food Calories Guide

###### This example allows users to explore a list of food items and their corresponding calorie information. Users can navigate through the list and select a food item to view more detailed calorie information on a separate page.

```swift

struct FoodItem: Identifiable {
    let id = UUID()
    let name: String
    let calories: Int
}

struct ListAndScrollView: View {
    let foodItems = [
        FoodItem(name: "Pizza", calories: 300),
        FoodItem(name: "Salad", calories: 150),
        FoodItem(name: "Burger", calories: 400),
        FoodItem(name: "Pasta", calories: 350),
        FoodItem(name: "Steak", calories: 500),
        FoodItem(name: "Ice Cream", calories: 250),
        FoodItem(name: "Fries", calories: 200),
        FoodItem(name: "Sushi", calories: 250),
        FoodItem(name: "Chicken Sandwich", calories: 350),
        FoodItem(name: "Cheese Cake", calories: 300),
        FoodItem(name: "Smoothie", calories: 200),
        FoodItem(name: "Apple", calories: 80),
        FoodItem(name: "Chocolate Bar", calories: 150),
        FoodItem(name: "Orange Juice", calories: 120),
    ]
    
    
    var body: some View {
        NavigationView {
            List {
                Section(header: Text("Information")) {
                    Text("This List shows information about foods and calories")
                        .font(.headline)
                }
                
                Section(header: Text("Food Items with Calorie Information")) {
                    ScrollView {
                        VStack(alignment: .leading, spacing: 20) {
                            
                            
                            ForEach(foodItems) { item in
                                NavigationLink(destination: FoodItemDetailView(foodItem: item)) {
                                    HStack {
                                        Text(item.name)
                                            .font(.headline)
                                        Spacer()
                                        Text("\(item.calories) calories")
                                            .foregroundColor(.gray)
                                    }
                                }
                            }
                        }
                        .padding()
                    }
                    
                    .frame(height: 300) // Adjust the height as needed
                }
                
                Section(footer: Text("Contact")) {
                    Text("Please contact us")
                        .font(.headline)
                }
            }
            .scrollContentBackground(.hidden)
            .padding()
        }
    }
}
struct FoodItemDetailView: View {
    let foodItem: FoodItem
    
    var body: some View {
        VStack(alignment: .leading, spacing: 20) {
            Text(foodItem.name)
                .font(.title)
            Text("\(foodItem.calories) calories")
                .foregroundColor(.gray)
        }
        .padding()
        .navigationBarTitle(foodItem.name)
    }
}

```

#### Gestures

###### onTapGesture
###### A gesture that detects a single tap or touch on a view, triggering an action when the tap occurs.

```swift
struct TapExample: View {
    @State private var tapCount = 0

    var body: some View {
        VStack {
            Text("Tap the rectangle below")
                .padding(.bottom, 20)

            Rectangle()
                .fill(Color.orange)
                .frame(width: 200, height: 100)
                .cornerRadius(10)
                .onTapGesture {
                    tapCount += 1
                }

            Text("Taps: \(tapCount)")
        }
        .padding()
    }
}

```
###### onLongPressGesture

###### A gesture that detects a long press or touch and hold on a view, triggering an action when the press is held for a specified duration.

```swift

struct LongPressExample: View {
    @State private var isPressed = false

    var body: some View {
        VStack {
            Text("Long press the rectangle below")
                .padding(.bottom, 20)

            Rectangle()
                .fill(isPressed ? Color.orange : Color.pink)
                .frame(width: 200, height: 100)
                .cornerRadius(10)
                .onLongPressGesture(minimumDuration: 1.0) {
                    isPressed.toggle()
                }
        }
        .padding()
    }
}
```
###### DragGesture

###### A gesture that detects the movement of a view as the user drags their finger across the screen, allowing the view to follow the drag movement.

```swift
struct DragExample: View {
    @State private var position = CGPoint(x: 100, y: 100)

    var body: some View {
        VStack {
            Text("Drag the circle below")
                .padding(.bottom, 20)

            Circle()
                .fill(Color.orange)
                .frame(width: 100, height: 100)
                .position(position)
                .gesture(
                    DragGesture()
                        .onChanged { value in
                            position = value.location
                        }
                        .onEnded { value in
                            // You can add any additional logic here
                        }
                )
        }
        .padding()
    }
}



```
###### RotationGesture

###### A gesture that detects the rotation of a view using two fingers, allowing the view to be rotated around its center point.


```swift

struct RotationExample: View {
    @State private var angle: Angle = .degrees(0)

    var body: some View {
        VStack {
            Text("Rotate the shape below")
                .padding(.bottom, 20)

            Rectangle()
                .fill(Color.blue)
                .frame(width: 200, height: 100)
                .rotationEffect(angle)
                .gesture(
                    RotationGesture()
                        .onChanged { value in
                            angle = value
                        }
                        .onEnded { value in
                            // You can add any additional logic here
                        }
                )
        }
        .padding()
    }
}




```
###### MagnificationGesture
###### A gesture that detects the pinch-to-zoom action using two fingers, allowing the view to be scaled up or down based on the pinch motion.

```swift
struct MagnificationExample: View {
    @State private var magnification: CGFloat = 1.0

    var body: some View {
        VStack {
            Text("Pinch and zoom the image below")
                .padding(.bottom, 20)
            
            Image("cat") // change image
                .resizable()
                .aspectRatio(contentMode: .fit)
                .frame(width: 200 * magnification, height: 200 * magnification)
                .gesture(
                    MagnificationGesture()
                        .onChanged { value in
                            magnification = value.magnitude
                        }
                        .onEnded { value in
                            // You can add any additional logic here
                        }
                )
        }
        .padding()
    }
}


```

## Advanced Programming in Swift

#### Enum

 
###### Raw values are pre-defined values that are associated with each case and have the same type

```swift
enum Weekday: Int {
    case monday = 1
    case tuesday
    case wednesday
    case thursday
    case friday
    case saturday
    case sunday
}

```
 
###### Enumerations can also have associated values, which allow each case to hold additional data of varying types.

```swift
enum Contact {
    case phone(String)
    case email(String)
    case address(String, Int)
}
```
 
###### To create instances of this enumeration:

```swift
let contact1 = Contact.phone("+1 123-456-7890")
let contact2 = Contact.email("example@example.com")
let contact3 = Contact.address("Main Street", 123)

```
 
###### Enum example 

```swift
import Foundation

// Enum for Pasta Types
enum PastaType: String {
    case spaghetti
    case penne
    case ravioli
    case rigatoni
}

// Enum for Pasta Cooking Status
enum CookingStatus {
    case cooked
    case uncooked
}

// Function to Check if Pasta is Cooked
func checkIfCooked(pasta: PastaType, cookingTime: Int) -> CookingStatus {
    switch pasta {
    case .spaghetti where cookingTime >= 8:
        return .cooked
    case .penne where cookingTime >= 10:
        return .cooked
    case .ravioli where cookingTime >= 11:
        return .cooked
    case .rigatoni where cookingTime >= 12:
        return .cooked
    default:
        return .uncooked
    }
}

// Sample Usage
let pastaType = PastaType.spaghetti
let cookingTime = 7
let cookingStatus = checkIfCooked(pasta: pastaType, cookingTime: cookingTime)

switch cookingStatus {
case .cooked:
    print("\(pastaType.rawValue.capitalized) is cooked, take it out of the water!")
case .uncooked:
    print("\(pastaType.rawValue.capitalized) is not cooked.")
}

```
 
###### Enum example 

```swift
//associated
enum ComputerType: String {
    case laptop = "Laptop"
    case desktop = "Desktop"
    case tablet = "Tablet"
}
//raw value
enum RAMSize: Int {
    case twoGB = 2
    case fourGB = 4
    case eightGB = 8
    case sixteenGB = 16
    case thirtyTwoGB = 32
}

struct Computer {
    let type: ComputerType
    let ramSize: RAMSize
}

let laptopComputer = Computer(type: .laptop, ramSize: .eightGB)

switch laptopComputer.type {
case .laptop:
    print("This is a \(laptopComputer.type.rawValue) with \(laptopComputer.ramSize.rawValue)GB RAM.")
case .desktop:
    print("This is a desktop with \(laptopComputer.ramSize.rawValue)GB RAM.")
case .tablet:
    print("This is a tablet with \(laptopComputer.ramSize.rawValue)GB RAM.")
}

```
 
#### Sets 
###### In Swift, a Set is a collection type used to store unique elements. It resembles an array but allows each element to be stored only once, ensuring data uniqueness. Sets are unordered and can be used for efficient handling of non-repeated values.

```swift

let fruits: Set<String> = ["Apple", "Orange", "Banana", "Apple", "Grapes", "Banana"]


```

<div style="text-align:center;">
  <img width="500" alt="Screenshot" src="https://github.com/rabiaabdioglu/SwiftBasics/assets/75799790/77a4d8b3-e686-4249-8a2f-d9a9b803e79f">
</div>


###### Example usage of Sets 

```swift

var numberSet: Set<Int> = []
var numberSet2: Set<Int> = [1,20,30,4,5]

numberSet.insert(10)
numberSet.insert(20)
numberSet.insert(30)
numberSet.insert(20)
numberSet.insert(30)
// Output: [30, 10, 20]
print(numberSet)

numberSet.remove(10)

// Output: [30, 20]
print(numberSet)

if numberSet.contains(20) {
    numberSet.update(with: 25)
}

// Output: [30, 25]
print(numberSet)
print(numberSet.count)
let numberUnion = numberSet.union(numberSet2)

// Output: [7, 4, 5, 6, 8, 1, 2, 3]
print(numberUnion)


```
 
#### Access-level Modifiers 

###### private - Allows the code within a code definition to access the code.

###### fileprivate - Allows the defining source file to access the code.

###### internal - Allows source files from the defining module to access the code.

###### public - Allows source files from other modules to access the code, however, other modules can’t subclass and override classes.

###### open - Allows source files from other modules to access the code. Other modules can subclass and override classes.
```swift

// ModuleA.swift
public struct Person {
    // Public property accessible from any module that imports ModuleA
    public var name: String
    
    // Internal property accessible within the same module (ModuleA)
    internal var age: Int
    
    // File-private property accessible only within this source file
    fileprivate var address: String
    
    // Private property accessible only within the Person struct
    private var phoneNumber: String
    
    public init(name: String, age: Int, address: String, phoneNumber: String) {
        self.name = name
        self.age = age
        self.address = address
        self.phoneNumber = phoneNumber
    }
}

// ModuleB.swift
import ModuleA

// Accessing public properties from ModuleA
let personA = Person(name: "John", age: 30, address: "123 Main St", phoneNumber: "555-1234")
print(personA.name) // Accessible
print(personA.age) // Not accessible (different module)

// Accessing internal properties from ModuleA
print(personA.address) // Not accessible (different source file)
print(personA.phoneNumber) // Not accessible (private)


```


#### Typecasting 

###### Typecasting in Swift allows flexible programming by converting between different data types. It involves upcasting and downcasting operations for seamless transitions
 

```swift
// Upcasting: Converting a subclass instance to its superclass type
class Vehicle { }
class Car: Vehicle { }

let myCar = Car()
let vehicle: Vehicle = myCar // Upcasting

// Downcasting: Converting a superclass instance to its subclass type
if let car = vehicle as? Car {
    print("Successfully downcasted to Car type.")
} else {
    print("Downcasting failed.")
}


```
 
#### Polymorphism 
###### Polymorphism is the ability of objects of different classes to be treated as objects of a common superclass.


```swift

class Animal {
    func makeSound() {
        print("Unknown sound")
    }
}

class Dog: Animal {
    override func makeSound() {
        print("Woof!")
    }
}

class Cat: Animal {
    override func makeSound() {
        print("Meow!")
    }
}

let animals: [Animal] = [Dog(), Cat(), Dog(), Cat()]

for animal in animals {
    if let dog = animal as? Dog {
        dog.makeSound() // Calls the Dog's makeSound() method
    } else if let cat = animal as? Cat {
        cat.makeSound() // Calls the Cat's makeSound() method
    } else {
        animal.makeSound() // Calls the default makeSound() method in Animal class
    }
}


```
 
###### Example that combines polymorphism, typecasting, access control, and subclassing  

```swift



class ElectronicDevice {
    private(set) var brand: String
    private var storageCapacity: Int
    
    init(brand: String, storageCapacity: Int) {
        self.brand = brand
        self.storageCapacity = storageCapacity
    }
    
    func printInfo() {
        print("Brand: \(brand)")
        print("Storage Capacity: \(storageCapacity) GB")
    }
}

class Computer: ElectronicDevice {
    private var cpuModel: String
    
    init(brand: String, storageCapacity: Int, cpuModel: String) {
        self.cpuModel = cpuModel
        super.init(brand: brand, storageCapacity: storageCapacity)
    }
    
    override func printInfo() {
        super.printInfo()
        print("CPU Model: \(cpuModel)")
    }
}

class Tablet: ElectronicDevice {
    private var screenSize: Double
    
    init(brand: String, storageCapacity: Int, screenSize: Double) {
        self.screenSize = screenSize
        super.init(brand: brand, storageCapacity: storageCapacity)
    }
    
    override func printInfo() {
        super.printInfo()
        print("Screen Size: \(screenSize) inches")
    }
}

class Smartphone: ElectronicDevice {
    private var hasFaceRecognition: Bool
    
    init(brand: String, storageCapacity: Int, hasFaceRecognition: Bool) {
        self.hasFaceRecognition = hasFaceRecognition
        super.init(brand: brand, storageCapacity: storageCapacity)
    }
    
    override func printInfo() {
        super.printInfo()
        print("Face Recognition: \(hasFaceRecognition ? "Yes" : "No")")
    }
}

let computer = Computer(brand: "ABC Computers", storageCapacity: 512, cpuModel: "Intel Core i5")
let tablet = Tablet(brand: "XYZ Tablets", storageCapacity: 256, screenSize: 10.5)
let smartphone = Smartphone(brand: "Phone Inc.", storageCapacity: 128, hasFaceRecognition: true)

let devices: [ElectronicDevice] = [computer, tablet, smartphone]

for device in devices {
    device.printInfo()
    print("------")
}

```
 
#### Protocol
###### Protocols in Swift define a blueprint of methods, properties, and other requirements that a class or struct must adhere to. They allow for the creation of generic code, enabling different types to conform to the same protocol, facilitating polymorphism and code reusability.

```swift
// Define a protocol named Animal
protocol Animal {
    var name: String { get }
    var sound: String { get }
    
    func makeSound()
}

// Create a class conforming to the Animal protocol
class Dog: Animal {
    var name: String
    var sound: String
    
    init(name: String) {
        self.name = name
        self.sound = "Woof"
    }
    
    func makeSound() {
        print("\(name) says \(sound)")
    }
}

// Create another class conforming to the Animal protocol
class Cat: Animal {
    var name: String
    var sound: String
    var weight: Int
    
    init(name: String, weight: Int) {
        self.name = name
        self.sound = "Meow"
        self.weight = weight
    }
    
    func makeSound() {
        print("\(name) says \(sound)")
    }
}

// Usage of the protocol
let dog = Dog(name: "Buddy")
let cat = Cat(name: "Whiskers", weight: 5)

dog.makeSound() // Output: Buddy says Woof
cat.makeSound() // Output: Whiskers says Meow
print(cat.weight)

```
 
#### Optional Protocol
###### There is a music app that can play different types of media (songs, podcasts and audiobooks). There is a Player class that can execute these different media types, and also other classes should notify when a media item has finished playing. That's why @objc is used.
  
```swift
// Step 1: Define the PlayerDelegate protocol
@objc protocol PlayerDelegate {
    func playerDidFinishPlaying()
    @objc optional func playerDidEncounterError(error: Error)
}

// Step 2: Create the Player class
class Player {
    var delegate: PlayerDelegate?
    
    func playMedia() {
        // Simulate media playback
        print("Playing media...")
        
        // Simulate media playback finishing
        delegate?.playerDidFinishPlaying()
        
        // Simulate an error during playback
        let error = NSError(domain: "com.example.musicapp", code: 100, userInfo: [NSLocalizedDescriptionKey: "An error occurred during playback."])
        delegate?.playerDidEncounterError?(error: error)
    }
}

// Step 3: Conform to the PlayerDelegate protocol in another class
class NowPlayingViewController: PlayerDelegate {
    func playerDidFinishPlaying() {
        print("Now Playing View: Media finished playing.")
        // Update UI with the currently playing media information
    }
    
    func playerDidEncounterError(error: Error) {
        print("Now Playing View: Encountered error during playback - \(error.localizedDescription)")
        // Show an error message to the user
    }
}

// Step 4: Instantiate the Player and NowPlayingViewController
let player = Player()
let nowPlayingViewController = NowPlayingViewController()

// Step 5: Set the NowPlayingViewController as the delegate of the Player
player.delegate = nowPlayingViewController

// Step 6: Play the media
player.playMedia()

```
 
#### Property and newValue

```swift

class Table {
    private var _area: Double = 0.0
    
    var area: Double {
        get {
            return _area
        }
        set(newValue) {
            if newValue < 0 {
                print("Warning: Table area cannot be negative. Setting it to zero.")
                _area = 0
            } else {
                _area = newValue
            }
        }
    }
}

let table = Table()
table.area = 120.0
print("Table Area: \(table.area)") // Output: Table Area: 120.0
table.area = -50.0 // Output: Warning: Table area cannot be negative. Setting it to zero.

print("Table Area: \(table.area)") // Output: Table Area: 0.0 (because it was set to zero in the set block)

table.area = 80.0
print("Table Area: \(table.area)") // Output: Table Area: 80.0

```
 
#### didSet 

```swift


class Table {
    var size: Int {
        didSet {
            if size < 4 {
                print("Warning: The table size is too small.")
            } else {
                print("Table size is set to \(size).")
            }
        }
    }
    
    init(size: Int) {
        self.size = size
    }
}

let table = Table(size: 6)
table.size = 3
print("Table size: \(table.size)")
// Output: Table size: 3 (the didSet block prevented it from being set to a smaller value)





```

 
#### Delegate 

```swift



// Protocol for Weather updates
protocol WeatherManagerDelegate: AnyObject {
    func didUpdateWeather(_ weather: Weather)
    func didFailWithError(_ error: Error)
}

// Weather Manager Class
class WeatherManager {
    
    weak var delegate: WeatherManagerDelegate?
    
    func fetchWeatherData(for city: String) {
        // Simulate API call and data retrieval
        let temperature = 25.0
        let weatherDescription = "Sunny"
        let weather = Weather(temperature: temperature, description: weatherDescription)
        
        // Notify the delegate about the updated weather
        delegate?.didUpdateWeather(weather)
    }
}

// Weather Data Model
struct Weather {
    let temperature: Double
    let description: String
}

// Weather View Controller
class WeatherViewController: WeatherManagerDelegate {
    
    let weatherManager = WeatherManager()
    
    func viewDidLoad() {
        weatherManager.delegate = self
        
        // Fetch weather data for a specific city
        weatherManager.fetchWeatherData(for: "New York")
    }
    
    func didUpdateWeather(_ weather: Weather) {
        print("Temperature: \(weather.temperature)°C")
        print("Description: \(weather.description)")
    }
    
    func didFailWithError(_ error: Error) {
    }
}

// Test using the WeatherViewController
let weatherVC = WeatherViewController()
weatherVC.viewDidLoad()

 
```
 
#### throwable functions 

```swift

enum DivideError: Error {
    case divisionByZero
}

func divide(_ numerator: Int, by denominator: Int) throws -> Int {
    guard denominator != 0 else {
        throw DivideError.divisionByZero
    }
    
    return numerator / denominator
}

do {
    let result = try divide(10, by: 2)
    print("Result: \(result)")
} catch DivideError.divisionByZero {
    print("Error: Division by zero is not allowed.")
} catch {
    print("An unknown error occurred.")
}
 
```
 
#### Error Handling 

```swift
enum CustomError: Error {
    case someError
}

func mayThrowError() throws {
    throw CustomError.someError
}

//try
do {
    try mayThrowError()
    print("Success")
} catch {
    print("Error: \(error)")
}

//try!
let result = try! mayThrowError()
print("Success: \(result)")

//try?
let result = try? mayThrowError()
print("Result: \(result)") // Output: Result: nil

```
 
#### Functional programming 
#### Map, filter and reduce

```swift


let numbers = [1, 5, 9, 12, 7, 3, 15]

// Double each number
let doubledNumbers = numbers.map { $0 * 2 }
// Output: [2, 10, 18, 24, 14, 6, 30]

// Use compactMap to convert strings to integers and filter out non-integer values
let strings = ["1", "5", "9", "12", "7", "3", "15"]
let convertedNumbers = strings.compactMap { Int($0) }
// Output: [1, 5, 9, 12, 7, 3, 15]

// Use flatMap to flatten the nested arrays into a single array (Note: 'numbers' is not a nested array)
let flattenedArray = numbers.flatMap { [$0] }
// Output: [1, 5, 9, 12, 7, 3, 15]

// Filter numbers greater than 10
let filteredNumbers = doubledNumbers.filter { $0 > 10 }
// Output: [18, 24, 14, 30]

// Sum all the remaining numbers
let sum = filteredNumbers.reduce(0, +)
// Output: 56 (18 + 24 + 14 + 30)

print(sum) // Output: 56


```
 
###### Example 
```swift

struct Product {
    let name: String
    let price: Int
    let category: String
}

func totalRevenueOf(products: [Product], category: String) -> Int {
    let productsInCategory = products.filter { $0.category == category }
    
    let productPrices = productsInCategory.map { $0.price }
    
    return productPrices.reduce(0, +)
}

let products = [
    Product(name: "iPhone", price: 1000, category: "Electronics"),
    Product(name: "Headphones", price: 150, category: "Electronics"),
    Product(name: "T-Shirt", price: 25, category: "Apparel"),
    Product(name: "Jeans", price: 70, category: "Apparel"),
    Product(name: "Book", price: 20, category: "Books"),
]

let result = totalRevenueOf(products: products, category: "Electronics")
print("Total revenue for Electronics category: $\(result)")

```
 
###### Example 
```swift
func add(_ a: Int, _ b: Int) -> Int {
    return a + b
}

```
 
#### Test 

```swift
import XCTest

class MyMathTests: XCTestCase {

    func testAddition() {
        XCTAssertEqual(add(2, 3), 5, "Adding 2 and 3 should be equal to 5")
        XCTAssertEqual(add(0, 0), 0, "Adding 0 and 0 should be equal to 0")
        XCTAssertEqual(add(-5, 5), 0, "Adding -5 and 5 should be equal to 0")
        XCTAssertEqual(add(10, -3), 7, "Adding 10 and -3 should be equal to 7")
    }
    
    func testAdditionWithLargeNumbers() {
        XCTAssertEqual(add(1000000, 500000), 1500000, "Adding large numbers should work correctly")
    }

    static var allTests = [
        ("testAddition", testAddition),
        ("testAdditionWithLargeNumbers", testAdditionWithLargeNumbers)
    ]
}

// Run the tests
XCTMain([testCase(MyMathTests.allTests)])
```
#### Using Fakes
###### Using fakes, also known as test doubles, is a technique in unit testing where you replace certain dependencies or collaborators of the code being tested with simplified implementations that provide controlled and predictable behavior. 


###### Example 

```swift
import XCTest

// Protocol to represent a data repository
protocol DataRepository {
    func fetchData() -> [String]
}

// Real implementation of the data repository
class RealDataRepository: DataRepository {
    func fetchData() -> [String] {
        // Simulate fetching data from a database or network
        // For this example, we will return some hardcoded data
        return ["Item 1", "Item 2", "Item 3"]
    }
}

// Fake implementation of the data repository for testing
class FakeDataRepository: DataRepository {
    func fetchData() -> [String] {
        // Return different data for testing purposes
        return ["Test Item 1", "Test Item 2", "Test Item 3"]
    }
}

// Example of a class that uses the data repository
class DataManager {
    private let repository: DataRepository
    
    init(repository: DataRepository) {
        self.repository = repository
    }
    
    func displayData() -> [String] {
        return repository.fetchData()
    }
}

// Unit Tests
class DataManagerTests: XCTestCase {
    func testRealData() {
        let realRepository = RealDataRepository()
        let dataManager = DataManager(repository: realRepository)
        let data = dataManager.displayData()
        XCTAssertEqual(data, ["Item 1", "Item 2", "Item 3"])
    }
    
    func testFakeData() {
        let fakeRepository = FakeDataRepository()
        let dataManager = DataManager(repository: fakeRepository)
        let data = dataManager.displayData()
        XCTAssertEqual(data, ["Test Item 1", "Test Item 2", "Test Item 3"])
    }
}

// Run the tests
DataManagerTests.defaultTestSuite.run()


```
 
## Working With Data


#### URL



###### URLComponents


###### Scheme: Describes the protocol of the website 

###### Host: Sets the main domain name

###### Path: Defines the particular website component, like images

```swift



var components = URLComponents()
components.scheme = "https"
components.host = "google.com"
components.path = "/images"
let url = components.url



```

###### URLSessionDownloadTask

```swift
import Foundation

let imageURLString = "https://www.example.com/image.jpg"
guard let imageURL = URL(string: imageURLString) else {
    fatalError("Invalid URL")
}

let task = URLSession.shared.downloadTask(with: imageURL) { localURL, response, error in
    if let error = error {
        print("Error: \(error)")
        return
    }

    guard let localURL = localURL else {
        print("No file downloaded")
        return
    }

    // Handle the downloaded file at 'localURL'
}

task.resume()


```


#### HTTP Request 


###### Basic HTTP Request and JSON Data Handling Example in Swift 


```swift

import Foundation

struct Todo: Codable {
    let userId: Int
    let id: Int
    let title: String
    let completed: Bool
}

let todoUrlString = "https://jsonplaceholder.typicode.com/todos/1"
guard let todoUrl = URL(string: todoUrlString) else {
    fatalError("Invalid URL")
}

let task = URLSession.shared.dataTask(with: todoUrl) { data, response, error in
    if let error = error {
        print("Error: \(error)")
        return
    }
    
    guard let data = data else {
        print("No data received")
        return
    }
    
    do {
        let todo = try JSONDecoder().decode(Todo.self, from: data)
        print("UserId: \(todo.userId)")
        print("Id: \(todo.id)")
        print("Title: \(todo.title)")
        print("Completed: \(todo.completed)")
    } catch {
        print("Error decoding JSON: \(error)")
    }
}

task.resume()



```
 


#### JSON

###### Basic Example




```swift

import Foundation


// JSON mapped using custom property names

let JSONExample = """
{
    "username": "xxxxx",
    "name": "XXX",
    "email" : "xxxx@gmail.com",
    "url" : "https://github.com/rabiaabdioglu/SwiftBasics"
}
"""

struct User: Decodable {
    enum CodingKeys: String, CodingKey { case
        username, name, email,
        url = "url"
    }
    
    
    let username: String
    let name: String
    let email: String
    let url: String
    }

let data = JSONExample.data(using: .utf8)!
let user = try! JSONDecoder().decode(User.self, from: data)
print(user)



```
 
#### JSON Decoding


```swift


import Foundation

let booksJSONString = """
[
    {
        "title": "1984",
        "author": "George Orwell",
        "genre": "Dystopian",
        "rating": 4.8
    },
    {
        "title": "To Kill a Mockingbird",
        "author": "Harper Lee",
        "genre": "Classic",
        "rating": 4.9
    },
    {
        "title": "The Great Gatsby",
        "author": "F. Scott Fitzgerald",
        "genre": "Classic",
        "rating": 4.7
    }
]
"""

struct Book: Decodable {
    let title: String
    let author: String
    let genre: String
    let rating: Double
}

let booksData = Data(booksJSONString.utf8)
let decoder = JSONDecoder()
let books = try! decoder.decode([Book].self, from: booksData)
books.forEach {
    print("\($0.title) by \($0.author) - Genre: \($0.genre), Rating: \($0.rating)")
}

```
 
#### Fetch Image from JSON API in SwiftUI

###### This SwiftUI code demonstrates how to fetch images from a JSON API by entering an index and displaying the corresponding image
```swift


import SwiftUI

// Define a struct to represent the image data
struct ImageData: Decodable {
    let id: Int
    let title: String
    let url: URL
}

struct ImageView: View {
    @State private var image: Image? // Placeholder image
    @State private var indexText: String = ""
    
    var body: some View {
        VStack {
            TextField("Enter index", text: $indexText)
                .textFieldStyle(RoundedBorderTextFieldStyle())
                .padding()
            
            Button("Get Image") {
                fetchImage()
            }
            
            if let image = image {
                image
                    .resizable()
                    .scaledToFit()
            } else {
                Image(systemName: "photo")
                    .resizable()
                    .scaledToFit()
            }
        }
        .padding()
    }
    
    func fetchImage() {
        guard let index = Int(indexText) else {
            print("Invalid index")
            return
        }
        
        let jsonURLString = "https://jsonplaceholder.typicode.com/photos"
        
        guard let url = URL(string: jsonURLString) else {
            print("Invalid URL")
            return
        }
        
        URLSession.shared.dataTask(with: url) { data, response, error in
            if let error = error {
                print("Error fetching data: \(error)")
                return
            }
            
            guard let data = data else {
                print("No data received")
                return
            }
            
            do {
                let imageArray = try JSONDecoder().decode([ImageData].self, from: data)
                if let requestedImage = imageArray.first(where: { $0.id == index }),
                   let imageData = try? Data(contentsOf: requestedImage.url),
                   let uiImage = UIImage(data: imageData) {
                    DispatchQueue.main.async {
                        self.image = Image(uiImage: uiImage)
                    }
                } else {
                    print("Failed to fetch and display the image")
                }
            } catch {
                print("Error decoding JSON: \(error)")
            }
        }.resume()
    }
}

struct JSONImage: View {
    var body: some View {
        VStack {
            Text("Fetched Image:")
            ImageView()
        }
    }
}

struct JSONImage_Previews: PreviewProvider {
    static var previews: some View {
        JSONImage()
    }
}




```
 
#### Core Data

###### Core Data entities and relationships


###### One-to-One
###### A one-to-one relationship means that each instance of one entity is related to one instance of another entity. For example, a "Person" entity may have a one-to-one relationship with an "Address" entity.
######
###### One-to-Many
###### A one-to-many relationship signifies that each instance of one entity is related to multiple instances of another entity. For instance, a "Department" entity may have a one-to-many relationship with "Employees" entities.
######
###### Many-to-Many
###### A many-to-many relationship represents that each instance of one entity can be related to multiple instances of another entity, and vice versa. For example, a "Student" entity may have a many-to-many relationship with a "Course" entity.



###### Fetching from Core Data


```swift



import CoreData

func fetchNotes() -> [Note] {
    let request: NSFetchRequest<NoteEntity> = NoteEntity.fetchRequest()
    do {
        let notes = try context.fetch(request)
        return notes.map { Note(id: $0.id, title: $0.title ?? "", content: $0.content ?? "") }
    } catch {
        print("Error fetching notes: \(error)")
        return []
    }
}


```

###### Update Data in Core Data



```swift



func updateNote(note: Note) {
    let request: NSFetchRequest<NoteEntity> = NoteEntity.fetchRequest()
    request.predicate = NSPredicate(format: "id == %@", note.id as CVarArg)
    do {
        let result = try context.fetch(request)
        if let existingNote = result.first {
            existingNote.title = note.title
            existingNote.content = note.content
            try context.save()
        }
    } catch {
        print("Error updating note: \(error)")
    }
}
```

###### Delete Data in Core Data


```swift


func deleteNote(note: Note) {
    let request: NSFetchRequest<NoteEntity> = NoteEntity.fetchRequest()
    request.predicate = NSPredicate(format: "id == %@", note.id as CVarArg)
    do {
        let result = try context.fetch(request)
        if let existingNote = result.first {
            context.delete(existingNote)
            try context.save()
        }
    } catch {
        print("Error deleting note: \(error)")
    }
}

```

###### Filtering


```swift

func fetchPersonsWithNameContainingNur() -> [Person] {
    let fetchRequest: NSFetchRequest<Person> = Person.fetchRequest()
    
    let predicate = NSPredicate(format: "name CONTAINS[c] %@", "el")
    
    fetchRequest.predicate = predicate
    
    do {
        let personsWithNameContainingNur = try context.fetch(fetchRequest)
        return personsWithNameContainingNur
    } catch {
        print("Error fetching persons with name containing 'nur': \(error)")
        return []
    }
}


```
 
###### Sorting


```swift


// Function to fetch sorted persons using NSSortDescriptor
func fetchSortedPersons() -> [Person] {
    let fetchRequest: NSFetchRequest<Person> = Person.fetchRequest()
    
    // Create the sort descriptor
    let sortDescriptor = NSSortDescriptor(key: "name", ascending: true,selector: #selector(NSString.localizedCompare))
    
    // Set the sort descriptors in the fetch request
    fetchRequest.sortDescriptors = [sortDescriptor]
    
    do {
        // Fetch the sorted persons
        let sortedPersons = try context.fetch(fetchRequest)
        return sortedPersons
    } catch {
        print("Error fetching sorted persons: \(error)")
        return []
    }
}

```



