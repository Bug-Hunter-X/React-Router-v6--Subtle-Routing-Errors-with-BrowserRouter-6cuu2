# React Router v6: Subtle Routing Errors

This repository demonstrates a common, yet subtle, issue that can occur when using `react-router-dom` v6, specifically concerning the `BrowserRouter` component and potential conflicts.

The problem often arises without clear error messages, making debugging difficult.  This example illustrates the issue and provides a solution.

## Problem

The `bug.js` file contains a basic React Router setup. While seemingly correct, this can lead to unexpected behavior in certain scenarios, particularly if you're:

* **Nesting routers:** Incorrectly nesting `BrowserRouter` instances can cause routing problems. 
* **Using server-side rendering (SSR):** `BrowserRouter` relies on the browser's history API, which might not be available during SSR.

## Solution

The `bugSolution.js` file provides a solution depending on the specific issue.  Consider these options:

* **Proper Router Nesting:** Use different types of routers (`BrowserRouter`, `HashRouter`, `MemoryRouter`) appropriately depending on your application's needs.
* **SSR Compatibility:** Use a router compatible with SSR (e.g., a server-side router for SSR). Use a client-side router for client-side routing.

This example focuses on illustrating the problem and highlighting potential solutions. The best approach depends on the precise environment and usage of `react-router-dom`.