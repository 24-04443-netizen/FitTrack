Overview

FitTrack is a Java-based fitness tracking and routine-generation system designed to help users monitor their fitness goals and maintain personalized workout plans. The program allows users to register, log in, and generate routines based on their fitness objective: weight loss, weight gain, or muscle building. Using object-oriented principles, the system suggests appropriate workouts and foods, saves user-selected routines, and lets users view or delete previously saved records.
This system aims to simplify fitness planning by providing structured recommendations and allowing users to record their progress conveniently.

OOP Concepts Applied

1 Abstraction
The program uses the abstract class RoutinePlan to define general behaviors (suggestWorkouts() and suggestFoods()) shared by all fitness plans. The specific details are hidden from the user and implemented only in the subclasses (WeightLossPlan, WeightGainPlan, MuscleGainPlan).
This allows different plan types to share the same structure while hiding internal logic.
2 Inheritance
The three fitness plan classes (WeightLossPlan, WeightGainPlan, MuscleGainPlan) inherit from the abstract parent class RoutinePlan.
They reuse the goal property and override the abstract methods to provide their own recommendations.
3 Polymorphism
The variable RoutinePlan plan can store objects of any subclass (WeightLossPlan, WeightGainPlan, MuscleGainPlan).
When calling methods such as suggestWorkouts() or suggestFoods(), Java automatically executes the correct version depending on the plan selected by the user.
This allows flexible behavior while using a single reference type.
4 Encapsulation
The User class demonstrates encapsulation using private fields (username, password, loggedIn) and public getter and login methods.
Sensitive data cannot be accessed or modified directly; instead, interaction occurs through controlled methods like login(), logout(), and isLoggedIn().
This protects data integrity and prevents unauthorized modifications.

Program Structure

Main Classes and Their Roles
• Main – Controls the overall program flow, menu navigation, input handling, and linking of all system features.
• User – Stores user information and handles login/logout functionality.
• RoutinePlan (abstract) – Base class representing a generic fitness plan with required methods for foods and workouts.
• WeightLossPlan, WeightGainPlan, MuscleGainPlan – Concrete subclasses providing specific workouts and foods for each goal.
• RoutineRecord – A model class representing a saved routine, including workout, food, goal, number of days, and timestamp.
Class Relationships (Text-Based Diagram)
RoutinePlan (abstract) / | \ / | \ WeightLossPlan WeightGainPlan MuscleGainPlan (inherit RoutinePlan) User ----> manages login/logout Main ----> controls program flow ----> creates RoutinePlan subclasses ----> stores RoutineRecord objects RoutineRecord ----> holds saved routine data 

How to Run the Program

• Open any Java-supported IDE or command-line terminal.
• Save the file as Main.java.
• Compile the program: javac Main.java 
• Run the program: java Main 
• Follow the menu: 
• Register an account
• Log in
• Choose a fitness goal
• Select recommended workouts and food
• Save, view, or delete routines
• Logout or exit

Sample Output

===== FITTRACK SYSTEM =====
[1] Register
[2] Login & Generate Routine
[3] Add Routine (must be logged in)
[4] View Saved Routines
[5] Delete Routine
[6] Logout
[7] Exit Program
Enter choice: 1
Enter username: aira
Enter password: 123
Registration successful! You may now log in.

===== FITTRACK SYSTEM =====
[1] Register
[2] Login & Generate Routine
[3] Add Routine (must be logged in)
[4] View Saved Routines
[5] Delete Routine
[6] Logout
[7] Exit Program
Enter choice: 2
Username: aira
Password: 123
Login successful! Welcome, aira.
Enter your age (years): 19
Enter your weight (kg): 40

Choose Goal:
[1] Lose Weight
[2] Gain Weight
[3] Build Muscle
Select (1-3): 2

--- Recommended Workouts ---
[1] Light Strength Training
[2] Low-Intensity Full Body Workout
Choose workout by number: 1

--- Recommended Foods ---
[1] High-Calorie Rice Meals
[2] Pasta
[3] Healthy Fats (nuts, avocado)
[4] Full-fat Dairy
Choose food by number: 1
How many days should this routine be performed? 5

Routine saved successfully!
Goal: Gain Weight
Workout: Light Strength Training
Food: High-Calorie Rice Meals
Days to Perform: 5
Saved On: 2025-12-02 04:16:53

===== FITTRACK SYSTEM =====
[1] Register
[2] Login & Generate Routine
[3] Add Routine (must be logged in)
[4] View Saved Routines
[5] Delete Routine
[6] Logout
[7] Exit Program
Enter choice: 3
Add another routine:
Enter your age (years): 19
Enter your weight (kg): 40

Choose Goal:
[1] Lose Weight
[2] Gain Weight
[3] Build Muscle
Select (1-3): 3

--- Recommended Workouts ---
[1] Weight Lifting (Compound lifts)
[2] Resistance Training (3 sets)
Choose workout by number: 2

--- Recommended Foods ---
[1] Steak / Lean Beef
[2] Eggs
[3] Protein Shake
[4] Brown Rice
Choose food by number: 1
How many days should this routine be performed? 3

Routine saved successfully!
Goal: Build Muscle
Workout: Resistance Training (3 sets)
Food: Steak / Lean Beef
Days to Perform: 3
Saved On: 2025-12-02 04:17:28

===== FITTRACK SYSTEM =====
[1] Register
[2] Login & Generate Routine
[3] Add Routine (must be logged in)
[4] View Saved Routines
[5] Delete Routine
[6] Logout
[7] Exit Program
Enter choice: 6
You have been logged out.

===== FITTRACK SYSTEM =====
[1] Register
[2] Login & Generate Routine
[3] Add Routine (must be logged in)
[4] View Saved Routines
[5] Delete Routine
[6] Logout
[7] Exit Program
Enter choice: 7
Program terminated. Goodbye!

=== Code Execution Successful ===


Acknowledgement
	
	 We would like to express our deepest appreciation to our instructor for her guidance and support throughout this semester and the completion of this project. We would also like extend our gratitude to our classmates and peers for their unwavering support that brought us motivation and encouragement during the progress of this project.

Disclaimer
	
	This project and its contents are provided for example and learning purposes only. Students are encouraged to use it as a reference and not copy it in its entirety.

Contributors

Jermae Balmes
France Javier
Aira Camino
	
	
