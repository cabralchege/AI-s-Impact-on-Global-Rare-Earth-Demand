# The Geothermal Champions League: A Global Energy Analysis

This project is a data-driven analysis of the global geothermal energy market, moving beyond simple production numbers to identify the true leaders, their strategic dependencies, and the "new challengers" racing to build the future.

### **The Problem Statement**

Geothermal energy is one of the only 24/7, "baseload" renewable power sources that doesn't depend on the sun shining or the wind blowing. However, its global adoption is highly concentrated.

This analysis seeks to answer: **Who are the true geothermal leaders?** What is the *real-world impact* of this energy on their grids? And who is winning the race to build the future?

### **The Final Dashboard**

This project's final output is a 6-visual dashboard in Tableau, designed with a minimalist, story-driven style inspired by *The Economist*.

*(Dashboard image)*
``

---

### **The Data Story: Key Questions & Insights**

This dashboard is designed to answer six key questions:

**1. Who is the biggest producer?**
* **Insight:** The **United States** is the undisputed heavyweight champion of *total production*. It generates more geothermal power than many other countries combined.

**2. Who is the most *dependent* on geothermal?**
* **Insight (What the naked eye misses):** Production numbers are misleading. The *real dependency* (per capita) is in countries like **Kenya** and **New Zealand**, where geothermal is a foundational pillar of the entire national energy strategy.

**3. Who is winning the *growth race*?**
* **Insight (The Changing of the Guard):** The "Old Guard" (like the USA) is **stagnant**. Their production has been flat for decades. The real story is the "New Challengers" like **Turkey** and **Kenya**, which show exponential, "hockey stick" growth, signaling massive national investment.

**4. Who is the fastest "sprinter" right now?**
* **Insight:** The year-over-year percentage growth chart highlights the emerging players who are most aggressively building capacity right now.

**5. What is the simplified trend?**
* **Insight:** By grouping the "Old Guard" vs. the "New Challengers," the story is unmistakable: the established leaders are flat, while the emerging players are on a clear upward path, closing the gap.

**6. Who is adding the most *actual power*?**
* **Insight:** This chart adds the final context. A high *percentage* jump in a small country is different from a small jump in a large one. This shows who added the most *absolute TWh* of new energy, balancing the "sprinter" view.

---

### **Data Source & Methodology**

#### **Data Source**
* **Provider:** Ember
* **Dataset:** `yearly_electricity_data.csv`
* **File Used:** `ember_yearly_electricity-generation - Other renewables - Multiple regions.csv.xlsx - Long Data Format.csv` (filtered for key geothermal-producing nations).

#### **ETL (Extract, Transform, Load) Process**

This project's technical challenge was a classic "data shape" problem:

1.  **Extract:** The data was downloaded from Ember as a "long" format CSV (one row per country, per year).

2.  **Transform (Attempt 1: Power Query):** My initial exploration involved pivoting the data in **Microsoft Excel (Power Query)** to a "wide" format (one row per country, with years as columns: `2000`, `2001`, `2002`... ).

3.  **The Challenge (Tableau):** This "wide" data was impossible to use in Tableau. It was loaded as 25 separate measures, making a simple line chart (generation *over time*) impossible.

4.  **Transform (Solution: Tableau Pivot):** The solution was to pivot the data *back* into a "long" format within Tableau itself.
    * **Action:** On the "Data Source" tab in Tableau, all year columns (`2000`...`2024`) were selected.
    * **Action:** Right-clicked > **"Pivot"**.
    * **Result:** This created two new columns: "Pivot Field Names" (renamed to **"Year"**) and "Pivot Field Values" (renamed to **"Generation (TWh)"**).

5.  **Load (Visualization):** With the data in the correct "long" format, I built the 6 visualizations. The *Economist* styling was achieved by:
    * Setting all fonts to a clean sans-serif (Arial/Tahoma).
    * Removing all gridlines, borders, and unnecessary axis labels.
    * Using the **"Duplicate Trick"** (duplicating the `entity` field) to apply strategic color (e.g., "red" for one country, "gray" for all others) to each chart without them interfering with each other.

---

### **Tools Used**

* **Microsoft Excel (Power Query):** For initial data cleaning and transformation exploration.
* **Tableau Public:** For data pivoting, visualization, and final dashboard creation.

### **View the Interactive Dashboard**

You can view, filter, and interact with the complete, live dashboard on Tableau Public:
[Tableau Link]

**[LINK TO YOUR TABLEAU PUBLIC DASHBOARD]**

