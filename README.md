#  Django Deployment on AWS (EC2) with CI/CD

This project demonstrates deploying a Django app to AWS EC2 using Gunicorn, Nginx, and GitHub Actions.

##  Project Setup

### CLone the repo
git clone <repo_url>

### Run Django Project
▪ python manage.py makemigrations
▪ python manage.py migrate
▪ python manage.py runserver

### add project requirements in requirements.txt

## Deployment on EC2

### SSH into the EC2 instance.

### Install dependencies: sudo apt install python3-venv nginx git

### Clone repo and repeat setup steps above.

### Start Gunicorn:

venv/bin/gunicorn --bind unix:/home/ubuntu/<repo>/gunicorn.sock deployment_task.wsgi:application

### Configure Nginx and then reload

### GitHub Actions (CI/CD)
Workflow runs tests on each push and deploys to EC2 on main branch.

### Required Secrets:
HOST, USERNAME, KEY

## Notes
### Use .env for secrets (add it to .gitignore)

### SSL configuration (Certbot + domain required)
