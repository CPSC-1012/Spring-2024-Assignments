# Winter 2024 Assignment 03 - Methods, Arrays, and File I/O
__Weight:__ 15% of final mark

__Submission requirements:__ On or before the deadline, commit a Visual Studio 2022 project to the GitHub repository. __You must commit and push to the classroom repository supplied for the assignment__; do not create your own repository. It is your responsibility to ensure that your work is in the correct repository. ___Work not in the repository will not be graded___.

## Context
A friend of yours sells has a small business with up to 25 employees, depending on the time of year. They need help building a sound financial system to create weekly pay slips. They shared with you that it would be nice to have a program that could produce such a system. After hearing about their plight, you offer your expertise to help them by building a program to help them out. It should be simple enough ...

### Requirements

Your program must meet the following requirements:

- Must allow the user to enter an employee weekly hours
- Must allow the user to alter an employee weekly hours
- Must allow the user to save the employee information (name, tax status, wage and weekly hours) to a weekly file
- Must allow the user to load a previously saved weekly file
- Must allow the user to view the current employee information in the program (name, status, wage and hours)
- Must allow the user to calculate and dislay a weekly pay slip for an employee
- Must allow the user to load a given list of employees from a file (name, status, and wage)

## Implementation Details

You will be provided with a starter project for this assignment ([Assignment3Starter.zip](./Assignment3Starter.zip)). Your job will be to complete the missing requirements where indicated. There are a number of tasks that are all identified by `// TODO: ` comments throughout the Program.cs file.

The program makes use of a main menu for user options. The program should continue to run until the user chooses to quit the program. Ask the user to supply the desired filename, when the program starts, that will hold the weekly hour data (Name, Status, Wage, Hours).

A second file has been supplied which contains the current employee list (Name, Status) to be used to initialize your employee information (name and status) when creating new weekly hours. 

Use three parallel arrays for storing the data in your program (one for names values, one for tax status and one for
corresponding hourly values). Keep an accurate record count for the number of employees that have
been loaded/entered.

The format of the weekly data files should be as follows (assume valid file format for input):

- Employee name
- Employee Tax Status
- Employee weekly hours (to one decimal place)

_Sample weekly data file format_

```sh
Shirley Ujest,Family,38.2
Lowand Behold,Family,43.5
Pat Downe,Single,38.2
Ima Stew-Dent,Student,18.0
Charity Kase,Married,33.6
...
```
_Sample employee list file format_

```sh
Shirley Ujest,Family
Lowand Behold,Family
Pat Downe,Single
Ima Stew-Dent,Student
Charity Kase,Married
...
```

You will use a modular approach when constructing this program. Ensure that, at a minimum, the
following methods are present and used (difficulty level is rated 1-easy, 2-moderate, 3-challenging):

- **void DisplayMainMenu()** --> displays the main menu options [difficulty 1]
- **string Prompt(string promptString)** --> displays the prompt string and returns user-entered string
(allow empty string to be returned) [difficulty 1]
- **double PromptDouble(string promptString)** --> displays the prompt string and returns user-entered
double (ensure that the program does not crash and always returns a valid double value)
[difficulty 1]
- **int LoadEmployees(string[] names, string[] status, double[] wages, double[] hours, string filename)** --> used when creatly a new weekly set of data; reads the current employee list file and loads the employee name, status and wage into their appropriate arrays; set the hours array to zero; returns the number of employees loaded [difficulty 2]
- **int LoadWeeklyFile(string[] names, string[] status, double[] wages, double[] hours, string filename)** --> loads the records from an existing weekly file
(filename) into the associative arrays used by the program; returns the record count (i.e. how
many employees were loaded) [difficulty 2]
- **void SaveWeeklyFile(string[] names, string[] status, double[] wages, double[] hours, string filename, int countOfEntries)** --> writes the
associative array data to a weekly file (filename) in the correct format [difficulty 2]
- **void DisplayWeeklyHours(string[] names, string[] status, double[] wages, double[] hours, int countOfEntries)** --> displays the current entered/loaded employee entries in a formatted table (i.e. ensure that proper columns and alignment are used). __You must use a for loop to loop through the arrays and produce the display__ [difficulty 2]
- **void EditWeeklyEntries(string[] names, double{} hours, int countOfEntries)** --> allows the user to view all current weekly entries and choose one to edit the employee weekly hours (i.e. overwrite hours) [difficulty 3]
- **void EmployePaySlip(string[] names, string[] status, double[] wages, double[] hours, int countOfEntries)** --> allows the user to view all current weekly entries and choose one to calculate and display the weekly pay slip for the employee. [difficulty 3]


The program should never crash and must deal with errors gracefully.

__Aside from what’s been presented in this document, do not make any assumptions. Seek clarity from your instructor if you do not understand something in this document.__

## Coding Requirements
- A C# comment block at the beginning of the source file describing the purpose, author, and last modified date of the program
- Write only one statement per line
- You must use four corresponding/parallel arrays for names, tax status, wages and weekly hours in your solution
- Use camelCase/PascalCase (dependent on instructor choice) for local variable names
- Use TitleCase for any constant variable names
- Use defensive programming where necessary
- Ensure graceful handling of exceptions
- All methods must be defined as **static** methods
- Include summary comments for all defined methods (these must be complete and include param and returns where appropriate)

