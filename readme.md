# Games Showcase Page

This project is a simple web page that dynamically displays a collection of games or apps using data loaded from a `JSON` file.  
It supports **tag-based filtering** (`mobile`, `desktop`, `web`) and provides links to external platforms such as App Store, Play Store, Steam, Itch.io, GitHub, or HTML5 builds.


<p align="center">
  <a href="https://markustieche.github.io/Games/" target="_blank" style="font-size: 1.5rem; text-decoration: none;">
    🎮 View Games Page
  </a>
</p>

---

## Features

- **Dynamic Cards**: App/game cards are generated directly from `apps.json`.
- **Filtering**: Users can filter apps by `mobile`, `desktop`, or `web` tags using the top-right navigation buttons.
- **Overlay**: A privacy policy (or any external HTML content) is loaded and displayed in an overlay when the footer link is clicked.
- **Responsive**: Works across devices using standard HTML, CSS, and JavaScript.

---

## JSON Structure (`apps.json`)

Each entry in `apps.json` represents one game/app card.  
Below is the format:

```json
[
  {
    "title": "Game Title",
    "description": "Short description of the game or app.",
    "icon": "https://example.com/icon.png",
    "playstoreUrl": "https://play.google.com/store/apps/details?id=...",
    "appstoreUrl": "https://apps.apple.com/app/...",
    "htmlUrl": "https://example.com/play",
    "itchUrl": "https://itch.io/example",
    "steamUrl": "https://store.steampowered.com/app/...",
    "githubUrl": "https://github.com/example",
    "tags": ["web", "mobile", "desktop"]
  }
]
````

### Field Descriptions

* **title** *(string)*: Display name of the app.
* **description** *(string)*: Short description shown on the card.
* **icon** *(string)*: URL of the app image. If missing, a placeholder is used.
* **playstoreUrl / appstoreUrl / htmlUrl / itchUrl / steamUrl / githubUrl** *(string, optional)*: Links to external platforms. If omitted, the button is not displayed.
* **tags** *(array of strings)*: Determines filtering behavior. Supported values: `mobile`, `desktop`, `web`.

---

## How to Add a New Game/App

1. Open `apps.json`.
2. Add a new object with the required fields (`title`, `description`, `icon`, `tags`).
3. Include links (`playstoreUrl`, `appstoreUrl`, etc.) as needed.
4. Save the file. The new game will automatically appear when you reload the page.

---

## Usage

* **Filter by tags**: Click the `Mobile`, `Desktop`, or `Web` button in the nav bar.

  * Clicking a tag once will filter cards.
  * Clicking the same tag again clears the filter.
  * Switching tags updates the filter accordingly.

* **View Privacy Policy**: Click *Privacy Policy* in the footer. Content is loaded from `privacypolicy.html` into the overlay.

---

