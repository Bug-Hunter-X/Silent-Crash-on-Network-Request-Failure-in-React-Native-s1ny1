# Silent Crash on Network Request Failure in React Native

This repository demonstrates a common yet subtle bug in React Native applications: silent crashes during network requests.  The issue occurs when a fetch call fails, but the error is not properly handled, leading to a seemingly inexplicable app crash.  The solution showcases how to effectively handle promise rejections to prevent these silent failures.

## Bug

The `DataFetch.js` component attempts to fetch data from a JSONPlaceholder API.  If the network request fails (e.g., no internet connection), the app crashes without any user-visible error message.  This is a frustrating user experience and difficult to debug.

## Solution

The `DataFetchSolution.js` component demonstrates the correct way to handle potential errors. It uses a `try...catch` block within the `useEffect` hook to catch and log errors, providing more information for debugging and potentially displaying a user-friendly error message within the app.