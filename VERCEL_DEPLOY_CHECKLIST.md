# VIZHIPPAAN — Vercel Deployment

This package is configured for TanStack Start + Vite + Nitro on Vercel.

## Vercel settings

- Root Directory: repository root (`./`)
- Install Command: `npm install`
- Build Command: `npm run build`
- Output Directory: leave blank
- Node.js: 22.x

The included `vercel.json` also fixes the install/build commands so Vercel does not guess them differently.

## Required environment variables

Add these to Vercel Project Settings → Environment Variables for Production (and Preview if you use previews):

```env
SUPABASE_URL=https://YOUR_PROJECT_REF.supabase.co
SUPABASE_PUBLISHABLE_KEY=YOUR_SUPABASE_PUBLISHABLE_KEY
VITE_SUPABASE_URL=https://YOUR_PROJECT_REF.supabase.co
VITE_SUPABASE_PUBLISHABLE_KEY=YOUR_SUPABASE_PUBLISHABLE_KEY
```

Do not expose a Supabase service-role key through any `VITE_` variable.

## Important

Do not set an Output Directory such as `dist` or `dist/client`. Nitro generates the Vercel server output during the build.
