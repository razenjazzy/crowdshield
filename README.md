## Introduction
“CrowdShield”: A Decentralized Donation-Based Crowdfunding Solution with Blockchain and Mobile Financial Payment Integration by SHAH BAIZID AREFIN, ID# 2303219, IIT University of Dhaka

## Description
CrowdShield is a decentralized crowdfunding platform built using blockchain, microservices, and modern web technologies.

## Abstract
“CrowdShield - Donation Crowdfunding Solution” is a decentralized, blockchain-based donation crowdfunding platform designed to foster transparency, security, and efficiency in fundraising for social causes. Built on a decentralized ledger, CrowdShield enables users to create and manage donation campaigns securely while ensuring that all transactions are immutable and publicly verifiable, thus eliminating common issues of fraud and misuse of funds. Leveraging blockchain technology, the platform ensures that donations reach their intended recipients through a transparent process that records each transaction.

The system integrates with mobile financial services, allowing users to contribute seamlessly through widely used digital wallets and mobile payment solutions. This integration expands accessibility, catering to diverse user groups by simplifying the donation process for both digital-savvy users and those who primarily rely on mobile banking. CrowdShield’s architecture employs a service-oriented approach (SOA) for modularity and scalability, with a backend powered by Node.js, MongoDB, and Ethereum smart contracts, ensuring efficient campaign management, contribution tracking, and transaction verification.

In addition to the core decentralized application (DApp), the platform provides a backend-for-frontend (BFF) API layer, enhancing user experience for different devices, including mobile and web interfaces built with React. The platform’s use of CQRS (Command Query Responsibility Segregation) further optimizes performance by separating write and read operations, improving the efficiency and scalability of data management for high-traffic campaigns.

Through CrowdShield, users can confidently support campaigns, knowing that their contributions are secure, transparent, and traceable, revolutionizing the traditional donation-based crowdfunding landscape. This project combines the strengths of blockchain and mobile payments, offering a secure and accessible way to empower community-driven initiatives.

## Feature List
Core Features
•	Campaign Management
o	Create, update, and manage donation campaigns.
o	Define donation targets, deadlines, and descriptions.
•	Donation System
o	Secure donations through Nagad Payment Gateway.
o	Blockchain-enabled transparency for fund distribution.
•	User Authentication
o	User registration and login (JWT-based authentication).
o	Role-based access (e.g., admin, campaign creator, donor).
•	Campaign Search & Discovery
o	Browse and filter campaigns by categories, goals, or popularity.
•	Real-Time Updates
o	View live donation progress and stats on the campaign dashboard.
•	Smart Contracts
o	Transparent fund storage and release using blockchain.

Additional Features
1.	Admin Panel
o	Monitor and manage active campaigns.
o	Generate reports for auditing and insights.
2.	Notifications
o	Real-time notifications for donations, campaign updates, or deadlines.
3.	Mobile-Friendly UI
o	Responsive design for a seamless experience across devices.
4.	Security
o	End-to-end encryption for transactions and user data.
o	Audit trails using blockchain for accountability.
5.	Analytics Dashboard
o	Visual insights for campaign creators to track progress.

## Technical Review
•	Design Patterns and Architecture
o	Service-Oriented Architecture (SOA): Separates functionalities into services (e.g., user management, campaign management, payment processing), allowing easier maintenance, scalability, and independent deployment.
o	Domain-Driven Design (DDD): Manage the complexity of the system by breaking it down into well-defined domains and subdomains. This approach ensures that each part of the system is focused on a specific aspect of the business logic.
o	Backend-for-Frontend (BFF): Customizes API responses specifically for frontend needs, enhancing efficiency and improving data flow between backend and frontend.
o	CQRS (Command Query Responsibility Segregation): Separates read and write operations in the backend to optimize performance, particularly in tracking donations and retrieving campaign data.
o	Mediator: Sends and registers correspondent handlers to process specific commands, queries, or events. This contains business logic for dispatching request from controllers and services. 
o	Event Sourcing: Keeps a record of all transactions/events, such as donations and withdrawals, improving audit trails and transparency.

•	Payment Gateway Integration
o	Nagad Payment Gateway: A widely used mobile financial service in Bangladesh, this gateway enables secure, accessible donations through local mobile payment options, integrating with Node.js for payments processing.

