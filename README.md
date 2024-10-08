﻿# Automated-Gmail-Replier

The Automated Gmail Replier is a Node.js application that automates the process of responding to unreplied emails during a specified period, such as a vacation. It leverages the Gmail API to interact with your Gmail account and perform actions like sending automated replies and labeling emails related to your vacation.

## Table of Contents

- Features
- Getting Started
  - Prerequisites
  - Installation
- Obtaining Credentials
- Configuration
- Usage

## Features

- Automatically sends a predefined vacation response to emails that haven't been replied to.
- Labels incoming emails during your vacation period for better organization.
- Periodically checks for unreplied emails and responds accordingly.

## Getting Started

### Prerequisites

1. Node.js installed on your machine. You can download it [here](https://nodejs.org/).
2. Gmail API credentials:
     - Follow the instructions in Obtaining credentials.json file section to create a project, enable the Gmail API, and obtain the `credentials.json` file.

### Installation

1. Clone the repository: `git clone https://github.com/gauravjalap/Automated-Gmail-Replier.git`
2. Go to the App Folder. `cd Automated-Gmail-Replier`
3. Open the CodeBase in your IDE. `code .`
4. Install the node_modules. `npm install`
5. Run the App. `node index.js`

The application will start on http://localhost:5000.

## Obtaining credentials.json File

To use the Gmail API, you need to set up API credentials. Follow these steps:

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project by clicking on the "Select a project" dropdown in the top bar, then click on "New Project."
3. Select the newly created project by clicking on "Select a project" again.
4. In the Cloud Console, navigate to the API & Services Dashboard by searching for "API & Services" in the top search bar.
5. Click on "Enable APIs and Services."
6. In the search bar, type "Gmail API" and select it.
7. Click the "Enable" button to enable the Gmail API for your project.
8. Go to the "OAuth consent screen" by clicking on it in the sidebar.
9. Choose the "External" user type for now and fill out the required information in the OAuth consent screen form. Click "Save and Continue" to proceed to the next step.
10. Add the required scopes by clicking on "Add or Remove Scopes" in the "Scopes" section. Add the following scopes:
    [https://www.googleapis.com/auth/gmail.readonly](https://www.googleapis.com/auth/gmail.readonly)
    
    [https://www.googleapis.com/auth/gmail.send](https://www.googleapis.com/auth/gmail.send)
    
    [https://www.googleapis.com/auth/gmail.labels](https://www.googleapis.com/auth/gmail.labels)
    
    [https://mail.google.com/](https://mail.google.com/)
12. Click "Save and Continue."
13. Add test user emails that you want to manage or send automated replies to using this application. Click "Save and Continue."
14. Go to the "Credentials" section in the sidebar.
15. In the "OAuth 2.0 Client IDs" section, find the entry related to your application. Click on the download icon to download the JSON file containing your credentials.
16. Rename the downloaded JSON file to `credentials.json`.
17. Place the `credentials.json` file in the root directory of the automated Gmail responder application.

## Configuration

1. Modify the `labelName` variable in the `index.js` file to set the name of the label for vacation-related emails.
2. Adjust the vacation response message in the `sendReply` function.
3. The interval for checking emails is set randomly between 45 to 120 seconds. You can modify this interval in the `setInterval` function.

## Usage

1. Access the application by visiting [http://localhost:5000](http://localhost:5000) in your browser.
2. The application will authenticate with your Gmail account using the credentials in `credentials.json`.
3. Once authenticated, it will create a label for vacation-related emails (if not already exists) and periodically check for unreplied emails, sending automated responses and applying the vacation label.
‣畁潴慭整ⵤ浇楡⵬敒汰敩ੲ
