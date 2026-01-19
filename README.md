# Chat Core IQ (dCQ)

AI-powered chatbot platform with multi-channel support, FAQ management, and cross-project knowledge base integration.

## Features

- 🤖 **AI Chatbot** - Conversational interface powered by Claude/OpenAI
- 📚 **FAQ Management** - Full CRUD for FAQs with semantic search
- 🔍 **Knowledge Base** - Cross-project search with pgvector embeddings
- 🌐 **Multi-language** - English/Spanish support
- 📱 **Multi-channel** - Web, IVR, SMS, WhatsApp integration
- 👤 **Admin Portal** - Content management and analytics

## Tech Stack

- **Framework**: Next.js 16 (App Router)
- **Language**: TypeScript
- **Database**: Supabase (PostgreSQL + pgvector)
- **AI**: Anthropic Claude / OpenAI
- **Embeddings**: Local (transformers.js, all-MiniLM-L6-v2, 384 dims)
- **Styling**: Tailwind CSS 4
- **UI**: Radix UI + shadcn/ui

## Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn
- Supabase account

### Installation

```bash
# Clone the repository
git clone https://github.com/aldrinstellus/chat-core-iq.git
cd chat-core-iq

# Install dependencies
npm install

# Copy environment variables
cp .env.example .env.local

# Start development server
npm run dev
```

### Environment Variables

Create a `.env.local` file with:

```env
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
ANTHROPIC_API_KEY=your_anthropic_api_key
OPENAI_API_KEY=your_openai_api_key
```

## URLs

| Page | Route |
|------|-------|
| Homepage | `/dcq/Home/index.html` |
| Admin | `/dcq/admin` |
| Admin Content | `/dcq/admin/content` |
| Demo IVR | `/dcq/demo/ivr` |

## Project Structure

```
src/
├── app/
│   ├── layout.tsx          # Root layout
│   ├── page.tsx            # Redirects to /homepage
│   ├── admin/              # Admin panel pages
│   ├── api/                # API routes
│   └── demo/ivr/           # IVR demo page
├── components/             # UI components
├── contexts/               # React contexts
├── hooks/                  # Custom hooks
└── lib/                    # Utilities & configs
```

## Scripts

```bash
npm run dev          # Start dev server (port 3002)
npm run build        # Production build
npm run start        # Start production server
npm run lint         # Run ESLint
npm run type-check   # TypeScript check
```

## License

Private - All rights reserved.

---

Part of the Digital Workplace AI Product Suite
