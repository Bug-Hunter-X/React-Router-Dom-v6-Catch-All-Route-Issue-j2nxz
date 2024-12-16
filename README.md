# React Router Dom v6 Catch All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router v6. The catch-all route should only be triggered when no other routes match, but in this case, it's always triggered, overriding other routes.

## Problem

The provided `App.js` file contains a simple React Router setup with three routes: `/`, `/about`, and a catch-all route `/*`.  The expectation is that the catch-all route (`NotFound` component) should only be triggered if the URL doesn't match `/` or `/about`. However, the catch-all route is always activated, preventing the `/` and `/about` routes from rendering.

## Solution

The solution in `AppSolution.js` addresses this by correctly placing the catch-all route at the end of the route definitions.  This ensures that the more specific routes are checked first, and the catch-all only takes effect if no other route matches.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to `/` or `/about` always results in the "Not Found" page.
5. Replace `App.js` with `AppSolution.js` and re-run the application. The routes will now work as expected.