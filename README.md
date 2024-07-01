## IBM watsonx Challenge
![](assets/2024-06-28-14-29-06.png)
Welcome to my personal repository for the 2024 IBMer watsonx Challenge! 

This repository is your ultimate guide to navigating the different tracks of the challenge and finding the resources you need to succeed.

### Challenge Tracks

| Track Number | Track Name                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                  | Tool                                                                                                                            | Tutorial                                                                                                                               |
| :----------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| 1            | Create a custom productivity workflow to enhance the IBMer AskIBM experience                                                                                                | Build AskIBM workflows using generative AI to improve productivity, automate tasks, and solve business problems. No coding skills needed.                                                                                                                                                                                                                              | AskIBM                                                                                                                           | [Link to AskIBM Tutorial](./track1/README.md)                                                                                    |
| 2            | Create new or combine existing Consulting Assistants to address a client or role-based business need in a new or innovative way                                             | Use IBM Consulting Assistants in predefined scenarios based on real-world opportunities or challenges. No coding skills needed.                                                                                                                                                                                                                                           | IBM Consulting Advantage/Assistants                                                                                              | [Link to IBM Consulting Advantage Tutorial](./track2/README.md)                 |
| 3            | Demonstrate how WCA@IBM transforms and accelerates your software development practices in the most creative and impactful way                                                 | Show how WCA@IBM, an AI Code Assistant, transforms your software development practices. Requires basic coding knowledge in supported languages.                                                                                                                                                                                                                          | WCA@IBM                                                                                                                        | [Link to WCA@IBM Tutorial](./track3/README.md)                                                                                 |
| 4            | Solve a use case supporting IBMer productivity using watsonx.ai                                                                                                                | Extract and summarize information from documents to answer questions and improve productivity. Option to bring your own business problem and dataset.                                                                                                                                                                                                                   | watsonx.ai                                                                                                                       | [Link to watsonx.ai Tutorial](./track4/README.md)                                                                            |
| 5            | Create a RAG-based generative AI workflow using watsonx platform (watsonx.ai and watsonx.data)                                                                                 | Create a Retrieval Augmented Generative (RAG) workflow using watsonx.ai and watsonx.data. Requires an experienced data engineer on the team. Option to bring your own use case and dataset.                                                                                                                                                                                    | watsonx.ai and watsonx.data                                                                                                    | [Link to watsonx.ai and watsonx.data Tutorial](./track5/README.md)                                         |
| 6            | Design an AI Assistant that helps users resolve a set of business tasks for a front or back office function to improve productivity                                         | Design, build, and launch an AI assistant using Watsonx Orchestrate to maximize productivity.                                                                                                                                                                                                                                                                   | watsonx Orchestrate                                                                                                          | [Link to watsonx Orchestrate Tutorial](./track6/README.md)                                                         |
| 7            | Modify existing or add new knowledge and skills to improve the accuracy of answers provided by Granite                                                                       | Suggest a use case for embedding Granite and use InstructLab to improve the model. Requires developer experience and specific hardware.                                                                                                                                                                                                                                | InstructLab                                                                                                                    | [Link to InstructLab Tutorial](./track7/README.md)                                                                         |



## Tutorials and Resources

Track 1: [AskIBM Tutorial](./track1/README.md)

Track 2: [IBM Consulting Advantage Tutorial](./track2/README.md)

Track 3: [WCA@IBM Tutorial](./track3/README.md)

Track 4: [watsonx.ai Tutorial](./track4/README.md)

Track 5: [watsonx.ai and watsonx.data Tutorial](./track5/README.md)

Track 6: [watsonx Orchestrate Tutorial](./track6/README.md)

Track 7: [InstructLab Tutorial](./track7/README.md)

General Challenge Resources: [2024 IBMer watsonx Challenge Website](./track8/README.md)

In the most of the python codes needed for this challenge you need a project id and api key.

### How to Retrieve `PROJECT_ID` and `API_KEY` in IBM Cloud for WatsonX Challenge

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
3. **Find the Project ID**: Under the `Details` section, you will find the `Project ID`. Copy this value for later use.

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

# Print out the credentials to verify (for debugging purposes only, remove in production)
print("Project ID:", project_id)
print("API Key:", credentials["apikey"])
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



I desire you the best of luck in the 2024 IBMer watsonx Challenge!
