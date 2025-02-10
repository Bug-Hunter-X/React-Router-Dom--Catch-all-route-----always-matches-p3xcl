# React Router Dom Catch-all Route Issue

This repository demonstrates a common issue with React Router Dom's catch-all route (`path="*"`).  The problem occurs when the catch-all route is placed after other routes, causing it to always match and preventing other routes from being rendered, even when a more specific route exists. 

## Problem

The provided `App.js` demonstrates this issue.  No matter what URL is accessed, the `NotFound` component always renders because the `path="*"` route always matches.

## Solution

The solution involves reordering the routes, placing the catch-all route at the end of the Routes component.  This ensures that it only matches if no other routes match.