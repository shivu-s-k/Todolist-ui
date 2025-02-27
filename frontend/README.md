# README.md  

## Project Overview  
This project involves using **Google AI Studio** to generate prompts for the **Gemini API**, setting up a **Python application**, and containerizing it using **Docker**. The goal is to ensure the application runs smoothly in a controlled environment and can interact with the AI model efficiently.  

---

## 1. Chosen Prompt  
I used the following prompt in **Google AI Studio**:  

> *"Generate a response for a chatbot that provides helpful and concise answers to users' questions about technology."*  

This prompt was tested and refined to ensure clear and informative responses from the Gemini API.  

---

## 2. Obtaining the Code  
1. I accessed **Google AI Studio** and tested the chosen prompt.  
2. Once satisfied, I copied the sample API request code.  
3. I created a local project folder and saved the code in a file .  

---

## 3. Setting Up the Docker Container  
1. **Install Docker** (if not installed) from [Docker's official website](https://www.docker.com/).  
2. **Create a `Dockerfile`** in the project folder and add the following content:  

   ```Dockerfile
   # Use an official Python runtime as a base image
   FROM node:14 

   # Set the working directory
   WORKDIR /app

   # Copy the project files
   COPY . .

   # Install dependencies
   RUN pip install -r requirements.txt

   # Expose port for the application
   EXPOSE 5000

   # Command to run the application
   CMD ["npm", "start"]
   ```  

3. **Create a `requirements.txt`** file with necessary dependencies:  

   ```
   flask
   google-generativeai
   requests
   ```  

---

## 4. Running the Code Locally with Docker  
1. **Build the Docker image**:  

   ```sh
   docker build -t my-ai-app .
   ```  

2. **Run the container**:  

   ```sh
   docker run -p 5000:5000 my-ai-app
   ```  

3. **Access the application**: Open **http://localhost:5000/** in a web browser to see the AI responses.  

---

## 5. Screenshot of the Running Application  
A screenshot of the application running on **http://localhost/** is included in the GitHub repository.  

---

## Conclusion  
This project helped me understand **AI prompt engineering**, **Docker containerization**, and how to deploy an AI-powered Python application. I also learned how to troubleshoot dependency issues and optimize the **Dockerfile** for better performance.
