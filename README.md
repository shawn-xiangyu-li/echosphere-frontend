# EchoSphere Frontend

> 🚧 **Work in progress.** This is the frontend of EchoSphere, a social media app where users share image and video posts.
> Backend: [echosphere-backend](https://github.com/shawn-xiangyu-li/echosphere-backend)

A single-page web app built with Next.js and TypeScript. It talks to a Go REST API for sign-up, login, posting, and search.

## Tech stack

- **Framework:** Next.js (App Router), React
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **Auth:** JWT from the backend, sent as a `Bearer` token on protected requests

## Features (so far)

- Sign up and log in
- Create a post with a caption and an image or video (JPG, PNG, GIF, MP4, MOV, up to 10 MB)
- Browse posts in a feed, and search by caption keywords or by creator
- Handles expired sessions: a `401` from the API signs the user out
- Loading, empty, and error states

## Project structure

```
src/
├── app/            # Next.js App Router: layout and home page
├── components/     # account form, post composer, feed, workspace
└── lib/api.ts      # API client: auth, search, and post upload
```

## Run locally

```bash
npm install
npm run dev
```

Then open http://localhost:3000.

The API address is set with an environment variable. Create a `.env.local` file (it is git-ignored):

```
NEXT_PUBLIC_API_BASE_URL=https://your-backend-url
```

## Roadmap

- [ ] AI-assisted post creation (image generation in the post editor)
- [ ] UI component library (shadcn/ui)
- [ ] Keep users signed in across page reloads
- [ ] Delete your own posts
- [ ] User profile pages
