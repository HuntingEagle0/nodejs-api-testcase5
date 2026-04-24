Test Case 5 — CI/CD Pipeline with GitHub Actions
Scenario: Your team requires an automated pipeline that runs on every code push to the main branch, installs dependencies, builds the Docker image, and simulates a deployment.

Tasks
Inside your nodejs-api repository, create the directory .github/workflows/.
Create a workflow file deploy.yml inside that directory with the following behaviour:
Trigger: On every push to the main branch.
Runner: Ubuntu latest.
Steps:
Check out the repository code.
Set up Node.js version 18.
Install project dependencies.
Build the Docker image tagged as nodejs-api.
Print the message: Deploying application to server...
Commit all changes with the message: "This is the new CI/CD pipeline for CA2" and push to main.
Navigate to the Actions tab on GitHub and confirm the pipeline ran successfully.
Expected Outcome
.github/workflows/deploy.yml is present in the repository.
The GitHub Actions run triggered by the commit shows all 5 steps completing with a green checkmark.
No step fails; the final step prints the deploy message in the logs.
