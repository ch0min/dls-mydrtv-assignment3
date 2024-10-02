# Project Summary
**Project Scope:** Building a global video streaming platform for MyDRTV with a social component in the form of ratings, comments, etc.

**Key Requirements:** High availability, scalability, GDPR compliance, interactivity with ratings and recommendations, and engaging users through a social network.

# Solution Architecture
Microservices architecture is the chosen solution based on the key requirements.

Firstly, since high availability is a ‘must have’, microservices are an ideal choice due to their fault-tolerant and distributed nature. Microservices also ensure scalability, as each service can be scaled independently, allowing for efficient handling of global traffic for video streaming and user interactions.

Additionally, microservices can isolate data services, ensuring that personal data management is handled securely and separately from other services, in accordance with GDPR regulations.

Microservices architecture supports easy extensibility, making it simpler to add or modify services without disrupting the entire system.

# Technology Stack
- Client-Side:
  - React:
    - Why: React’s component-based architecture, ease of state management, and flexibility for integration API’s for dynamic content like video streams and ratings. 
    - Other Tools: React Router or React Navigation (for navigation), Axios (for API calls), Vite (for bundling).
  - TypeScript:
    - Why: TypeScript adds a static typing to JavaScript, allowing for better type safety, reduced bugs, and easier collaboration on larger codebases. TypeScript integrates seamlessly with React, improving maintainability and scalability.
    - Other Tools: “tsconfig” for TypeScript configuration, Tailwind for css, and Prettier for formatting to ensure consistent code quality.
- Server-Side:
  - Go (Golang):
    - Why: Go’s performance and scalability, native support for concurrency, simple learning curve, and strong community for microservices.
    - REST APIs: REST for simpler HTTP-based communication.
    - Database: PostgreSQL for relational database.
  - Deployment and DevOps:
    - Docker: For containerizing services, ensuring scalability and resilience.
    - CI/CD: GitHub Actions for continuous integration and deployment pipelines.
  - Security:
    - OAuth2/JWT: For user authentication and session management.
    - GDPR Compliance: Highlight the focus on user data protection and how microservices isolate sensitive data for easier compliance.
