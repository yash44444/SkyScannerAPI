# SkyScannerAPI
Download Postman
Import all the files present in repo.
Run collections.

## Test Plan

* Define the API endpoints to be tested and the scope of the testing.
* Identify the input parameters required by each API endpoint, including headers, query parameters, and request bodies.
* Identify the expected output for each API endpoint, including response codes, response bodies, and any other relevant output.
* Determine the automation framework and tools to be used for testing the API endpoints.
* Develop test cases that cover all possible scenarios for the API endpoints, including both positive and negative test cases.
* Create test data and test environment setup for testing the API endpoints.
* Execute the test cases and report any issues or bugs found during testing.
* Analyze the results of the testing and identify areas for improvement.
* Automate the regression testing process to ensure that any changes to the API endpoints do not break existing functionality.
* Integrate the API automation testing with the CI/CD pipeline for continuous testing and deployment.
* Ensure that the API automation test plan is maintained and updated as new features and endpoints are added to the API.

## How would you Integrate API tests with CI/CD pipelines ?

* Create a repository in Github: Create a new repository in Github to store UI/API tests.
* Clone the repository to your local machine: Clone the repository to your local machine using Git or Github Desktop.
* Create the test scripts: Create the test scripts and save them in the repository.
* Push the changes: check in local changes to github using necessary git commands. The default branch would be Master/Main.
* Setup CI/CD tool: Install Jenkins locally on local host.
* Install and configure the Jenkins Github plugin: You can install the Github plugin in Jenkins by going to "Manage Jenkins" > "Manage Plugins" > "Available" > "Github Plugin". 
* Once installed, configure the plugin with your Github credentials, including the access token, which can be generated from Github.
* Create a new Jenkins job: In the Jenkins dashboard, select "New Item" and give your job a name. Choose the "Freestyle project" or "Pipeline" job type depending on your needs.
* Configure the job: In the job configuration, configure the Source Code Management section to connect to your Github repository. Specify the repository URL, branch, and credentials. If using Jenkinsfile, specify the path to the Jenkinsfile in the "Pipeline script from SCM" section.
* Add build triggers: To trigger builds automatically when changes are pushed to Github, enable "Github webhook trigger" in the Build Triggers section. You'll need to * specify a unique webhook URL provided by Jenkins, and configure Github to send a webhook notification to this URL.
* Define build steps: Specify the build steps that Jenkins will run when triggered. This can include compiling the code, running tests, deploying to a server, and more.
* Save and run the job: Save the job configuration and trigger the first build manually to test the integration.
* Monitor the job and logs: Check the job status and console output to verify that the integration is working as expected. If there are any issues, debug the logs to determine the root cause.

## Explain a particularly challenging testing project they you have worked on in the past and how did you overcome the obstacles?

SOR Automation framework - 
Problem statement:  The project was to automate the API fields present in different System of records ( SOR ) like SAP, CIS, BASE24, Transform 
for different nationwide journeys like Current account opening, Saving account opening, Credit card journey.  There were almost 150 fields present
in these different SORs. The existing approach was to run the APIs in solo and validate the response manually in the SORs. SOR here means DB. 
Validating these many fields manually in different sections of SORs was a time consuming and exhaustive task. Another problem was about the licencing cost
of Ready API tool since the team which do system testing using Ready API but the team which do System integration testing and SOR validation used Postman.
So the new framework was finalized to be built in postman to avoid licencing cost. Also the SIT team were familiar with Javacript, so we decided to upskil
ourselves to learn JS, Postman han using Groovy scripting. 

Solution - First of all, list of all the fields were collected from SIT testers which were validated during their run. Then a hunt started to identify all 
the nationwide APIs which would retrieve these fields in their response and could be compared with SOR in automated way. This exercise ran almost 3 months since
multiple teams were needed to be discussed with. All the APIs were then analysed , setting up required data and build the request to run on postman in different
environments. Faced challenges wrt tokens, ssl certificates, end points, request, infra set up, deploying postman on individual machines, communicating with infra team, 
automation testers from other team, mock run of e2e framework n number of times. Getting the results verified from SIT testers. 
Finally when the framework became stable n mature, now the SOR validation was made easy n reduced SIT effort by almost 40%. 
