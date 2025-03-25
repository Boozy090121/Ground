# Organization Management Hub

A full-stack, scalable, and modular web application for quality teams to plan, structure, assign, and optimize resources across departments, clients, and focus factories.

## Features

- Position-based RACI mapping
- Skills matrix tied to roles and people
- Full org chart builder (current & future state)
- Team assignment by client
- Summary dashboards for leadership
- Exportable, client-safe views

## Prerequisites

Before getting started, make sure you have the following installed:

- Node.js (LTS version)
- Git
- Firebase CLI (`npm install -g firebase-tools`)

## Setup Instructions

1. Clone the repository:
   ```
   git clone <repository-url>
   cd organization-management-hub
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Set up Firebase:
   - Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Enable Email/Password Authentication, Firestore, and Storage (optional)
   - Configure security rules for Firestore and Storage
   - Create a `.env` file by copying `.env.example`:
     ```
     cp .env.example .env
     ```
   - Fill in your Firebase configuration values in the `.env` file

4. Start the development server:
   ```
   npm start
   ```

5. Access the application at [http://localhost:3000](http://localhost:3000)

## Project Structure

```
/src
  /components      # Reusable UI components
  /pages           # Application pages
  /services        # Services like Firebase integration
  /contexts        # React contexts for state management
  /utils           # Utility functions
  /assets          # Static assets
/public            # Public static files
```

## Core Modules

### Org Designer
Interactive org chart with drag-and-drop functionality, role details, and export capabilities.

### RACI Matrix
Position-based RACI mapping for tasks and processes with export options.

### Skills Matrix
Track required skills by role and actual skills by person to identify gaps.

### Client Assignments
View and manage team assignments by client with export options.

### Dashboard
Overview of key metrics and team composition across factories and clients.

## Deployment

The application can be deployed using Firebase Hosting:

1. Build the production version:
   ```
   npm run build
   ```

2. Deploy to Firebase:
   ```
   firebase login
   firebase init    # If not already initialized
   firebase deploy
   ```

## License

[MIT License](LICENSE) 