# VIZHIPPAAN

Child Education Risk Intelligence Platform.

## Local development

Requirements: Node.js 20+ and npm.

```sh
npm install
npm run dev
```

## Environment variables

Create a `.env` file with the Supabase project values used by this application:

```env
SUPABASE_PROJECT_ID="your-project-id"
SUPABASE_PUBLISHABLE_KEY="your-publishable-key"
SUPABASE_URL="https://your-project.supabase.co"
VITE_SUPABASE_PROJECT_ID="your-project-id"
VITE_SUPABASE_PUBLISHABLE_KEY="your-publishable-key"
VITE_SUPABASE_URL="https://your-project.supabase.co"
```

If server-side administrative functions are used, configure `SUPABASE_SERVICE_ROLE_KEY` only in the server/deployment environment. Never expose it with a `VITE_` prefix.

## Google authentication

Google OAuth is initiated directly through Supabase Auth. Configure your own Google OAuth client in Google Cloud and place its Client ID and Client Secret in the Google provider settings for this Supabase project. Add your deployed application URL to the allowed redirect URLs in Supabase and Google Cloud.

The name displayed on Google's consent screen is controlled by your Google Cloud OAuth consent/branding configuration. Use your own OAuth client and set the app name to **VIZHIPPAAN** (or your preferred product name).

## Launch video

The application expects the existing startup video at:

`public/vizhippaan-launch.mp4`

Keep the original video at that path to preserve the launch experience exactly.

## Production deployment

The project is configured for TanStack Start SSR deployment through Nitro. For the exact Vercel setup and required environment variables, see `DEPLOYMENT.md`.

```sh
npm install
npm run build
npm run start
```
