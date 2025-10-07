# Healthcare-Claims-Performance-Dashboard
Claims Analytics Dashboard: Finding Clarity in Complexity


### About This Project

This project is my answer to a critical business question: How can a health insurance company navigate the complex sea of claims data to make faster, smarter decisions? I designed and built this end-to-end Power BI dashboard to transform thousands of raw data points into a clear, interactive, and insightful story.

This isn't just a report; it's a command center for understanding business performance, managing costs, and optimizing operations.

---

### The Scenario: Lost in a Sea of Data

Every single day, thousands of claims arrive. Each claim is a story—a patient, a procedure, a cost. Now, multiply that by a year. You have millions of data points.

**The problem is clear:**
* **Slow Answers:** How long does it take to figure out your approval rate for last month? 
* **Hidden Costs:** Which medical specialties are driving the most cost? Is it a trend or a one-time spike?
* **Operational Blind Spots:**What is the average claim amount per claim type?
Without the right tool, answering these questions is a slow, manual process of wrestling with spreadsheets. Opportunities are missed, and problems can grow unnoticed.

---

### The Solution: A Clear Map and a Powerful Compass

My solution was to build that map and compass. I developed this interactive dashboard in Power BI to serve as a single source of truth. It takes that overwhelming data and organizes it into a simple, visual narrative that anyone can understand.

**The dashboard is designed to help leaders:**
* **See the Big Picture:** Instantly grasp key metrics on the main summary page.
* **Ask Deeper Questions:** Drill down into a dedicated financial page to understand *why* things are happening.
* **Make Data-Driven Decisions:** Move from guessing to knowing, with confidence.

---

### A Tour of the Dashboard

The dashboard is split into two main views:

#### 1. The Mission Control (Executive Summary)
This is the first page you land on. It gives you a real-time health check of the entire claims process. You can immediately see the total number of claims, how much has been paid out, and how your approval and denial rates are tracking against your goals.

#### 2. The Financial X-Ray (Financial Deep Dive)
When you need to understand the costs, this is where you go. This page helps you see exactly where the money is going—which medical specialties are most expensive, how costs vary by the type of claim, and how patient age groups impact the financials.

### The Tools of the Trade

* **Platform:** Microsoft Power BI
* **Data Cleaning & Transformation:** Power Query 
* **Calculations & KPIs:** Data Analysis Expressions (DAX)

---

### Under the Hood: A Glimpse into the Logic

To show you how the magic happens, here’s the DAX formula for the **Approval Rate**. It might look technical, but the logic is simple:

```dax
Approval Rate =
VAR ApprovedClaims =
    CALCULATE(
        [Total Claims Processed],
        'enhanced_health_insurance_claims'[ClaimStatus] = "Approved"
    )
VAR TotalClaims = [Total Claims Processed]
RETURN
    DIVIDE(ApprovedClaims, TotalClaims, 0)
```

**In plain English, this code does three simple things:**
1.  First, it creates a temporary variable (`ApprovedClaims`) to count only the claims marked "Approved".
2.  Next, it gets the total count of all claims processed.
3.  Finally, it divides the 'approved' number by the 'total' number to get the percentage.

This simple but powerful logic is what drives the gauges and KPIs on the dashboard.

---

### The Bottom Line: Real-World Impact

So, what does this all mean for the business?

* **Faster Decisions:** What used to take hours of digging through spreadsheets can now be answered in seconds.
* **Smarter Spending:** By pinpointing high-cost specialties or providers, the company can ask better questions and potentially save millions in the long run.
* **Better Processes:** Identifying bottlenecks (like high denial rates for paper claims) provides clear evidence to support changes that can make the entire system more efficient.


Thank you for taking the time to review my work!

**Lekhana K** | Linkedin Profile : https://www.linkedin.com/in/lekhana-k-11b028270/
