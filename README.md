# `next` recipe

The `next` recipe showcases one of the most powerful ways to implement Puck using to provide an authoring tool for any route in your Next app.

## Demonstrates

- Next.js 13 App Router implementation
- JSON database implementation with HTTP API
- Catch-all routes to use puck for any route on the platform
- Incremental static regeneration (ISR) for all Puck pages

## Prerequisites

- Bun

  ### Installation

  #### MacOS/Linux

  ```bash
  curl -fsSL https://bun.sh/install | bash
  ```

  #### Windows

  ```bash
  powershell -c "irm bun.sh/install.ps1|iex"
  ```

## Clone Repository

```bash
git clone https://github.com/PfadiMH/puck.git
cd puck/
```

## Install dependencies

```bash
bun i
```

## Usage

Start the server

```
bun dev
```

Navigate to the homepage at https://localhost:3000. To edit the homepage, access the Puck editor at https://localhost:3000/edit.

You can do this for any route on the application, **even if the page doesn't exist**. For example, visit https://localhost:3000/hello/world and you'll receive a 404. You can author and publish a page by visiting https://localhost:3000/hello/world/edit. After publishing, go back to the original URL to see your page.

## Using this recipe

To adopt this recipe you will need to:

- **IMPORTANT** Add authentication to `/edit` routes. This can be done by modifying the example API routes in `/app/puck/api/route.ts` and server component in `/app/puck/[...puckPath]/page.tsx`. **If you don't do this, Puck will be completely public.**
- Integrate your database into the API calls in `/app/puck/api/route.ts`
- Implement a custom puck configuration in `puck.config.tsx`

By default, this recipe will generate static pages by setting `dynamic` to [`force-static`](https://nextjs.org/docs/app/api-reference/file-conventions/route-segment-config#dynamic) in the `/app/[...puckPath]/page.tsx`. This will strip headers and cookies. If you need dynamic pages, you can delete this.

## License

MIT © [Measured Co.](https://github.com/measuredco)

```

```

```

```
