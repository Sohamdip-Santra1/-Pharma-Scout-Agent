# -Pharma-Scout-Agent
📌 Overview

Pharma-Scout Agent is an AI-powered prescription analysis tool built using the Google GenAI SDK and ADK (Agent Development Kit).
It extracts medicines from handwritten/printed prescriptions using Gemini Vision, retrieves or estimates prices from major online pharmacy platforms, compares total basket prices, and recommends the most cost-effective vendor.

This README describes how to set up, configure, and run the project in a Kaggle Notebook or any local environment.

The system uses:

- Gemini 2.5 Flash Vision → Extracts medicine names & dosages from prescription images

- Hybrid Price Engine → Scrapes + AI-estimates prices from 1mg, PharmEasy, Netmeds, Apollo

- Automated Deal Analysis → Computes total basket cost & identifies the cheapest vendor

- Interactive UI → Upload → Analyze → View Results → Order / Download Report

This project demonstrates how multimodal AI and tool-based agents can solve a real-world healthcare logistics problem: affordable, accurate, and fast medicine procurement.

🎯 Key Features
🔍 1. AI Prescription OCR (Gemini Vision)

- Extracts medicine names, strengths, mg/ml, and formats

- Ignores patient/doctor personal details

- Returns structured JSON with confidence metrics

🌐 2. Multi-Vendor Price Retrieval

Supports:

- 1mg

- PharmEasy

- Netmeds

- Apollo 24/7

- Local chemist (AI estimation)

Includes:

- Intelligent fallback to AI price estimation

- Vendor-specific market factor adjustments

- Delivery-time estimation

🧮 3. Automated Deal Analysis

Computes total basket cost for each vendor

Ranks vendors (🥇🥈🥉)

Calculates maximum savings

Provides itemized breakdown per vendor

🛒 4. Smart Ordering

One-click redirect to cheapest vendor’s search page

Medicine name auto-populated in search URL

📥 5. Downloadable CSV Report

Winner vendor highlighted

Item-level pricing for all vendors

Summary (total cost + savings)

🛠️ Tech Stack

Google GenAI SDK (Gemini 2.5 Flash Vision)

Python

- Requests / BeautifulSoup (scraping)

- Pillow (image handling)

- Pandas (reporting)

- IPyWidgets (user interface)

🔧 Installation & Setup
1. Install dependencies

pip install google-genai pillow beautifulsoup4 lxml requests pandas ipywidgets

2. Add your Gemini API Key

 in notebook:

 API_KEY = "YOUR_API_KEY"

3. Run the notebook

Execute cells sequentially.

🚀 How to Use
Step 1 — Upload Prescription

Click 📁 Upload and select a .jpg or .png.

Step 2 — Analyze

Click 🔍 Analyze Prescription.
The agent performs:

- Vision OCR

- Medicine extraction

- Price retrieval

- Vendor ranking

- Deal analysis

- Step 3 — View Results

You get:

- Extracted medicines

- Vendor-wise pricing tables

- Best vendor recommendation

- Savings summary

Step 4 — Take Action

- Order from the best vendor

- Download CSV for reference

📊 Example Output (Simplified)
Medicines Detected (High Confidence):
1. Paracetamol 650mg
2. Pantoprazole 40mg

Best Vendor: PharmEasy
Total Cost: ₹210
Savings: ₹45

Delivery: 2–3 Days

🧪 Testing Recommendations

Test with:

- Clear printed prescriptions

- Handwritten prescriptions

- Multiple-dosage prescriptions

- Low-resolution images (to validate OCR robustness)

⚖️ Limitations

- OCR accuracy depends on handwriting clarity

- Scraping is subject to vendor website changes

- AI estimations may differ slightly from live prices

- Not intended for any form of clinical decision-making

🔐 Ethical & Privacy Notes

- Personal identifiers (patient name, doctor info, hospital name) are intentionally ignored by the OCR prompt

- Prescription images should be handled according to relevant privacy policies

- Tool is for convenience and informational use only

🏁 Conclusion

Pharma-Scout Agent showcases a practical, real-world application of multimodal AI and agent workflows in healthcare. By combining OCR, information retrieval, robust fallback mechanisms, and automated price analysis, it reduces manual effort and improves cost transparency for patients.

A complete, reliable, and efficient AI assistant for prescription handling and medicine comparison.
