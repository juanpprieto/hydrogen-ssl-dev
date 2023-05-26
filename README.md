# Hydrogen template: Hello World + HTTPS/SSL dev

<img width="894" alt="ssl" src="https://github.com/juanpprieto/hydrogen-ssl-dev/assets/12080141/2794f9f8-e7eb-450c-9b3b-c78534fbb246">

Hydrogen is Shopify’s stack for headless commerce. Hydrogen is designed to dovetail with [Remix](https://remix.run/), Shopify’s full stack web framework. This template contains a **minimal setup** of components, queries and tooling to get started with Hydrogen.

[Check out Hydrogen docs](https://shopify.dev/custom-storefronts/hydrogen)
[Get familiar with Remix](https://remix.run/docs/en/v1)

## SSL dev instructions

Instructions for Mac:

One time install via your terminal

```bash
brew install mkcert
```

```bash
mkcert -install
```

```bash
npm install -g local-ssl-proxy
```

From the root folder of the hydrogen project run:

```bash
mkcert localhost
```

Should output:

```bas
Created a new certificate valid for the following names 📜
 - "localhost"

The certificate is at "./localhost.pem" and the key at "./localhost-key.pem" ✅

It will expire on XX Moth YYYY 🗓
```

Finally, start the development server as usual with:

```bash
npm run dev
```

The proxied HTTPS/SSL dev server will be available on `https://localhost:3010` and
the standard HTTP at `http://localhost:3000`

You can adjust the ports [here](https://github.com/juanpprieto/hydrogen-ssl-dev/blob/a1f848b857e3eb63199d366927420396331dfa25/package.json#L10)  

## What's included

- Remix
- Hydrogen
- Oxygen
- Shopify CLI
- ESLint
- Prettier
- GraphQL generator
- TypeScript and JavaScript flavors
- Minimal setup of components and routes

## Getting started

**Requirements:**

- Node.js version 16.14.0 or higher

```bash
npm create @shopify/hydrogen@latest -- --template hello-world
```

Remember to update `.env` with your shop's domain and Storefront API token!

## Building for production

```bash
npm run build
```

## Local development

```bash
npm run dev
```
