# GitHub Actions CI/CD with Python and AWS EC2

## Project Overview
This project demonstrates Continuous Integration (CI) and Continuous Deployment (CD) using GitHub Actions, Python, and AWS EC2.

## Technologies Used
- Python
- Git and GitHub
- GitHub Actions
- AWS EC2
- Ubuntu Linux
- SSH

## Project Structure

```text
Github-actions-demo/
├── app.py
├── README.md
└── .github/
    └── workflows/
        ├── ci.yml
        └── deploy.yml
```

## Continuous Integration (CI)
The CI workflow runs automatically when code is pushed to the `main` branch.

CI steps:
1. Checkout source code.
2. Set up Python.
3. Run the Python application.
4. Verify that the workflow completes successfully.

## Continuous Deployment (CD)
The CD workflow deploys the Python application to an AWS EC2 instance.

CD steps:
1. Run the Python application check.
2. Connect to EC2 using SSH.
3. Copy `app.py` to the EC2 server.
4. Execute the Python application on EC2.

## Setup Instructions

1. Install Python and Git.
2. Clone this repository.
3. Configure the AWS EC2 Ubuntu instance.
4. Add the required GitHub repository secrets:
   - `EC2_HOST`
   - `EC2_USERNAME`
   - `EC2_SSH_KEY`
5. Push changes to the `main` branch.
6. Check the **Actions** tab to monitor workflow runs.

## Run Locally

```bash
python app.py
```

## Expected Output

```text
Hello GitHub Actions CI/CD
```

## Security Notes
- Never commit private SSH keys or credentials to the repository.
- Store deployment credentials in GitHub Actions Secrets.
- Restrict server access and review third-party GitHub Actions before using them.

## Author
Mohan Kumar Reddy