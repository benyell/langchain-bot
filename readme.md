### LangChain Chatbot Project
An end-to-end AI chatbot application built with a FastAPI backend and a Next.js frontend. This project demonstrates a full-stack, containerized system for an AI agent, showcasing skills in API development, modern front-end frameworks, and robust deployment practices.

## Features
* AI Agent Backend: A FastAPI API that hosts a LangChain agent capable of using tools to interact with data.

* Decoupled Architecture: A clean separation of the backend API and the front-end user interface.

* Streaming Responses: The API supports streaming to provide a real-time conversational experience with the chatbot.

* Containerized Development: The entire application is containerized using Docker and Docker Compose for consistent local development and production deployment.

## Project Architecture
This project is structured as a monorepo, containing two distinct services:

* lc-backend: A Python-based FastAPI application that contains the core AI agent logic.

* lc-frontend: A Next.js application that provides the user interface for the chatbot.

The services communicate over a defined API, and the entire system can be launched locally with a single command.

## Technologies Used
### Backend
* Python: The core language for the backend logic.
* FastAPI: A modern, high-performance web framework for building the API.
* LangChain: The framework used to build the AI agent and tools.
* uv: A fast and modern dependency manager for Python.
* Docker: Used to containerize the backend for a reproducible environment.

### Frontend
* Next.js: A React framework for building a fast, static-ready front end.
* React & TypeScript: The language and library for building the user interface.
* Node.js: The runtime environment for the Next.js application.