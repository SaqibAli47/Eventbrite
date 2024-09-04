# EventBright - SaaS Web Application with NextJS

EventBright is a full-stack SaaS web application developed with **NextJS**, **TypeScript**, **ShadCN**, **Mongoose**, and **Stripe Payment** integration. The project also supports complete social authentication with modern technologies. This app allows users to create, manage, and discover events, offering a seamless experience for both event organizers and attendees.

## :ledger: Index

- [About](#beginner-about)
- [Usage](#zap-usage)
  - [Installation](#electric_plug-installation)
  - [Commands](#package-commands)
- [Development](#wrench-development)
  - [Pre-Requisites](#notebook-pre-requisites)
  - [Development Environment](#nut_and_bolt-development-environment)
  - [File Structure](#file_folder-file-structure)
  - [Build](#hammer-build)  
  - [Deployment](#rocket-deployment)  
- [Community](#cherry_blossom-community)
  - [Contribution](#fire-contribution)
  - [Branches](#cactus-branches)
  - [Guideline](#exclamation-guideline)

## :beginner: About

EventBright is a comprehensive event management platform that allows users to discover and create events with ease. Built on **NextJS** for fast and efficient server-side rendering, the app uses **TypeScript** for static typing, ensuring a scalable and maintainable codebase. **ShadCN** is employed for a beautiful and responsive UI, while **Mongoose** serves as the data layer, managing interactions with a **MongoDB** database. 

The application features **Stripe** for secure payment processing and supports full **social authentication** (Google, Facebook, GitHub, etc.), making it easy for users to log in and manage their events.

## :zap: Usage

This repository leverages **NextJS** for both server-side rendering and client-side navigation, **TypeScript** for type safety, **ShadCN** for the UI, and **Mongoose** for handling data models and schemas.

### :electric_plug: Installation

Follow these steps to set up the project locally:

1. Clone the repository:

    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Install dependencies:

    ```sh
    npm install
    ```

3. Set up environment variables in a `.env.local` file:

    ```sh
    NEXT_PUBLIC_STRIPE_PUBLIC_KEY=<your-stripe-public-key>
    STRIPE_SECRET_KEY=<your-stripe-secret-key>
    MONGO_URI=<your-mongo-db-uri>
    NEXTAUTH_SECRET=<your-next-auth-secret>
    NEXTAUTH_URL=http://localhost:3000
    ```

### :package: Commands

- To run the development server:

    ```sh
    npm run dev
    ```

- To build the app for production:

    ```sh
    npm run build
    ```

- To run the app in production mode:

    ```sh
    npm start
    ```

## :wrench: Development

Contributors and developers can follow these steps to set up the project and contribute to its development.

### :notebook: Pre-Requisites

Ensure the following tools are installed on your machine:

- **Node.js** (>= 18.x)
- **npm** (>= 8.x) or **Yarn** (>= 1.x)
- **MongoDB** (>= 5.x)
- **Stripe account** for payment integration

This project also utilizes:

- **ESLint** for code linting
- **Prettier** for code formatting

### :nut_and_bolt: Development Environment

1. Clone the repository and install the dependencies:

    ```sh
    git clone <repository-url>
    cd <repository-directory>
    npm install
    ```

2. Set up the database:

    Ensure **MongoDB** is running locally or use a MongoDB cloud service. Update your `.env.local` with your MongoDB connection string.

3. Run the development server:

    ```sh
    npm run dev
    ```

The app will be available at `http://localhost:3000`.

### :file_folder: File Structure

###  :file_folder: File Structure
```
.
├── components 
├── constants 
├── lib 
├── public  
        │ 
        └── images 
├── types 
├── middleware.ts 
├── next.config.js 
├── package-lock.json 
├── package.json 
├── postcss.config.json 
├── README.md 
├── tailwind.config.json 
└── tsconfig.json
```

###  :hammer: Build
- Before going to production make sure to make the production ready build with this following commond.
```sh
npm run build
```

### :rocket: Deployment
- To deploy the application, follow these steps:
- Ensure the build step is complete.
- Upload the build artifacts to your server or hosting service.
- Configure your server to serve the built files.
- Refer to the deployment documentation specific to your hosting provider for detailed instructions.


##  :cherry_blossom: Community

###  :fire: Contribution

Your contributions are always welcome and appreciated. Here are ways you can contribute:

1. **Report a bug** <br>
If you think you have encountered a bug, and I should know about it, feel free to report it [here]() and I will take care of it.

2. **Request a feature** <br>
You can also request for a feature [here](), and if it will viable, it will be picked for development.  

3. **Create a pull request** <br>
It can't get better then this, your pull request will be appreciated by the community. You can get started by picking up any open issues from [here]() and make a pull request.

> If you are new to open-source, make sure to check read more about it [here](https://www.digitalocean.com/community/tutorial_series/an-introduction-to-open-source) and learn more about creating a pull request [here](https://www.digitalocean.com/community/tutorials/how-to-create-a-pull-request-on-github).

### :cactus: Branches

I use an agile continuous integration methodology, so the version is frequently updated and development is really fast.

1. **`development`** is the development branch.

3. No other permanent branches should be created in the main repository, you can create feature branches but they should get merged with the master.

**Steps to work with feature branch**

1. To start working on a new feature, create a new branch github username and prefixed with `feat` and followed by feature name. (ie. `username/feat-FEATURE-NAME`)
2. Once you are done with your changes, you can raise PR.
**Steps to work with issue branch**

1. To start working on a issue, create a new branch github username and prefixed with `issue` and followed by issue name. (ie. `username/issue#Number`)
2. Once you are done with your changes, you can raise PR.

**Steps to create a pull request**

1. Make a PR to `development` branch.
2. Comply with the best practices and guidelines e.g. where the PR concerns visual elements it should have an image showing the effect.
3. It must pass all continuous integration checks and get positive reviews.

After this, changes will be merged.


### :exclamation: Guideline
coding guidelines or other things you want people to follow should follow.

**Consistent Naming Conventions**
   - Use meaningful and descriptive names for variables, functions, and classes.
   - Follow camelCase for variables and functions, PascalCase for classes, and SCREAMING_SNAKE_CASE for constants.

**Code Formatting**
   - Use a consistent code style for indentation, spacing, and braces. Configure your IDE to use the project's `.editorconfig` or `.prettierrc`.
   - Run a code formatter like Prettier before committing your code.

**Comments and Documentation**
   - Write clear and concise comments for complex logic and important sections of the code.
   - Use JSDoc or similar tools for documenting functions, parameters, and return values.
   - Keep the documentation up-to-date with code changes.

**Modular Code**
   - Break down large functions and classes into smaller, reusable modules.
   - Use design patterns where appropriate to improve code organization and readability.

**Error Handling**
   - Implement proper error handling using try-catch blocks or error-first callbacks.
   - Provide informative error messages and log them appropriately.

**Testing**
   - Write unit tests for all critical functions and modules using testing frameworks like Jest or Mocha.
   - Ensure that your code has good test coverage and that tests are run regularly.

**Version Control**
   - Commit code frequently with clear and descriptive commit messages.
   - Use feature branches for new features or significant changes, and merge them into `staging` or `production` through pull requests.

**Code Reviews**
   - Participate in code reviews to ensure code quality and share knowledge.
   - Be open to feedback and constructive criticism to improve the codebase.

**Prototyping**
   - Create prototypes for complex features before full implementation to validate ideas and approaches.
   - Use tools like Figma for UI/UX prototyping and flow diagrams.

**Code Refactoring**
   - Regularly refactor code to improve readability, reduce complexity, and eliminate technical debt.
   - Follow the "Boy Scout Rule": Always leave the code better than you found it.

**Performance Optimization**
   - Profile and optimize critical code paths to enhance performance.
   - Use efficient algorithms and data structures to reduce computational overhead.

**Single Responsibility Principle**
   - Ensure that each function or class has a single responsibility and adheres to the SRP.

**DRY (Don't Repeat Yourself)**
   - Avoid code duplication by creating reusable functions, modules, and components.

**KISS (Keep It Simple, Stupid)**
   - Write simple and straightforward code. Avoid unnecessary complexity.

**YAGNI (You Aren't Gonna Need It)**
   - Do not add functionality until it is necessary. Focus on the current requirements.

### Additional Resources

- [Clean Code by Robert C. Martin](https://www.goodreads.com/book/show/3735293-clean-code)
- [Design Patterns: Elements of Reusable Object-Oriented Software](https://www.goodreads.com/book/show/85009.Design_Patterns)
- [You Don't Know JS (book series)](https://github.com/getify/You-Dont-Know-JS)

   By following these guidelines and best practices, we can maintain a high-quality codebase that is easy to understand, maintain, and extend.