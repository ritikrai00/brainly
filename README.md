# Brainly

Brainly is a modern full-stack application that helps users store, organize, and share important links for future reference. Users can maintain a personal "brain" of saved links, categorize them with tags, and even share them publicly. Whether it's articles, tutorials, or social media content, Brainly makes it easy to keep everything organized and accessible.

---

## Features

### Core Functionality
- **Save Links**: Store important URLs with details for future reference.
- **Organize by Tags**: Categorize links using custom tags for easy retrieval.
- **Public Sharing**: Make your saved links public to share knowledge with others.

### Future Enhancements
- **Search Functionality**: Quickly search saved links by keywords or tags.
- **AI Integration**: Receive AI-powered suggestions and insights based on saved links.

---

## Tech Stack

- **Frontend**: React.js, Redux Toolkit, TypeScript, Tailwind CSS
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JSON Web Tokens (JWT)

---

## Environment Variables

Brainly uses environment variables to manage sensitive information and API endpoints.

### Backend

Create a `.env` file in the **root of the backend** project:

```env
MONGO_URI=your-mongodb-connection-string
JWT_SECRET=your-secret-key
PORT=5000
```

**Usage in Backend (Node.js + Express):**

```ts
import express from "express";
import dotenv from "dotenv";

dotenv.config();

const app = express();
const PORT = process.env.PORT || 5000;

app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});

const mongoUri = process.env.MONGO_URI;
```

### Frontend (React / Vite)

Create a `.env` file in the **root of the frontend** project:

```env
VITE_BACKEND_URL=http://localhost:5000/api/v1
```

> ⚠️ **Note**: In Vite, all frontend env variables must start with `VITE_`.

**Usage in Frontend (TypeScript + Axios):**

```ts
import axios from "axios";

const result = await axios.post(
  `${import.meta.env.VITE_BACKEND_URL}/auth/signup`,
  { username, password }
);
```

---

## How It Works

1. **Sign Up or Log In**: Access your personal Brainly account.
2. **Save Links**: Add URLs with relevant titles, descriptions, and tags.
3. **Manage Links**: Edit or delete links anytime.
4. **Public Brain**: Share your curated collection publicly.

---

## Installation

### Prerequisites

- Node.js and npm installed
- MongoDB (local or MongoDB Atlas account)

### Steps

1. **Clone the repository**

```bash
git clone https://github.com/your-username/brainly.git
cd brainly
```

2. **Install dependencies**

```bash
npm install
```

3. **Set up environment variables**
   Follow the instructions in the **Environment Variables** section above.

4. **Run the application**

```bash
npm run dev
```

5. **Access the app**
   Open [http://localhost:5173/](http://localhost:5173/) in your browser.

---

## Usage

- **Log In**: Access your personal Brainly account.
- **Add Links**: Save URLs along with tags and descriptions.
- **Organize Links**: Group links using tags for quick access.
- **Public Sharing**: Share your saved links publicly with others.

---


## License

This project is licensed under the MIT License.

---

## Notes

- Currently, Brainly does not support search functionality or AI-powered question answering.
- These features are planned for future updates.

---

## Acknowledgements

- Inspired by the concept of a "Second Brain" for personal knowledge management.
- Built with modern web technologies to provide a seamless experience.