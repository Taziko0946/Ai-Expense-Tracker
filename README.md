# 💸 Spendwise — AI Expense Tracker

A sleek, AI-powered personal expense tracker built as a single HTML file. Spendwise uses **Claude AI** to automatically classify your expenses by category and generate personalized financial insights — all in a beautiful dark-themed UI.

![Spendwise](https://img.shields.io/badge/Built%20With-Claude%20AI-ff6b47?style=for-the-badge&logo=anthropic&logoColor=white)
![HTML](https://img.shields.io/badge/HTML-Single%20File-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Chart.js](https://img.shields.io/badge/Charts-Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white)

---

## ✨ Features

- **🤖 AI Auto-Classification** — Describe an expense in plain text and Claude AI automatically categorizes it (Food, Travel, Entertainment, Shopping, Bills, Health)
- **📊 Visual Dashboard** — Doughnut chart showing spending breakdown by category
- **📈 Budget Tracking** — Per-category budget bars with color-coded alerts (yellow at 70%, red at 90%)
- **💡 AI Insights** — Personalized finance advice powered by Claude, tailored for Indian users (₹ INR)
- **💳 Payment Methods** — Track expenses by UPI, Card, or Cash
- **📋 Expense History** — Full history with category filters and bulk clear
- **💾 Local Persistence** — All data saved in `localStorage`, no backend needed
- **🎨 Premium Dark UI** — Grain overlay, ambient glow animations, and glassmorphism aesthetics

---

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- An [Anthropic API key](https://console.anthropic.com/)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Taziko0946/Ai-Expense-Tracker.git
   cd Ai-Expense-Tracker
   ```

2. **Open the file**
   ```bash
   open "ai_expense_tracker (1).html"
   ```
   Or simply double-click the HTML file in your file explorer.

3. **Add your API Key**

   The app calls the Anthropic API directly from the browser. To enable AI features, open the HTML file in a text editor and replace the API key in the fetch headers:
   ```js
   headers: {
     'Content-Type': 'application/json',
     'x-api-key': 'YOUR_ANTHROPIC_API_KEY_HERE',
     'anthropic-version': '2023-06-01',
     'anthropic-dangerous-direct-browser-access': 'true'
   }
   ```

   > ⚠️ **Note:** Exposing API keys in client-side code is not recommended for production. This project is intended for personal/local use.

---

## 🖥️ Usage

| Tab | Description |
|-----|-------------|
| ➕ **Add** | Enter expense description + amount, choose payment method, click Add |
| 📋 **History** | View, filter, and delete past expenses |
| 📊 **Dashboard** | Visual spending breakdown and budget progress bars |
| 💡 **Insights** | Get AI-generated personalized spending advice |

### Adding an Expense
1. Type a description (e.g., *"Zomato pizza order"*)
2. Enter the amount in ₹
3. Select payment method: UPI / Card / Cash
4. Hit **Add Expense** — Claude AI classifies it instantly!

---

## 🗂️ Project Structure

```
Ai-Expense-Tracker/
└── ai_expense_tracker (1).html   # Complete single-file app
```

Everything — HTML, CSS, and JavaScript — lives in one self-contained file. No build tools, no dependencies to install.

---

## 🧠 AI Integration

This project uses the **Claude claude-sonnet-4-20250514** model via the Anthropic Messages API for two features:

### 1. Expense Classification
```
POST https://api.anthropic.com/v1/messages
→ Returns one word: food | travel | entertainment | shopping | bills | health | other
```

### 2. Spending Insights
```
POST https://api.anthropic.com/v1/messages
→ Returns 4 actionable finance tips based on your spending patterns
```

---

## 💡 Budget Defaults (Monthly)

| Category | Budget |
|----------|--------|
| 🍕 Food | ₹5,000 |
| ✈️ Travel | ₹3,000 |
| 🎮 Entertainment | ₹2,000 |
| 🛍️ Shopping | ₹4,000 |
| 📄 Bills | ₹3,000 |
| 💊 Health | ₹2,000 |

---

## 🛠️ Built With

- **HTML5 / CSS3 / Vanilla JS** — No frameworks
- **[Chart.js 4.4.1](https://www.chartjs.org/)** — Doughnut charts
- **[Claude AI (claude-sonnet-4-20250514)](https://www.anthropic.com/)** — Expense classification & insights
- **Google Fonts** — Playfair Display, Syne, JetBrains Mono

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙌 Acknowledgements

- [Anthropic](https://www.anthropic.com/) for the Claude API
- [Chart.js](https://www.chartjs.org/) for beautiful charts

---

*Made with ❤️ and ₹ in mind.*
