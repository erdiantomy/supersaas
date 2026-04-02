# Super SaaS - AI-First Custom Software Agency

Welcome to the repository for the Super SaaS landing page and AI-powered lead generation chatbot.

## 🚀 Tech Stack

* **Frontend Framework:** React 18 with Vite
* **Styling:** Tailwind CSS
* **Animations:** Framer Motion (`motion/react`)
* **Icons:** Lucide React
* **AI Integration:** Google Gemini API (`@google/genai`)

## 🛠️ Local Development

1. **Clone the repository:**
   ```bash
   git clone https://github.com/erdiantomy/supersaas.git
   cd supersaas
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up environment variables:**
   Create a `.env` file in the root directory and add your Gemini API key:
   ```env
   VITE_GEMINI_API_KEY=your_api_key_here
   ```
   *(Note: In the AI Studio environment, this is handled automatically via `process.env.GEMINI_API_KEY`, but for local Vite development outside of AI Studio, you may need to adjust the env variable prefix to `VITE_` depending on your build setup, or use a backend proxy).*

4. **Start the development server:**
   ```bash
   npm run dev
   ```

## 📦 Deployment

This project is optimized for deployment on platforms like **Vercel**, **Netlify**, or **Cloudflare Pages**.

* **Build Command:** `npm run build`
* **Output Directory:** `dist`

### Deploying to Vercel
1. Go to [Vercel](https://vercel.com) and import this GitHub repository.
2. Vercel will automatically detect the Vite framework.
3. Add your `GEMINI_API_KEY` in the Vercel Environment Variables settings.
4. Click **Deploy**.

## 💬 Features

* **Modern UI/UX:** Dark mode, neon accents, and smooth scroll animations.
* **Interactive Chatbot:** Replaces the traditional contact form with a multi-turn Gemini AI assistant that qualifies leads and hands them off to a WhatsApp technical advisor.
* **Responsive Design:** Fully optimized for mobile, tablet, and desktop.
