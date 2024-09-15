---
difficulty: 1
training: true
chapter: "Chapter 5: Best Practices"
tags: vue
---

# A Custom ErrorBoundary Component

In this challenge, we've created a dummy blog post with comments rigged to randomly fail.

Your task is to create a custom `ErrorBoundary` component. It will be responsible for handling errors that occur within its default slot.

In order for this to work, you'll need to use the `onErrorCaptured` hook.

## Requirements

The `ErrorBoundary` component should:

1. Prevent the error from bubbling up to the top level
2. Render the #error slot when an error is caught
3. Provide a function `clearError` to the error slot
4. Provide the error to the error slot

> 💡 HINT: If you do not prevent the error from bubbling up to the top level of the app
> the following message will be logged to the console ("Error reached top level of the app")
> See main.js lines 10-13 to see why.

![Screenshot of the solution](https://images.certificates.dev/csvd-training-code-challenge-14.gif)
