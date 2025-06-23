# 📦 Corrugated Box Profit/Loss Calculator

A web-based profit/loss calculator for **Dharma Group’s** corrugated box manufacturing. It supports **3, 5, 7, 9, and 12-ply** boxes with detailed cost breakdowns and a responsive design.

🔗 **Live Demo:** [Click here](https://naveen-greyhat.github.io/corrugated-box-calculator/profitcal.html)

---

## 📌 Features

### ✅ Input Specifications
- 📐 Box dimensions: Length, Width, Height (cm)
- 📦 Box Type: 3, 5, 7, 9, or 12-ply
- 📄 Material Costs: Paper GSM, Paper Rate (₹/kg), Wastage %, Gum, Pinch Wire
- ⚙️ Operational Costs: Electricity, Printing, Labor
- 💰 Financials: Selling Price per Box, GST %

### 📊 Calculation Results
Organized into detailed sections:
- **Raw Materials:** Paper, Gum, Wire cost (total)
- **Operational Costs:** Labor, Electricity, Printing (per box)
- **Per Box Metrics:** Weight, Total Cost, Selling Price
- **Order Totals:** Cost without/with GST, Profit/Loss per Box and Total
- **Summary:** Expected Price (20% margin), Your Price, Net Profit/Loss Status (color-coded)

### 🎨 UX & Design
- ✅ Responsive layout for desktop and mobile
- 🎯 Conditional styling (green = profit, red = loss)
- 💾 LocalStorage to remember inputs
- 🔁 Reset functionality

---

## 📂 Project Structure

```

corrugated-box-calculator/
├── profitcal.html    # Main file with UI, logic, and style
└── README.md         # Project documentation

````

---

## 🚀 Usage

1. Open the [live calculator](https://naveen-greyhat.github.io/corrugated-box-calculator/profitcal.html)
2. Enter all required details:
   - Dimensions
   - Ply type
   - Material costs
   - Operational costs
   - Selling price and GST %
3. Click **"Calculate"**
4. Review results under each section
5. Click **"Reset"** to clear inputs

> ✅ *All fields are required and must be positive numbers.*

---

## 🧪 Example Test Cases

### 🔹 Test Case 1 – 3-ply (Profit)

**Inputs:**
- Length: 30 cm, Width: 20 cm, Height: 10 cm
- Box Type: 3-ply
- GSM: 120, Rate: ₹40/kg, Wastage: 12%
- Quantity: 1000
- Gum: 10 gm/box @ ₹60/kg
- Wire: 5 gm/box @ ₹80/kg
- Electricity: ₹0.50, Printing: ₹0.25, Labor: ₹3200
- Selling Price: ₹60, GST: 18%

**Expected Output:**
- ✅ Profit: ₹22.80/box → ₹22,803.60 net

---

### 🔹 Test Case 2 – 12-ply (Loss)

**Same as above, but Box Type = 12-ply**

**Expected Output:**
- ❌ Loss: ₹71,610.40 net

---

## 📐 Calculations Summary

- **Surface Area:** `2 × (L×W + W×H + H×L)` in m²
- **Paper Weight:** SurfaceArea × Ply × GSM
- **Costs:**
  - Paper: `(paperWeight/1000) × (1 + wastage%) × rate`
  - Gum & Wire: Based on usage per box
- **Total Cost per Box:** Raw materials + Ops costs
- **Expected Price (20% margin):** `cost × 1.2`
- **Profit/Loss:** `(Selling Price - Cost) × Quantity`

---

## 💡 Notes

- Fixed profit margin: 20% (can modify in JS ~line 570)
- No validation for box feasibility (e.g., 12-ply for tiny sizes)
- Internet required for Font Awesome icons (CDN used)
- To use offline: Download the FA CSS and update link

---

## 🛠️ Installation (For Local Use)

### Clone Repository:
```bash
git clone https://github.com/Naveen-GreyHat/corrugated-box-calculator.git
cd corrugated-box-calculator
````

### Run Locally:

* Open `profitcal.html` in browser


## 🐛 Debugging Tips

If calculations don’t work:

* Open **Developer Tools (F12)** → Check **Console** for JS errors.

---

## 🤝 Contributing

* 🐞 Report bugs or suggestions in the [issues tab](../../issues)
* 🍴 Fork the repo → Make changes → Submit a Pull Request

---

## 📜 License

© 2025 Dharma Group. All rights reserved.

---

## 📬 Contact

For support, contact Dharma Group IT team or reach out to [@greyhat127](https://github.com/Naveen-GreyHat)
