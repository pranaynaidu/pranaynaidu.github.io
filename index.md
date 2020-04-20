# Personal Self-Assessment
The Computer Science Program has been a tremendous journey for me and, quite honestly, it has had its ups and downs.  
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
    - Perhaps the most important measure of success in a software system is the bottom-line for stakeholders.  The coursework has taught me the concepts for software creation that encompasses the mind of the stakeeholder. In an Agile framework, communication occurs in a slightly different way than in a Waterfall framework.  
    The Computer Science Program has taught me the principles of working with all key players in both an informal and formal manner.  This includes face-to-face conversation, electronic communciation, and creating executive summaries that provide a high level overview for the management team. 
- *Data structures and algorithms*
    - Any complex software system must incorporate data structures and algorithms. By studying and understanding how data structures and algorithms exist in complex computing problems, I was able to showcase my strenghths to highlight how algorithms can process and manipulate information in the data. 
- *Software engineering and databases*
    - I've learned that databases are a convenient way to organize a collection of data.  I was able to incorporate several programming languages including Python, Java, SQL, and C/C++ to create databases and engineer a system that effectively manage data through CRUD functionality. 
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


## *Artifact I - Software Design and Engineering*
The artifact used to illustrate competency and demonstration of key outcomes in the area of software design and engineering is the final project from IT145 – Foundation in Application Development.  This artifact was chosen because it demonstrates the use of software engineering and design, but also algorithms and data structures.  It was created early on in the Computer Science curriculum, so the program is somewhat basic, but showcases some of the basics of software design.  Since there are many stages of the software development life cycle, it is important to incorporate elements that represent the core concepts of software design.  This artifact demonstrates design elements such as patterns, separation of data, and modularity.  

When discussing these design elements, we can see the project uses patterns to identify solutions to recurring problems.  This concept is showcased through user menu options; since we know that the user can circulate throughout the menu by selecting specific options, we can implement a pattern that is guaranteed to work so that it may be reused over and over.  We also maintained a separation of data by reading .txt files rather than hardcoding data structures within the various functions and classes.  When the user selected a specific menu option, the corresponding file was read to display the contents of the file; in this case it was information on animals and habitats.  Finally, modularity included predetermined functions of code to help increase the overall efficiency of the program.  The components within this 

When improving the artifact, the aim was to improve the overall quality of the code.  To start, the initial enhancement used standard naming conventions to help the readability of the code.  Originally, for example, the program did not adhere to consistent naming conventions for start types such as classes as well as other types such as functions and variables.  Normally, a project wouldn’t involve going back and reworking the entire naming convention, unless the entire system was being reworked.  However, for this simple project it was easy to enhance the readability of the variables.  The artifact was subsequently enhanced to use `CamelCase` for all names, and more specifically, starting with a capital letter for classes and lower-case letter for all other types.  

Another enhancement involved the overall efficiency of the project.  For example, there were instances between the class files and the `.java` file containing the `main` method.  Because of the lack of experience when first creating this program, there were variable declarations in each class file that were unused.  These were identified through the effective use of the IDE’s internal debugger and error notifications.  The artifact has subsequently been enhanced to remove these unnecessary lines of code and improve efficiency by creating a program with the least amount of code possible.  

Finally, understanding code is very important for developers in a team setting.  When looking at the original artifact, the use of annotations and comments were virtually nonexistent.  It is important to comment portions of the code to help other developers understand what it does in the even they need to make any changes or add additional modules that would be integrated with your own code.  To enhance the existing project, annotations and comments were embedded at specific portions of the code to help other developers understand how the program performs and the intention of the various modular functions.

Check out the Artifact I enhancement below
```ruby
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

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/pranaynaidu/pranaynaidu.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.


```
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
