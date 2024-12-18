# Nest-TDA

A simple [NestJS](https://nestjs.com/) application that demonstrates the core features of the framework, including controllers, providers, modules, and basic CRUD operations.

## Features

- **TypeScript-First:** Strong typing for better reliability and developer experience.
- **Modular Architecture:** Easily scale and maintain your application as it grows.
- **Simple CRUD Example:** Provides endpoints to create, read, update, and delete resources.
- **Extensible:** Add authentication, integrate databases, and more with minimal effort.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (Recommended: LTS Version)
- npm (comes with Node.js) or [Yarn](https://yarnpkg.com/) as a package manager.

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://https://github.com/iamrajhans/nest-tda.git
   cd your-repo
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

   or

   ```bash
   yarn install
   ```

### Running the Application

**Development mode (with hot reload):**
```bash
npm run start:dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

**Production mode:**
```bash
npm run build
npm run start:prod
```

### Project Structure

A typical NestJS application structure:

```
.
├─ src
│  ├─ app.module.ts          # Root application module
│  ├─ main.ts                # Application bootstrap (entry point)
│  ├─ tasks
│  │  ├─ tasks.controller.ts # Handles incoming requests for tasks
│  │  ├─ tasks.service.ts    # Business logic for tasks
│  │  ├─ tasks.module.ts     # Tasks module
│  │  └─ dto
│  │     └─ create-task.dto.ts # Data Transfer Object for task creation
│  └─ ...other files/modules
├─ test                      # Unit and e2e tests
├─ package.json
└─ README.md
```

### Example Endpoints

- `POST /tasks` - Create a new task
- `GET /tasks` - Retrieve all tasks
- `GET /tasks/:id` - Retrieve a specific task by ID
- `PATCH /tasks/:id` - Update a task’s properties
- `DELETE /tasks/:id` - Delete a task

Use [Postman](https://www.postman.com/), [cURL](https://curl.se/), or any other HTTP client to test these endpoints.

### Environment Variables

Create a `.env` file at the root if needed. Some examples:
```
PORT=3000
DATABASE_URL=your_database_url
JWT_SECRET=your_secret_key
```

> **Note:** `.env` is typically included in `.gitignore` to avoid leaking sensitive information.

### Testing

**Running unit tests:**
```bash
npm run test
```

**Running end-to-end (e2e) tests:**
```bash
npm run test:e2e
```

**Test coverage:**
```bash
npm run test:cov
```

### Deployment

Compile for production:
```bash
npm run build
```

Then run:
```bash
npm run start:prod
```

You can deploy the compiled `dist` folder to any Node.js hosting environment. If using a service like Heroku, ensure you have a `Procfile` with:
```
web: node dist/main.js
```

### Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have suggestions or improvements.

```
