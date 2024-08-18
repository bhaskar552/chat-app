# Real-Time Chat Application

## Overview

This project is a real-time chat application built with modern web technologies. It enables users to communicate instantly, observe online/offline status, receive typing indicators, and share media files.

## Features

- **Real-time messaging** between users
- **User authentication** (signup and login)
- **Online/offline status** indicators
- **"Typing..." indicator** while chatting
- **Read/unread message** sorting system
- **Image and video upload** functionality
- **Infinite scrolling** of messages
- **Last seen timestamp** for users

## Tech Stack

### Frontend

- **React** (Vite)
- **Tailwind CSS**
- **Socket.IO Client**

### Backend

- **Node.js**
- **Express.js**
- **Socket.IO**
- **Neon Postgres** (Database)
- **Drizzle ORM**

### Authentication & Security

- **bcrypt** (for password hashing)
- **JSON Web Tokens (JWT)**

## Project Structure

The project is divided into two main folders:

1. `messaging-app/`: Contains the frontend React application
2. `server/`: Houses the backend Node.js server

## Prerequisites

- **Node.js** (v14 or later recommended)
- **npm** (Node Package Manager)
- **PostgreSQL database** (We're using Neon Postgres)

## Setup & Installation

### Install dependencies for the frontend and backend:

```bash
cd messaging-app
npm install
cd ..
cd server
npm install
cd ..
```
# Chat Application Setup Guide

## Environment Setup

1. Create a `.env` file in the server directory with the following content:

   ```bash
   PORT=3001
   CLIENT_URL=http://localhost:5173
   DATABASE_URL="your neon postgres url"
   JWT_SECRET=your_secret_key
   ```

   Replace `DATABASE_URL` and `JWT_SECRET` with your actual database URL and a secure secret key.

## Database Setup



Use Drizzle ORM migrations to create the database schema 
run the migrations commands 
```bash
cd server
npm run migrate
npm run push
```



## Running the Application

1. Start the backend server:

   ```bash
   
   npm run dev
   
   ```

   The backend server will start at `http://localhost:3001`.

2. Start the frontend application:
   start a new terminal 

   ```bash
   cd messaging-app
   npm run dev
   ```

   The frontend will be available at `http://localhost:5173`.

4. Access the application:
   Open your web browser and go to `http://localhost:5173`.

## Usage

1. Sign up for a new account or log in with existing credentials.
2. Select a user from the available list to start chatting.
3. Send messages and share media files instantly.
4. View user status (online/offline), typing indicators, and read/unread messages.
5. Scroll up to load previous messages (infinite scrolling).

## Key Components

- **Authentication**: Passwords are securely hashed using bcrypt, and JWTs manage user sessions.
- **Real-time Communication**: Socket.IO is used to facilitate instant messaging and real-time status updates.
- **Media Uploads**: Images and videos are stored on the server, with references in the database.
- **Database Interactions**: Drizzle ORM is used for efficient and type-safe operations with Neon Postgres.


