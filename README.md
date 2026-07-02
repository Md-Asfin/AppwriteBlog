# 📝 12MegaBlog

A full-featured blogging platform built with **React**, **Vite**, and **Appwrite** — supporting rich-text authoring, user authentication, and complete post management.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Vercel-black?style=for-the-badge&logo=vercel)](https://appwrite-blog-seven-mauve.vercel.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github)](https://github.com/Mohammad-Asfin/AppwriteBlog)

---

## ✨ Features

- 🔐 **User Authentication** — Sign up, log in, and log out powered by Appwrite Auth
- 📄 **Create & Edit Posts** — Rich text editing via TinyMCE with image upload support
- 🗂️ **All Posts View** — Browse all published blog posts in one place
- 🔒 **Protected Routes** — Auth-guarded pages using a reusable `AuthLayout` component
- 🗃️ **State Management** — Global auth state managed with Redux Toolkit
- 📱 **Responsive UI** — Styled with Tailwind CSS for a clean, adaptive layout
- ⚡ **Blazing Fast** — Powered by Vite with Hot Module Replacement (HMR)

---

## 🛠️ Tech Stack

| Layer         | Technology                          |
|---------------|-------------------------------------|
| Frontend      | React 18, React Router DOM v6       |
| Build Tool    | Vite 4                              |
| Styling       | Tailwind CSS 3                      |
| State         | Redux Toolkit, React-Redux          |
| Backend/BaaS  | Appwrite (Auth, Database, Storage)  |
| Rich Text     | TinyMCE (`@tinymce/tinymce-react`)  |
| Forms         | React Hook Form                     |
| HTML Parsing  | html-react-parser                   |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- An [Appwrite](https://appwrite.io/) account and project

### 1. Clone the Repository

```bash
git clone https://github.com/Mohammad-Asfin/AppwriteBlog.git
cd AppwriteBlog
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Copy the sample environment file and fill in your Appwrite credentials:

```bash
cp .env.sample .env
```

Then open `.env` and set the values:

```env
VITE_APPWRITE_URL="https://cloud.appwrite.io/v1"
VITE_APPWRITE_PROJECT_ID="your_project_id"
VITE_APPWRITE_DATABASE_ID="your_database_id"
VITE_APPWRITE_COLLECTION_ID="your_collection_id"
VITE_APPWRITE_BUCKET_ID="your_bucket_id"
```

> **Tip:** All environment variables must be prefixed with `VITE_` to be exposed to the browser by Vite.

### 4. Run the Development Server

```bash
npm run dev
```

The app will be available at `http://localhost:5173`.

---

## 📁 Project Structure

```
src/
├── appwrite/          # Appwrite service wrappers (auth, database, storage)
├── components/        # Reusable UI components
│   ├── Header/        # Top navigation bar
│   ├── Footer/        # Page footer
│   ├── post-form/     # Create/Edit post form with TinyMCE
│   ├── AuthLayout.jsx # Route guard for protected pages
│   ├── Login.jsx      # Login form component
│   ├── Signup.jsx     # Registration form component
│   ├── PostCard.jsx   # Blog post preview card
│   ├── RTE.jsx        # Rich Text Editor wrapper
│   └── ...
├── conf/              # App-wide configuration (env vars)
├── pages/             # Route-level page components
│   ├── Home.jsx
│   ├── Login.jsx
│   ├── Signup.jsx
│   ├── AllPosts.jsx
│   ├── AddPost.jsx
│   ├── EditPost.jsx
│   └── Post.jsx
├── store/             # Redux store & slices
│   └── authSlice.js
├── App.jsx            # Root component with routing layout
└── main.jsx           # App entry point & router config
```

---

## 📜 Available Scripts

| Command           | Description                              |
|-------------------|------------------------------------------|
| `npm run dev`     | Start development server with HMR        |
| `npm run build`   | Build the app for production             |
| `npm run preview` | Preview the production build locally     |
| `npm run lint`    | Run ESLint to check for code issues      |

---

## ☁️ Appwrite Setup

1. Create a new project in your [Appwrite Console](https://cloud.appwrite.io/).
2. Enable **Email/Password** authentication under **Auth → Settings**.
3. Create a **Database** with a **Collection** for posts. Add the required attributes (e.g., `title`, `content`, `status`, `featuredImage`, `userId`).
4. Create a **Storage Bucket** for post images.
5. Copy your Project ID, Database ID, Collection ID, and Bucket ID into your `.env` file.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
