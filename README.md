# Dayline CRM

A customizable customer tracking workspace built with React and Vite.

## Development

Requires Node.js 20.19+ or 22.12+.

```sh
npm ci
npm run dev -- --port 5173
```

Production build: `npm run build`. Serve the build with `npm run preview`.

## Features

- Pipeline board with drag-and-drop stage changes and searchable list view
- Customer creation and editing, deal values, and custom customer fields
- Daily conversation history and follow-up dates
- Customizable pipeline stages (the final stage is counted as won)
- Browser-local persistence and JSON backup export
- Responsive desktop and mobile layouts

The initial customers are demonstration data. Data is stored in localStorage in the current browser; this version has no backend, authentication, or multi-user synchronization. Export workspace backups before clearing browser storage. Overview metrics summarize the current customer records. Customize stages by keeping existing stages in their current position when renaming: customer assignments are mapped by stage position.

## Validation

The production build and browser workflow were verified: customer creation, conversation logging, stage changes, persistence after reload, stage/field customization, search, and responsive rendering.

## Mobile and GitHub Pages

The phone layout includes bottom navigation, touch-sized controls, swipeable pipeline stages, and a stage selector in each customer profile. Data is local to each browser; desktop and phone data do not synchronize.

To publish, push this project to `main`, then choose **GitHub Actions** in repository **Settings → Pages → Build and deployment → Source**. The included Pages workflow builds and deploys the site. If the first workflow runs before Pages is enabled, rerun it after enabling Pages.

Expected project URL after a successful deployment: https://sirawattemz-maker.github.io/CRM-Daily-tracking/

On a phone, open the deployed URL in Safari or Chrome. Use the browser's Add to Home Screen option for a shortcut. Offline operation is not implemented.
