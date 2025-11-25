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

*Document Status: Step 1 Complete ✓*  
*Last Updated: November 25, 2025*