•	Application & Frameworks
o	Blockchain & Ethereum: Adds transparency and decentralized trust in donation management, ensuring funds are locked, traceable, and managed by smart contracts.
o	Nagad Payment Gateway: Vital for local users who prefer mobile payments, making the platform accessible to a wider range of donors in Bangladesh.
o	React & Node.js with TypeScript: A modern, efficient stack that enables responsive frontend, scalable backend, and maintainable codebase using static typing and service-oriented patterns.

•	NoSQL / Document model with Mongo
o	Mongo aligns well with the JSON-like data structures used in web applications, making it easier to store and retrieve complex data types such as user profiles, campaign details, and transaction histories.

## Technology Used
•	Backend
o	Node.js: A JavaScript runtime for building scalable backend services.
o	Express.js: A minimal Node.js framework for creating REST APIs to support microservices.
o	MongoDB: A NoSQL database to store campaign data, user profiles, and transaction histories.
o	Mongoose: An ORM to manage MongoDB interactions with defined schemas.
o	Nagad Ecomm API (Mock for Local): Since the Nagad Payment Gateway may not be directly accessible in a local environment, use mock services or sandbox to simulate API calls and responses.

•	Blockchain
o	Ethereum/Polygon Blockchain (Local Testnet): Use ganache-cli for a local blockchain network to simulate smart contracts.
o	Truffle: A development framework for compiling, deploying, and testing smart contracts.
o	Solidity: The programming language to write smart contracts (CrowdShield.sol) for handling crowdfunding transactions.
o	Web3.js: A library to connect frontend components with blockchain functions.

•	Frontend (React-based BFF)
o	React: A frontend library for building a single-page application (SPA) to display campaigns, allow donations, and provide user authentication.
o	Redux: For managing application state across React components, particularly useful for handling user authentication and campaign data.
o	Axios: For making API requests to the backend microservices and Nagad mock services.
o	Material-UI: A UI framework to design a responsive and user-friendly frontend interface.

•	Development Tools
o	Docker: To containerize backend, database, and frontend services for local development consistency.
o	Postman: For testing APIs and mock Nagad API responses.
o	VS Code: With plugins for Docker, ESLint, Prettier, Solidity, and other project-specific needs.
o	Husky and Lint-Staged: For managing pre-commit hooks to enforce code standards.
o	Mocha & Chai: For backend unit testing and integration testing.

•	Blockchain
o	Ethereum Blockchain (with Solidity): Enables the decentralized management of donations, immutability, and transparency in campaign funding. Smart contracts will handle donation tracking, fund locking, and distribution rules without central authority.
o	Ganache (for local testing): A personal blockchain for Ethereum development, allowing testing and experimentation of smart contracts before deploying to a live or testnet blockchain environment.

•	Implementation Setup
o	Clone repositories for frontend, backend, and blockchain folders.
o	Use Docker Compose to orchestrate services like Node.js backend, MongoDB, and local blockchain.
o	Start Ganache for local blockchain testing and interact with the smart contract using Truffle.
o	Run frontend, backend, and blockchain test suites to ensure the local environment behaves as expected.

## Implementation
•	Step 1: Installation
o	Prerequisites: Node.js, Git, Docker (Optional), Truffle (npm install -g truffle)
o	Configure Environment Variables
o	Install Dependencies (npm install)
o	Docker Setup (Optional)
o	Migrate Blockchain Contracts (Optional)
o	Start the Development Servers backend (npm run dev) and frontend (npm start)
o	Verify the Installation
o	Run Tests (Optional) backend (npm test) blockchain (truffle test)
•	Step 2: Code Construction
•	Step 4: Testing and Quality Assurance
•	Step 3: Deployment

## Setup Instructions
1. Run `npm install` in `frontend`, `backend`, and `blockchain` directories.
2. Start the frontend with `npm start`.
3. Start the backend with `npm run dev`.
4. Deploy blockchain contracts using Truffle.

## Directory Structure
- `frontend`: React application for user interaction.
- `backend`: Node.js API for handling business logic and database.
- `blockchain`: Solidity smart contracts for secure funding.
- `docs`: Documentation files.
