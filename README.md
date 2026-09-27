Prime Motors — Used Car Sales, Pricing & Profitability Analytics

A Power BI portfolio project simulating the analytics function of a used-car dealership — from raw data to a decision-ready, 3-page interactive dashboard.

<img width="1437" height="812" alt="executive-overview" src="https://github.com/user-attachments/assets/f88873d3-7bd8-4c8e-94bb-a27e716646c5" />


 About This Project

Used-car dealerships operate on thin margins and depend heavily on getting three things right: pricing cars correctly, moving inventory fast, and understanding who their customers are. Get any one of these wrong, and capital sits idle or deals stop being profitable.

This project simulates the analytics function for a fictional dealership, Prime Motors, operating across 14 cities in India. I built it to practice — and demonstrate — the full analyst workflow: understanding a business problem, shaping raw data around it, modeling it correctly, and turning it into a dashboard that a manager could actually use to make decisions.

  Why I Built This

Most beginner Power BI projects stop at "here's a bar chart of sales by region." I wanted this project to go further and reflect how analytics actually gets used in a business:

Start from real business questions (below), not from "what charts can I make with this data"
Build a proper data model rather than dumping one flat table into visuals
Add engineered features (Car Age, Price Segment, Mileage Segment) that make the analysis sharper, not just charts that restate the raw columns
Design the dashboard so that every page answers a different question, instead of cramming everything onto one screen
Back every KPI and insight with a DAX measure, not a manually typed number

❓ Business Questions This Dashboard Answers
Which brands, models, and regions bring in the most revenue — and profit?

How much does mileage and car age actually pull down resale price?

Which price and mileage segments are most (and least) profitable to stock?

How much capital is sitting idle in aging inventory, and which models are stuck?

Who is the typical buyer — age, income, gender — and what do they prefer (fuel type, transmission, ownership history)?

🗂️ The Dataset
63,600 records — 60,000 completed sales + 3,600 cars currently in stock (Jan 2022 – Dec 2025)
16 brands · 60 models · 14 cities across 4 regions
28 raw columns spanning pricing, mileage, ownership, customer demographics, and dealer/salesperson details
Deliberately built with realistic imperfections (a small share of loss-making distress sales, some missing customer fields) rather than a clean textbook dataset, so the cleaning and modeling steps mean something

  Raw data: Prime_Motors_Used_Car_Sales.csv

 How It Was Built
Stage	What I did
Data cleaning (Power Query)	Corrected date locale issues, handled nulls, standardized categorical fields
Feature engineering	Added Car_Age, Price_Segment, and Mileage_Segment to enable segment-level analysis that raw columns couldn't support
Data modeling	Structured the data with fact-style transactional rows and dimension-style attributes (car, customer, dealer, date) for clean, scalable filtering
DAX	Wrote 20+ measures covering revenue, profit, margin, YoY growth, inventory aging, and customer metrics — every KPI on the dashboard is a live calculation, not a static number
Dashboard design	Built a 3-page report with synced slicers, page navigation buttons, and a consistent dark theme, so it behaves like a real internal tool rather than a one-off chart dump

📈 Inside the Dashboard

1. Executive Overview — company-wide health check: revenue, profit, margin, monthly trend, and top brands/cities/models at a glance.

2. Sales & Pricing Analysis — where the money comes from and how pricing behaves: revenue by region/brand/price segment, selling price vs. purchase price trends, and discount patterns.

3. Inventory & Customer Insights — the operational side: which stock is aging and blocking capital, and who the buyers actually are.

<img width="1435" height="842" alt="inventory-customer" src="https://github.com/user-attachments/assets/86446c13-2488-4fff-bb15-dcf844401ae0" />

<br><br>

<img width="1440" height="815" alt="sales-pricing" src="https://github.com/user-attachments/assets/a88b7172-ff22-4886-bbff-f1dc12176784" />


 What the Data Showed
North region leads with 32.6% of total revenue, followed closely by West
Maruti Suzuki is the top-selling brand — the top 5 brands together drive 57.5% of revenue
The mid-range segment (₹5–10L) dominates: 48.8% of units and 43.2% of revenue
99.2% of deals are profitable — selling price consistently exceeds purchase cost
Luxury cars (BMW, Mercedes, Audi) take the longest to sell — roughly 65–69 days on average
354 cars (9.8% of stock) have been sitting 90+ days, tying up an estimated ₹30 Cr in capital
The core buyer is 29–44 years old, and 76.1% of buyers are first owners
💡 What I'd Do Next

Given more time, I'd extend this with drill-through pages for individual brands, a tooltip page for quick chart-level detail, and a bookmark-driven "reset view" — features I scoped out but chose to prioritize the core three pages first.
