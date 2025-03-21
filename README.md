# sit323-2025-prac2p

# Simple Node.js Web Server

This project demonstrates a simple web server using Node.js and the Express framework.

## Prerequisites

- Node.js
- npm (Node Package Manager)
- Git

---

## Installation

### Step 1: Install Node.js and Git

1. Download and install Node.js from the [Node.js Official Site](https://nodejs.org).
2. Check if Node.js and npm are installed:

3. Download and install Git from the [Git Official Site](https://git-scm.com).
4. Check if Git is installed:

### Step 2: Set Up Your Project Directory

1. Open your terminal or command prompt.
2. Create a new directory for your project:

3. Initialize a Git repository:

4. Create a new Node.js project:

5. Install Express:

---

### Step 3: Create the Web Server

1. In your project directory, create a new file named `server.js`:

```javascript
const express = require("express");
const path = require("path");
const app = express();
const PORT = 3000;

app.use(express.static(path.join(__dirname, "public")));

app.get("/", (req, res) => {
  res.sendFile(path.join(__dirname, "public", "index.html"));
});

app.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}`);
});
```
