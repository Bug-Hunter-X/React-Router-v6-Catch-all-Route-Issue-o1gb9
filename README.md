# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue with React Router v6's catch-all route (`/*`).  The catch-all route, intended to handle unmatched routes, is unexpectedly overriding more specific routes.  This example shows how to correctly handle this case.

## Problem

The provided `App.js` contains a catch-all route (`/*`) that is inappropriately matching all routes, preventing the `/` and `/about` routes from working as intended.  The `NotFound` component is always rendered, regardless of the URL.

## Solution

The `AppSolution.js` file demonstrates the solution.  This involves ensuring that the catch-all route is placed at the very end of the routes array to avoid unintended matching.  By placing `/*` as the last route, it only matches if no other routes match.