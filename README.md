# HHA504_assignment_containers

## Step 1: created a flask app
- Created new directory for project
- Added to code from module 10
<img width="1310" alt="1" src="https://github.com/user-attachments/assets/56b6eaae-5f9a-4fde-9ebf-d2a9ef3c22fa">

  - Generates a random number between 1 and 100 and go back to a home page in the `app.py`

```python
from flask import Flask
import random


app = Flask(__name__)   #creates a flask app instance

@app.route("/")
def home():
    return "<h1> Hello, World! Welcome to My Flask App!</h1>"

@app.route("/random")
def random_number():
    return f"<h2>Your random number is: {random.randint(1, 100)}</h2>"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=8080)
```

- Added to requirements.txt
- Created dockerfile
- Test app locally

## Step 2: push docker image to Docker Hub
- Tag and push image
<img width="672" alt="3" src="https://github.com/user-attachments/assets/35e51848-2e6b-47e7-ad34-3734eb1726c5">


## Step 3: Deploy to GCP Cloud Run
- Deploy appplication
<img width="1303" alt="2" src="https://github.com/user-attachments/assets/4d9bd372-a554-4dd6-b8bb-22d45e5f2c5e">

<img width="587" alt="4" src="https://github.com/user-attachments/assets/9c3c8571-86df-4cc1-9848-ea388c6a9b80">

## Step 4: Deploy to Azure Container Apps (Optional)
-  Setup Azure
<img width="821" alt="1" src="https://github.com/user-attachments/assets/589701db-1911-49cf-8a0c-280b71346255">
<img width="413" alt="2" src="https://github.com/user-attachments/assets/3fc13e6c-8a53-4984-b234-8442264054d3">

-  Deploy application
-  Configure port settings

## Reflections: 
-  GCP was a friendly UX design and more simple. If I ran into an issue it was a relatively easy fix.
-  Azure was also simply but was more stuck a few times and failed to deploy it in multiple instances.
-  Both had different configure steps and some I clicked around and played with it until it works.
-  The most frequent error that happened was an error I couldn't get pass from Azure is the registry login server
-  When I ran into a coding issue it was related to the pip install or finding the correct file path.

