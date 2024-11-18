# HHA504_assignment_containers


## 1. Created a simple flask app  
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
