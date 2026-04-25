# BookWith

BookWith is an AI-powered ePub reader.

It helps you read with:
- AI chat based on the current page
- highlights and notes
- memory across past conversations
- semantic search across reading history

## Key Features

- **AI Reading Assistant**: Ask questions while reading and get context-aware answers.
- **Smart Annotation**: Highlight text, add notes, and reuse them in AI chat.
- **Memory System**: Keeps short-term and long-term context for continuity.
- **Semantic Search**: Find related ideas across books, notes, and chats.
- **AI Podcast Generation**: Convert book content into audio summaries.

## Quick Start (Local Development)

1. Install dependencies from the repo root:

   ```bash
   pnpm i
   ```

2. Set up API environment:

   ```bash
   cd apps/api
   cp src/config/.env.example src/config/.env
   ```

3. Start required Docker services:

   ```bash
   make docker.up
   ```

4. Run backend API:

   ```bash
   make configure
   make run
   ```

5. In another terminal, run frontend:

   ```bash
   cd apps/reader
   pnpm dev
   ```

## Common Commands

From repo root:

```bash
pnpm dev
pnpm build
pnpm lint
```

API:

```bash
cd apps/api
make run
make lint
```

Reader:

```bash
cd apps/reader
pnpm dev
pnpm ts:check
```

## Tech Stack

- **Backend**: FastAPI, SQLAlchemy, Pydantic, Weaviate, LangChain
- **Frontend**: Next.js, TypeScript, Tailwind CSS, SWR, ePub.js
- **Monorepo**: Turbo + pnpm workspaces

## Documentation

- Local setup and development details: [docs/DEVELOPMENT_GUIDE.md](docs/DEVELOPMENT_GUIDE.md)
