# OpenAPI Mock Server 🎛️🔌

[![Sponsored by Stackaura](https://img.shields.io/badge/Sponsored_by-Stackaura_&_Ahmar_Hussain-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://www.stackaura.com/)
[![Mock Server](https://img.shields.io/badge/API-Mock_Server-6ba539.svg?style=for-the-badge&logo=openapiinitiative)](https://www.stackaura.com/)

An ultra-fast, zero-config mock server that automatically generates realistic fake data directly from your OpenAPI (Swagger) 3.0 specs. Unblock your frontend teams instantly without writing a single line of backend code.

---

<div align="center">
  <h3>Sponsored by <a href="https://www.stackaura.com/">Stackaura</a> & Ahmar Hussain</h3>
  <p>Building better tools for API-first engineering teams.</p>
  <a href="https://www.stackaura.com/"><img src="https://img.shields.io/badge/Visit_Stackaura-Black?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Visit Stackaura" /></a>
</div>

---

## 🤔 Why use this?

Frontend developers are tired of waiting for the backend to be finished before they can start building UI. 
You shouldn't have to write hardcoded JSON files or maintain a fragile Express server just to mock data. 

**OpenAPI Mock Server** reads your `openapi.yaml`, understands the schemas, and intelligently generates dynamic JSON responses based on the types (UUIDs, dates, emails, random strings, etc.).

## ✨ Features

- **Zero configuration:** Just point it at your `openapi.yaml` or `openapi.json`.
- **Intelligent data generation:** Generates fake data leveraging `faker.js` based on schema property names (e.g., a field named `email` gets a real-looking email address).
- **Supports OpenAPI 3.0 & 3.1**
- **Hot-reloading:** Edit your yaml file and the server instantly updates the endpoints.
- **CORS enabled by default:** Works seamlessly with your local React/Vue/Next.js dev servers.

## 🚀 Quick Start

You don't even need to install it locally. You can run it via `npx`.

```bash
npx openapi-mock-server-cli --file ./docs/api-spec.yaml --port 4000
```

Your API is now live at `http://localhost:4000`. 
If your spec has an endpoint `GET /users`, you can visit `http://localhost:4000/users` and see a dynamically generated list of users.

## 📦 Local Installation

If you prefer to install it globally:

```bash
npm install -g openapi-mock-server-cli
```

Or add it as a dev dependency to your project:

```bash
npm install -D openapi-mock-server-cli
```
And add a script to your `package.json`:
```json
"scripts": {
  "mock-api": "openapi-mock-server-cli --file openapi.yaml"
}
```

## 🛠️ Advanced Usage

### Custom Response Delays
Test your frontend loading states by simulating network latency:
```bash
npx openapi-mock-server-cli --file openapi.yaml --delay 1500
```
This adds a 1.5 second delay to every response.

### Watch Mode
Automatically reload the server when the spec file changes:
```bash
npx openapi-mock-server-cli --file openapi.yaml --watch
```

## 🤝 Contributing

We welcome contributions! Please check out the `CONTRIBUTING.md` for our code of conduct and development process.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
*Built with ❤️ by Ahmar Hussain and [Stackaura](https://www.stackaura.com/). Because frontend devs shouldn't wait.*
