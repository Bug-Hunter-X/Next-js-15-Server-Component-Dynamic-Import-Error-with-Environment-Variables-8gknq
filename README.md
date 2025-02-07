# Next.js 15 Server Component Dynamic Import Bug

This repository demonstrates a subtle bug in Next.js 15 related to dynamic imports within server components and the use of environment variables. The bug manifests when a dynamically imported module relies on environment variables that aren't available during the server-side rendering (SSR) phase. This results in an error during the initial rendering, before the client-side hydration takes over.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Observe the error in the browser console.

## Solution

The solution involves ensuring the necessary environment variables are accessible during SSR. This can be done by using a strategy that properly handles their availability or by providing default values during SSR. This improved example uses conditional importing to handle the environment variable during SSR.