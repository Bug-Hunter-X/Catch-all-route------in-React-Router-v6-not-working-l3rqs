# React Router v6 Catch-all Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router v6.  The issue is that the catch-all route is not matching any unmatched paths, even though other routes are working correctly.

## Problem

The application has routes for `/` and `/about`.  A catch-all route is added to handle any other paths. However, navigating to a path not explicitly defined does not trigger the catch-all route.

## Solution

The solution involves rearranging the order of routes.  The catch-all route should always be placed last in the `Routes` component to ensure it only matches paths not matched by other more specific routes.