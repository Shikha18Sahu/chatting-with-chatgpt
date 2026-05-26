# 🤖 Chatting with ChatGPT

<div align="center">

![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)

**A full-stack AI chat application powered by OpenAI — built with Next.js & TypeScript**

[🌐 Live Demo](#) • [📁 Browse Code](https://github.com/Shikha18Sahu/chatting-with-chatgpt) • [🐛 Report Bug](#) • [💡 Request Feature](#)

</div>

---

## ✨ About The Project

**Chatting with ChatGPT** is a full-stack conversational AI web app that replicates a ChatGPT-like experience. Built using **Next.js App Router**, **TypeScript**, and **TailwindCSS**, it connects to the **OpenAI API** to enable real-time AI conversations with a clean, modern UI.

> 🎯 **Goal:** Build and deploy a production-ready AI chat interface using modern full-stack tools.

---

## 🖼️ Preview

> *(Add a screenshot here)*
```
📸 Tip: Take a screenshot → save as preview.png → replace this with:
![Preview](preview.png)
```

---

## 🗂️ Project Structure

```
chatting-with-chatgpt/
│
└── 📁 my-app/                    # Main Next.js application
    │
    ├── 📁 app/                   # App Router (Next.js 13+)
    │   ├── 📁 api/
    │   │   └── 📁 chat/          # API route → OpenAI integration
    │   ├── assistant.tsx          # Assistant component
    │   ├── favicon.ico
    │   ├── globals.css            # Global styles
    │   ├── layout.tsx             # Root layout
    │   └── page.tsx               # 🏠 Main entry page
    │
    ├── 📁 components/             # Reusable UI components
    │   ├── 📁 assistant-ui/       # Chat UI components
    │   │   ├── markdown-text.tsx  # Markdown message renderer
    │   │   ├── thread-list.tsx    # Chat thread list
    │   │   ├── thread.tsx         # Individual thread view
    │   │   ├── tool-fallback.tsx  # Tool fallback handler
    │   │   └── tooltip-icon-butt...  # Tooltip icon button
    │   ├── 📁 ui/                 # shadcn/ui base components
    │   └── app-sidebar.tsx        # Sidebar navigation
    │
    ├── 📁 hooks/
    │   └── use-mobile.ts          # Mobile detection hook
    │
    ├── 📁 lib/
    │   └── utils.ts               # Utility functions
    │
    ├── .gitignore
    ├── components.json            # shadcn/ui config
    ├── eslint.config.mjs
    ├── next.config.ts             # Next.js config
    ├── package.json
    ├── postcss.config.mjs
    ├── tailwind.config            # Tailwind config
    └── tsconfig.json
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have these installed:
- [Node.js](https://nodejs.org/) v18+
- An **OpenAI API Key** → [Get one here](https://platform.openai.com/api-keys)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Shikha18Sahu/chatting-with-chatgpt.git

# 2. Navigate into the project
cd chatting-with-chatgpt/my-app

# 3. Install dependencies
npm install

# 4. Create your environment file
cp .env.example .env.local
```

### Environment Variables

Create a `.env.local` file in the `my-app/` folder:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

> ⚠️ **Never commit your API key!** The `.gitignore` already excludes `.env.local`.

### Run the App

```bash
# Development mode
npm run dev

# Production build
npm run build
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser. 🎉

---

## 🎨 Features

| Feature | Description |
|--------|-------------|
| 💬 **AI Chat** | Real-time conversations powered by OpenAI API |
| 🧵 **Thread List** | View and manage multiple chat threads |
| 📝 **Markdown Support** | AI responses render with full markdown formatting |
| 📱 **Mobile Responsive** | `use-mobile` hook for adaptive layout |
| 🗂️ **Sidebar Navigation** | Clean sidebar to switch between conversations |
| 🎨 **shadcn/ui Components** | Beautiful, accessible UI components |
| ⚡ **Next.js App Router** | Fast routing with server & client components |
| 🔒 **Secure API Route** | OpenAI key stays server-side — never exposed |

---

## 🛠️ Built With

| Technology | Purpose |
|-----------|---------|
| ![Next.js](https://img.shields.io/badge/Next.js-000?style=flat-square&logo=next.js) **Next.js 13+** | App Router, API routes, SSR |
| ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) **TypeScript** | Type-safe codebase |
| ![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) **TailwindCSS** | Utility-first styling |
| ![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white) **OpenAI API** | AI chat completions |
| **shadcn/ui** | Accessible component library |
| **PostCSS** | CSS processing |

---

## 🔌 API Reference

### `POST /api/chat`

Sends a user message to OpenAI and returns an AI response.

```json
// Request body
{
  "messages": [
    { "role": "user", "content": "Hello!" }
  ]
}

// Response
{
  "message": "Hi there! How can I help you today?"
}
```

---

## 📚 What I Learned

- Building **full-stack AI apps** with Next.js App Router
- Creating **secure API routes** that protect secret keys
- Working with the **OpenAI Chat Completions API**
- Using **shadcn/ui** for production-ready components
- Rendering **markdown in chat messages** dynamically
- Building **responsive layouts** with a custom `use-mobile` hook

---

## 🔮 Future Plans

- [ ] Add **authentication** (sign in / sign out)
- [ ] **Persist chat history** with a database (MongoDB/Supabase)
- [ ] Support for **multiple AI models** (GPT-4, GPT-3.5)
- [ ] Add **streaming responses** (token-by-token output)
- [ ] Export chat as **PDF or Markdown**
- [ ] **Dark / light mode** toggle

---

## 🚢 Deployment

### Deploy on Vercel (Recommended)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

> Don't forget to add `OPENAI_API_KEY` in your Vercel environment variables!

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

---

## 🤝 Contributing

Contributions are welcome!

```bash
# Fork → Clone → Branch → Commit → PR
git checkout -b feature/your-feature
git commit -m "Add: your feature"
git push origin feature/your-feature
```

---

## 👩‍💻 Author

**Shikha Sahu**

[![GitHub](https://img.shields.io/badge/GitHub-Shikha18Sahu-181717?style=for-the-badge&logo=github)](https://github.com/Shikha18Sahu)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Shikha%20Sahu-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/shikha-sahu-3b003b285/)

---

<div align="center">

Made with ❤️ using Next.js & OpenAI

⭐ **Star this repo if you found it helpful!**

</div>
