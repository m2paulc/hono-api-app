# Hono API App

## Getting Started

```bash
npx create-next-app@latest
```

- [ ] Install Hono

```bash
npm install hono
```

- [ ] create api route (src/app/api/[[...route]]/route.ts)

example:

```ts
import { Hono } from "hono";
import { handle } from "hono/vercel";

export const runtime = "edge";

const app = new Hono().basePath("/api");

app.get("/hello", (c) => {
  return c.json({
    message: "Hello Next.js!",
  });
});

export const GET = handle(app);
export const POST = handle(app);
```
