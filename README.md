# Washington EV Market Overview

An executive Tableau dashboard analyzing Washington State electric vehicle registrations by county, manufacturer, vehicle type, and model year.

The project was designed as a self-service analytical product that helps users quickly understand market concentration, manufacturer leadership, fleet composition, and data-quality limitations.

> **Live dashboard:** [View on Tableau Public](https://public.tableau.com/app/profile/david.edmonds5066/viz/WashingtonEVMarketOverview/Dashboard1#1)  
> **Portfolio case study:** [View portfolio project](https://davidedmonds-portfolio-f46ac7.webflow.io/) (Will be replaced with Case study link on site)

## Dashboard Preview

![Washington EV Market Overview](Images/Washington_EV_Market_Overview.png)

## Business Challenge

The source data contains detailed vehicle-level registration records, but the raw file does not provide a fast way to answer leadership questions such as:

- Where are registered EVs concentrated across Washington?
- Which manufacturers hold the strongest market position?
- How does the registered fleet vary by vehicle type and model year?
- Which data-quality issues could distort executive reporting?

The objective was to turn the public dataset into a clear, interactive dashboard that supports both statewide monitoring and focused exploration.

## Analytical Approach

The project followed a consulting-oriented workflow:

1. **Diagnose** - Reviewed the dataset structure, field completeness, and reporting risks.
2. **Govern** - Defined KPI logic and established rules for missing or placeholder values.
3. **Design** - Built an executive layout centered on KPIs, geography, manufacturer rankings, and model-year distribution.
4. **Validate** - Tested calculations, filters, set actions, and dashboard interactions across multiple selections.

## Dashboard Capabilities

- Dynamic KPI cards for total EVs, average reported range, top make, and top county
- County-level geographic analysis with exact totals available in tooltips
- Context-aware Top 10 manufacturer ranking
- Dynamic highlighting of the leading manufacturer
- Model-year selection that labels the selected year and returns to the peak year when cleared
- Collapsible filter panel for county, make, vehicle type, and model year
- Cross-filtering between the dashboard's visual components

## Data Preparation and Quality Controls

### Reported electric range

Missing and zero electric-range values were excluded only from the **Average Reported Range** metric. They were not removed from total vehicle counts, county analysis, manufacturer rankings, or model-year analysis.

### Model-year interpretation

The dataset describes the model year of currently registered vehicles. It does not represent the calendar year in which each vehicle was registered. The dashboard wording was designed to prevent that common misinterpretation.

### Geographic color scaling

The county distribution is highly skewed because the leading county has a substantially larger registered EV population than most others. A transformed color scale improves visual separation among lower-volume counties while the tooltip continues to display the actual registration count.

## Key Findings

- EV registrations are concentrated in Washington's largest population centers, with King County leading the state.
- Tesla maintains the strongest manufacturer position, while the remaining market is distributed across several competing brands.
- The registered fleet is concentrated in newer model years, although the newest model-year totals may be incomplete.
- Missing and placeholder electric-range values can materially distort the reported average when they are not handled separately.

## Strategic Recommendations

- Prioritize high-volume counties when evaluating near-term charging infrastructure and service demand.
- Add population-adjusted measures to compare adoption intensity rather than only total registrations.
- Separate battery electric and plug-in hybrid vehicles when analyzing charging requirements.
- Integrate historical registration extracts to measure actual adoption growth over time.
- Compare vehicle concentration with charging-station availability to identify potential infrastructure gaps.

## Tools and Techniques

- Tableau
- Data validation and cleansing
- KPI definition and governance
- Calculated fields and table calculations
- Top-N sets and context filters
- Set actions and dashboard filter actions
- Geographic analysis
- Dynamic labels and conditional formatting
- Executive dashboard design

## Limitations

- The dataset reflects available current registration records rather than a complete historical adoption timeline.
- Model year should not be interpreted as registration year.
- Reported electric range is unavailable for some vehicles.
- County totals are not adjusted for population.
- Newer model-year records may be incomplete.

## Repository Contents

```text
.
├── README.md
├── Electric_Vehicle_Population_Data.csv
├── Dashboards/
│   ├── Washington_EV_Market_Overview.twbx
│   └── EV_Data_Analytics.pbix
├── Images/
│   └── Washington_EV_Market_Overview.png
└── Documentation/
    └── Washington_EV_Market_Overview_Case_Study.pdf
```

## Data Source

Washington State Department of Licensing, **Electric Vehicle Population Data**:  
https://data.wa.gov/Transportation/Electric-Vehicle-Population-Data/f6w7-q2d2

## About the Analyst

**David Edmonds**  
Senior Data Analyst and Business Intelligence Professional  
[LinkedIn](https://www.linkedin.com/in/david-c-edmonds/)
