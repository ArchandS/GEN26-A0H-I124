# Genesis 2026: Ideathon

## GEN26-A0H-I124
### Team Details
#### **Team Name** IntelliHive <br/>
#### Team Members
|        Role      |         👤 Name          |   🎓 Roll Number     |   ⚧️ Gender   |   🏫 Department / Programme    |   🏠 Hosteller / Day Scholar   |
|:---------------:|:------------------------|:----------------------|:---------------:|:------------------------------:|:------------------------------:|
|   Team Leader   | Archand S                | CB.AI.U4QTS25007      |  MALE     |       AI                       | HOSTELLER  (KASYAPA BHAVANAM ANNEX)                    |
|    Member 2     | Kruthic Kumar N L        | CB.PS.I5DAS25014      |  MALE      |      IDAS                      | HOSTELLER (VASISHTA BHAVANAM)                       |
|    Member 3     | Pranav S                 | CB.PS.I5DAS25128      |  MALE     |       IDAS                 | DAY SCHOLAR                       |
|    Member 4     | Swetha T                 | CB.PS.I5DAS25136      |  FEMALE      |    IDAS              | HOSTELLER(MYTHREYI BHAVANAM)                       |

Amrita Vishwa Vidyapeetham, Coimbatore Campus

---

## Domain
Domain 4: Climate Action, Water & Environmental Resilience

## Idea: Urban Flood Guardian
**A rainfall and drainage based flood warning system for cities**

### Problem Statement
Rainfall forecasts tell us how much rain is coming, but not which street will drown, how deep, or when. Without a street-level warning, cities react only after the water rises, and the cost is paid in gridlock, damaged property and lives.

### Why This Matters
Floods in cities are very local. They depend on ground level, concrete surfaces and whether the drains can cope. Today these are not looked at together, so authorities and citizens get no clear early warning.

---

## Our Idea
Urban Flood Guardian predicts which streets will flood in the next **3 hours**, and tells people what to do about it.

1. **Rainfall forecast:** use radar rainfall data to predict rain for the next 0–3 hours.
2. **Water flow on streets:** work out how the rain runs over the ground and collects in low areas.
3. **Drain check:** treat the drains as a network (manholes and pipes) and find where they will overflow. The overflow water is added back onto the street.
4. **Smart learning:** a machine learning model learns from past floods to improve accuracy and explain why a street floods.
5. **Action:** show the result on a map, send alerts, and suggest safe routes.

**What it tells us for each street:** how deep the water will be (in cm), how risky it is, and how soon it becomes critical.

## Key Features
- Street-level flood depth forecast for the next 0–3 hours
- Links rainfall, streets and drain capacity in one view
- Explains why a street is at risk
- Web map with a time slider
- Alerts when water depth crosses a safe limit
- Flood-safe route suggestions for ambulances, buses and commuters

## How It Works
```
Rainfall data + Terrain + Drain maps
        → Rain flows over streets ⇄ Drains fill and overflow
        → Machine learning improves and explains the result
        → Flood depth (cm) + risk level + time to critical
        → Alerts · Safe routes · Map for authorities and citizens
```

## Proposed Tools
| Part | Tools |
|---|---|
| Rainfall forecasting | pySTEPS (radar-based) |
| Maps and terrain | QGIS, GDAL, GeoPandas, Rasterio |
| Drain network | NetworkX |
| Machine learning | XGBoost, SHAP |
| Database and backend | PostgreSQL + PostGIS, FastAPI |
| Map dashboard | React, MapLibre GL |
| Alerts | Firebase Cloud Messaging, SMS |

## Data We Plan to Use
- Radar rainfall and nowcasts (IMD)
- Terrain model (CartoDEM 30 m, finer data where available)
- Stormwater drain maps (Greater Chennai Corporation)
- Roads and land cover (OpenStreetMap)
- Past flood records (e.g. Chennai 2015, Cyclone Michaung 2023)

If some data is missing, we would start with simple assumed values and replace them with real data later.

## Who Benefits
- City corporations and disaster management teams
- Ambulance, fire and police teams
- Traffic police and transport operators
- Citizens, commuters and businesses in flood-prone areas

## Expected Outcome
- Early warnings before streets flood
- Safer routes for emergency vehicles and commuters
- Clear priority list of roads and drains that need attention
- Less damage to property and fewer lives at risk

## Next Steps
- Start with one flood-prone area in Chennai
- Compare the predictions with past flood events
- Expand to other areas after testing

## Team Contribution
| Member | Responsibility |
|---|---|
| Archand S | Flood prediction model and testing |
| Kruthic Kumar N L | Terrain, road and drain data |
| Pranav S | Database, alerts and routing |
| Swetha T | Map dashboard, research and presentation |

## References
- Yang, Y., Sun, L., Li, R., Yin, J., Yu, D. (2020). Linking a Storm Water Management Model to a Novel Two-Dimensional Model for Urban Pluvial Flood Modeling. *International Journal of Disaster Risk Science.*
- Farahmand, H., Xu, Y., Mostafavi, A. (2023). A spatial–temporal graph deep learning model for urban flood nowcasting leveraging heterogeneous community features. *Scientific Reports*, 13, 6768.
- Pulkkinen, S. et al. (2019). Pysteps: an open-source Python library for probabilistic precipitation nowcasting (v1.0). *Geoscientific Model Development*, 12(10), 4185–4219.
- Mugume, S. N., Adeke, D. P. (2025). Water level prediction in urban drainage systems using explainable deep learning models. 13th Urban Drainage Modelling Conference. DOI: 10.71573/m854dw13
