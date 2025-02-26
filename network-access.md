# Figma CSS Variables: Network Access

This document outlines the network resources the Figma plugin connects to when using the Community build.

## Sentry

We use **Sentry** to track errors and crashes, which helps us identify and resolve issues efficiently.

The plugin sends error reports to **sentry.io**. These reports do not contain any personally identifiable information (PII).

## Netlify API

Certain features are made available to a subset of users based on predefined criteria. To manage access, the plugin checks the Figma user ID via a Netlify-hosted API endpoint on `netlify.app` **only when the "Push" action is triggered** for deployment.

**No user data is stored**. The API simply checks whether the provided Figma user ID is authorized for certain features.

## Git Providers

When users use the **Git provider** feature, the plugin connects directly to **GitHub, GitLab, or a self-hosted GitLab instance** to deploy CSS files.

Connections are made directly from the plugin to the user's selected Git provider, and no data passes through our infrastructure. The plugin only interacts with the API endpoints specified by the user.
