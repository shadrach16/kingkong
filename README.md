# KingKong: AI-Native Backend-as-a-Service

KingKong is a revolutionary platform that allows developers to build and deploy robust backends using simple, natural language prompts. This project is structured as a monorepo, containing both the React frontend and the Node.js backend.

KingKong AI Platform Features

The KingKong platform is designed to provide developers and businesses with a centralized environment for AI task execution, custom tool integration, and serverless deployment.

# Core Feature Set

1. AI Task Execution & Playground

    `AI Playground: A dedicated interface (PlaygroundPage.jsx) for users to test prompts and queries against the underlying AI models.`

    `Prompt Templates: Support for saving and utilizing pre-defined prompt templates to streamline common tasks (e.g., "Find users by country," "Count users by status").`

    `AI Configuration: Users can configure AI execution settings, such as the optimiseTask toggle, to fine-tune the performance and output of the AI tasks.`

    `Core AI Task API: A dedicated backend route (/kingkong/run-tasks) to process and execute AI-driven tasks programmatically.`

2. Internal Functions and Tooling

    `Internal Functions Management: Complete CRUD (Create, Read, Update, Delete) functionality for managing custom, user-defined "Internal Functions" (InternalFunctionsPage.jsx, internalFunctionRoutes.js).`

    `Function Execution: API support for running these internal functions (/internal-functions/:projectId/functions/:functionId/run), suggesting they are tools the AI can call or that can be triggered manually.`

    `Integration with AI: The playground data suggests these functions are callable via natural language prompts (e.g., !sendEmail), indicating a powerful AI Tool-Use or Function Calling capability.`

3. Serverless Deployment

    `Serverless Function Creation: Dedicated routes (serverlessRoutes.js) for creating and deploying serverless functions, likely to host external or more complex user logic on the platform.`

4. Logging and Monitoring

    `Centralized Logging Dashboard: A comprehensive LogsPage.jsx for viewing all system, function, and AI execution logs.`

    `Advanced Filtering: Capabilities to filter logs by severity level, associated project, specific date, and content search term.`

    `Log Control: Functionality to sort logs in ascending or descending chronological order.`

5. Platform Management and Analytics

    `Project Scoping: All core features (Internal Functions, Logs) are organized and accessed within specific user-created projects.`

    `Usage Metrics: A dedicated route (usageMetricsRoutes.js) to retrieve and display usage metrics, allowing users to monitor their consumption of platform resources.`

    `Plan and Billing: API access to different pricing plans (planRoutes.js), indicating support for managing subscription tiers and features.`

## Getting Started

Follow the steps below to set up the project and begin development.

### Prerequisites

-   Node.js (v18 or higher)
-   npm

### Installation

1.  Clone the repository:
    `git clone <repository-url> kingkong`
    `cd kingkong`

2.  Install dependencies for both the client and server:
    `npm run install:all`

### Running the Application

To start both the frontend and the backend concurrently in development mode, run:
`npm run dev`

The frontend will be available at `http://localhost:3000` and the backend at `http://localhost:5000`.

Seed the database for billings, run:
`npm run seed`

## Directory Structure

-   `client/`: The React frontend application.
-   `server/`: The Node.js backend application.