# Architecture

## Pipeline

| Step | Component | Role |
|---|---|---|
| 1 | WhatsApp Business API | Receives the farmer's voice note |
| 2 | Whisper | Speech-to-text (Darija) |
| 3 | Open-Meteo | Live weather and evapotranspiration for the farmer's town |
| 4 | Claude | Combines weather + farm profile, computes liters per tree, writes the advice |
| 5 | Text-to-speech | Converts the advice into a Darija voice note |
| 6 | Dashboard | Stores anonymized answers to map water use by region |

## Agronomic basis

Irrigation needs are estimated with the **FAO evapotranspiration** approach: reference evapotranspiration from weather data, adjusted for crop type and growth stage, minus effective rainfall.

## Farm profile

Each farmer's profile holds the information needed for the calculation, such as location, crop, number of trees and irrigation method.

## Data & privacy

- Data is shared with third parties **only with farmer opt-in**.
- Dashboards and reports use **anonymized, aggregated** data.
- Farmers who opt in receive a benefit (for example, free Pro access).

## Running costs

AI and speech APIs (cents per message), WhatsApp Business API, servers, and two field agents during harvest season.
