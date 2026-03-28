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

---

## ⚙️ How it Works

1. The **Google Apps Script** acts as a middleware, fetching data and converting it to a JSON format.
2. The **Frontend** calls the API:
   ```javascript
   fetch('YOUR_GOOGLE_SCRIPT_WEB_APP_URL')
     .then(response => response.json())
     .then(data => {
        // Process and display your BRVM data
     });

3. The app is automatically deployed and hosted via GitHub Pages.
### Tips for your Deployment:
* **Privacy:** Ensure your Google Apps Script is deployed with the setting *"Who has access: Anyone"* if you want your GitHub Pages site to be able to fetch the data without authentication.
* **CORS:** Google Apps Script handles CORS automatically when deployed as a Web App, which is perfect for GitHub Pages.

---
**Would you like me to provide a template for the Google Apps Script (GS) code to help you process the data on that side?**