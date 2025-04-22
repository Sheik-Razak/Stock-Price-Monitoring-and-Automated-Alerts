# 📈 Stock Price Monitoring and Automated Alerts

This UiPath-based RPA project automatically monitors stock prices and sends email alerts when specific conditions are met. It helps users track stocks without constantly checking the market manually.

---

## 🚀 Features

- ✅ Extracts live stock data from a webpage
- ✅ Iterates through multiple stock symbols using Excel
- ✅ Compares current prices against defined thresholds
- ✅ Sends automated email alerts when limits are crossed
- ✅ Uses Orchestrator assets for flexible configuration

---

## 🛠️ Built With

- [UiPath Studio Community](https://www.uipath.com/)
- Orchestrator Assets
- SMTP Email Integration
- Excel File Processing
- Data Scraping / Web Automation

---

## 📂 Folder Structure

Stock-Price-Monitoring-and-Automated-Alerts/ ├── Main.xaml ├── project.json ├── Data/ │ └── StockList.xlsx ├── Screenshots/ │ └── MainWorkflow.png └── README.md

yaml
Copy
Edit

---

## 🧠 Orchestrator Integration

This project uses **Orchestrator Assets** for dynamic value management:

- `url` – URL of the stock market site (e.g., `https://rpachallenge.com/assets/rpaStockMarket/index.html`)
- You can create/manage assets in the **Orchestrator → Assets** section.

---

## 📝 Input File Format

The `StockList.xlsx` file should be formatted like this:

| Stock Name | Alert Price |
|------------|-------------|
| TCS        | 3200        |
| INFY       | 1400        |
| RELIANCE   | 2500        |

The bot checks each stock's real-time price and sends an alert if the current price exceeds or drops below the specified Alert Price.

---

## 💌 Email Alerts

The bot uses SMTP to send email notifications. Configure these in the UiPath `Send SMTP Mail Message` activity:

- SMTP Server: e.g., `smtp.gmail.com`
- Port: `587`
- Email Credentials: Provided through secure assets or inside the workflow (use secure string)

Sample email:
Subject: 📉 Stock Alert: INFY has dropped below ₹1400!

Body: Current price of INFY is ₹1352.5, which is below your set threshold of ₹1400.

yaml
Copy
Edit

---

## 🔧 How to Run

1. Open the project in **UiPath Studio**
2. Update the Excel file with stock names and thresholds
3. Update email and creditals.
4. Add Orchestrator Assets (`url`, optional credentials)
5. Run the bot
6. Check email inbox for alerts (if conditions are met)

---

## ✅ Future Enhancements

- UI for adding stock watchlist
- Integration with APIs (like Yahoo Finance)
- Desktop notifications or mobile push
- Scheduled triggers via Orchestrator

---

## 👨‍💻 Author

**Sheik Razak**  
[GitHub](https://github.com/Sheik-Razak)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
