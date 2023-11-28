# SmartClassPlanningTool

Table of Contents: 

Purpose 

Prerequisites 

Download Steps 

Build/Configuration/Installation/Deployment 

Usage 

 

**Purpose**: 

The purpose of this project is to design and implement a smart class planning tool, which particularly works on scheduling of courses across multiple semesters to facilitate timely graduation, 
manually planning demands substantial dedication and resources from both students and faculty members. So, our smart class advising tool can be executed on Windows, Linux, etc. 
to generate an efficient class plan for students to graduate. It checks for any pre-requisite courses and later produces an Excel document containing a 
semester-wise list of recommended courses to graduate efficiently. 
 

**Prerequisites**: 

Before using the Smart Advising Tool, ensure that the following prerequisites are met: 

 

List of Remaining Courses: Obtain a PDF document that lists the courses a student still needs to complete graduation. 

Prerequisite Graph: Acquire the prerequisite course or all the required courses for the student's track and provide them in the text format file. 

Program Map: Access the class schedule that indicates when the required courses will be offered. We will consider this input also in the pdf format. 

 

**Download Steps: **

Get the advising_home.exe file 

Open the command prompt and navigate to the project directory. 

execute the below script: 

start advising_home.exe “full path of input sample file” “full path of  pre-	requisite file” “full path of class schedule” 

After executing the above command, the Excel file will be generated in the project directory. 
 

**Build/Configuration/Installation/Deployment:** 

We have generated the executable file using the below steps: 

In the terminal of PyCharm, we use the below command to install pyinstaller 

pip install pyinstaller 

To create an executable file use the below command 

pyinstaller --onefile advising _home.py 

After this command is executed, the exe file is created in the ‘dist’ folder within the project folder 

 

**Usage**: 

**Inputs: **
Input 1 - is a pdf file containing information about all the courses required for the student to graduate. 
Input 2 - contains a pre-requisite graph. We are using a NetworkX python library which will parse the pre-requisite graph and get the necessary information about the pre-requisite courses the student needs to take. Acquire the prerequisite course or all required courses for the student's track and provide this in the text format file. 
Input 3 - is a pdf file containing information about the class schedule informing which courses will be offered in different semesters such as Fall, Summer, and Spring. 

Run the Executable file advising_home through the command line providing the path of all three input files (The command is shown in previous steps). 

The tool will analyze the inputs and generate the recommended graduation plan. 

The output is obtained in the form of Excel which has different courses scheduled across all the semesters in the project directory. 
 
 