### Sample Runs

#### Sample Program Run
_NOTE: the sample runs do not demonstrate exception handling, ensure your program handles exceptions gracefully and does not crash._

#### Enter values, perform analysis, and save file
![Enter values, perform analysis, and save file](images/assign3-1.gif)

#### Load file and edit entries
![Load file and edit entries](images/assign3-2.gif)

## Submission
Commit and push your solution to your GitHub classroom assignment repository before the deadline. Ensure that your solution follows the best coding and style practices, as your instructor has shown you in class. Failed adherence to the prescribed style guidelines may result in lost marks. __Your program must compile; a program that fails to compile will not be graded.__

_NOTE: push early and often to your repository to recieve feedback from your instructor prior to the deadline. Your instructor will not be providing feedback for every commit every day. However, the eariler and more often you commit, the greater the chances of your instructor reviewing your work and providing constructive feedback that you can act on before the deadline._

## Rubric [25 Marks Total]
### Program Completion and Modularization
| Mark | Description |
|---|---|
| 15 | Outstanding - program exhibits all requirements for Excellent, meets all course standards, no errors  |
| 13-14  | Excellent – program implements, at a minimum, all three difficulty 1 methods, all four difficulty 2 methods, 1 difficulty 3 method (total 8). Methods are correctly implemented, including proper documentation comments, and are called appropriately in the main program. Functionality of each method is correct and each task is fully implemented (e.g. returns expected values, proper file read/write, proper array management, etc.). Meets all course standards, no errors. |
| 10-12  | Very Good – program implements, at a minimum, three difficulty 1 methods, three difficulty 2 methods, 1 difficulty 3 method (total 7). Methods are correctly implemented, including proper documentation comments, and are called appropriately in the main program. Functionality of each method is correct and each task is fully implemented (e.g. returns expected values, proper file read/write, proper array management, etc.). Meets all course standards, no errors.|
| 7-9  | Acceptable – program implements, at a minimum, three difficulty 1 methods and three difficulty 2 methods (total 6). Methods are correctly implemented, including proper documentation comments, and are called appropriately in the main program. Functionality of each method is correct and each task is fully implemented (e.g. returns expected values, proper file read/write, proper array management, etc.). Meets all course standards, no errors. |
| 4-6  | Needs Work – program implements, at a minimum, three difficulty 1 methods and two difficulty 2 methods (total 5). Methods are correctly implemented, including proper documentation comments, and are called appropriately in the main program. Functionality of each method is correct and each task is fully implemented (e.g. returns expected values, proper file read/write, proper array management, etc.). Meets all course standards, minor errors. |
| 1-3  | Unsatisfactory – program implements, at a minimum, three difficulty 1 methods. Methods are correctly implemented, including proper documentation comments, and are called appropriately in the main program. Functionality of each method is correct and each task is fully implemented (e.g. returns expected values, proper file read/write, proper array management, etc.). Does not meets all course standards, minor errors. |
| 0  | Not done; poorly attempted; program implements none (0) of the required methods. Does not meets all course standards, major errors. |

### Array Implementation
| Mark | Description |
|---|---|
| 5  | Excellent – program implements and correctly uses associative arrays; correct elementcount is kept; arrays are correctly loaded and traversed for output. |
| 4  | Very Good – program implements and correctly uses associative arrays; element count is always accurate; arrays are correctly loaded and traversed for output; pay slip may contain a minor error |
| 3  | Acceptable – program implements and correctly uses associative arrays; element count is accurate in most cases; arrays are correctly loaded and traversed for output in most cases; pay slip may contain minor errors |
| 2  | Needs Work – program implements and uses associative arrays; element count is not accurate; program suffers from minor error(s) when loading or traversing arrays for output; contains major error(s) |
| 1  | Unsatisfactory – program implements and uses insufficient arrays; element count is not accurate; program suffers from major error(s) when loading or traversing arrays for output; contains major error(s) |
| 0  | Not done; poorly attempted; major logic errors; major design problems; program does not implement any arrays. |

### FileI/O Implementation
| Mark | Description |
|---|---|
| 5  | Excellent – program correctly reads and writes files as required by the program specifications; errors when reading/writing files will not crash the program; required CSV file format is implemented for written files; defensive programming techniques are applied when appropriate |
| 4  | Very Good – program correctly reads and writes files as required by the program specifications; errors when reading/writing files will not crash the program; required CSV file format is implemented for written files with minor error(s); defensive programming techniques are applied in some cases |
| 3  | Acceptable – program correctly reads and writes files as required by the program specifications; errors when reading/writing files will crash the program in most cases; required CSV file format is implemented for written files with minor error(s); defensive programming techniques are not applied in most cases |
| 2  | Needs Work – program reads or writes files with slight error(s); errors when reading/writing files will crash the program; required CSV file format is not implemented; defensive programming techniques are not applied |
| 1  | Unsatisfactory – program only reads or writes files with; program reads or writes to files with errors; errors when reading/writing files will crash the program; required CSV file format is not implemented; defensive programming techniques are not applied |
| 0  | Not done; poorly attempted; files are neither written or read by the program |
