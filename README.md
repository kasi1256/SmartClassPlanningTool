
Smart Class Planning Tool

Table of Contents:

•Purpose
•Prerequisites
•Download Steps
•Build/Configuration/Installation/Deployment
•Usage

(1)	**Purpose**:
The purpose of this project is to design and implement a smart class planning tool, which particularly works on scheduling courses across multiple semesters to facilitate timely graduation, manually planning demands substantial dedication and resources from both students and faculty members. So, our smart class advising tool can be executed on Windows, Linux, etc. to generate an efficient class plan for students to get graduate. It checks for any pre-requisite courses and later produces an Excel document containing a 	semester-wise list of recommended courses to graduate efficiently.

(2)	**Prerequisites**:
Before using the Smart Advising Tool, ensure that the following software requirements are met:

•	Python 3.0 or above must be installed
•	Any Code Editor of your choice, prefer to go with PyCharm Community Edition.
•	Install the PyPDF2, XLSXWriter, pyinstaller, and NetworkX libraries using the pip tool
       **Pip install networkX**
Note:- The project setup is explained by keeping windows users as the base users.

(3)	**Download Steps**:
	Get the advising_home.exe file from the main branch of below GitHub repository below.
        https://github.com/kasi1256/SmartClassPlanningTool

(4)	**Build/Configuration/Installation/Deployment:**
**Configuration** – No Additional configuration is needed.
**Installation** – 
1)	Clone the GitHub repository and open the project folder in the IDE.
2)	To Run the application in the local environment the starting point of the project is advising_home.py
3)	We need to pass the input values from the command line of the IDE(the process to send the command line arguments varies from IDE to IDE, refer to IDE Documentation).
4)	Once the Command line values are provided, the application can be tested by clicking the Run Button.

**Deployment** - 
  We have generated the executable file using the below steps:
•	In the terminal of PyCharm use the below command to install pyinstaller if not installed using the GUI of your IDE.
                                **pip install pyinstaller**
•	To create executable file use below command
                                **pyinstaller --onefile advising _home.py**
•	After this command is executed, advising_home.exe file is created in the ‘dist’ folder within the project folder

(5)	**Usage**:
i)	Inputs:
Input 1 - is a pdf file containing information about all the courses required for the student to graduate.
Input 2 -  contains a pre-requisite graph. We are using a NetworkX python library which will parse the pre-requisite graph and get the necessary information about the pre-requisite courses the student needs to take. Acquire the prerequisite course or all required courses for the student's track and provide this in the text format file.
Input-3 is a pdf file containing information about the class schedule informing which courses will be offered in different semesters such as Fall, Summer, and Spring.
ii)	Run the Executable file advising_home through the command line using the below steps.
     i.	Open the command prompt and navigate to the project directory using the “cd” command.
     ii. execute the below script:
        **start advising_home.exe “full path of input sample file” “full path of  pre-	requisite file” “full path of class schedule”**
     iii. After executing the above command, the Excel file will be generated in the same directory where the input1 is located.

iii)	The tool will analyze the inputs and generate the recommended graduation plan.
iv)	The output is obtained in the form of Excel which has different courses scheduled across all the semesters in the project directory.

