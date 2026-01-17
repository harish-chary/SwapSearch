# Swapper Search Tool - Chrome Extension

This project is a **Chromium-based browser extension** that allows users to easily swap search engines while browsing the web. The extension supports the following search engines: **Google, Bing, Yahoo, DuckDuckGo**.

## Features
- **Seamless Search Engine Switching**: Allows users to search using different search engines easily, directly from any page.
- **Support for Multiple Search Engines**: Integrates **Google**, **Bing**, **Yahoo**, and **DuckDuckGo** as available search engines.
- **Real-time Search**: Detects the current search engine being used on the page and allows you to swap to another engine.
- **Customizable**: Users can search with their preferred engine at any time without manually changing the search URL.
- **Lightweight & Fast**: Lightweight extension that performs fast search engine redirection.

## Tech Stack
- **JavaScript** (for extension functionality)
- **HTML/CSS** (for the UI and extension structure)
- **Chrome Extensions API** (for background and content script communication)
- **Manifest V3** (for Chrome extension setup)

## Getting Started

### Prerequisites
To use this extension, you need a **Chromium-based browser** like Google Chrome.

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/harish-chary/SearchSwap.git
    cd search-swap
    ```

2. Open **Chrome** and go to **chrome://extensions/**.

3. Enable **Developer mode** (top right corner).

4. Click **Load unpacked** and select the directory where this repository is located.

5. The extension icon will appear on the browser toolbar.

### How to Use

- **Search Engine Detection**: Once the extension is installed, it will automatically detect the search engine currently in use on a page (Google, Bing, Yahoo, or DuckDuckGo).
- **Switch Search Engines**: Click on the extension icon and select a search engine (Google, Bing, Yahoo, or DuckDuckGo) to search the term entered in the search box.

### File Structure
- **manifest.json**: Configuration file for the extension.
- **popup.html**: HTML file for the extension's popup interface.
- **style.css**: Styles for the extension popup interface.
- **script.js**: JavaScript file containing logic to switch between search engines.
- **logos**: Images for logos of supported search engines (Google, Bing, DuckDuckGo, Yahoo).

### Functionality Overview

1. **Detect Current Search Engine**: 
   - Based on the URL of the current page, the extension identifies the search engine in use (Google, Bing, Yahoo, DuckDuckGo).
   - This is done by matching URL patterns for each search engine.

2. **Generate Search URL**:
   - The extension dynamically creates a search URL based on the selected search engine and the search term entered by the user.
   - Supported search engines: Google, Bing, Yahoo, DuckDuckGo.

3. **Redirect or Open in New Tab**:
   - If no search engine is detected, the search term is opened in a new tab using the default search engine.
   - Otherwise, the current page is redirected to the new search engine with the entered search term.

4. **UI**: 
   - Users can click on a button to change the search engine (Google, Bing, Yahoo, DuckDuckGo).
   - Displays the current search engine and the search term used.

### Example Use Case

1. A user is on a Google search page.
2. They decide to switch to Yahoo.
3. The extension captures the current search term and redirects them to the corresponding Yahoo search results page.

## Files

- **`manifest.json`**: This is the configuration file for the Chrome extension. It specifies permissions, background scripts, and other necessary metadata.
- **`popup.html`**: This is the HTML file for the extension's popup window that users interact with.
- **`style.css`**: Contains the styles for the popup interface.
- **`script.js`**: The core JavaScript file that handles the search engine detection, generation of search URLs, and redirection.
- **`logos`**: Contains images for the logos of the supported search engines.
