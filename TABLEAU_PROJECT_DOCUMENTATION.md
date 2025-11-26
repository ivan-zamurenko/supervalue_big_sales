# 📊 Tableau Sales Analytics Project

> **A comprehensive guide to building enterprise-level sales dashboards with Tableau**

---

## 🎯 Project Overview

This document outlines the complete process of building two interactive Tableau dashboards designed to help stakeholders analyze sales performance and customer behavior. The project demonstrates advanced data visualization techniques, dashboard design principles, and business intelligence best practices.

---

## 📋 Table of Contents

- [Step 1: Analyze Requirements](#step-1-analyze-requirements)
  - [1.1 Collect Requirements](#11-collect-requirements)
  - [1.2 Choose the Right Charts](#12-choose-the-right-charts)
  - [1.3 Draw Mockups](#13-draw-mockups)
  - [1.4 Choose Colors](#14-choose-colors)
- [Step 2: Build Data Source](#step-2-build-data-source)
- [Step 3: Build Charts](#step-3-build-charts)
- [Step 4: Build Dashboards](#step-4-build-dashboards)

---

## Step 1: Analyze Requirements

> **Objective:** Establish a solid foundation by understanding business needs, selecting appropriate visualizations, and defining the visual language of the project.

### 1.1 Collect Requirements

#### 📌 Project Context

This project focuses on building **two dashboards** using Tableau to help stakeholders analyze sales performance and customers effectively. The first phase concentrates on the **Sales Dashboard**.

---

### 🎯 Dashboard 1: SALES DASHBOARD

#### **Purpose**
To present a comprehensive overview of sales metrics and trends, enabling stakeholders to analyze year-over-year sales performance and make data-driven decisions.

---

### 1.2 Choose the Right Charts

Understanding which chart type serves each analytical purpose is crucial for effective data visualization. Here's the strategic chart selection for each requirement:

#### **📊 Key Performance Indicators (KPIs)**

**Requirement:** Summary of total sales, profits, and quantity for current year and previous year

**Chart Type:** `BANs (Big Associated Numbers)`

**Rationale:**
- **Best for:** Displaying primary metrics and large numerical values
- **Use case:** Total sales, quantity, and income figures
- **Visual impact:** Immediate attention to key business metrics
- **Design benefit:** Clean, scannable, executive-friendly format

```
┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐
│  Total Sales    │  │  Total Profit   │  │  Total Quantity │
│                 │  │                 │  │                 │
│   $2,456,892    │  │    $342,567     │  │     15,847      │
│   ↑ 12.5%       │  │    ↑ 8.3%       │  │     ↑ 6.7%      │
└─────────────────┘  └─────────────────┘  └─────────────────┘
```

---

#### **📈 Sales Trends Analysis**

**Requirement 1:** Present data for each KPI on a monthly basis for current and previous years

**Chart Type:** `Line Chart`

**Rationale:**
- **Best for:** Showing trends over continuous time periods
- **Use case:** Monthly progression comparison
- **Visual impact:** Easy identification of patterns, seasonality, and growth trajectories
- **Interaction:** Compare current year vs. previous year performance

**Requirement 2:** Identify months with highest and lowest sales

**Chart Type:** `Sparkline Chart`

**Rationale:**
- **Best for:** Compact trend visualization with quick insights
- **Use case:** At-a-glance performance indicators
- **Visual impact:** Minimal space with maximum information density
- **Design benefit:** Supports the main line chart without cluttering

```
Month-by-Month Sales Trends
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
        ╱╲
       ╱  ╲    ╱╲
      ╱    ╲  ╱  ╲        2024
     ╱      ╲╱    ╲      ━━━━━
    ╱              ╲     2023
   ╱                ╲    ┄┄┄┄┄
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Jan Feb Mar Apr May Jun Jul Aug Sep Oct Nov Dec
```

---

#### **📊 Product Subcategory Comparison**

**Requirement:** Compare sales performance by different product subcategories for current year and previous year, including sales vs. profit comparison

**Chart Type:** `Bar-in-Bar Chart`

**Rationale:**
- **Best for:** Direct comparison between two periods or metrics
- **Use case:** Year-over-year subcategory performance
- **Visual impact:** Clear side-by-side comparison with nested values
- **Analysis benefit:** Enables identification of top/bottom performers and profit margins

```
Product Subcategory Performance
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Phones       ████████████████ 2024
             ███████████ 2023

Chairs       ████████████ 2024
             ██████████ 2023

Storage      ██████████ 2024
             ████████ 2023

Tables       ████████ 2024
             ██████ 2023
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
      0    50k   100k  150k  200k
```

---

#### **📉 Weekly Trends for Sales & Profit**

**Requirement:** Present weekly sales and profit data for the current year, display average weekly values, and highlight weeks above/below average

**Chart Type:** `Line Chart with Reference Lines`

**Rationale:**
- **Best for:** Granular time-series analysis with benchmarking
- **Use case:** Week-by-week performance tracking
- **Visual impact:** Quick identification of high/low performance weeks
- **Design benefit:** Reference line provides context and highlights anomalies

```
Weekly Sales & Profit Trends
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
         Peak Week
            ╱╲
           ╱  ╲
          ╱    ╲    ╱╲
─────────────────────────────────── Average Line
        ╱      ╲  ╱  ╲
       ╱        ╲╱    ╲
      ╱                ╲  
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
W1  W5   W10  W15  W20  W25  W30  W35
Above Avg: Green | Below Avg: Red
```

---

### 1.3 Draw Mockups

**Purpose:** Create a visual blueprint of the dashboard layout before development to ensure optimal user experience and information hierarchy.

#### **Dashboard Layout Strategy**

The mockup organizes information following the **F-Pattern** reading behavior:

1. **Top Section:** KPI BANs (immediate attention to key metrics)
2. **Middle-Left:** Monthly trends (primary analytical focus)
3. **Middle-Right:** Product subcategory comparison (categorical insights)
4. **Bottom:** Weekly trends (detailed performance drill-down)

![Dashboard Mockup](mockup/sales_dashboard_mockup.png)

**Key Design Decisions:**
- **White space:** Adequate padding for visual breathing room
- **Hierarchy:** Largest metrics at top, detailed analysis below
- **Flow:** Left-to-right, top-to-bottom natural reading pattern
- **Balance:** Equal weight distribution across quadrants

---

### 1.4 Choose Colors

> **Design Principle:** Limit the color palette to maintain visual consistency and professional appearance. Maximum of **4 colors** following corporate brand guidelines.

#### **Color Palette Strategy**

##### **🎨 Basic Colors (Neutrals)**

| Color | Hex Code | Usage | Purpose |
|-------|----------|-------|---------|
| **Dark Gray** | `#303030` | Text, borders, headers | Primary readability, professional tone |
| **Light Gray** | `#b3b3b3` | Background, secondary text, gridlines | Subtle contrast, non-intrusive elements |

##### **🎨 Custom Colors (Brand)**

| Color | Hex Code | Usage | Purpose |
|-------|----------|-------|---------|
| **Orange** | `#ff5500` | Highlights, current year data, CTAs | Brand identity, attention-drawing |
| **Dark Gray** | `#303030` | Previous year data, comparison baseline | Consistency, contrast with brand color |

#### **Color Application Guidelines**

```
┌─────────────────────────────────────────────────────┐
│  Dashboard Title & Headers → #303030               │
├─────────────────────────────────────────────────────┤
│                                                     │
│  KPI Cards                                         │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐        │
│  │ #ff5500  │  │ #ff5500  │  │ #ff5500  │  ← Current Year
│  │ #303030  │  │ #303030  │  │ #303030  │  ← Previous Year
│  └──────────┘  └──────────┘  └──────────┘        │
│                                                     │
│  Charts & Graphs                                   │
│  • Current Year Line/Bar → #ff5500                │
│  • Previous Year Line/Bar → #303030 (or #b3b3b3)  │
│  • Positive Performance → #ff5500                  │
│  • Negative Performance → #b3b3b3                  │
│  • Background Elements → #b3b3b3                   │
│                                                     │
└─────────────────────────────────────────────────────┘
```

**Why This Palette Works:**
- ✅ **Brand alignment:** Custom colors reflect company identity
- ✅ **Accessibility:** High contrast ratios ensure readability
- ✅ **Consistency:** Limited palette creates cohesive visual experience
- ✅ **Professionalism:** Neutral base with strategic accent colors
- ✅ **Focus:** Orange draws eyes to current performance and actionable insights

---

### 🎯 Design and Interactivity Requirements

To maximize dashboard utility and user engagement, the following interactive features will be implemented:

#### **📅 Time Navigation**
- **Date Parameter Filter:** Enable users to select any historical year for comparative analysis
- **Dynamic Updates:** All charts automatically adjust to selected time period

#### **🔀 Dashboard Navigation**
- **Easy Transitions:** Smooth navigation between Sales and Customer dashboards
- **Persistent Filters:** Maintain filter selections across dashboard switches (when applicable)

#### **🎛️ Interactive Filtering**

**Chart-Based Filtering:**
- Click on any chart element to filter related visualizations
- Enable cross-filtering across all dashboard components

**Hierarchical Filters:**

1. **Product Hierarchy:**
   - Category → Subcategory
   - Example: Technology → Phones → Specific Models

2. **Geographic Hierarchy:**
   - Region → State → City
   - Example: West → California → San Francisco

#### **Filter Panel Features**
```
┌─────────────────────────┐
│  📍 FILTERS             │
├─────────────────────────┤
│  📅 Year: [2024    ▼]   │
│                         │
│  📦 Product Category    │
│  ☐ Technology          │
│  ☐ Furniture           │
│  ☐ Office Supplies     │
│                        │
│  🗺️  Region             │
│  ☐ West                │
│  ☐ East                │
│  ☐ Central             │
│  ☐ South               │
│                         │
│  [Apply] [Reset]        │
└─────────────────────────┘
```

---

## 📊 Summary: Step 1 Completion Checklist

- [x] **Requirements Collected:** Defined dashboard purpose and key metrics
- [x] **Charts Selected:** Mapped analytical needs to optimal chart types
- [x] **Mockup Created:** Designed layout following UX best practices
- [x] **Colors Chosen:** Established 4-color palette aligned with brand guidelines
- [x] **Interactivity Defined:** Specified filtering and navigation requirements

---

### ✨ Key Takeaways from Step 1

| Aspect | Decision | Impact |
|--------|----------|--------|
| **Dashboard Focus** | Sales performance & trends | Clear analytical purpose |
| **Chart Strategy** | 5 chart types (BANs, Line, Sparkline, Bar-in-Bar) | Comprehensive visual coverage |
| **User Experience** | Multi-level filtering + navigation | Enhanced interactivity |
| **Visual Identity** | 4-color palette (2 neutral, 2 brand) | Professional, consistent design |
| **Time Analysis** | Monthly, weekly, YoY comparison | Multi-granularity insights |

---

### 🎓 Skills Demonstrated

- ✅ **Requirements Analysis:** Translating business needs into technical specifications
- ✅ **Data Visualization Theory:** Selecting appropriate chart types for different data stories
- ✅ **UX/UI Design:** Creating user-centric dashboard layouts
- ✅ **Brand Consistency:** Applying design systems and color theory
- ✅ **Interaction Design:** Planning dynamic and responsive dashboard features

---

> **Next Step:** [Step 2: Build Data Source](#step-2-build-data-source)  
> We'll connect to data sources, create a robust data model, and prepare our data for visualization.

---

## Step 2: Build Data Source

> **Objective:** Establish a clean, well-structured data foundation by connecting data sources, creating proper data models, and ensuring data quality through type validation and field optimization.

### 2.1 Connect Data

#### **📁 Data Source Location**

The project data is stored in the `/dataset` folder. This centralized location contains all necessary files for building the sales analytics dashboard.

**Connection Process:**
1. Open Tableau Desktop
2. Navigate to **Data** → **Connect to Data**
3. Select appropriate connector (Excel, CSV, Database, etc.)
4. Browse to `/dataset` folder
5. Select the data file(s)
6. Verify successful connection in the Data Source tab

```
📂 Project Structure
└── dataset/
    ├── location.csv
    ├── customers.csv
    └── products.csv
    └── orders.csv
```

---

### 2.2 Create Data Model

#### **🔍 Identify Data Types: Dimensions vs. Facts**

Understanding the distinction between **Dimension** and **Fact** data is crucial for building an effective data model.

##### **📐 Dimension Tables (DIM)**

**Definition:** Descriptive attributes that provide context to business metrics. Used for filtering, grouping, and categorizing data.

**Characteristics:**
- Typically text-based or categorical data
- Represent the "Who, What, Where, When, Why"
- Used in filters, rows, columns, and color encoding
- Lower cardinality (fewer unique values relative to dataset size)

**Common Dimensions in Sales Data:**

| Dimension | Description | Example Values |
|-----------|-------------|----------------|
| **Product Name** | Individual product identifier | iPhone 14, Dell Monitor, Office Chair |
| **Category** | High-level product grouping | Technology, Furniture, Office Supplies |
| **Sub-Category** | Detailed product classification | Phones, Chairs, Storage, Tables |
| **Customer Name** | Individual customer identifier | John Smith, ABC Corporation |
| **Region** | Geographic territory | West, East, Central, South |
| **State** | State/Province location | California, Texas, New York |
| **City** | City location | San Francisco, Austin, New York City |
| **Segment** | Customer classification | Consumer, Corporate, Home Office |
| **Ship Mode** | Delivery method | Standard Class, First Class, Same Day |
| **Order Date** | Date dimension | 2024-01-15, 2023-12-31 |

##### **📊 Fact Tables (FACT)**

**Definition:** Quantitative data representing business measurements and metrics. Used for calculations and aggregations.

**Characteristics:**
- Numeric data that can be aggregated
- Represent measurable business events
- Used in calculations, aggregations (SUM, AVG, COUNT)
- High cardinality (many unique values)

**Common Facts in Sales Data:**

| Fact | Description | Aggregation Type |
|------|-------------|------------------|
| **Sales** | Total revenue amount | SUM, AVG |
| **Profit** | Profit amount | SUM, AVG |
| **Quantity** | Number of units sold | SUM, AVG, COUNT |
| **Discount** | Discount percentage/amount | AVG, SUM |
| **Shipping Cost** | Cost of delivery | SUM, AVG |

**Visual Distinction:**

```
┌─────────────────────────────────────────────────────┐
│  DATA MODEL STRUCTURE                               │
├─────────────────────────────────────────────────────┤
│                                                     │
│  DIM_Products                    FACT_Sales         │
│  ┌──────────────┐               ┌──────────────┐    │
│  │ Product ID   │◄──────────────│ Product ID   │    │
│  │ Product Name │               │ Order ID     │    │
│  │ Category     │               │ Customer ID  │    │
│  │ Sub-Category │               │ Order Date   │    │
│  └──────────────┘               │ Sales        │    │
│                                 │ Profit       │    │
│  DIM_Customers                  │ Quantity     │    │
│  ┌──────────────┐               │ Discount     │    │
│  │ Customer ID  │◄──────────────│              │    │
│  │ Customer Name│               └──────────────┘    │
│  │ Segment      │                                   │
│  │ Region       │                                   │
│  │ State        │                                   │
│  │ City         │                                   │
│  └──────────────┘                                   │
│                                                     │
└─────────────────────────────────────────────────────┘
```

---

### 2.3 Rename Fields & Tables

#### **🏷️ Purpose of Renaming**

Clean, descriptive names improve:
- **Readability:** Easier for team members to understand
- **Consistency:** Standardized naming conventions
- **Professionalism:** Client-ready field names in tooltips and filters
- **Maintenance:** Simpler troubleshooting and updates

#### **Naming Best Practices**

**Before → After Examples:**

| Original Name | Renamed To | Reason |
|---------------|------------|--------|
| `prod_cat` | `Product Category` | More descriptive, readable |
| `OrderDt` | `Order Date` | Consistent formatting |
| `cust_seg` | `Customer Segment` | Professional appearance |
| `qty` | `Quantity` | Full word clarity |
| `rev` | `Sales Revenue` | Explicit meaning |
| `Table1` | `Sales Transactions` | Meaningful table name |
| `Sheet1` | `Customer Master` | Descriptive purpose |

**Renaming Process in Tableau:**
1. Navigate to **Data Source** tab
2. Right-click on field name
3. Select **Rename**
4. Enter new descriptive name
5. Press Enter to confirm

```
✓ Use clear, business-friendly terminology
✓ Avoid abbreviations unless industry-standard
✓ Use Title Case for consistency
✓ Remove underscores, replace with spaces
✓ Make names self-explanatory
```

---

### 2.4 Check Data Types

> **⚠️ CRITICAL STEP:** Incorrect data types are the most common source of errors in Tableau dashboards. Always validate data types before proceeding with analysis.

#### **🔢 Priority Data Type Checks**

##### **1️⃣ DATE Fields (HIGHEST PRIORITY)**

**Problem:** Date fields frequently import as STRING (text) instead of DATE type.

**Impact if Incorrect:**
- ❌ Cannot perform time-based calculations
- ❌ Date filters won't work properly
- ❌ Unable to extract year, month, quarter
- ❌ Trend analysis becomes impossible

**Validation Process:**

```
┌────────────────────────────────────────┐
│  Field: Order Date                     │
├────────────────────────────────────────┤
│  Current Type: Abc (String) ❌         │
│                                        │
│  Should Be: 📅 (Date) ✓                │
│                                        │
│  Action Required: Change Data Type     │
└────────────────────────────────────────┘
```

**How to Fix in Tableau:**
1. Click the data type icon next to the field name
2. Select **Date** from dropdown menu
3. Verify the date format is recognized correctly
4. Check a few sample values to confirm

**Date Fields to Check:**
- ✓ Order Date
- ✓ Ship Date
- ✓ Delivery Date
- ✓ Return Date
- ✓ Any timestamp fields

---

##### **2️⃣ GEOGRAPHIC Fields (REGION, STATE, CITY)**

**Problem:** Geographic fields import as STRING instead of Geographic Role type.

**Impact if Incorrect:**
- ❌ Cannot use map visualizations
- ❌ Missing automatic latitude/longitude generation
- ❌ No geographic hierarchy
- ❌ Spatial analysis unavailable

**Validation Process:**

```
┌────────────────────────────────────────┐
│  Field: Region                         │
├────────────────────────────────────────┤
│  Current Type: Abc (String) ❌         │
│                                        │
│  Should Be: 🌍 (Geographic) ✓          │
│                                        │
│  Available Roles:                      │
│  • Country/Region                      │
│  • State/Province                      │
│  • City                                │
│  • ZIP Code/Postcode                   │
└────────────────────────────────────────┘
```

**How to Assign Geographic Role:**
1. Right-click on the field
2. Select **Geographic Role**
3. Choose appropriate option:
   - **Country/Region** → for Region field
   - **State/Province** → for State field
   - **City** → for City field
   - **ZIP Code/Postcode** → for postal codes
4. Tableau will validate and assign coordinates

**Geographic Fields to Check:**
- ✓ Region → Assign "Country/Region" role
- ✓ State → Assign "State/Province" role
- ✓ City → Assign "City" role
- ✓ Country → Assign "Country/Region" role
- ✓ Postal Code → Assign "ZIP Code/Postcode" role

**Verification:**
- Look for globe icon 🌍 next to field name
- Test by dragging to sheet - should auto-generate map

---

##### **3️⃣ NUMBER Fields (CRITICAL FOR CALCULATIONS)**

**Problem:** Numeric fields may import as STRING type, preventing mathematical operations.

**Impact if Incorrect:**
- ❌ Cannot sum, average, or aggregate
- ❌ Calculations will fail or produce errors
- ❌ Unable to create KPIs
- ❌ Year-over-year comparisons impossible

**Validation Process:**

```
┌────────────────────────────────────────┐
│  Field: Sales                          │
├────────────────────────────────────────┤
│  Current Type: Abc (String) ❌         │
│  Sample Value: "1,234.56"              │
│                                        │
│  Should Be: #️⃣ (Number - Decimal) ✓    │
│  Sample Value: 1234.56                 │
│                                        │
│  Field: Quantity                       │
│  Should Be: #️⃣ (Number - Whole) ✓      │
└────────────────────────────────────────┘
```

**How to Fix in Tableau:**
1. Click the data type icon (Abc or #)
2. Select appropriate number type:
   - **Number (Decimal)** → for currency, percentages
   - **Number (Whole)** → for quantities, counts
3. Verify sample values display correctly
4. Check for any null or error values

**Number Fields to Check:**

| Field | Expected Type | Reason |
|-------|---------------|--------|
| **Sales** | Number (Decimal) | Currency values with cents |
| **Profit** | Number (Decimal) | Can be negative, has decimals |
| **Quantity** | Number (Whole) | Integer count of items |
| **Discount** | Number (Decimal) | Percentage values |
| **Shipping Cost** | Number (Decimal) | Currency values |
| **Product ID** | String | Identifier, not for calculation |
| **Order ID** | String | Identifier, not for calculation |
| **Year** | Number (Whole) or Date Part | Depends on use case |

**⚠️ Important Note on IDs:**
- Even if IDs contain only numbers, keep them as STRING
- IDs are identifiers, not measures for calculation
- Examples: Order ID, Customer ID, Product ID

---

### 2.5 Understand Data

#### **🔍 Data Exploration Checklist**

Before building visualizations, thoroughly understand your dataset:

##### **Data Profiling Activities:**

**1. Check Data Quality:**
```
□ Identify null/missing values
□ Check for duplicate records
□ Verify data ranges (min/max values)
□ Look for outliers or anomalies
□ Confirm date ranges align with expectations
```

**2. Understand Relationships:**
```
□ Identify primary keys (unique identifiers)
□ Understand foreign key relationships
□ Determine cardinality (one-to-many, many-to-many)
□ Document join conditions
```

**3. Data Profiling in Tableau:**
```
┌─────────────────────────────────────────┐
│  Quick Data Profile View                │
├─────────────────────────────────────────┤
│  Sales:                                 │
│  • Min: $0.44                           │
│  • Max: $22,638.48                      │
│  • Avg: $229.86                         │
│  • Null Count: 0                        │
│                                         │
│  Order Date:                            │
│  • Earliest: 2020-01-03                 │
│  • Latest: 2024-12-30                   │
│  • Date Range: 5 years                  │
│                                         │
│  Region:                                │
│  • Unique Values: 4                     │
│  • Values: West, East, Central, South   │
└─────────────────────────────────────────┘
```

**4. Business Logic Validation:**
```
□ Profit = Sales - Costs (verify formula)
□ Negative profits indicate losses
□ Discounts should be between 0-100%
□ Quantities should be positive integers
□ Dates should be within business operating period
```

---

### 📋 Step 2 Completion Checklist

```
✅ Data Source Connected
   └─ Files loaded from /dataset folder

✅ Data Model Created
   └─ Dimensions identified (Product, Customer, Location, Time)
   └─ Facts identified (Sales, Profit, Quantity)

✅ Fields & Tables Renamed
   └─ Descriptive, business-friendly names applied
   └─ Consistent naming convention established

✅ Data Types Validated (CRITICAL)
   └─ ✓ DATE fields converted from String → Date
   └─ ✓ REGION/LOCATION fields assigned Geographic Roles
   └─ ✓ NUMBER fields verified (Sales, Profit, Quantity)
   └─ ✓ String fields retained for identifiers

✅ Data Understanding Complete
   └─ Data quality assessed
   └─ Relationships documented
   └─ Business logic validated
```

---

### 🎓 Skills Demonstrated in Step 2

- ✅ **Data Integration:** Connecting and importing data from multiple sources
- ✅ **Data Modeling:** Distinguishing dimensions from facts, creating star schema
- ✅ **Data Quality Management:** Validating data types, identifying issues
- ✅ **ETL Fundamentals:** Understanding Extract, Transform, Load processes
- ✅ **Metadata Management:** Renaming and organizing fields for usability
- ✅ **Geographic Data Handling:** Assigning spatial roles for mapping capabilities
- ✅ **Data Profiling:** Exploring and validating data before analysis

---

### ⚠️ Common Pitfalls to Avoid

| Issue | Problem | Solution |
|-------|---------|----------|
| **String Dates** | Cannot perform time analysis | Always convert to Date type |
| **String Numbers** | Calculations fail | Verify all metrics are Number type |
| **Missing Geo Roles** | Maps don't work | Assign geographic roles to location fields |
| **Unclear Names** | Confusion in analysis | Use descriptive, business-friendly names |
| **Skipped Validation** | Errors in dashboard | Always verify data types before building |

---

### 💡 Pro Tips

```
🎯 Create a Data Dictionary
   Document all fields, their types, and business definitions
   
🎯 Save Data Source as .tds File
   Reusable connection for multiple workbooks
   
🎯 Use Data Source Filters
   Exclude test data or irrelevant records early
   
🎯 Create Calculated Fields for Common Metrics
   Set up foundational calculations in data source
   
🎯 Test Joins with Sample Data
   Verify relationships before building complex views
```

---

> **Next Step:** [Step 3: Build Charts](#step-3-build-charts)  
> With clean, validated data in place, we'll create calculated fields and build the visualizations designed in Step 1.

---

*Document Status: Step 2 Complete ✓*  
*Last Updated: November 25, 2025*

---

## Step 3: Build Charts

> **Objective:** Transform clean data into powerful visualizations by creating calculated fields, building charts, and applying professional formatting to highlight insights and minimize distractions.

This step is divided into two critical phases:
1. **Chart Construction:** Creating calculated fields and building visualizations
2. **Chart Formatting:** Applying minimalist design principles for maximum impact

---

### 3.1 Create Calculated Fields & Build Charts

#### **📊 Chart 1: BANs (Big Associated Numbers) - KPI Cards**

BANs display key performance indicators prominently, showing current year performance with year-over-year comparison.

##### **🎯 Objective**
Display total sales amount per year with dynamic year selection and percentage difference between current year (CY) and previous year (PY).

---

##### **Step 1: Create Parameter for Year Selection**

**Purpose:** Enable users to dynamically select which year to analyze.

**How to Create:**
1. Right-click in the Data pane → **Create Parameter**
2. Configure parameter settings:

```
┌─────────────────────────────────────────┐
│  Create Parameter: Select Year          │
├─────────────────────────────────────────┤
│  Name: Select Year                      │
│  Data type: Integer                     │
│  Current value: 2024                    │
│  Display format: ####                   │
│                                         │
│  Allowable values: List                 │
│  ┌────────┬────────┐                   │
│  │ Value  │ Display│                   │
│  ├────────┼────────┤                   │
│  │ 2024   │ 2024   │                   │
│  │ 2023   │ 2023   │                   │
│  │ 2022   │ 2022   │                   │
│  │ 2021   │ 2021   │                   │
│  └────────┴────────┘                   │
└─────────────────────────────────────────┘
```

3. Click **OK** to create parameter
4. Right-click parameter → **Show Parameter** to display selector on dashboard

---

##### **Step 2: Create CY (Current Year) Calculated Field**

**Purpose:** Calculate total sales for the selected year.

**Calculated Field Name:** `CY Sales`

**Formula:**
```
IF YEAR([Order Date]) = [Select Year]
THEN [Sales]
END
```

**Explanation:**
- Filters sales data to only include the year selected in the parameter
- Returns sales values for the current year, null for other years
- Aggregates to show total when used in visualization

**How to Create:**
1. Right-click in Data pane → **Create Calculated Field**
2. Name: `CY Sales`
3. Enter formula
4. Click **OK**

**Expected Result:** When aggregated (SUM), shows total sales for selected year

---

##### **Step 3: Create PY (Previous Year) Calculated Field**

**Purpose:** Calculate total sales for the year before the selected year.

**Calculated Field Name:** `PY Sales`

**Formula:**
```
IF YEAR([Order Date]) = [Select Year] - 1
THEN [Sales]
END
```

**Explanation:**
- Filters sales data for the year prior to selection
- `[Select Year] - 1` automatically calculates previous year
- Enables year-over-year comparison

**Expected Result:** When aggregated (SUM), shows total sales for previous year

---

##### **Step 4: Create YoY % Difference Calculated Field**

**Purpose:** Calculate percentage change between current year and previous year.

**Calculated Field Name:** `YoY Sales % Diff`

**Formula:**
```
(SUM([CY Sales]) - SUM([PY Sales])) / SUM([PY Sales])
```

**Explanation:**
- Calculates the difference: CY - PY
- Divides by PY to get percentage change
- Result: Positive = growth, Negative = decline
- Example: If CY=$120K, PY=$100K → (120-100)/100 = 0.20 = 20% growth

**Formatting:**
1. Right-click field → **Default Properties** → **Number Format**
2. Select **Percentage**
3. Set decimal places: **1**

**Visual Indicator Logic (Optional Enhancement):**
```
// Add color indicator
IF SUM([CY Sales]) > SUM([PY Sales])
THEN "▲ Positive"
ELSE "▼ Negative"
END
```

---

##### **Step 5: Build the BAN Visualization**

**Creating Total Sales BAN:**

1. Create new worksheet: Name it `BAN - Total Sales`
2. Drag `CY Sales` to **Text** on Marks card
3. Change aggregation to **SUM**
4. Format the number:
   - Right-click → **Format**
   - Numbers → **Currency (Custom)**
   - Set to display as: `$#,##0K` or `$#,##0,000`

**Layout Structure:**
```
┌───────────────────────────────┐
│      Total Sales              │
│                               │
│      $2,456,892              │
│      ↑ 12.5%                 │ ← YoY % Diff
│                               │
│      CY: $2,456,892          │
│      PY: $2,187,234          │
└───────────────────────────────┘
```

5. Add `PY Sales` below CY for reference
6. Add `YoY Sales % Diff` with arrow indicator
7. Apply color coding:
   - Green (#00ff00) for positive growth
   - Red (#ff0000) for negative growth

**Repeat for Other KPIs:**
- **BAN - Total Profit:** Use `[Profit]` field instead of `[Sales]`
- **BAN - Total Quantity:** Use `[Quantity]` field instead of `[Sales]`

---

#### **📈 Chart 2: SPARKLINE - Sales Trends with Min/Max**

Sparklines provide compact trend visualization showing monthly patterns and highlighting extreme values.

##### **🎯 Objective**
Display monthly sales trends for current and previous year, identifying months with highest and lowest sales.

---

##### **Step 1: Build Basic Sparkline Structure**

**Creating the Chart:**

1. Create new worksheet: Name it `Sparkline - Sales Trend`
2. **Columns:** Drag `Order Date` → Right-click → Select **MONTH** (continuous)
   - Ensure it shows as green pill (continuous) not blue (discrete)
3. **Rows:** Drag both `CY Sales` and `PY Sales` to create dual-axis
   - This combines both years on same chart

**Setting Up Dual Axis:**
1. Drag `CY Sales` to Rows
2. Hold **Control/Cmd** and drag `CY Sales` pill to create duplicate axis
3. Right-click second axis → **Dual Axis**
4. Right-click axis → **Synchronize Axis**

**Chart Configuration:**
```
Columns: MONTH(Order Date)
Rows:    SUM(CY Sales), SUM(PY Sales)

Result:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
        ╱╲                      CY 2024
       ╱  ╲    ╱╲               ━━━━━━
      ╱    ╲  ╱  ╲              
     ╱      ╲╱    ╲             PY 2023
    ╱              ╲            ┄┄┄┄┄┄
   ╱                ╲           
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Jan Feb Mar Apr May Jun Jul Aug Sep Oct Nov Dec
```

5. Change mark type to **Line** for both measures
6. Apply colors:
   - CY Sales → `#ff5500` (brand orange)
   - PY Sales → `#b3b3b3` (light gray)

---

##### **Step 2: Create Min/Max Sales Calculated Fields**

**Purpose:** Identify and highlight the months with highest and lowest sales performance.

**⚠️ IMPORTANT: Always Test Calculated Fields First**

Before applying complex calculations to your main chart, create a test sheet to verify the formula works correctly.

---

**Calculated Field: Maximum Sales Month**

**Field Name:** `Max Sales Month`

**Formula:**
```
IF SUM([CY Sales]) = WINDOW_MAX(SUM([CY Sales]))
THEN SUM([CY Sales])
END
```

**Explanation:**
- `WINDOW_MAX()` finds the highest sales value across all months in the view
- `IF` statement checks if current month equals the maximum
- Returns value only for the peak month, null for others
- Enables specific highlighting of best performance

---

**Calculated Field: Minimum Sales Month**

**Field Name:** `Min Sales Month`

**Formula:**
```
IF SUM([CY Sales]) = WINDOW_MIN(SUM([CY Sales]))
THEN SUM([CY Sales])
END
```

**Explanation:**
- `WINDOW_MIN()` finds the lowest sales value across all months
- Returns value only for the worst performing month
- Helps identify periods needing attention

---

##### **Step 3: Test Calculated Fields on Separate Sheet**

**⚠️ CRITICAL STEP:** Never apply untested calculations directly to production charts.

**Testing Process:**

1. Create new worksheet: Name it `TEST - Min Max Calculations`
2. Build test view:
   - **Columns:** `MONTH(Order Date)`
   - **Rows:** `SUM(CY Sales)`
3. Add `Max Sales Month` and `Min Sales Month` to the view
4. Verify results:

```
Test Sheet Layout:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Month    | CY Sales  | Max Month | Min Month
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Jan      | $185,234  |           |
Feb      | $165,890  |           | $165,890 ✓
Mar      | $234,567  |           |
...
Nov      | $287,945  | $287,945 ✓|
Dec      | $201,234  |           |
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Validation Checklist:**
```
□ Only ONE month shows value in Max column
□ Only ONE month shows value in Min column
□ Max value is indeed the highest in dataset
□ Min value is indeed the lowest in dataset
□ All other cells show null/empty
```

5. If test passes → proceed to apply to sparkline
6. If test fails → revise formula and retest

---

##### **Step 4: Apply Min/Max Highlights to Sparkline**

**Enhancing the Sparkline:**

1. Return to `Sparkline - Sales Trend` worksheet
2. Drag `Max Sales Month` to the view
   - Change mark type to **Circle**
   - Set color to `#ff5500` (highlight color)
   - Increase size for visibility
3. Drag `Min Sales Month` to the view
   - Change mark type to **Circle**
   - Set color to `#303030` (dark gray)
   - Increase size for visibility

**Final Sparkline Appearance:**
```
Monthly Sales Sparkline with Min/Max
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
            ⬤ MAX                   CY 2024
        ╱╲  │                       ━━━━━━
       ╱  ╲ │╱╲                     
      ╱    ╲│  ╲                    PY 2023
     ╱      ╲   ╲                   ┄┄┄┄┄┄
    ╱        ╲   ╲                  
   ╱⬤         ╲   ╲                 ⬤ = Key Points
  │ MIN        ╲   ╲                
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Jan Feb Mar Apr May Jun Jul Aug Sep Oct Nov Dec
```

4. Adjust table calculations if needed:
   - Right-click calculated field → **Edit Table Calculation**
   - Compute using: **Table (across)**
   - Ensure calculation runs across months correctly

---

### 3.2 Format Charts - Minimalist Design Principles

> **Philosophy:** Reduce visual clutter to focus attention on data insights. Every element should serve a purpose; remove everything else.

**Design Goal:** Stay minimalistic - let the data tell the story without distraction.

---

#### **🎨 Formatting Step 1: Remove Grid Lines & Reference Lines**

**Purpose:** Eliminate visual noise that doesn't add analytical value.

**How to Remove:**

1. Right-click on chart → **Format**
2. In Format pane, select **Lines** tab
3. Set all line types to **None:**

```
Format Lines Panel:
┌─────────────────────────┐
│ Grid Lines              │
│ ├─ Rows:      None     │
│ └─ Columns:   None     │
│                         │
│ Zero Lines              │
│ └─ All:       None     │
│                         │
│ Axis Rulers             │
│ └─ Tick Marks: None    │
│                         │
│ Reference Lines         │
│ └─ All:       None     │
└─────────────────────────┘
```

**Before vs After:**
```
BEFORE (Cluttered):          AFTER (Clean):
┌─────────────────┐          ┌─────────────────┐
│  │  │  │  │  │ │          │                 │
├──┼──┼──┼──┼──┼─┤          │      ╱╲         │
│──┼──┼──╱╲─┼──┼─│          │     ╱  ╲        │
│──┼──╱──┼─╲┼──┼─│          │    ╱    ╲       │
│──┼╱─┼──┼──┼╲─┼─│          │   ╱      ╲      │
├──┼──┼──┼──┼──┼─┤          │  ╱        ╲     │
│  │  │  │  │  │ │          └─────────────────┘
└─────────────────┘          Cleaner, focused
Distracting lines            on trend only
```

---

#### **🎨 Formatting Step 2: Clean Up Axes & Headers**

**Purpose:** Remove unnecessary labels and scales that don't enhance understanding.

##### **Remove or Simplify Axes:**

**For Sparklines:**
1. Right-click Y-axis → **Uncheck "Show Header"**
2. Right-click X-axis → **Uncheck "Show Header"**
   - Sparklines are meant to be compact, axis labels defeat purpose

**For BANs:**
- No axes needed - just display the number

**For Detailed Charts (when axes ARE needed):**
1. Format axis numbers:
   - Right-click axis → **Format**
   - Numbers → Currency or Number
   - Use abbreviations: `$#,##0K` instead of `$#,##0,000`
2. Remove axis titles if self-explanatory
3. Keep minimal tick marks only

##### **Simplify Headers:**

```
BEFORE:                      AFTER:
┌─────────────────────┐      ┌─────────────────────┐
│ SUM(Sales) by Month │      │ Monthly Sales       │
│ for Current Year... │      │                     │
└─────────────────────┘      └─────────────────────┘

Remove technical jargon      Use business language
```

**How to Edit:**
1. Double-click chart title
2. Replace with clear, concise business-friendly title
3. Or right-click title → **Hide** if obvious from context

---

#### **🎨 Formatting Step 3: Apply Color Scheme**

**Purpose:** Maintain brand consistency and use color strategically to highlight insights.

##### **Color Application Strategy:**

**Base Color Palette (from Step 1):**
- Primary: `#ff5500` (Orange - Current year, highlights, positive)
- Secondary: `#303030` (Dark Gray - Previous year, text, negative)
- Tertiary: `#b3b3b3` (Light Gray - Backgrounds, secondary elements)
- Text: `#303030` (Dark Gray)

##### **Applying Colors to Each Chart Type:**

**1. BANs (KPI Cards):**
```
┌───────────────────────────────┐
│  Total Sales (#303030 text)   │
│                               │
│  $2,456,892 (#ff5500 - bold) │ ← Main metric
│  ↑ 12.5% (#ff5500)           │ ← Positive growth
│                               │
│  PY: $2,187,234 (#b3b3b3)    │ ← Previous year
└───────────────────────────────┘
```

**How to Apply:**
1. Click on text element → Format
2. Font color → Select color from palette
3. Add background shading if needed (subtle `#f5f5f5`)

---

**2. Line Charts (Trends):**
- Current Year line: `#ff5500` (thick, prominent)
- Previous Year line: `#b3b3b3` (thin, subdued)
- Reference lines (avg): `#303030` (dashed)

**How to Apply:**
1. Click on line mark → Color
2. Select color, adjust opacity if needed
3. Adjust line thickness in Size property

---

**3. Bar Charts (Comparisons):**
- Current Year bars: `#ff5500`
- Previous Year bars: `#303030` or `#b3b3b3`
- Alternating transparency for layered bars

---

**4. Highlights & Annotations:**
- Key insights: `#ff5500` (attention-grabbing)
- Min/Max points: Contrasting colors with larger markers
- Text annotations: `#303030`

##### **Color Testing Checklist:**
```
□ Colors align with brand guidelines
□ Sufficient contrast for readability
□ Consistent color meaning across all charts
□ Color blind friendly (test with simulator)
□ Not too many colors (max 4 as per guidelines)
```

---

#### **🎨 Formatting Step 4: Design Effective Tooltips**

**Purpose:** Provide contextual information on hover without cluttering the visual.

##### **Tooltip Best Practices:**

**Default Tooltip (❌ Avoid):**
```
┌─────────────────────────────┐
│ Order Date: January 2024    │
│ SUM(CY Sales): 185234.567   │
│ SUM(PY Sales): 165890.234   │
│ YEAR(Order Date): 2024      │
└─────────────────────────────┘
Too technical, unformatted
```

**Optimized Tooltip (✅ Use This):**
```
┌─────────────────────────────┐
│ 📅 January 2024             │
│                             │
│ Sales: $185,235             │
│ Previous Year: $165,890     │
│ Growth: +11.7% ↑            │
└─────────────────────────────┘
Clean, formatted, insightful
```

##### **How to Customize Tooltips:**

1. Click on worksheet → **Tooltip** in Marks card
2. Edit tooltip text using Insert menu:

**Example Tooltip Code:**
```html
<b>📅 <MONTH(Order Date)> <YEAR(Order Date)></b>

Current Year Sales: <b><SUM(CY Sales)></b>
Previous Year Sales: <SUM(PY Sales)>

Year-over-Year Change: <YoY Sales % Diff>
```

3. Format embedded fields:
   - Right-click field in tooltip editor → **Format**
   - Set number format, font style, color

**Tooltip Formatting Options:**
```
┌─────────────────────────────────┐
│ Font: Arial, 11pt               │
│ Bold: For emphasis              │
│ Color: Match chart colors       │
│ Emojis: ✓ Use sparingly        │
│ Line breaks: For readability    │
│ Dynamic content: Filter-aware   │
└─────────────────────────────────┘
```

##### **Advanced Tooltip Features:**

**Viz in Tooltip (Optional):**
- Show related chart on hover
- Example: Hover over category → see subcategory breakdown
- Keep it simple to avoid overwhelming users

**Conditional Formatting in Tooltips:**
```
Growth: <IF YoY % > 0 THEN "↑" ELSE "↓" END> <YoY Sales % Diff>
```

---

### 📋 Step 3 Completion Checklist

```
✅ Calculated Fields Created
   └─ ✓ Parameter: Select Year
   └─ ✓ CY Sales (Current Year)
   └─ ✓ PY Sales (Previous Year)
   └─ ✓ YoY % Difference
   └─ ✓ Max Sales Month (tested)
   └─ ✓ Min Sales Month (tested)

✅ Charts Built
   └─ ✓ BANs: Total Sales, Profit, Quantity
   └─ ✓ Sparkline: Monthly trends with min/max highlights

✅ Formatting Applied
   └─ ✓ Grid lines removed
   └─ ✓ Axes and headers cleaned/hidden
   └─ ✓ Brand colors applied consistently
   └─ ✓ Tooltips customized and formatted
   └─ ✓ Minimalist design principles followed
```

---

### 🎓 Skills Demonstrated in Step 3

- ✅ **Tableau Calculated Fields:** Creating complex formulas with IF, YEAR, WINDOW functions
- ✅ **Parameter Creation:** Enabling dynamic user interaction
- ✅ **Year-over-Year Analysis:** Calculating growth metrics and trends
- ✅ **Table Calculations:** Using WINDOW_MAX and WINDOW_MIN for extrema identification
- ✅ **Testing Methodology:** Validating calculations before production deployment
- ✅ **Visual Design:** Applying minimalist principles and brand guidelines
- ✅ **Data Storytelling:** Using color and formatting to highlight insights
- ✅ **User Experience:** Creating informative, clean tooltips

---

### 💡 Pro Tips for Chart Building

```
🎯 Always Test First
   Create separate test sheets for complex calculations
   Validate logic before applying to main visualizations

🎯 Use Consistent Naming
   Prefix calculated fields: CY_, PY_, YoY_
   Makes formulas easier to read and maintain

🎯 Comment Complex Calculations
   Add // comments in calculated field editor
   Helps future you and team members understand logic

🎯 Save Formatting as Default
   Right-click formatted element → Set as Default
   Applies to all new worksheets automatically

🎯 Create a Style Guide Sheet
   Build a reference sheet with all brand colors
   Copy formatting quickly with Format Painter

🎯 Use Aliases for Clean Display
   Right-click field → Aliases
   Show "Q1 2024" instead of technical values
```

---

### ⚠️ Common Mistakes to Avoid

| Mistake | Problem | Solution |
|---------|---------|----------|
| **Not Testing Calculations** | Errors go unnoticed in production | Always create test sheets first |
| **Too Many Colors** | Visual chaos, hard to interpret | Stick to 4-color palette maximum |
| **Cluttered Charts** | Distracting gridlines and labels | Remove all non-essential elements |
| **Generic Tooltips** | Technical jargon confuses users | Write business-friendly descriptions |
| **Inconsistent Formatting** | Unprofessional appearance | Apply formatting standards to all charts |
| **Skipping Mobile View** | Poor experience on smaller screens | Test responsive design |

---

### 🔄 Formatting Workflow Summary

```
1. BUILD
   └─ Create calculated fields
   └─ Test on separate sheet
   └─ Build visualization

2. CLEAN
   └─ Remove gridlines
   └─ Hide/simplify axes
   └─ Remove headers if obvious

3. COLOR
   └─ Apply brand palette
   └─ Maintain consistency
   └─ Use color purposefully

4. TOOLTIP
   └─ Write clear descriptions
   └─ Format numbers properly
   └─ Add relevant context

5. REVIEW
   └─ Check all formatting
   └─ Test interactivity
   └─ Validate calculations
```

---

> **Next Step:** [Step 4: Build Dashboards](#step-4-build-dashboards)  
> With formatted charts ready, we'll assemble them into cohesive, interactive dashboards.

---

*Document Status: Step 3 Complete ✓*  
*Last Updated: November 26, 2025*
