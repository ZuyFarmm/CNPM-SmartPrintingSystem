# HCMUT STUDENT SMART PRINTING SERVICE

This repository contains the codebase for a **Printing Service** system. The service enables users to upload files, configure printing preferences, manage print queues, and track print history. Designed with scalability, efficiency, and ease of use in mind, the printing service includes various components to ensure smooth operation and meet both functional and non-functional requirements.

## Features
- **Login**: Authenticate with HCMUT_SSO authentication service.
- **File Upload**: Allows users to upload documents for printing.
- **Print Configuration**: Supports customization options such as color, paper size, and orientation.
- **Print History Tracking**: Records job details for future reference, including job timestamps, document names, and print configurations.
- **Wallet**: Allows users to buy some more pages using the feature Buy Printing Pages of the
system and pay the amount through some online payment system like the BKPay system of the university.
## System Architecture
- **Printer Mananagement**: The SPSO has a feature to manage printers such as add/enable/disable a printer.
- **Printer Modification**The SPSO also has a feature to manage other configuration of the system such as changing the
default number of pages, the dates that the system will give the default number of pages to all
students, the permitted file types accepted by the system.
- **SPSO Report**: The reports of the using of the printing system are generated automatically at the end of each month and each year and are stored in the system, and can be viewed by the SPSO anytime.

The printing service follows a modular architecture for maintainability and scalability, with key components outlined below:

1. **User Interface (UI)**: The front-end interface that enables users to interact with the printing service.
2. **API Gateway**: Manages communication between the UI and backend components, handling user requests and responses.
3. **Backend Microservices**: Includes services responsible for file handling, job processing, and print configuration management.
4. **Database**: Stores information on print jobs, configurations, and user history for tracking and reporting.

This separation allows each component to scale independently and maintain smooth interactions even under heavy load.

## System Models

To support clear and effective system development, various models are used to define requirements and interactions:

- **Use Case Diagrams**: Illustrate user interactions, including file upload, print configuration, and history tracking.
- **Sequence Diagrams**: Define the workflow of a print job from upload to completion.
- **Acitvity Diagrams**: Describe the step-by-step flow of activities involved in the printing process, including file selection, configuration setup, job submission, and completion notification.
- **Class Diagrams**: invaluable for designing, understanding, and maintaining a smart printing system by providing a clear and structured visual representation of the system's components and their interactions.

## Getting Started

### Prerequisites
Frontend
- **npm**: Required for managing packages and running the React application.
- **React**: A JavaScript library for building user interfaces.
- **Tailwind CSS**: Required for styling your application.
Backend
- **Java and Maven/Gradle**: Required to run the Spring Boot application.
- **Spring Boot**
- **Docker**
Optional Dependencies
- **IDE or Editor**: include IntelliJ IDEA, Visual Studio Code
- **Postman or cURL**: Tools for testing your APIs.
### Installation: You will run both BackEnd and FrontEnd simultaneously to run the project 

Clone the repository:
   ```bash
   git clone https://github.com/negative318/CNPM-BTL.git

FrontEnd
1. Navigate to the frontend directory
   cd FE
2. Install dependencies:
   npm install

3. Start the application:
   npm run dev

Test the application by accessing the frontend at (http://localhost:3000) and performing the necessary actions.

BackEnd
1. Navigate to the backend directory
   cd BE
2. install the packaged project into the local Maven repository.
   mvn install
3. compile the code and package it into its distributable format
   mvn package
4. build a Docker image from a Dockerfile in the current directory.
   docker build -t smart-printing-system .
5. run a container from a Docker image with the name and tag smart-printing-system:latest.
   docker run -d -p 8080:8080 smart-printing-system:latest

- BackEnd will run on http://localhost:8080