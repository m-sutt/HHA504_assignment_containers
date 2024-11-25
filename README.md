# HHA504_assignment_containers

## Step 1: created a flask app
- Created new directory for project
- Added to code from module 10
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

## Step 3: Deploy to GCP Cloud Run
- Deploy appplication

## Step 4: Deploy to Azure Container Apps (Optional)
-  Setup Azure
-  Deploy application
-  Configure port settings

## Reflections: 
-  GCP was a friendly UX design and more simple. If I ran into an issue it was a relatively easy fix.
-  Azure was also simply but was more stuck a few times and failed to deploy it in multiple instances.
-  Both had different configure steps and some I clicked around and played with it until it works.
-  I ususally run into a network or permission issues
-  When I ran into a coding issue it was related to the pip install or finding the correct file path.
-  
