# devops-practical-test
Solutions to the practical test for devops job evaluation

# CI/CD Pipeline Tasks

## Task 1: Setup a Simple CI/CD Pipeline

### Steps to Complete

1. **Used a GitHub Actions Template**  
   - Picked a basic CI/CD workflow for Node.js and modified it for my needs.

2. **Cloned the Repository**  
   - Ran `git clone` to get the repo locally.

3. **Initialized a Node.js Project**  
   - Inside the `task1` folder, ran `npm init -y` to create a basic `package.json`.

4. **Updated `package.json` for Testing**  
   - Searched online for a simple way to make `npm test` work without real tests.
   - Added a basic test script:
     "scripts": {
       "test": "echo \"Tests passed!\""
     }
     ```

5. **Ran the Pipeline**  
   - Committed and pushed changes to GitHub.
   - The GitHub Actions pipeline installed dependencies and executed test steps.

6. **Checked the Results**  
   - Verified in GitHub Actions that everything ran successfully.
   - Saw the message **"Ready for Deployment"** confirming success.


