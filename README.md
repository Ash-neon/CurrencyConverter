# CurrencyConverter
Currency Converter Web App

# Currency Converter – Single-File Web App

A lightweight, responsive currency converter web application built with HTML, CSS, and JavaScript. It fetches real-time exchange rates from the [Frankfurter API](https://www.frankfurter.app/) without requiring an API key. All logic and styling are contained within a single HTML file.

## Features
- **Live exchange rates** fetched directly from the Frankfurter API.
- **Swap currencies** with a single click.
- **Conversion history** stored locally in the browser (last 20 conversions saved).
- **Copy result** to clipboard functionality.
- **Responsive design** for mobile and desktop.
- **Offline fallback** with common currencies if the API is unavailable.

## Tech Stack
- **HTML5** – Markup for structure and layout.
- **CSS3** – Responsive styling and theme variables.
- **JavaScript (ES6)** – Core application logic and API interaction.
- **Frankfurter API** – Free currency exchange rates provider.

## Getting Started
### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari).
- Internet connection (for live rates).

### Installation & Usage
1. **Download** the `index.html` file.
2. **Open** it in your browser.
3. Enter the amount, select currencies, and click **Convert**.
4. Use **Swap** to reverse the conversion direction.
5. Check the **Conversion History** table for recent conversions.

### Optional: Run with a Local Server
```bash
# Using Python
python3 -m http.server 8000
# Using Node.js (serve)
npx serve
```
Visit `http://localhost:8000` in your browser.

## File Structure
```
index.html         # Single-file app with HTML, CSS, and JS
```

## How It Works
1. **Fetch Symbols**: On load, the app requests currency codes and names from `/currencies` endpoint.
2. **Populate Dropdowns**: Fills 'From' and 'To' selects with available currencies.
3. **Convert**: On button click or Enter key, calls `/latest` endpoint with selected currencies.
4. **Display Result**: Shows converted amount and rate, updates history.
5. **Store History**: Saves recent conversions to `localStorage`.

## Known Limitations
- Requires internet access for live rates.
- Rates are for demo purposes and may not be updated in real-time for financial transactions.

## License
This project is released under the MIT License.

## Acknowledgments
- [Frankfurter API](https://www.frankfurter.app/) for providing free exchange rate data.
