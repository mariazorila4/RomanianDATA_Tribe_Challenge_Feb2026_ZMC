# RomanianDATA_Tribe_Challenge_Feb2026_ZMC


## Context

This project was developed for the #RomanianDATA Tribe Challenge. It's focused on *visualizing Romania's internal migration and population shifts in 2012-2025*.

## References

The initial report: [Check here to see the support report](https://cumstam.ro/grafice/875)

Data source link: [Click here](https://lnkd.in/dcDyN3SS)

> **Note:** I do not own any of the reports or datasets linked above.  
> Full credit goes to their respective developers and data providers.

## Project Overview

The analysis moves beyond a static "Traffic Light" design to a dynamic percentage change (%) model. This approach highlights the stark contrast between nationwide population decline and specific growth "magnets".

Key Insights:

- **The 50% Surge:** While most Romanian counties face significant demographic decline, Ilfov stands out as a unique outlier with a growth rate exceeding 50%.

- **Regional Magnets:** Major economic hubs like Cluj and Timiș show high resilience, attracting internal migration due to local career and lifestyle opportunities.

- **Suburbanization Trend:** The data reveals a clear migration pattern: people are not necessarily leaving the capital region but are relocating from Bucharest to the surrounding Ilfov area for a better quality of life.

## Technical Details

To achieve a high-fidelity "makeover" of the original dataset, the following technical steps were implemented:

- Data Source: Processed raw population data from INSSE (Tempo Online).

- DAX Measures: Developed custom measures to calculate the Percentage Change (%Change) relative to the 2012 baseline, ensuring accurate tracking across the 13-year timeline.
  
- DAX Formula: To calculate the population shift relative to the 2012 baseline, I used the following measure:

```dax
%Change = DIVIDE([Total Pop] - [Pop 2012], [Pop 2012], 0)
```

- Dynamic Titles: Implemented a DAX-driven title system that updates based on the selected county and year, providing instant context for the user.

- Advanced Conditional Formatting: Applied a custom Diverging Rule set (Red to Blue) to instantly distinguish between counties in decline and those experiencing growth.

- Dual-Map Visualization: Integrated a main country-wide map with a localized zoom inset for the Bucharest-Ilfov region to emphasize the suburbanization phenomenon.

## How to Use
To explore the demographic shifts within the dashboard, follow these steps:

1. **Select a Timeframe**: Use the **Timeline (Slicer)** on the left to select a specific year. The dashboard will automatically calculate the population change relative to the 2012 baseline.
2. **Interact with the Map**: Click on any county on the **Main Map** to filter the entire report. The KPI cards and the bar chart will update to show data specific to that region.
3. **Analyze Growth Hubs**: Observe the **Suburban Expansion** inset for a detailed look at the Bucharest-Ilfov area, or check the **Top Growth Leaders** chart to see which counties are resisting the national decline.
4. **Reset View**: To return to the national average, simply click on any empty space within the map or clear the selection in the slicer.


---

> **Author:** [Maria Cristina Zoriă](https://www.linkedin.com/in/maria-cristina-zoril%C4%83-42bb57232/).  
> **Event:** #RomanianDATA Tribe Challenge - Feb 2026

![Dashboard report 2025](https://github.com/mariazorila4/RomanianDATA_Tribe_Challenge_Feb2026_ZMC/blob/main/Dashboard_2025_report.png)
