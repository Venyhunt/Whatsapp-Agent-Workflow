##Automated WhatsApp Birthday Messaging Workflow

Overview:
This project is an automated workflow that sends personalized birthday messages via WhatsApp.

It reads contact data from Google Sheets, checks for birthdays daily, generates a custom message using a language model, and sends it automatically using a WhatsApp API.

The goal of this project was to explore how simple AI-powered workflows can be built for real-world personal use cases.

Features:
Daily automated birthday check
Personalized message generation using an LLM
WhatsApp message delivery via API
Contact management using Google Sheets
Logging of sent messages

Tech Stack:
n8n – workflow automation
Green API – WhatsApp messaging
Google Sheets – data storage
Mistral 7B – message generation

Workflow Architecture:
A scheduled trigger runs daily
Contact data is fetched from Google Sheets
Birthdays matching the current date are filtered
A personalized message is generated using an LLM
The message is sent via WhatsApp using Green API
The sent message is logged back into Google Sheets

Setup Instructions:

1. Clone the repository
git clone https://github.com/Venyhunt/Whatsapp-Agent-Workflow

2. Set up n8n
Install and run n8n locally
Import the provided workflow JSON file

3. Configure Google Sheets
Create a sheet with the following columns:
Name | Phone | Birthday | Notes
Ensure phone numbers are stored without country code
Update n8n credentials for Google Sheets access

4. Set up Green API
Create an account on Green API
Generate an instance and API token
Scan the QR code to connect your WhatsApp
Replace the API URL and token in the HTTP Request node

5. Configure LLM
Connect your LLM provider (Mistral 7B or equivalent)
Update the prompt in the LLM node as needed

6. Run the workflow
Execute manually for testing
Enable the schedule trigger for automation

Limitations:
Uses a workaround for WhatsApp personal messaging (not an official API)
Free-tier APIs may have rate limits
Requires the WhatsApp session to remain active

Future Improvements:
Integrate with official WhatsApp Business API
Add retry and error handling
Improve message personalization using richer context
Build a UI/dashboard for managing contacts



This project was inspired by discussions around automation and agent-based workflows, and serves as a small step toward exploring practical AI systems.
