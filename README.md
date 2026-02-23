<div align="center">

# 🏗️ Draftly

### AI-Powered Floor Plan to 3D Visualization

Transform your 2D floor plans into stunning, photorealistic 3D architectural renders — instantly.

[![Live Demo](https://img.shields.io/badge/🌐_Live_Demo-draftly--psi.vercel.app-blue?style=for-the-badge)](https://draftly-psi.vercel.app/)
[![React Router](https://img.shields.io/badge/React_Router-v7-CA4245?style=for-the-badge&logo=react-router&logoColor=white)](https://reactrouter.com/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-v4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Puter](https://img.shields.io/badge/Puter.js-Cloud_Platform-8B5CF6?style=for-the-badge)](https://puter.com/)

</div>

---

## ✨ Features

| Feature | Description |
|---|---|
| 🤖 **AI-Powered Rendering** | Converts 2D floor plans into photorealistic top-down 3D renders using **Gemini 2.5 Flash** |
| 📤 **Drag & Drop Upload** | Intuitive file upload with drag-and-drop support for JPG, PNG, and WebP formats |
| 🔍 **Before / After Comparison** | Interactive slider to compare the original floor plan with the AI-generated 3D render |
| 💾 **Cloud Storage** | Projects are stored and hosted via **Puter.js** cloud infrastructure |
| 📥 **One-Click Export** | Download your rendered visualization as a PNG with a single click |
| 🔐 **Authentication** | Seamless sign-in / sign-up powered by Puter authentication |
| 📱 **Responsive Design** | Fully responsive UI built with TailwindCSS v4 |

---

## 🖼️ Screenshots

<!-- Add your screenshots here -->
<!-- ![Homepage](screenshot-url-here) -->
<!-- ![Visualizer](screenshot-url-here) -->

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| [React 19](https://react.dev/) | UI library |
| [React Router v7](https://reactrouter.com/) | Full-stack framework (SSR, routing, data loading) |
| [TailwindCSS v4](https://tailwindcss.com/) | Utility-first CSS styling |
| [Puter.js](https://puter.com/) | Auth, cloud storage, hosting & AI gateway |
| [Gemini 2.5 Flash](https://deepmind.google/technologies/gemini/) | AI image generation model |
| [Lucide React](https://lucide.dev/) | Icon library |
| [React Compare Slider](https://github.com/nerdyman/react-compare-slider) | Before/after image comparison |
| [TypeScript](https://www.typescriptlang.org/) | Type safety |
| [Vite](https://vitejs.dev/) | Build tool & dev server |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v20+
- [pnpm](https://pnpm.io/) (recommended) or npm

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/draftly.git
cd draftly

# Install dependencies
pnpm install
```

### Environment Variables

Create a `.env.local` file in the root directory:

```env
VITE_PUTER_WORKER_URL=<your-puter-worker-url>
```

### Development

```bash
pnpm run dev
```

The app will be available at `http://localhost:5173`.

### Production Build

```bash
pnpm run build
pnpm run start
```

---

## 🐳 Docker

```bash
# Build the image
docker build -t draftly .

# Run the container
docker run -p 3000:3000 draftly
```

---

## 📁 Project Structure

```
draftly/
├── app/
│   ├── routes/
│   │   ├── home.tsx              # Landing page with upload zone
│   │   └── visualizer.$id.tsx    # AI render viewer + comparison slider
│   ├── root.tsx                  # App shell, auth context provider
│   ├── routes.ts                 # Route definitions
│   └── app.css                   # Global styles
├── components/
│   ├── Navbar.tsx                # Navigation bar with auth controls
│   ├── Upload.tsx                # Drag-and-drop file upload component
│   └── ui/
│       └── Button.tsx            # Reusable button component
├── lib/
│   ├── ai.action.ts              # Gemini AI image generation logic
│   ├── constants.ts              # App-wide constants & AI prompt
│   ├── puter.action.ts           # Puter auth, project CRUD
│   ├── puter.hosting.ts          # Puter hosting & image upload
│   ├── puter.worker.js           # Web worker for Puter operations
│   └── utils.ts                  # Image processing utilities
├── type.d.ts                     # Global TypeScript type definitions
├── vite.config.ts                # Vite configuration
├── react-router.config.ts        # React Router configuration
├── Dockerfile                    # Multi-stage Docker build
└── package.json
```

---

## 🔄 How It Works

```
┌──────────────┐     ┌──────────────┐     ┌──────────────────┐     ┌──────────────┐
│  Upload 2D   │────▶│  Store via   │────▶│  Generate 3D     │────▶│  View &      │
│  Floor Plan  │     │  Puter Cloud │     │  via Gemini AI   │     │  Compare     │
└──────────────┘     └──────────────┘     └──────────────────┘     └──────────────┘
```

1. **Upload** — Drag and drop or click to upload your 2D floor plan (JPG, PNG, WebP)
2. **Store** — The image is stored in Puter's cloud and a project is created
3. **Generate** — Gemini 2.5 Flash converts the floor plan into a photorealistic 3D render
4. **Compare** — Use the interactive slider to compare before and after, or export as PNG

---

## 🌐 Deployment

The app is deployed on **Vercel** and live at:

👉 **[https://draftly-psi.vercel.app/](https://draftly-psi.vercel.app/)**

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">

Built with ❤️ using React Router, Puter.js & Gemini AI

</div>
