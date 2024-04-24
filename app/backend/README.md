# Backend Application Documentation

## Overview
The backend application is a Python-based service that interacts with various APIs and services such as Azure Search, OpenAI, and Azure Blob Storage. It is responsible for handling chat interactions, user authentication, file uploads, and more.

## Key Files

### [`[`app/backend/app.py`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22app%2Fbackend%2Fapp.py%22%5D "app/backend/app.py")`](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fazureuser%2Fazure-search-openai-demo%2Fapp%2Fbackend%2Fapp.py%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\azure-search-openai-demo\app\backend\app.py")
This is the main entry point of the backend application. It sets up the routes for the application and initializes various clients for interacting with external services. It contains the following key routes:

- [`/chat`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22%2Fchat%22%5D "app/backend/app.py"): Handles chat interactions.
- [`/auth_setup`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22%2Fauth_setup%22%5D "app/backend/app.py"): Sends MSAL.js settings to the client UI.
- [`/config`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22%2Fconfig%22%5D "app/backend/app.py"): Returns configuration information.
- [`/upload`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22%2Fupload%22%5D "app/backend/app.py"): Handles file uploads.
- [`/delete_uploaded`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22%2Fdelete_uploaded%22%5D "app/backend/app.py"): Deletes uploaded files.
- [`/list_uploaded`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22%2Flist_uploaded%22%5D "app/backend/app.py"): Lists uploaded files.

### [`[`app/backend/prepdocs.py`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22app%2Fbackend%2Fprepdocs.py%22%5D "app/backend/app.py")`](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fazureuser%2Fazure-search-openai-demo%2Fapp%2Fbackend%2Fprepdocs.py%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\azure-search-openai-demo\app\backend\prepdocs.py")
This file contains functions for setting up file processors and running the main strategy for document preparation.

### [`[`app/backend/approaches/approach.py`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22app%2Fbackend%2Fapproaches%2Fapproach.py%22%5D "app/backend/app.py")`](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fazureuser%2Fazure-search-openai-demo%2Fapp%2Fbackend%2Fapproaches%2Fapproach.py%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\azure-search-openai-demo\app\backend\approaches\approach.py")
This file defines the [`Approach`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapproaches%2Fapproach.py%22%2C%22Approach%22%5D "app/backend/approaches/approach.py") abstract base class and related data classes. An approach represents a strategy for handling chat interactions.

## Setup
The backend application requires several environment variables to be set, including credentials for Azure and OpenAI. These are set up in the [`setup_clients`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22setup_clients%22%5D "app/backend/app.py") function in [`[`app.py`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fapp.py%22%2C%22app.py%22%5D "app/backend/app.py")`](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fazureuser%2Fazure-search-openai-demo%2Fapp%2Fbackend%2Fapp.py%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\azure-search-openai-demo\app\backend\app.py").

## Running the Application
The application can be started by running the [`main`](command:_github.copilot.openSymbolInFile?%5B%22app%2Fbackend%2Fprepdocs.py%22%2C%22main%22%5D "app/backend/prepdocs.py") function in [``prepdocs.py``](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fazureuser%2Fazure-search-openai-demo%2Fapp%2Fbackend%2Fprepdocs.py%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\azure-search-openai-demo\app\backend\prepdocs.py").

For more detailed information, please refer to the code in the [`app/backend`](app/backend) directory and the provided documentation in the [`docs`](docs) directory.