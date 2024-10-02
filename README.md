# Project Summary

## Project Scope

Building a global video streaming platform for MyDRTV with a social component in the form of ratings, comments, etc.

## Key Requirements

- High availability
- Scalability
- GDPR compliance
- Interactivity with ratings and recommendations
- Engaging users through a social network

## Solution Architecture

Microservices architecture is the chosen solution based on the key requirements:

- Since high availability is a ‘must-have,’ microservices are an ideal choice due to their fault-tolerant and distributed nature.
- Microservices ensure scalability, as each service can be scaled independently, allowing for efficient handling of global traffic for video streaming and user interactions.
- Microservices can isolate data services, ensuring that personal data management is handled securely and separately from other services, in accordance with GDPR regulations.
- Microservices architecture supports easy extensibility, making it simpler to add or modify services without disrupting the entire system.

---

# Technology Stack

## Client-Side:

### React:

- **Why**: React’s component-based architecture, ease of state management, and flexibility for integrating APIs for dynamic content like video streams and ratings.
- **Other Tools**: React Router or React Navigation (for navigation), Axios (for API calls), Vite (for bundling).

### TypeScript:

- **Why**: TypeScript adds static typing to JavaScript, allowing for better type safety, reduced bugs, and easier collaboration on larger codebases. TypeScript integrates seamlessly with React, improving maintainability and scalability.
- **Other Tools**: `tsconfig` for TypeScript configuration, Tailwind for CSS, and Prettier for formatting to ensure consistent code quality.

## Server-Side:

### Go (Golang):

- **Why**: Go’s performance and scalability, native support for concurrency, simple learning curve, and strong community for microservices.
- **REST APIs**: REST for simpler HTTP-based communication.
- **Database**: PostgreSQL for relational database.

### Deployment and DevOps:

- **Docker**: For containerizing services, ensuring scalability and resilience.
- **CI/CD**: GitHub Actions for continuous integration and deployment pipelines.

### Security:

- **OAuth2/JWT**: For user authentication and session management.
- **GDPR Compliance**: Focus on user data protection, with microservices isolating sensitive data for easier compliance.

---

# Architecture Diagram

![image](DLS_myDrTv.png)

---

# Domain Model

## ![image](<Screenshot 2024-10-02 at 12.20.07.jpg>)

# Requirements

## User Stories:

### 1. User Registration and Login

- **As a user**, I want to create an account on MyDRTV, rate videos, and save my preferences.
- **As a user**, I want to log in securely so that my personal data is protected and I can access my account.

### 2. Search and Discovery

- **As a user**, I want to search for programs by title, genre, and production year so that I can quickly find the content I'm interested in.
- **As a user**, I want to filter search results by different categories like documentaries, films, and TV shows to easily explore specific types of content.

### 3. Content Ratings

- **As a user**, I want to rate videos after watching them so that I can share my opinion and help others choose what to watch.
- **As a user**, I want to see the average rating for a video before watching so that I can make an informed decision.

### 4. GDPR Compliance

- **As a user**, I want to manage my personal data, including downloading a copy of it or requesting its deletion, so that I can comply with GDPR and control my information.

---

# Non-Functional Requirements

- **Performance**: The system must ensure low latency and high throughput.
- **Security**: Authentication must be handled via OAuth2, with full GDPR compliance and encryption of all communications.
- **Resilience**: The architecture must guarantee fault tolerance by using microservices, ensuring the system remains operational even in the event of individual service failures.

---

# Conclusion

In conclusion, the combination of Go and React within a microservices architecture offers the flexibility, scalability, and resilience necessary to meet the requirements of this project. This architecture not only enables high availability and seamless scaling but also ensures GDPR compliance through modular and isolated services. After some consideration, we found this approach to be the optimal and simplest solution, balancing ease of maintenance with the ability to adapt to future needs, when compared to other architectural options.
