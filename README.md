# EventCommand HQ

**AI-Powered Event Planning Software & Management Dashboard**

> Stop using spreadsheets for event planning. EventCommand HQ gives you one AI-powered dashboard to plan weddings, birthdays, church events, conferences, and more — saving hours with smart checklists, seating planners, and automated invitations.

🌐 **Live:** [eventcommand.co](https://eventcommand.co)  
🏢 **By:** Novyra LLC

---

## ✨ What is EventCommand HQ?

EventCommand HQ is a full-featured, AI-enhanced SaaS platform that replaces scattered spreadsheets and overwhelming tools with a single, intelligent event planning dashboard. Whether you're coordinating a 200-guest wedding, a church fundraiser, or a corporate retreat, EventCommand HQ handles every moving piece — from guest lists and budgets to vendor contracts and seating charts — with AI assistants that do the heavy lifting for you.

---

## 🚀 Key Features

### 📋 Event & Task Management
- **Command Center Dashboard** — A unified view of your event's guests, budget, tasks, and timeline at a glance.
- **Kanban Task Board** — Drag-and-drop task management with customizable columns and priority levels.
- **AI Milestone Generator** — Automatically creates a timeline of key milestones based on your event type and date.
- **AI Task Prioritizer** — Intelligently ranks your to-do list so you always know what to tackle next.
- **Calendar Reminders** — Never miss a deadline with built-in scheduling and notifications.

### 👥 Guest Management
- **Guest List Management** — Add, edit, search, and organize guests with detailed profiles.
- **Bulk Import** — Upload guest lists from CSV or spreadsheets in seconds.
- **RSVP Tracking** — Shareable RSVP pages with real-time response tracking.
- **AI Invitation Writer** — Generates beautifully worded, personalized invitations for any event type.
- **Email Invitations** — Send invite and RSVP links directly from the dashboard.
- **Export** — Download guest data in multiple formats.

### 💰 Budget Tracking
- **Budget Dashboard** — Track spending vs. budget with visual breakdowns by category.
- **AI Budget Advisor** — Get smart recommendations on where to save and where to splurge based on your event type and priorities.

### 🏪 Vendor Management
- **Vendor Directory** — Store vendor contacts, contracts, and notes in one place.
- **AI Vendor Matcher** — Recommends the best vendors for your event based on budget, location, and requirements.
- **Google Places Integration** — Search for real local vendors directly within the app.
- **Document Upload & Viewer** — Attach and review contracts, proposals, and receipts per vendor.

### 🪑 Seating & Logistics
- **AI Seating Planner** — Automatically generates optimized seating arrangements based on guest relationships, preferences, and party size.

### 🤖 AI Assistant
- **AI Event Chat** — A conversational AI assistant that can answer questions, brainstorm ideas, and help you troubleshoot any aspect of your event.
- **Plan My Event** — Describe your event in plain English and get a comprehensive, step-by-step plan generated instantly.

### 📱 Progressive Web App (PWA)
- Installable on any device — iOS, Android, and desktop.
- Works offline for viewing event details on the go.
- QR code for easy mobile install.

### 💳 Pricing & Plans
- **Free tier** for small events.
- **Pro and Premium tiers** with Stripe-powered checkout for advanced features, higher guest limits, and priority AI usage.

### 🔐 Authentication & Sharing
- Secure sign-up/login with Supabase Auth.
- Password reset flow with email verification.
- Shareable event pages for co-planners and stakeholders.

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| **Framework** | React 18 + TypeScript |
| **Build Tool** | Vite 5 |
| **Styling** | Tailwind CSS 3 + shadcn/ui |
| **Animations** | Framer Motion |
| **State / Data** | TanStack React Query |
| **Backend & Auth** | Supabase (PostgreSQL, Auth, Edge Functions) |
| **AI** | OpenAI via Supabase Edge Functions |
| **Payments** | Stripe (Checkout + Webhooks) |
| **PWA** | vite-plugin-pwa |
| **Forms** | React Hook Form + Zod |
| **Charts** | Recharts |
| **Drag & Drop** | @hello-pangea/dnd |
| **Typography** | Inter + Space Grotesk |
| **Testing** | Vitest + React Testing Library |

---

## 📂 Project Structure

```
Event Command/
├── public/                  # Static assets, PWA icons
├── scripts/                 # Build scripts (sitemap generator)
├── src/
│   ├── assets/              # Images and static resources
│   ├── components/
│   │   ├── admin/           # Admin panel components
│   │   ├── auth/            # Authentication components
│   │   ├── blog/            # Blog components
│   │   ├── dashboard/       # Core dashboard (34 components)
│   │   │   ├── CommandCenter.tsx
│   │   │   ├── KanbanBoard.tsx
│   │   │   ├── AIFloatingChat.tsx
│   │   │   ├── PlanMyEventDialog.tsx
│   │   │   └── ...
│   │   ├── landing/         # Marketing site components
│   │   ├── seo/             # SEO components
│   │   └── ui/              # shadcn/ui primitives
│   ├── data/                # Static data and constants
│   ├── hooks/               # Custom React hooks
│   ├── integrations/        # Supabase client and types
│   ├── lib/                 # Utility functions
│   ├── pages/               # Route pages (25 pages + 6 sub-directories)
│   ├── test/                # Test setup and test files
│   └── types/               # TypeScript type definitions
├── supabase/
│   ├── functions/           # 18 Edge Functions
│   │   ├── ai-budget-advisor/
│   │   ├── ai-event-planner/
│   │   ├── ai-vendor-matcher/
│   │   ├── ai-seating-planner/
│   │   ├── ai-invitation-writer/
│   │   ├── ai-task-prioritizer/
│   │   ├── ai-milestones/
│   │   ├── ai-event-chat/
│   │   ├── stripe-checkout/
│   │   ├── stripe-webhook/
│   │   ├── send-invite-email/
│   │   ├── send-welcome-email/
│   │   ├── send-rsvp-link/
│   │   ├── send-rsvp-confirmation/
│   │   ├── send-task-reminders/
│   │   ├── push-notifications/
│   │   ├── change-plan/
│   │   └── vendor-places-search/
│   └── migrations/          # Database migrations
└── package.json
```

---

## 🏁 Getting Started

### Prerequisites

- **Node.js** 18+ and **npm** — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
- A **Supabase** project (for backend, auth, and edge functions)
- An **OpenAI API key** (for AI features)
- A **Stripe** account (for payments — optional for development)

### Installation

```sh
# Clone the repository
git clone <YOUR_GIT_URL>
cd event-command

# Install dependencies
npm install

# Set up environment variables
# Copy .env.example or create a .env file with your Supabase and Stripe keys

# Start the development server
npm run dev
```

The app will be available at `http://localhost:5173`.

### Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start the Vite dev server with HMR |
| `npm run build` | Generate sitemap and build for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |
| `npm run test` | Run tests with Vitest |
| `npm run test:watch` | Run tests in watch mode |

---

## ☁️ Deployment

### Frontend

Deploy the built frontend to any static hosting provider (Vercel, Netlify, Cloudflare Pages, etc.):

```sh
npm run build
```

The output will be in the `dist/` directory.

### Supabase Edge Functions

Edge Functions must be deployed separately:

```sh
# Install Supabase CLI
npm install -g supabase

# Log in and link your project
supabase login
supabase link --project-ref YOUR_PROJECT_REF

# Set required secrets
supabase secrets set OPENAI_API_KEY=sk-your-openai-key

# Deploy all functions
supabase functions deploy

# Or deploy a single function
supabase functions deploy ai-vendor-matcher
```

After deployment, functions are available at:  
`https://YOUR_PROJECT_REF.supabase.co/functions/v1/<function-name>`

---

## 📄 License

Proprietary — © Novyra LLC. All rights reserved.
