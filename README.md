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
