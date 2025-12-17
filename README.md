# HR-Assistant-Bedrock-Agent
HR Assistant Bedrock Agent
This repository contains a Jupyter Notebook (Hr_Assistant-1.ipynb) that demonstrates how to build, deploy, and manage an automated HR Assistant using Amazon Bedrock Agents and AWS Lambda. The agent is designed to help employees interact with HR data, such as checking vacation balances and booking time off, using natural language.

# 🚀 Features
Serverless Architecture: Uses AWS Lambda to execute backend logic and Amazon Bedrock to host the AI agent.

Natural Language Processing: Leverages Foundation Models to understand user intent and parameters.

Automated Data Management: Includes a built-in SQLite database generator to simulate employee records and vacation tracking.

Dynamic Action Groups: Features an "Action Group" that allows the agent to call specific Python functions (like get_available_vacations_days) based on the conversation.

Full Lifecycle Management: The notebook covers everything from IAM role creation and resource provisioning to the final cleanup of all AWS assets.

# 🛠️ Technology Stack
Amazon Bedrock: For creating and invoking the AI Agent.

AWS Lambda: To run the backend logic and database queries.

SQLite: A lightweight database used for storing mock employee data.

Boto3: The AWS SDK for Python used to orchestrate the infrastructure.

# 📋 Prerequisites
Before running the notebook, ensure you have:

An AWS Account with appropriate permissions for IAM, Bedrock, and Lambda.

Model Access enabled in the Amazon Bedrock console (e.g., Anthropic Claude or other supported foundation models).

A Python environment with boto3 installed.

# 📖 Usage
Initialize Environment: The notebook sets up the necessary clients and retrieves your AWS account details.

Database Generation: It creates a local employee_database.db file with 10 mock employees and random vacation history.

#Infrastructure Setup:

Creates IAM execution roles for the Agent and Lambda.

Deploys the Lambda function with the HR logic.

Configures the Bedrock Agent with instructions and the action group schema.

Agent Invocation: Test the agent by asking questions like: "How much vacation does the employee with employee_id set to 1 have available?".

Cleanup: Execute the final cells to delete all created roles, policies, and AWS resources to avoid unnecessary charges.

⚠️ Important Note
The notebook includes a comprehensive cleanup section. It is highly recommended to run these cells once you are finished testing to ensure all policies, roles, and functions are removed from your AWS environment.
