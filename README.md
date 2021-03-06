# Trishan-Vassan-Kza-Test-Automation-Challenge

## Table of Contents

* [Deliverables](#deliverables)

* [How to Setup Repo, Run Tests and Generate Test Results](#how-to-setup-repo-run-tests-and-generate-test-results)

* [Screen Recording Showing Backend Test Running and Test results Generation](#screen-recording-showing-backend-test-running-process-and-test-report-generation)

<br />

# Deliverables

[Table of Contents](#table-of-contents)

* Create a series of **manual test cases** that covers the CRUD operations on Trello board. Cover both **positive** & **negative** cases.
  * This Deliverable can be found in this folder : [Deliverables](/Deliverables/) , in the ***Manual Test Cases.pdf*** file

<br />

* Create **test plan** for the above created test cases. Approach to decide what needs to be tested at Back-End & Front-End
  * This Deliverable can be found in this folder : [Deliverables](/Deliverables/) , in the ***Test Plan.pdf*** file
  
<br />

* Perform **CRUD operations** on Trello board. Automate (at least three) of the previously created test cases for both UI and Back-End.

<br />

This Deliverable can be found here :
  
* Frontend Automated Test Features
  * [Create Frontend Scenarios](/FrontendAutomatedTests/Features/CreateScenarios.feature)
  * [Read Frontend Scenarios](/FrontendAutomatedTests/Features/GetScenarios.feature)
  * [Update Frontend Scenarios](/FrontendAutomatedTests/Features/UpdateScenarios.feature)
  * [Delete Frontend Scenarios](/FrontendAutomatedTests/Features/DeleteScenarios.feature)

<br />

* Frontend Automated Test Features
  * [Post/Create Backend Scenarios](/BackendAutomatedTests/Features/CreateScenarios.feature)
  * [Get/Read Backend Scenarios](/BackendAutomatedTests/Features/GetScenarios.feature)
  * [Put/Update Backend Scenarios](/BackendAutomatedTests/Features/UpdateScenarios.feature)
  * [Delete Backend Scenarios](/BackendAutomatedTests/Features/DeleteScenarios.feature)
  
<br />

* **Provide a test report.**

  * This Deliverable can be found in this folder : [Deliverables](/Deliverables/) , in the ***Test Report.pdf*** file

  * Frontend Test Results Report can be found here : [Frontend Automated Results](/Test_Results/LivingDocFrontend.html) - To open correctly , you will need to clone the repo first then You can download the HTML file and then open it in a browser to view test results
  * Backend Test Results Report can be found here : [Backend Automated Results](/Test_Results/LivingDocBackend.html) - To open correctly , you will need to clone the repo first then You can download the HTML file and then open it in a browser to view test results

<br />

* How to Setup Repo, run tests and produce test results
  * This Deliverable is listed step by step in the next section but can also be found can be found in this folder : [Deliverables](/Deliverables/) , in the ***Test Setup and Run.pdf*** file

<br />

**Alternatively, all Deliverables are available in the following Google Drive folder :**  [Google Drive Deliverables folder](https://drive.google.com/drive/folders/1g9KNgwbqAdbl6i_D7t3sO0kpdaOeCRks?usp=sharing)

<br />

# How to Setup Repo, Run Tests and Generate test results

[Table of Contents](#table-of-contents)

Once the Repo has been successfully cloned these steps can be used to set up the tests and execute them locally

1. Clone the repo if not done yet

````
git clone https://github.com/Trishan97/Trishan-Vassan-Kza-Test-Automation-Challenge.git
````

or through Visual Studio or any other C# compatible IDE

![IDE clone](/Media/Screenshots/clone_vs.PNG)

<br />

2. Once the Repo has been successfully cloned , open up the TrishanKzaAssessment.sln solution file if it has not automatically been opened

   Once opened you may get a prompt to Install the targeting version of .NET if you do not have it installed yet  :

   ![not installed](/Media/Screenshots/Not_installed.PNG)

    **This is only relevant if you have received the above Prompt**
   Install the targeting version of .NET Core 3.1 Runtime (LTS) through the visual studio installer :

   ![Netcore3](/Media/Screenshots/netcore.PNG)

You may need to reopen visual studio and the project after installation and open the sln file again

<br />

3. Once that dependency has been installed successfully your solution should open up and look like this

<br />

* ![Solution](/Media/Screenshots/solution.PNG)

<br />

4. The next step is to restore Nuget packages for the solution , this can be done by right clicking on the Solution file **Solution 'TrishanKzaAssessment' (2 of 2 projects)** and clicking on the **Restore NuGet Packages** Option

   ![Nuget](/Media/Screenshots/RestoreNuget.PNG)

<br />

5. After that has been successfully completed the next step is to build the solution, this can be done by right clicking on the Solution file **Solution 'TrishanKzaAssessment' (2 of 2 projects)** and clicking on the **Build Solution** Option

You can verify that the solution has built successfully by looking at the output window and gettgng a build succeeded message :

![Nuget](/Media/Screenshots/BuildSolution.PNG)

6. The next step is to click on the **Test** option in the top ribbon and then select the **Test Explorer** option

   ![ribbon](/Media/Screenshots/TestRibbon.PNG)

This will then open the test explorer view with all available tests, and view each scenario by clicking on the little arrow next to each Test

7. In order to run the test you can either:

* Run an individual test by right clicking on a test case you would like to run, then selecting the **Run** option

   ![Individual Test Run ](/Media/Screenshots/IndividualTestRun.PNG)

or

* Run all tests by selecting the **Run all tests in view** option on the top left of the Test Explorer

  ![All Tests Run ](/Media/Screenshots/RunAllTestsOption.PNG)

8. Once you have run either individual tests or all test cases the results will be displayed in the test explorer with the pass or fail status as well as how long each test took

   ![Test results explorer](/Media/Screenshots/TestResultsExplorer.PNG)

9. These next steps are **Optional** if you would like to get a current test report of the tests you have just run. This can be done so by installing Specflows' living doc CLI and then following the remaining steps listed. Also **please note** that a current test report can only be generated **once a test run has been completed** (this can be a single test, selected test or all tests) but a test does need to be run before completing the following steps for either the Frontend or backend :

* Open a command prompt and install living doc with this command :

````
   dotnet tool install --global SpecFlow.Plus.LivingDoc.CLI
````

* [Link to LivingDoc Documentation](https://docs.specflow.org/projects/specflow-livingdoc/en/latest/LivingDocGenerator/Installing-the-command-line-tool.html)

* Once that has been successfully installed, navigate to the folder where the repo has been cloned to, an easy way to do this is by right clicking on the Solution file **Solution 'TrishanKzaAssessment' (2 of 2 projects)** and selecting the **Open Folder in File Explorer** option :

   ![File Explorer](/Media/Screenshots/OpenFileInExplorer.PNG)

* This should then open up the following folder :

   ![Batch File](/Media/Screenshots/Batchfile.PNG)

* Finally you can open either the **ViewBackendTestsResults.bat** file or the **ViewFrontendTestResults.bat** file to view the results of the automated tests in a nicely presented GUI format e.g. :

   ![ Report eg ](/Media/Screenshots/reportExample.PNG)

* What the batch files execute for Frontend report:

````
cd FrontendAutomatedTests\bin\Debug\netcoreapp3.1

livingdoc test-assembly "FrontendAutomatedTests.dll" -t TestExecution.json
LivingDoc.html
````

* For Backend Test Report

````
cd BackendAutomatedTests\bin\Debug\netcoreapp3.1

livingdoc test-assembly "BackendAutomatedTests.dll" -t TestExecution.json
LivingDoc.html
````

* **Note Again** the TestExecution.json file will only be generated once a test run has been completed and the report generation can only be done through the batch file if the SpecFlow.Plus.LivingDoc.CLI has been installed as stated in one of the previous steps

* From these reports you can view in detail each scenario and additional information about each, there is also an analytics page which shows the tests run vs tests passed or failed, which can be useful when presenting test results to a client, team or stakeholder

   ![ Analytics ](/Media/Screenshots/analytics.PNG)

<br />

# Screen Recording showing Backend Test Running Process and Test Report Generation

[Table of Contents](#table-of-contents)

<https://user-images.githubusercontent.com/30235965/155113551-be451673-f41e-4f47-a243-b0a3e50f470e.mp4>
