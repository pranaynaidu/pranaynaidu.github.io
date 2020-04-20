# Personal Self-Assessment
The Computer Science Program has been a tremendous journey for me and quite honestly, it has had its ups and downs.  
The three most important concepts learned that I think would benefit for my career advancement are:  

- **Preplanning**
    - I found it quite useful to use tools such as pseudocode and wireframing in the initial planning stages of a project.  Although most of the course project requirements were explicitly given, it was important to initialize a plan of action that included time management, allocating the course reading materials to supplement the design, and creating a structured process to design, test, and implement program functions to produce the required results.

- **Backing up code**
    - Backing up code often and with a purpose is another concept that I think is crucial for developers.
    Chances are that the real-world workplace will find me working on a team with multiple developers working on the same    code.  
    Thus, making frequent backups in the event of a program crash due to new code being introduced would allow going backwards to a known working version.  

- **Annotating**
    - This fundamental concept in software engineering is crucial for entire development life cycle. Annotation of code helps  other developers on the team understand exactly how your code functions.
    
Of course, there are a mountain of other concepts that were learned, but I think these broad concepts could serve as core skills to have while working in different sectors of the IT field.  

Completing the coursework and developing this ePortfolio showcases my strengths in the following topics:  

- *Collaborating in a team environment*
    - On an enterprise level, software engineering involves working on teams. The Computer Science Program has taught me skills on creating repositories through various sources such as Bitbucket and here on Github.  This is useful because it allows me to work collaboratively and allows for other developers to `commit` versions and updates of code to be linked to the `master` branch of a project.  
    I also have a stronger understanding of of key functions of development team which include planning, testing, analysis, and of course programming.  Learning about the software development life cycle (SDLC) through an Agile framework taught me the benefits of iterative development that allows for the creation of a fluid software system through cross-functional teams.
- *Communicating to stakeholders*
    - Perhaps the most important measure of success in a software system is the bottom-line for stakeholders.  The coursework has taught me concepts for software creation that encompasses the mind of the stakeholder. In an Agile framework, communication occurs in a slightly different way than in a Waterfall framework.  
    The Computer Science Program has taught me the principles of working with all key players in both an informal and formal manner.  This includes face-to-face conversation, electronic communciation, and creating executive summaries that provide a high level overview for the management team. 
- *Data structures and algorithms*
    - Any complex software system must incorporate data structures and algorithms. By studying and understanding how data structures and algorithms exist in complex computing problems, I was able to showcase my strenghths to highlight how algorithms can process and manipulate information in the data. 
- *Software engineering and databases*
    - I've learned that databases are a convenient way to organize a collection of data.  I was able to learn several programming languages including Python, Java, SQL, and C/C++ to create databases and engineer a system that effectively manages data through CRUD functionality. 
- *Security*
    - The concepts within secure coding have helped me showcase the importance of coding from a security standpoint. Because many software systems require external user input, there is a possibility that cybersecurity threats can occur.  I've learned that if software has a security vulnerability, it could pose a serious threat to the system as a whole and could result in high costs to fix.  My ePortfolio showcases instances where validating user input could mitigate any risk within the program.

The purpose of my ePortfolio is to showcase my strengths and learnings in the above topics.  I will introduce various artifacts created during the Computer Science Program and conduct an informal code review on these artifacts.  This code review will serve as a baseline for enhancements that illustrate the concepts learned and how the existing artifacts can be improved.

Each artifact will include an accompanying narrative to discuss the enhancements and will focus on satisfying the following course outcomes:  

- \[CS-499-01] Employ strategies for building collaborative environments that enable diverse audiences to support organizational decision making in the field of computer science. 

- \[CS-499-02] Design, develop, and deliver professional-quality oral, written, and visual communications that are coherent, technically sound, and appropriately adapted to specific audiences and contexts. 

- \[CS-499-03] Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution, while managing the trade-offs involved in design choices (data structures and algorithms).  

- \[CS-499-04] Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals (software engineering/design/database).  

- \[CS-499-05] Develop a security mindset that anticipates adversarial exploits in software architecture and designs to expose potential vulnerabilities, mitigate design flaws, and ensure privacy and enhanced security of data and resources.


# Code Review

