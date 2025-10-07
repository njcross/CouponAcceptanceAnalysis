# Practical Application 5.1 — Will the Customer Accept the Coupon?

This project explores the drivers of coupon acceptance using exploratory data analysis (EDA) and visualization. The goal is to compare customers who **accepted** a coupon (Y=1) vs those who **rejected** it (Y=0), and surface actionable recommendations for targeting and timing.

---

## 🔗 Quick Links
- 📓 **Notebook:** [Will_the_Customer_Accept_the_Coupon.ipynb](./Will_the_Customer_Accept_the_Coupon.ipynb)
- 📄 **Dataset:** `coupons.csv` (UCI ML Repository / MTurk survey)
- 📁 **Exported tables (optional):** `tables/` (created by the Appendix cell)

---

## 📦 Repository Contents
- `Will_the_Customer_Accept_the_Coupon.ipynb` — full analysis notebook
- `coupons.csv` — dataset
- `tables/` — exported summary tables (if you ran the Appendix cell)
- `requirements.txt` — dependencies

Recommended structure:
```
coupon_project/
├─ data/                 # optional; or keep coupons.csv at repo root
├─ tables/               # created by Appendix cell (optional)
├─ Will_the_Customer_Accept_the_Coupon.ipynb
├─ coupons.csv
├─ README.md
└─ requirements.txt
```

---

## ▶️ How to Run
1. Place `coupons.csv` in the repo root (or `data/`).  
2. Open the notebook in Jupyter and run cells **top → bottom**.  
3. (Optional) Run the **Appendix: Utility Tables** cell to export CSVs into `tables/` for your README/slides.  
4. If needed, install deps:
   ```bash
   pip install -r requirements.txt
   ```

---

## 📊 Key Results (from this run)
- **Overall acceptance rate:** **56.8%**
- **Top 3 coupon types by acceptance:**  
  - Carry out & Take away: **73.5%**  
  - Restaurant(<20): **70.7%**  
  - Coffee House: **49.9%**
- **Least accepted coupon types:**  
  - Restaurant(20–50): **44.1%**  
  - Bar: **41.0%**

> See the **“Least Accepted”** section in the notebook for visuals focused on Bar vs. Expensive Restaurants.

---

## 🖼️ Visual Highlights
- **Acceptance by coupon type** (count plot + acceptance rates)  
- **Income distribution** among accepters vs. rejecters (box plot; income ranges parsed to numeric)  
- **Least-accepted focus:** Bar vs **Expensive Restaurants (20–50)** (rates + raw counts)  
- **Additional explorations:** acceptance by **time**, **passenger**, **destination**, **weather**, **expiration**  
- **Demographic & behavioral trends:** Younger drivers, trips with **friends/partner**, **daylight**, and **sunny** weather associate with higher acceptance

---

## 🧠 Findings (Nontechnical)
- **Type & context drive acceptance.** Coffee house and inexpensive restaurant coupons perform best; **Bar** and **Expensive Restaurants (20–50)** lag.  
- **Behavior matters.** Acceptance is higher during **daylight** and in **good weather**, and for trips with **friends/partner**. Younger drivers tend to be more responsive to time‑sensitive offers.

---

## ✅ Recommendations
1. **Timing & channel:** Push coffee/carryout offers during commute windows via mobile notifications.  
2. **Social context:** Frame promos for group outings (friends/partner); schedule bar promos for weekends/evenings.  
3. **Offer design:** Use shorter expirations and simple CTAs for impulse categories; emphasize value for expensive restaurants.  
4. **Experimentation:** A/B test timing, copy, and expiration lengths; validate on live campaign data.

---

## ⚠️ Notes & Limitations
- Survey-based data (MTurk) may not perfectly reflect live campaign behavior—treat as directional.  
- Minor cleaning steps applied (e.g., `passanger` → `passenger`, income ranges → numeric midpoints).

---