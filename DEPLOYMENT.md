# VIZHIPPAAN deployment

## Vercel

The project is configured for TanStack Start through Nitro.

1. Push the contents of this folder to the root of a GitHub repository.
2. Import the repository into Vercel.
3. Use Node.js 22.x.
4. Build command: `npm run build`.
5. Leave Output Directory empty.
6. Add the Supabase environment variables from `.env.example`.
7. Deploy.

The Vite config explicitly uses `srcDirectory: "./src"`, and the repository contains `src/router.tsx`, `src/server.ts`, and `src/routeTree.gen.ts`.