Check out my code review [here](https://youtu.be/gu795jxS6So).


# Artifact I - Software Design and Engineering
The artifact used to illustrate competency and demonstration of key outcomes in the area of software design and engineering is the final project from IT145 – Foundation in Application Development.  This artifact was chosen because it demonstrates the use of software engineering and design, but also algorithms and data structures.  It was created early on in the Computer Science curriculum, so the program is somewhat basic, but showcases some of the basics of software design.  Since there are many stages of the software development life cycle, it is important to incorporate elements that represent the core concepts of software design.  This artifact demonstrates design elements such as patterns, separation of data, and modularity.  

When discussing these design elements, we can see the project uses patterns to identify solutions to recurring problems.  This concept is showcased through user menu options; since we know that the user can circulate throughout the menu by selecting specific options, we can implement a pattern that is guaranteed to work so that it may be reused over and over.  We also maintained a separation of data by reading `.txt` files rather than hardcoding data structures within the various functions and classes.  When the user selected a specific menu option, the corresponding file was read to display the contents of the file; in this case it was information on animals and habitats.  Finally, modularity included predetermined functions of code to help increase the overall efficiency of the program.  The components within this 

When improving the artifact, the aim was to improve the overall quality of the code.  To start, the initial enhancement used standard naming conventions to help the readability of the code.  Originally, for example, the program did not adhere to consistent naming conventions for start types such as classes as well as other types such as functions and variables.  Normally, a project wouldn’t involve going back and reworking the entire naming convention, unless the entire system was being reworked.  However, for this simple project it was easy to enhance the readability of the variables.  The artifact was subsequently enhanced to use `CamelCase` for all names, and more specifically, starting with a capital letter for classes and lower-case letter for all other types.  

Another enhancement involved the overall efficiency of the project.  For example, there were instances between the class files and the `.java` file containing the `main` method.  Because of the lack of experience when first creating this program, there were variable declarations in each class file that were unused.  These were identified through the effective use of the IDE’s internal debugger and error notifications.  The artifact has subsequently been enhanced to remove these unnecessary lines of code and improve efficiency by creating a program with the least amount of code possible.  

Finally, understanding code is very important for developers in a team setting.  When looking at the original artifact, the use of annotations and comments were virtually nonexistent.  It is important to comment portions of the code to help other developers understand what it does in the even they need to make any changes or add additional modules that would be integrated with your own code.  To enhance the existing project, annotations and comments were embedded at specific portions of the code to help other developers understand how the program performs and the intention of the various modular functions.

**Below is the enhancement for Artifact I**
```java
/* IT145 Final Project - Zoo Monitoring System (Option 2)
 * Pranay Naidu
 * pranay.naidu@snhu.edu
 */

package zoomonitoringsystem;


import java.io.FileInputStream;   // Imports the File Input reader function to allow data from files for be read
import java.util.Scanner;         // Allows for user keyboard inputs

public class ZooMonitoringSystem {


   //Method to print Main Menu
   public static void MainMenu() {
      System.out.println("1) Monitor an animal");
      System.out.println("2) Monitor a habitat");
      System.out.println("3) Quit\n");
   }

   /* The following nested loops iterate through the user inputs
    * and only allows for the three numeric (3) choices to be entered
    * if an invalid choice is keyed, program continues to ask for valid input
    */
   public static void MainMenuChoice(int mainMenuSelection){
      Scanner scnr = new Scanner (System.in);   // Initialize scanner function for user input within this method

         switch (mainMenuSelection) {
            case 1:  // This loop runs if user selects animal option to monitor
               System.out.println("Displaying Animal Options");
               System.out.println("-------------------------");
               animalMenu(); //calls the function to show the animals options if options 1 is chosen
               System.out.println("Please select an animal you would like more details on:");
               mainMenuSelection = scnr.nextInt();  //sets the variable to the user's numerical menu selection
               System.out.println();
    
               chosenAnimal(mainMenuSelection); //calls the function to display the chosen animal
               return;
               }
                 
                      
            case 2:  // This loop runs if user selects habitat option to monitor
               System.out.println("Displaying Habitat Options");
               System.out.println("--------------------------");
               habitatMenu();  //calls the function to show the habitats options if options 2 is chosen
               System.out.println("Please select a habitat you would like more details on:");
               mainMenuSelection = scnr.nextInt();  //sets the variable to the user's numerical menu selection
               System.out.println();
            
               chosenHabitat(mainMenuSelection);  //calls the function to display the chosen animal
               return;
            }

         }
            default:  // Quits program if user enters "3"
               break;
                
      }
      System.out.println("Thank you for using the zoo monitoring system. Goodbye");     
   }
   }
   
   
   //Method to print Animal Sub-Menu
   public static void animalMenu() {
      FileInputStream fileByteStream;  // Initializing the FileInputStream function and assigning it to fileByteStream
      Scanner inFS;
      String line;
      fileByteStream = new FileInputStream("animals.txt");  // Reads data from the "animals" text file into fileByteStream

      inFS = new Scanner(fileByteStream);
      int i = 0;
      while ((inFS.hasNextLine())) {   //loop reads the animals.txt data and continues to read each line until there is an empty line
         line = inFS.nextLine();
         if (!line.isEmpty()) {
            i += 1;
            System.out.println(i + ") " + line);  //as each line contains an animal type, it prints to screen. Hence creating a simple menu by reading text file rather than hardcoding data.
         }
         else {
            break;
         }
      }
      System.out.println("5) Return to Main Menu");
      fileByteStream.close();
      System.out.println();
   }
   


   //Method to print Habitat Sub-Menu
   public static void habitatMenu() {
   FileInputStream fileByteStream;  // Initializing the FileInputStream function and assigning it to fileByteStream
   Scanner inFS;

   String line;
   fileByteStream = new FileInputStream("habitats.txt");  // Reads data from the "animals" text file into fileByteStream
   inFS = new Scanner(fileByteStream);
   int i = 0;
   while ((inFS.hasNextLine())) {  //loop reads the animals.txt data and continues to read each line until there is an empty line
   line = inFS.nextLine();
      if (!line.isEmpty()) {
         i += 1;
         System.out.println(i + ") " + line); //as each line contains an habitat type, it prints to screen. Hence creating a simple menu by reading text file rather than hardcoding data.
      }
      else {
         break;
      }
   }
   System.out.println("4) Return to Main Menu");
   fileByteStream.close();
   System.out.println();
}


   //Method to print info on user's chosen type of Animal
   public static void chosenAnimal(int typeOfAnimal) {
   Scanner scnr = new Scanner (System.in);
   int returnToPreviousMenu;
   while (typeOfAnimal <=5) {
      switch (typeOfAnimal) {
         case 1:  //Displays Lion information
            System.out.println("Displaying Lions");
            System.out.println("----------------");
            lion.lion();  //calls the specific java class file for lion
            System.out.println("\nReturning to Main Menu"); 
            System.out.println("----------------------");
            break;            
         case 2:  //Displays Tiger information
            System.out.println("Displaying Tigers");
            System.out.println("-----------------");
            tiger.tiger();  //calls the specific java class file for tiger
            System.out.println("\nReturning to Main Menu");
            System.out.println("----------------------");
            break;
         case 3:  //Displays Bear information
            System.out.println("Displaying Bears");
            System.out.println("----------------");
            bear.bear();  //calls the specific java class file for bear
            System.out.println("\nReturning to Main Menu");  
            System.out.println("----------------------");
            break;
         case 4:  //Displays Giraffe information
            System.out.println("Displaying Giraffes");
            System.out.println("-------------------");
            giraffe.giraffe();  //calls the specific java class file for giraffe
            System.out.println("\nReturning to Main Menu");
            System.out.println("----------------------");
            break;
         default: // Returns to the main menu          
            break;
      }
      MainMenu();
      System.out.println("Please make a selection");
      returnToPreviousMenu = scnr.nextInt();
      MainMenuChoice(returnToPreviousMenu);
      return;
   }
   }


   //Method to print info on user's chosen habitat
   public static void chosenHabitat(int typeOfHab)
      Scanner scnr = new Scanner (System.in);
      int returnToPreviousMenu = 0;
      while (typeOfHab <=4) {
         switch (typeOfHab) {
            case 1:  //Displays Penguin Habitat information
               System.out.println("Displaying Penguin Habitat");
               System.out.println("--------------------------");
               penguin.penguin();  //calls the specific java class file for penguin
               System.out.println("\nReturning to Main Menu");
               System.out.println("----------------------");
               break;
            case 2:  //Displays Bird House information
               System.out.println("Displaying Bird House ");
               System.out.println("----------------------");
               bird.bird();  //calls the specific java class file for bird
               System.out.println("\nReturning to Main Menu");
               System.out.println("----------------------");
               break;
            case 3:  //Displays Aquarium information
               System.out.println("Displaying Aquarium");
               System.out.println("-------------------");
               aquarium.aquarium();  //calls the specific java class file for aquarium
               System.out.println("\nReturning to Main Menu");
               System.out.println("----------------------");
               break;
            default:  //Returns to the main menu    
               break;
         
         }        
         MainMenu();
         System.out.println("Please maka a selection");
         returnToPreviousMenu = scnr.nextInt();
         MainMenuChoice(returnToPreviousMenu);
         return;
      }
      }
   

   //Start of main() method
   public static void main (String [] args){
      Scanner scnr = new Scanner (System.in);  	//Initializes scanner to allow for user input
      int userMenuChoice;  //Initializes user's first choice as integer variable     
      System.out.println("Welcome to the Zoo Monitoring System");
      System.out.println("------------------------------------");
      MainMenu(); 	//function call to performs the function MainMenu()
      System.out.println("What would you like to monitor today:");
      userMenuChoice = scnr.nextInt();
      System.out.println();    
      MainMenuChoice(userMenuChoice); //calls the function and uses the user's choice to present information
   }
}
```

# Artifact II - Algorithm and Data Structures
The artifact used to illustrate competency and demonstration of key outcomes in the area of algorithms and data structures is the final project from IT145 – Foundation in Application Development.  This artifact was chosen because it demonstrates the use of software engineering and design, but also algorithms and data structures.  As mentioned in Milestone Two Enhancement One, this artifact was created early on in the Computer Science curriculum and showcases various elements of algorithms and data structures.  It makes sufficient use of data structures within data files to retrieve information on zoo animals and habitats; however, the algorithms are somewhat rudimentary.  Because of this, I decided to use this artifact to showcase enhancements that include more sophisticated algorithms using a secure coding approach.  

First, looking at the use of manipulating data within `.txt` files, the program made good use of Java’s `FileInputStream` library to read the data files line by line, and display data based on user input.  This showcases the ability of the program to effectively read data from a file into the `fileByteStream`, and essentially checks for data the user requested based on their menu selection.  

When dealing with a program that allows users to enter input, it is imperative to ensure that malicious input does not mimic actual code that could cause very adverse effects in behavior of the program.  This was the purpose of the most important enhancement within this artifact: the use of exception handling.  Originally, the program stores the user input into an integer type variable.  However, it did not check for exceptions such as a non-integer value, or whether the user selects a valid integer option.  Therefore, all functions that included loops and conditional statements were checked and enhanced to catch any attempts of invalid user input.  Additional code review revealed that switch cases defaulted to quitting the program if the user does not choose a menu item.  However, this could create security threats if the program does not conditionally check that a valid option is selected so each loop was enhanced to explicitly check the user’s input for a “quit” menu selection.  

Considering developer issues within the architecture of the program helped to identify inherent flaws in the conditional loops and fulfilled the course outcomes \[CS-499-03], \[CS-499-04], and \[CS-499-05].  This artifact enhances the original algorithms by taking a secure coding approach to solve the problem of user input vulnerabilities by anticipating exploits in user inputs. 

**Below is the enhancement for Artifact II**
```java
/* IT145 Final Project - Zoo Monitoring System (Option 2)
 * Pranay Naidu
 * pranay.naidu@snhu.edu
 */

package zoomonitoringsystem;


import java.io.FileInputStream;   // Imports the File Input reader function to allow data from files for be read
import java.util.Scanner;         // Allows for user keyboard inputs
import java.io.IOException;      // This allows for catching of any exceptions when reading from file (i.e. file not found)
public class ZooMonitoringSystem {
    
    //Method to print Main Menu
    public static void MainMenu() {
        System.out.println("1) Monitor an animal");
        System.out.println("2) Monitor a habitat");
        System.out.println("3) Quit\n");
        
    }
    
    /* The following nested loops iterate through the user inputs
    * and only allows for the three numeric (3) choices to be entered
    * if an invalid choice is keyed, program continues to ask for valid input
    */
    public static void MainMenuChoice(int mainMenuSelection) throws IOException {  // Throws clause catches any error with file reading
        Scanner scnr = new Scanner (System.in);   // Initialize scanner function for user input within this method
        while (mainMenuSelection != 3) {       // while loop is used to check that user does not want to quit.  If not, loop continues.
            while (mainMenuSelection != 5) {    // same concept as previous while loop
                switch (mainMenuSelection) {
                    case 1:  // This loop runs if user selects animal option to monitor
                        System.out.println("Displaying Animal Options");
                        System.out.println("-------------------------");
                        animalMenu(); //calls the function to show the animals options if options 1 is chosen
                        System.out.println("Please select an animal you would like more details on:");
                        mainMenuSelection = scnr.nextInt();  //sets the variable to the user's numerical menu selection
                        System.out.println();
                        
                        if ((mainMenuSelection >=1) && (mainMenuSelection <=5)) {  // inner loop checks that valid option is entered by user
                            chosenAnimal(mainMenuSelection);
                            return;
                        }
                        
                        else {
                            while (mainMenuSelection > 5) {
                                System.out.println("Invalid Selection.");
                                System.out.println("Please type a valid option number:");
                                int animalSelection = scnr.nextInt();
                                chosenAnimal(animalSelection);
                                return;
                            }
                     }
                        
                    case 2:  // This loop runs if user selects habitat option to monitor
                        System.out.println("Displaying Habitat Options");
                        System.out.println("--------------------------");
                        habitatMenu();  //calls the function to show the habitats options if options 2 is chosen
                        System.out.println("Please select a habitat you would like more details on:");
                        mainMenuSelection = scnr.nextInt();  //sets the variable to the user's numerical menu selection
                        System.out.println();
                        if ((mainMenuSelection >= 1) && (mainMenuSelection <=4)) {  // inner loop checks that valid option is entered by user
                            chosenHabitat(mainMenuSelection);  //calls the function to display the chosen animal
                            return;
                        }
                        
                        else {
                            while (mainMenuSelection > 4) {
                                System.out.println("Invalid Selection.");
                                System.out.println("Please type a valid option number:");
                                habitatMenu();
                                int habitatSelection = scnr.nextInt();
                                chosenHabitat(habitatSelection);
                                return;
                            }
                        }
                    case 3:  // Quits program if user enters "3"
                        break;
                    default:
                        System.out.println("You have made an invalid selection.");
                        System.out.println("Please type a valid option number:");
                        mainMenuSelection = scnr.nextInt();
                }
                System.out.println("Thank you for using the zoo monitoring system. Goodbye");
            }
        }
        
    //Method to print Animal Sub-Menu
    public static void animalMenu() {
        FileInputStream fileByteStream;  // Initializing the FileInputStream function and assigning it to fileByteStream
        Scanner inFS;
        String line;
        fileByteStream = new FileInputStream("animals.txt");  // Reads data from the "animals" text file into fileByteStream
        inFS = new Scanner(fileByteStream);
        int i = 0;
        while ((inFS.hasNextLine())) {   //loop reads the animals.txt data and continues to read each line until there is an empty line
            line = inFS.nextLine();
            if (!line.isEmpty()) {
                i += 1;
                System.out.println(i + ") " + line);  //as each line contains an animal type, it prints to screen. Hence creating a simple menu by reading text file rather than hardcoding data.
            }
            else {
                break;
            }
        }
        System.out.println("5) Return to Main Menu");
        fileByteStream.close();
        System.out.println();
    }
        
        
    //Method to print Habitat Sub-Menu
    public static void habitatMenu() {
        FileInputStream fileByteStream;  // Initializing the FileInputStream function and assigning it to fileByteStream
        Scanner inFS;
        String line;
        fileByteStream = new FileInputStream("habitats.txt");  // Reads data from the "animals" text file into fileByteStream
        inFS = new Scanner(fileByteStream);
        int i = 0;
        while ((inFS.hasNextLine())) {  //loop reads the animals.txt data and continues to read each line until there is an empty line
            line = inFS.nextLine();
            if (!line.isEmpty()) {
                i += 1;
                System.out.println(i + ") " + line); //as each line contains an habitat type, it prints to screen. Hence creating a simple menu by reading text file rather than hardcoding data.
            }
            else {
                break;
            }
        }
        System.out.println("4) Return to Main Menu");
        fileByteStream.close();
        System.out.println();
    }


    //Method to print info on user's chosen type of Animal
    public static void chosenAnimal(int typeOfAnimal) throws IOException {  // Throws clause catches any error with file reading
        Scanner scnr = new Scanner (System.in);
        int returnToPreviousMenu;
        while (typeOfAnimal <=5) {
            switch (typeOfAnimal) {
                case 1:  //Displays Lion information
                    System.out.println("Displaying Lions");
                    System.out.println("----------------");
                    lion.lion();  //calls the specific java class file for lion
                    System.out.println("\nReturning to Main Menu");
                    System.out.println("----------------------");
                    break;
                case 2:  //Displays Tiger information
                    System.out.println("Displaying Tigers");
                    System.out.println("-----------------");
                    tiger.tiger();  //calls the specific java class file for tiger
                    System.out.println("\nReturning to Main Menu");
                    System.out.println("----------------------");
                    break;
                case 3:  //Displays Bear information
                    System.out.println("Displaying Bears");
                    System.out.println("----------------");
                    bear.bear();  //calls the specific java class file for bear
                    System.out.println("\nReturning to Main Menu");
                    System.out.println("----------------------");
                    break;
                case 4:  //Displays Giraffe information
                    System.out.println("Displaying Giraffes");
                    System.out.println("-------------------");
                    giraffe.giraffe();  //calls the specific java class file for giraffe
                    System.out.println("\nReturning to Main Menu");
                    System.out.println("----------------------");
                    break;
                case 5: // Returns to the main menu
                    break;
                default: // If User selects invalid option
                    System.out.println("You have made an invalid selection number.");
                    System.out.println("Returning to the previous menu\n");
                    System.out.println("------------------------------\n");
                    animalMenu();
                    System.out.println("Please select an animal you would like more details on:");
                    return;
            }
            MainMenu();
            System.out.println("Please make a selection");
            returnToPreviousMenu = scnr.nextInt();
            MainMenuChoice(returnToPreviousMenu);
            return;
        }
    }


    //Method to print info on user's chosen habitat
    public static void chosenHabitat(int typeOfHabitat) throws IOException {  // Throws clause catches any error with file reading
        Scanner scnr = new Scanner (System.in);
        int returnToPreviousMenu = 0;
        while (typeOfHabitat <=4) {
            switch (typeOfHabitat) {
                case 1:  //Displays Penguin Habitat information
                    System.out.println("Displaying Penguin Habitat");
                    System.out.println("--------------------------");
                    penguin.penguin();  //calls the specific java class file for penguin
                    System.out.println("\nReturning to Main Menu");
                    System.out.println("----------------------");
                    break;
                case 2:  //Displays Bird House information
                    System.out.println("Displaying Bird House ");
                    System.out.println("----------------------");
                    bird.bird();  //calls the specific java class file for bird
                    System.out.println("\nReturning to Main Menu");
                    System.out.println("----------------------");
                    break;
                case 3:  //Displays Aquarium information
                    System.out.println("Displaying Aquarium");
                    System.out.println("-------------------");
                    aquarium.aquarium();  //calls the specific java class file for aquarium
                    System.out.println("\nReturning to Main Menu");
                    System.out.println("----------------------");
                    break;
                case 4:  //Returns to the main menu
                    break;
                default:
                    System.out.println("You have made an invalid selection.");
                    System.out.println("\nReturning to Main Menu");
                    System.out.println("-----------------------\n");
                    habitatMenu();
                    System.out.println("Please select a habitat you would like more details on:");
                    typeOfHabitat = scnr.nextInt();
                    return;
            }
            MainMenu();
            System.out.println("Please maka a selection");
            returnToPreviousMenu = scnr.nextInt();
            MainMenuChoice(returnToPreviousMenu);
            return;
        }
    }
    
    //Start of main() method
    public static void main (String [] args) throws IOException {
        Scanner scnr = new Scanner (System.in);  	//Initializes scanner to allow for user input
        int userMenuChoice;  //Initializes user's first choice as integer variable
        System.out.println("Welcome to the Zoo Monitoring System");
        System.out.println("------------------------------------");
        MainMenu(); 	//function call to performs the function MainMenu()
        System.out.println("What would you like to monitor today:");
        userMenuChoice = scnr.nextInt();
        System.out.println();
        MainMenuChoice(userMenuChoice); //calls the function and uses the user's choice to present information
    }
}
```

**Enhancements to the Aquarium Class File**
```java
package zoomonitoringsystem;

import java.io.FileInputStream;
import java.util.Scanner;

public class aquarium {
    
   public static void aquarium()
    FileInputStream fileByteStream = null;  // Initializing the FileInputStream function and assigning it to fileByteStream
    Scanner inFS = null;
    Scanner scnr = new Scanner(System.in);
      
      // Initialize variables set to each line in the data file
      String line;
      String temperature;
      String foodSource;
      String cleanliness;
      String alertLine;
      
      fileByteStream = new FileInputStream("habitats.txt"); // Reads data from the "habitats" text file into fileByteStream
      inFS = new Scanner(fileByteStream);
    
      while ((inFS.hasNextLine())) {  //Reads data until there are no more lines in the data file
      line = inFS.nextLine();    
      
         if (line.contains("Aquarium")) {   //Check to see if habitat contains "Aquarium" and prints when user choice is for Aquarium Habitat
            temperature = inFS.nextLine();          
            foodSource = inFS.nextLine();
            cleanliness = inFS.nextLine(); 
            
            if (foodSource.contains("*****")) {  //Check for alert on Food Source field
               alertLine = foodSource;
               System.out.println("\n!!!!!ALERT!!!!!");
               System.out.println(alertLine.replace("*", "") + "\n"); //Uses the .replace command to replace the asterisks with empty space
               System.out.println("Press Enter to view full details");
               fullDetails = scnr.nextLine();
               System.out.println(temperature);
               System.out.println(foodSource.replace("*" , ""));
               System.out.println(cleanliness);             
            }
            
            else if (cleanliness.contains("*****")) {  
               alertLine = cleanliness;
               System.out.println("\n!!!!!ALERT!!!!!");
               System.out.println(alertLine.replace("*", "") +"\n");  //Uses the .replace command to replace the asterisks with empty space
               System.out.println("Press Enter to view full details");
               fullDetails = scnr.nextLine();
               System.out.println(temperature);
               System.out.println(foodSource);
               System.out.println(cleanliness.replace("*" , ""));             
            }
            
            else {
               System.out.println(temperature + "\n" + foodSource + "\n" + cleanliness + "\n");
            }
                   
      fileByteStream.close();  //Needed to close the File Input Stream
         }
      }
   }
}
```

# Artifact III - Databases
The artifact used for Milestone Four’s enhancement on databases comes from CS340 – Advanced Programming Concepts.  The original artifact used structured query language to perform a series of `CRUD` functions to showcase effective manipulation of database design and structure.  This course was taken during the late stages of the Computer Science Program, so it illustrates a more complex knowledge of databases and how to write code using the Python language and implementing SQL commands within `MongoDB` to manipulate databases to display useful information about the data within.  

This artifact was chosen because it took the basic CRUD functionality of the original submitted project, but enhances it in a way to implement a RESTful API.  Representational State Transfer allows the access of data across different sources to work with an application programming interface (API).  The enhanced artifact uses the API to provide functionality that allows the user to perform CRUD functions to a data document within a specific `URL`.  

Once the python code was written to implement the RESTful API, we used SQL commands to display specific data.  For instance, the following command typed into the terminal would add a new document in a database consisting of a collection of stocks:
```
curl -H "Content-Type:application/json" -X POST -d '{"Volume" : 40, "Sector Name" : "New Sector"}' http://localhost:8080/addDocument
```
For the above command to be successful, we created a function that uses the data supplied and incorporated the MongoDB function `create()` to add the new document.  For example, there is a line in the code `jsonData = request.json` which passes the data in the `json` object.  Similar functionality was implemented throughout the enhancement to include updating, deleting, and reading information within the database.  

This artifact meets course objective \[CS-499-04].  Because modern software allows users to integrate various programs to communicate with each other, this artifact showcases the creation of an API on the server-side which allows communication with the client-side.  We are able to separate the concerns associated with both the user interface and the data storage associated with it.  A key feature of the RESTful API enhancement is that the information can be retrieved from any resource such as a document or image.  

This enhancement was a challenging one.  I had originally attempted to implement RESTful API functionality, but was unsuccessful.  It took a lot of research, preplanning, and several adjustments to successfully enhance this artifact.  It helped to realize the capabilities of `REST` that allows the user to access data from several resources (in this case a `.json` file).  I also learned more that `REST` and `HTTP` are not the same even though developers use `REST` to make web integration across platforms.  It was interesting to learn the architectural side of a RESTful API and how it is used as a resource to be accessed using Uniform Resource Identifiers (URI).  

**Below are the enhancements for Artifact III**  

*RESTful API
```python
#!/usr/bin/python
import json
from bson import json_util
from bson.json_util import dumps
import bottle
from bottle import route, run, request, abort
#imports for database
from pymongo import MongoClient
connection = MongoClient('localhost', 27017)
db = connection['market']
collection = db['stocks']

# URI paths for restfull services
#
#
   #UPDATING OUR STOCK BY PROVIDING THE CRITERIA, WE USE METHOD PUT, When Key Value is Specified
#
@route('/update/<TickerValue>', method='PUT')
def UpdateMyStock(TickerValue):
  jsondata = request.json #Retrive all the data passed in the url
  query = { "Ticker" : TickerValue} #Query Used To Search Documents For Updating
 
  #We use a loop to update the Colection using the parameters from the url
  for key in jsondata:
    update =  { "$set":{key:jsondata[key]}}
    #updating collection
    collection.update(query,update)
  updateDocs = collection.find({"Ticker":TickerValue})
  line = "--" * 45 +"\n" #this will print a line
  result = dumps(updateDocs) #
  return line+"\n   All These Details Got Updated>>  \n"+str(result)+"\n  End Of Document >> \n"+line

   
  
# We would wish to add document to our stock collection
# we use put

##when no parameter is added, we still add the object to the collection
##---------------------------------------No Ticker Value Added----------------------------------------
#
@route('/addDocument', method='POST')
def addDocumentStock():
  #get all passed dat in a json object using the request.json
  jsonData = request.json
  #Lets insert the document passed to the collection
  newDocument = collection.insert(jsonData) #returns the _id
  retriveDoc = collection.find_one({"_id":newDocument})
  line = "--" * 45 +"\n"
  return line+ "\nAdded Document >> \n "+dumps(retriveDoc)+"\n End Of Document >>\n "+line #return inserted document.

##-----------------------------When Ticker Value Is Added --------------------------------------------
@route('/addDocument/<tickerValue>', method='POST')
def addDocumentStock(tickerValue):
  #get all passed dat in a json object using the request.json
  jsonData = request.json
  jsonData.update( {'Ticker' : tickerValue} ) 
  #Lets insert the document passed to the collection
  recordId = collection.insert(jsonData) #insert data to the stocks collection
  retriveDoc = collection.find_one({"_id":recordId})
  line = "--" * 45 +"\n"
  return line+ "\nAdded Document>> \n "+dumps(retriveDoc)+" \n End Of Document >>\n "+line #return inserted document.




##---------------------------------------Deleting Data --------------------------------------------------------------
#

@route('/remove/<TickerValue>', method='GET')
def removeStock(TickerValue):
  query = {"Ticker" :TickerValue} #Query to Search Target Data
  result = collection.delete_many(query) #Will delete all documents that matching the query
  return "\n Requested Document Has Been Deleted.... \n" #return results to the user.



##-----------------------------Reading Data From Collectiosn Given Ticker Value-------------------------------------------

@route('/RequestDoc/<TickerValue>', method='GET')
def requestDocument(TickerValue):
  readDocument = collection.find({"Ticker":TickerValue}) #
  #provided
  line = "--" * 45 +"\n"
  return line+"\nCreteria Added [Ticker Value] \n This Is The Requested Document >>\n "+dumps(readDocument)+" \n End Of Requested Document >>"

#When no parameter is added

@route('/RequestDoc/', method='GET')
def requestDocument():
  readDocument = collection.find().limit(1) #First Records Will Displayed
  #provided
  line = "--" * 45 +"\n"
  return line+"\n No Creteria Added [Ticker Value]\n This Is The Requested Document >>\n "+dumps(readDocument)+" \n End Of Requested Document >>\n"


##-----------------------------Getting A Stock Report--------------------------------------


@route('/stockSummery/', method='POST')
def getReport(): 
  line = "--" * 45 +"\n"
  tickerSymbols = request.json.get('list') #retrieves the value of the list key in the url data
  #Removing the curl Braces from the List 
  tickerSymbols = tickerSymbols.replace("[","")
  tickerSymbols = tickerSymbols.replace("]","")
  tickerSymbols = list(tickerSymbols.split(",")) #create a list from the remaining list
  EmptyTickers = list()
  print(tickerSymbols)
  underline = "_" * 30;
  #This for loop uses each ticker in the list,
  #get ist summer and add the summery to the items list
  for ticker in tickerSymbols:
      item = Pipeline(ticker)
      print(item)
      #Building string for display
      EmptyTickers.append(line+" \t\t\t **Report For Symbol ["+ticker+"] ** \n \t\t\t"+underline+" \n"+item+"\n\n "+line)
  return EmptyTickers  #return a lit of items


##-----------------------------Getting Industry Report--------------------------------------
#
#
#
#

#Most URLs replaces spaces with +, therefore for an industry 
#That has spaces, we replace the spaces with + sign
@route('/getIndustryReport/<industryName>', method='GET')
def getReport(industryName):
  industry = industryName.replace("+"," ")
  #Pipeline is composed of Stages, each stage 
  #Stage One In The Pipeline, Fields To Be Produces
  print("\n\n\n "+industry+"\n\n")
  result2 = IndustryPipeline(industry)
  firstStage = { '$project': {'Industry':1, 'Ticker':1,'Float Short':1,'Relative Volume':1,'Volume':1,'Performance (Year)':1 } }
  #Second Stage
  secondStage = { '$match': { "Industry": industry } }
  print("\n\n\n "+str(secondStage)+"\n\n")
  #Stage Three
  thirsStage = { '$group': { '_id': "$Industry", 'Total Float Short': {'$sum': "$Float Short" },
                           'Average Relative Volume':{'$avg':"$Relative Volume"},
                           'Average Volume':{'$avg':'$Volume'},
                           'Max Performance (Year)':{'$max':'$Performance (Year)'},
                           'Total Volume':{'$sum':'$Volume'} } }
  #Adding Limit
  fourthStage = { '$limit' : 5 }
  query = [firstStage,secondStage,thirsStage,fourthStage]
  print(str(query))
  result=collection.aggregate(query)
  result = dumps(result)
  #print results to user.
  return "-------- \n \t\t\t Portfolio Report For  ["+industry+"] Industrie(s) \n\n "+result+" \n-------- \n"+result2+"\n"

##************************************************End Of Industry Report *****************************************
#
#

#--------------------------Pipeline -------------------------------------------------------------------------------
#
#
#
#
#This pipeline retrive data depending on several specified data
#we sum fields, calculate Voume, 

def Pipeline(ticker):
  #stage one specifies the fields to be passed to the next stages
  firstStage = { '$project': { 'Ticker':1,'Float Short':1,'Relative Volume':1,'Volume':1,'Performance (Year)':1 } }
  #Specifies the query [$match] << The Targeted Documents
  #
  secondStage = { '$match': { "Ticker": ticker } }
  #We do all The Operations Here sum, Divion, Multiplication and Others
  thirdStage = { '$group': { '_id': "$Ticker", 'Total Float Short': {'$sum': "$Float Short" },
                           'Average Relative Volume':{'$avg':"$Relative Volume"},
                           'Total Accupied Volume':{'$sum':'$Volume'},
                           'Max Performance (Year)':{'$max':'$Performance (Year)'},
                           'Minimum Volume Used':{'$min':'$Volume'} } }
  myQuery = [firstStage,secondStage,thirdStage]
  result=collection.aggregate(myQuery) 
  result = dumps(result)
  return result



def IndustryPipeline(industry):
  #stage one specifies the fields to be passed to the next stages
  firstStage = { '$project': { 'Industry':1,'Float Short':1,'Price':1,'Average True Range':1,'50-Day Simple Moving Average':1,'Change':1 } }
  #Specifies the query [$match] << The Targeted Documents
  #
  secondStage = { '$match': { "Industry": industry } }
  #We do all The Operations Here sum, Divion, Multiplication and Others
  thirdStage = { '$group': { '_id': "$Industry", 'Total Float Short': {'$sum': "$Float Short" },
                           'Average Average True Range':{'$avg':"$Average True Range"},
                           'Total Price':{'$sum':'$Price'},
                           'Max 50-Day Simple Moving Average (Year)':{'$max':'$50-Day Simple Moving Average'},
                           'Minimum Change':{'$min':'$Change'} } }
  
  #Adding Limit
  fourthStage = { '$limit' : 5 }
  myQuery = [firstStage,secondStage,thirdStage,fourthStage]
  result=collection.aggregate(myQuery) 
  result = dumps(result)
  return "-------- \n More Usefull Information \n\n"+result+"\n\n"

#--------------------------Main Program Start ----------------------------------------------------
#
#
#
#
  
if __name__ == '__main__':
  run(debug=True,reloader = True)
  #run(host='localhost', port=8080)
```

*Finding documents by a string*
```python
import json
from bson import json_util
from bson.json_util import dumps
from pymongo import MongoClient
connection = MongoClient('localhost', 27017)
database = connection['market']
collection = database['stocks']

def findDocument(query,userDisplay):
  try:
    line = "--" * 45 
    print(line+"\n")
    result=collection.find(query,userDisplay)
    print(dumps(result))
    print(line+"\n")
    print("Thank you...we are Done Processing... \n")
  except ValidationError as ve:
    abort(400, str(ve))
  

def main():
  line = "--" * 45  
  print("\t\t   Welcome, Lets Find Documents Using The Industry Key Value ")
  print("\t\t Enter The Name Of The Industry... \n");
  print(line+"\n")
  userIndustry = raw_input("Name Of The Industry# ")
  query = {"Industry" : userIndustry}
  userDisplay = {"Ticker":1,"_id":0}
  print("Thank you...We Are Processing... \n")
  findDocument(query,toDisplay)
 
main()
```
*Deleting a Document*
```python
import json
from bson import json_util
from bson.json_util import dumps
from pymongo import MongoClient
connection = MongoClient('localhost', 27017)
database = connection['market']
collection = database['stocks']

def deleteDocument(document,tvalue):
  try:
    line = "--" * 45  
    print(line)
    result = collection.remove(document)
    print("----------Documents With Ticker Value "+tvalue+" Have Been Deleted  \n")
    print(dumps(result))
  except ValidationError as ve:
    abort(400, str(ve))
  

def main():
  line = "--" * 45  
  print(line+"\n\n")
  print("\t\t   DELETING DOCUMENT")
  print("\t\t Provide The Ticker Value for The Documents To Be DELETED, All Documents With\n\t\t That Ticker Value Will Be DELETD \n");
  print(line+"\n")
  tvalue = raw_input("Enter Ticker Value #")
  
  myquery = {"Ticker" : tvalue}
  
  print("--" * 50 +" Below Items Will Be Deleted " + "--"*50+" \n")
  result=collection.find(myquery).limit(10)
  print(dumps(result))
  deleteDocument(myquery,tvalue)
main()
```
*Inserting a Document*
```python
import json
from bson import json_util
from pymongo import MongoClient
connection = MongoClient('localhost', 27017)
database = connection['market']
collection = database['stocks']

def insertDocument(document):
  message = ""
  try:
    result=collection.insert(document)
    message = "Document Added Successifully"
  except ValidationError as ve:
    abort(400, str(ve))
    message = "Document Could Not Be Added.."
  return message

def main():
  line = "--" * 45  
  print(line+"\n\n")
  document = raw_input("Enter Your Document:")
  print("Processing Document.....\n Received Document \n"+line)
  print(document)
  print insertDocument(json.loads(document))
  print("Thank you for using Our Service....Byee \n")
  print(line+"\n\n")
  
main()
```
*Implementing Pipeline Functionality*
```python
import json
from bson import json_util
from bson.json_util import dumps
from pymongo import MongoClient
connection = MongoClient('localhost', 27017)
database = connection['market']
collection = database['stocks']

def pipeline(pipe):
  try:
    line = "--" * 45  
    print(line+"\n")
    result=collection.aggregate(pipe)
    result = dumps(result)
    print(result)
    print(line+"\n")
  except ValidationError as ve:
    abort(400, str(ve))
  

def main():
  line = "--" * 45  
  print("\t\t Aggregation Pipeline Statements")
  print("\t\t You will need to Enter Sector Name \n");
  print(line+"\n")
  userSector = raw_input("Name Of The Sector# ")
  #I will add each stage separetly in the next query
  firstStage = { '$match': { "Sector": userSector } }
  secondStage= { '$group': { '_id': "$Industry", 'Total Austanding Shares:': {'$sum': "$Shares Outstanding" } } }
  pipe = [firstStage,secondStage]
  pipeline(pipe)
  print("Thank You.\n")
main()
```
