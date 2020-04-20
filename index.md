# Personal Self-Assessment
The Computer Science Program has been a tremendous journey for me and, quite honestly, it has had its ups and downs.  

Check out my code review [here] (https://youtu.be/gu795jxS6So).

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
