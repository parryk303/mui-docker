# mui-docker

A fullstack Docker setup with React (Vite + TypeScript) frontend and a Node.js/Express backend using MUI for the UI.

---

## Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- [Docker](https://www.docker.com/)
- [npm](https://www.npmjs.com/) (comes with Node.js)

---

## 🚀 Getting Started

### 1. Create the React Client

```bash
npm create vite@latest client --template react-ts
cd client
npm install
```

### 2. Create the Server

```bash
mkdir server
npm init
cd server
touch tsconfig.json
```
### 2. Update tsconfig.json
```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "rootDir": "src",
    "outDir": "dist",
    "strict": true,
    "esModuleInterop": true
  }
}
```

### 4. Dockerize
```bash
docker build -t my-fullstack-app .
docker run -d -p 3000:3000 --name fullstack-app-container my-fullstack-app
```