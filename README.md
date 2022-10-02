## This is a GraphQL Yoga v3 example using next-auth.js
https://github.com/dotansimha/graphql-yoga/tree/v3/examples/nextjs-auth

This is a Next.js example using [next-auth.js](https://next-auth.js.org/).

Before running this example you need to set upa GitHubOAuth App. [Follow the instructions here](https://docs.github.com/en/developers/apps/building-oauth-apps/creating-an-oauth-app).

Use `http://localhost:3000/` as the homepage URL.

Use `http://localhost:3000/api/auth/callback/github` as the authorization callback URL.

Afterwards, you must copy the `.env.sample` to `.env` (`cp .env.sample .env`) and fill in the environment variables (`GITHUB_ID` and `GITHUB_SECRET`) you received from your GitHub OAuth application.

Run the app with `yarn dev`.

You can log in on `http://localhost:3000`.

Run the following operation on `http://localhost:3000/api/graphql`.

```graphql
query Session {
  session {
    expires
    user {
      id
      email
      image
    }
  }
}
```

---

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
