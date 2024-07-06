# How to Retrieve `PROJECT_ID` and `API_KEY` in IBM Cloud for WatsonX Challenge

In the most of the python codes needed for this challenge you need a project id and api key.

#### 1. Create an IBM Cloud Account
First, ensure you have an IBM Cloud account. If not, sign up at [IBM Cloud](https://cloud.ibm.com/).

#### 2. Create a Watsonx.ai Project
1. **Log in to IBM Cloud**: Go to [IBM Cloud Dashboard](https://cloud.ibm.com/).
2. **Navigate to Watsonx.ai**: In the IBM Cloud dashboard, use the search bar to search for "Watsonx.ai" and select it.
3. **Create a Project**:
   - Click on `Create Project`.
   - Choose a project name and configure any necessary settings.
   - After creation, the project will appear in your list of projects.

#### 3. Retrieve the `PROJECT_ID`
1. **Open the Project**: Click on the name of your project from the list.
2. **Go to the Manage Tab**: Navigate to `Manage -> General`.
3. **Find the Project ID**: Under the `Details` https://github.ibm.com/ruslan-idelfonso-magana-cic/IBM-Learning-Paths-WatsonX/blob/master/Section, you will find the `Project ID`. Copy this value for later use.

#### 4. Create an API Key
1. **Navigate to IAM (Identity and Access Management)**: In the IBM Cloud dashboard, go to `Manage -> Access (IAM)`.
2. **Create an API Key**:
   - Click on `API keys` on the left-hand side.
   - Click on `Create an IBM Cloud API key`.
   - Provide a name and description for the API key.
   - Click `Create`.
   - Once created, make sure to copy the API key as you won't be able to see it again.

### Setting Up the Environment

#### 5. Create a `.env` File
Create a `.env` file in your project directory to store the `PROJECT_ID` and `API_KEY`. This file should look like this:

```
PROJECT_ID=your_project_id_here
API_KEY=your_api_key_here
```

Replace `your_project_id_here` and `your_api_key_here` with the actual values you retrieved earlier.

#### 6. Loading Credentials in Python
Use the following Python snippet to load these credentials from the `.env` file.

```python
import os
from dotenv import load_dotenv

# Load environment variables from the .env file
load_dotenv()

# Retrieve project ID and API key from environment variables
project_id = os.getenv("PROJECT_ID", None)
credentials = {
    "url": "https://us-south.ml.cloud.ibm.com",
    "apikey": os.getenv("API_KEY", None)
}

# Ensure project_id is obtained
try:
    project_id = os.environ["PROJECT_ID"]
except KeyError:
    project_id = input("Please enter your project_id (hit enter): ")


```

### How to Create and Use the `.env` File

1. **Create the `.env` File**: In your project directory, create a file named `.env`.
2. **Add Credentials to the `.env` File**:
   ```
   PROJECT_ID=your_project_id_here
   API_KEY=your_api_key_here
   ```
   Replace `your_project_id_here` and `your_api_key_here` with the actual values.

3. **Ensure `python-dotenv` Library is Installed**: Install the `python-dotenv` package if you haven't already.
   ```bash
   pip install python-dotenv
   ```

4. **Load the `.env` File in Your Python Script**: Use the provided Python snippet to load the credentials.
By following these steps, you will be able to securely store and load your IBM Cloud credentials for use with the Watsonx API.
