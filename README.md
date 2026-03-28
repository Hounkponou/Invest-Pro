# Invest-Pro 
## 🛠️ Technical Stack & Architecture

This project is built using a **Serverless Architecture** to ensure it remains lightweight and easy to maintain.

### 1. Frontend (`index.html`)
* **Vanilla JavaScript:** Handles the UI rendering and user interactions.
* **Data Visualization:** Uses the `dividends` and `stocks` objects to display interactive charts or tables.
* **Responsive Design:** Styled with CSS (or a framework like Tailwind/Bootstrap) to work on mobile and desktop.

### 2. Backend & API (Google Apps Script)
Instead of a traditional server, this project leverages **Google Apps Script (GAS)** as a custom API:
* **Data Sourcing:** The script fetches real-time or updated market data directly from Google Sheets or external web scrapers.
* **Processing:** The API processes raw BRVM data (calculating averages, filtering by sector) before sending it to the frontend.
* **Endpoint:** The frontend communicates with the GAS Web App URL via `fetch()` to get the latest updates.

