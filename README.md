# Piezometric Network of Catalonia — Groundwater Analysis

> **ACA Open Data · Time Series · Piezometric Trends · Folium Interactive Map**  
> Independent analysis using public data from the Catalan Water Agency (ACA)

---

## Project Description

This project analyzes **groundwater piezometric levels in Catalonia** using open data from the monitoring network of the Catalan Water Agency (ACA). The dataset is updated daily and contains historical measurements from dozens of piezometers distributed across the groundwater bodies of Catalonia's internal basins.

The analysis addresses specific water management questions:

- Are groundwater levels dropping in Catalonia?
- Which water bodies present the highest water stress?
- What is the typical seasonal cycle of Catalan aquifers?
- Where are the most concerning downward trends concentrated?

---

## Data Source

| Field | Detail |
|-------|---------|
| **Publisher** | Agència Catalana de l'Aigua (ACA) — Generalitat de Catalunya |
| **Dataset** | Nivell piezomètric de les aigües subterrànies de Catalunya |
| **Update Frequency** | Daily |
| **License** | Open Data Generalitat de Catalunya (CC BY 4.0) |
| **Direct URL** | `https://analisi.transparenciacatalunya.cat/api/views/6899-hrme/rows.csv` |

The data includes: station description, water body name, UTM coordinates, well depth, and piezometric level (meters above sea level).

---

## Analysis Performed

1. **Exploration and Cleaning** — temporal coverage, level distribution, active stations per water body.
2. **General Network Trend** — monthly evolution of the mean level with linear fit and uncertainty band.
3. **Trend per Station** — individual linear regression for each piezometer, classified into 5 categories.
4. **Time Series** — detailed visualization of stations with the highest historical coverage.
5. **Seasonality** — mean monthly anomaly to identify the annual recharge-discharge pattern.
6. **Interactive Map** — geospatial visualization with Folium, colored by trend and organized into interactive layers.

---

## Visualizations

![Exploratory Analysis](output/01_exploratorio.png)
*Temporal distribution, level statistics, and coverage by water body*

![General Trend](output/02_tendencia_general.png)
*Temporal evolution of the network with fitted linear trend*

![Trend Distribution](output/03_distribucion_tendencias.png)
*Individual trends per station and Top 10 water bodies*

![Time Series](output/04_series_temporales.png)
*Historical evolution of key stations*

![Seasonality](output/05_estacionalidad.png)
*Annual seasonal cycle of piezometric levels*

---

## Interactive Map

The analysis generates an interactive HTML map (`output/mapa_piezometrico_catalunya.html`) that allows you to:

- View the location of all ACA network piezometers
- Check the individual trend of each station (m/year)
- Filter and toggle layers between positive and negative trends independently using grouped clusters
- View full details by clicking on each point

**Color Legend:**
- 🔴 Severe Drop (< −0.5 m/year)
- 🟠 Moderate Drop (−0.5 to −0.1 m/year)
- 🟡 Stable (−0.1 to +0.1 m/year)
- 🟢 Moderate Rise (+0.1 to +0.5 m/year)
- 🔵 Significant Rise (> +0.5 m/year)

---

## Repository Structure
