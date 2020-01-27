# Pair Project

# Functional requirements

Design and implement a program called RainfallV2 that reads a list of floating-point numbers from the standard input (console) representing daily rainfall amounts in millimeters as entered by a user. Ignore negative values, but include zero values. Produce the following statistics based on the non-negative values in the list up to end of file:

- total number of (nonnegative) values read
- average rainfall
- cumulative rainfall
- number of rainy days (defined as above the daily average)
- number of dry days (defined as at most 5% of the daily average)

Input items (whole and/or floating point numbers) can be spread over one or more lines. If there is at least one input item, the program prints the resulting statistics and exits. If there is no valid numerical input item, the program prints nothing and exits.

# Nonfunctional requirements

- Performance: 
  - Time: For each additional input item, the program should produce a small, finite number of steps.
  - Space: For each additional input item, the program should use at most a constant amount of space.
- Testability: Your program could support automatic unit testing of the core functionality, without the user entering any data or reading any data from an external file.

Implement your solution to the recurring rainfall problem as a working Java program using JUnit for testing.

- Define separate classes for main (i/o), core logic, and testing.
- Define a class called RainfallStats for representing the statistics given above as a single object.
- In the core logic class, define a (static) method that takes a List (important: List, not just an ArrayList) and returns a RainfallStats instance.
- In main, read the data into a list, initialized as an empty ArrayList, invoke the method for generating the stats, and print the resulting stats.
- For testing, use Arrays.asList(x1, x2, ...) to programmatically create suitable sample test data, then use assertions (such as assertEquals) on the individual stats.

# Reflection

- Why do we have to store the input items to provide the required functionality?
- Why does the user no longer need to specify the item count up front?
- What is the key capability of Java lists, such as ArrayList, that makes it a better choice for this solution than basic native arrays?
- What is the purpose of the RainfallStats class in terms of helping with maintainability and testability?
- Why does the core method need to take a List instead of just an ArrayList?

# Submission

- Make sure you have created a separate project for this activity. 
- Include a project-specific readme file including your reflection and any other thoughts or design decisions. 
- In IDEA, export your project as a zip file and attach here. 

# Grading (total 5)

- 2 submission exists
- 0.5 correct average calculation for one or more inputs
- 0.5 empty output (rather than NaN or error) for empty input
- 0.5 detect EOF (rather than specific sentinel value) following Scanner-based idiom
- 0.5 input can have zero or more double values on each line
- 0.5 good coding style (indentation, use of final everywhere except when a variable has to be updated one or more times)
- 0.5 meaningful reflection (one or more sentences per item) in separate readme file