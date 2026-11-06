
# PantryPulse
### Know where hunger is heading before the line forms.

**AI-Powered Food Bank Demand Forecasting & Resource Planning**

Developed by **Team Impact Trio | Impact Hackathon 2026**

## Overview

Food banks often rely on historical visits and manual estimates to plan volunteer shifts, food inventory, and community outreach. When demand unexpectedly increases, resources may already be stretched.

**PantryPulse** is an AI-powered decision-support application designed to help food banks anticipate demand and plan resources proactively.

It combines machine learning forecasting, economic indicators, capacity analysis, and AI-generated recommendations to help food banks prepare for the next **8 weeks**.

## Key Features

### 1. Eight-Week Demand Forecasting
- Uses Meta's Prophet forecasting model.
- Predicts weekly household visits with uncertainty intervals.
- Incorporates seasonality, school breaks, SNAP trends, and economic indicators.
- Provides county-level forecasts for 13 North Texas Food Bank counties.

### 2. Resource Capacity Planning
- Compares forecast demand against available volunteer shifts and food inventory.
- Identifies whether volunteers or food are the limiting resource.
- Estimates additional shifts, pounds of food, meals, and funding requirements.
- Supports interactive capacity adjustments.

### 3. AI-Powered Action Planning
- Integrates Anthropic Claude for operational recommendations.
- Prioritizes resource gaps and suggests actions.
- Generates draft volunteer and donor outreach messages.
- Keeps humans responsible for approving recommendations.

### 4. Economic Intelligence
- Integrates economic indicators through the FRED API.
- Uses unemployment and grocery price trends to inform demand forecasting.
- Supports broader economic context for planning.

### 5. Community Reach Analysis
- Compares food insecurity estimates with simulated pantry visits.
- Highlights counties where community need may exceed current service reach.
- Supports targeted outreach and mobile pantry planning.

## How PantryPulse Works

1. **Data Collection:** Combine county food insecurity estimates, USDA SNAP data, and economic indicators.
2. **Demand Forecasting:** Use Prophet to estimate household visits over the next eight weeks.
3. **Capacity Assessment:** Compare expected demand with volunteer and food capacity.
4. **Resource Gap Analysis:** Calculate additional shifts, food, meals, and estimated funding needs.
5. **AI Recommendations:** Generate prioritized operational actions using Claude.
6. **Human Approval:** Review and approve proposed actions before implementation.

## Technology Stack

| Component | Technology |
|---|---|
| Programming | Python |
| Application Interface | Streamlit |
| Forecasting | Prophet |
| AI Strategist | Anthropic Claude API |
| Economic Data | FRED API |
| Data Processing | Pandas, NumPy |
| Visualization | Plotly |

## Data Sources

PantryPulse combines public datasets with simulated operational data.

**Public Data**
- Feeding America — Map the Meal Gap, county-level food insecurity estimates.
- USDA Food and Nutrition Service — SNAP participation trends.
- Federal Reserve Economic Data (FRED) — unemployment and economic indicators.

**Simulated Data**
- Weekly food pantry visits.
- Available volunteer shifts.
- Food inventory and operational capacity.

**Important:** The current prototype uses simulated pantry visit histories and capacity assumptions. Forecast accuracy measured on simulated visits should not be interpreted as validated performance on real food bank operations.

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/RatikaNankani/Pantry-Pulse.git
cd Pantry-Pulse
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure API Keys

The application may require credentials for Anthropic Claude and FRED integrations.

Keep API credentials in local environment variables or Streamlit secrets. Never commit private API keys to GitHub.

### 4. Launch the Application

```bash
streamlit run app.py
```

The application should open in your browser.

Some features may require API credentials, additional source datasets, or an internet connection.

## Project Documentation

Detailed technical documentation is available in the [`docs/`](docs/) folder.

- [System Architecture](docs/ARCHITECTURE.md)
- [Data Sources](docs/DATA.md)
- [Forecasting Model](docs/FORECAST_MODEL.md)
- [Capacity and Alerts](docs/CAPACITY_AND_ALERTS.md)
- [Dashboard](docs/DASHBOARD.md)
- [AI Strategist](docs/AI_STRATEGIST.md)
- [FRED Economic Data](docs/FRED_ECONOMIC_DATA.md)
- [Setup and Troubleshooting](docs/SETUP_AND_TROUBLESHOOTING.md)
- [Limitations and Roadmap](docs/LIMITATIONS_AND_ROADMAP.md)

## Limitations and Future Improvements

- Replace simulated visit data with actual food bank operational records.
- Validate forecasting performance using real-world historical demand.
- Integrate food donation forecasting.
- Pilot the system with a North Texas food bank.
- Expand operational planning capabilities.


