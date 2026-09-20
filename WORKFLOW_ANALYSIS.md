What triggers this workflow to run? (Look at the on: section)
Workflow is triggered by two different events. When any code is pushed to main, or anytime a pull request is opened or updated against main.

What are the four main steps this workflow performs? (List each step name)
The four main steps that workflow performs are Checkout Code (get the code from the repository), Validate HTML (validates HTML files), Check links (check for broken links), and Upload artifact (upload the built site for deployment)

What does the "Checkout code" step do and why is it necessary?
It copies the code on the runner, without this step there would be no fies for other step to check and deply.

What is the purpose of the environment configuration?
It tells GitHub this job is deploying to the github-pages. This lets GitHub track deployment history and show the live site's URL after deploying.

How does this automated deployment improve reliability compared to manual deployment?
- It runs the same steps every time, so there is no chance of forgetting a step.
- It checks the HTML code and the links automatically before deploying.
- It only deploys from main, so other branches cannot be deployed on accident.
- The only way it can get deployed is if all the checks are passed first.
- Everything that is deployed is logged

What would happen if you pushed code to a different branch (not main)?
Nothing would happen, because the workflow is only triggered on pushes or pull request to main, so a push to other branch does not do anything.