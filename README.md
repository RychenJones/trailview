# TrailView

https://trailview.netlify.app

**TrailView** is a responsive hiking-trail website developed as a class project to demonstrate front-end web development skills. The project focuses on building an interactive user experience using HTML, CSS, and JavaScript, including client-side data handling, form validation, browser storage, URL parameters, accessibility, and modular JavaScript.

The trail information is based on a local JSON data file rather than a backend database or external API.

## Features

* **Trail exploration** — Browse trail cards with location, distance, difficulty, and images.
* **Detailed trail views** — Select a trail to view expanded information and imagery.
* **Favorites** — Save and remove favorite trails using browser storage.
* **Form validation** — The hike-planning form validates required fields, email format, character limits, and trail selection, with accessible field-level error feedback.
* **Local storage persistence** — Favorite trails are stored in `localStorage` and persist between sessions.
* **JSON data fetching** — Trail information is loaded dynamically from a local JSON file using the JavaScript Fetch API.
* **Drop-down menus** — Trail selection and filtering use dynamically populated dropdown controls.
* **Filtering** — Filter trails by difficulty or display only saved favorites.
* **URL parameters** — Trail IDs are passed through URL query parameters to load the corresponding detailed trail view.
* **CSS animations and transitions** — Interactive elements use CSS animations and transitions to provide visual feedback.
* **Responsive design** — The layout adapts to mobile and desktop screen sizes.
* **User experience and accessibility** — The interface incorporates semantic HTML, ARIA attributes, keyboard navigation, focus states, status messaging, accessible labels, and reduced-motion support.
* **JavaScript modules** — Functionality is organized into separate ES modules for data loading, rendering, favorites, form validation, and page-specific behavior.

## Technologies

* HTML5
* CSS3
* JavaScript (ES Modules)
* Vite
* Fetch API
* Local Storage
* JSON
* Responsive CSS
* Automated JavaScript tests

## How It Works

TrailView uses a local JSON file as its source of trail data. JavaScript fetches the data asynchronously and uses separate modules to process, filter, and render it in the interface.

The main page allows users to:

1. Browse available trails.
2. Filter trails by difficulty or favorites.
3. Select a trail to view its details.
4. Save trails as favorites.
5. Fill out a hike-planning form with client-side validation.

When a trail is selected, its ID is included in the URL as a query parameter:

```text
detailed-view.html?id=1
```

The detailed-view page reads the ID from the URL, finds the corresponding trail in the JSON data, and displays its information.

This project does **not** use a backend, database, user accounts, or an external API. Its interactive functionality is implemented on the client side using JavaScript and browser features such as `localStorage`.

## Project Structure

```text
trailview/
├── public/
│   └── data/
│       └── trails.json
├── src/
│   ├── css/
│   │   ├── detailed.css
│   │   ├── index.css
│   │   └── style.css
│   └── js/
│       ├── data.js
│       ├── detailed.js
│       ├── favorites.js
│       ├── form.js
│       ├── main.js
│       └── render.js
├── tests/
│   └── form-validation.test.mjs
├── detailed-view.html
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js
```

The JavaScript is organized into focused modules rather than placing the application's logic in a single file. For example:

* `data.js` handles loading and validating trail data.
* `render.js` handles displaying trail information.
* `favorites.js` manages saved trails using `localStorage`.
* `form.js` contains the hike-planning form validation logic.
* `detailed.js` handles the detailed trail page.

## Accessibility

Accessibility was incorporated into the interface and interaction design.

Examples include:

* Semantic HTML elements
* ARIA labels and states
* Keyboard-accessible controls
* Visible focus states
* Screen-reader status messaging
* Accessible favorite buttons
* `aria-invalid` feedback for invalid form fields
* Automatic focus on the first invalid form field
* Reduced-motion support through `prefers-reduced-motion`

## Design

TrailView uses an outdoor-inspired visual design with a forest-green, warm neutral, orange, and gold color palette. The interface emphasizes clear visual hierarchy, readable trail information, compact trail cards, and straightforward navigation.

The design was intended to demonstrate how a functional and accessible user interface can be built with standard front-end technologies without relying on a backend or external services.
