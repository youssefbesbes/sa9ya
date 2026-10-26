# Sa9ya 💧

> **Your water engineer on WhatsApp, in Tunisian Darija.**
> Built at an IEEE ISI Student Branch × IEEE SIGHT event.

A farmer sends a **voice note in Darija** on WhatsApp. Sa9ya replies with a **voice message** telling him exactly how much to water this week, based on live weather and his farm profile. No new app, no reading, no typing.

## The problem

- Tunisia uses **133%** of its renewable water, and **34,000 of its 50,000** deep wells are illegal.
- Farming uses **77%** of all water, and **more than half** is lost in irrigation.
- **2024** was the hottest year since 1950 (+1.6°C). In Sfax, the Chaâl olive farm fell from **695 to under 150 kg** of oil per hectare.

The farmer isn't the bad guy. He just has no simple tool that tells him how much to water.

## How it works

```
🎙️ Voice note ──► 📝 Speech-to-text ──► 🌦️ Live weather ──► 🤖 AI advisor ──► 🔊 Voice reply ──► 📊 Dashboard
   (WhatsApp)        (Whisper)          (Open-Meteo)        (Claude)          (TTS, Darija)     (anonymous)
```

1. **Voice note:** the farmer records a question in Darija on WhatsApp.
2. **Speech-to-text:** Whisper transcribes it.
3. **Live weather:** Open-Meteo provides temperature, rain and evapotranspiration for the farmer's town.
4. **AI advisor:** Claude combines the weather with the farm profile and FAO evapotranspiration methods to compute liters per tree for the week.
5. **Voice reply:** text-to-speech sends a Darija voice note back, plus a short text.
6. **Data dashboard:** every answer is logged anonymously to map water use by region.

See [`docs/architecture.md`](docs/architecture.md) for details.

## Who it's for

| | |
|---|---|
| **Users** | Small and medium olive and vegetable farmers in Sfax, Sousse, Monastir and Mahdia |
| **Paying customers** | Farmers (Pro plan) and data buyers: exporters, mills, insurers, banks (with farmer consent) |
| **Beneficiaries** | Everyone who shares the aquifer, and the climate |

## Business model

| Stream | Description |
|---|---|
| **Free** | Basic watering advice for every farmer |
| **Pro** | 5 DT / month *(estimate, to be tested)* |
| **Exporters** | Verified farm data for EU traceability requirements |
| **Insurers** | Weather and farm data to build affordable drought insurance |
| **Banks** | Data supporting green loans for drip irrigation |
| **Government & NGOs** | Paid anonymous water-use reports |

More in [`docs/business-model.md`](docs/business-model.md).

## Impact & measurement

We measure instead of just naming SDGs (6, 13, 2). Each week the bot asks *"how many hours did you pump?"*, so water saved is tracked as before vs. after.

**KPIs:** m³ of water per hectare · pumping hours · kg of oil per hectare · active farmers

> ⚠️ Water-saving percentages are **not proven yet**; they will be measured during the pilot. Reach figures below are **targets, not results**.

## Roadmap

| Phase | Timing | Goal |
|---|---|---|
| 1 | Now | Prototype: WhatsApp voice bot in Darija + live weather |
| 2 | 3 months | Pilot with 100 olive farmers in Sfax through a farmer group (GDA) |
| 3 | 1 year | 1,000 farmers in the Sahel, Pro plan, first exporter deal |
| 4 | 2–3 years | All of Tunisia, insurers and banks, then Algeria and Morocco |

## Why Sa9ya

| | Sa9ya | Seabex | SMS projects (ICT2Scale) |
|---|---|---|---|
| Channel | WhatsApp voice | Dashboard | SMS |
| Language | Darija | French / English | Text |
| Two-way | ✅ | ✅ | ❌ |
| Built for | Small farmers | Larger farms | Small farmers |
| Reading required | No | Yes | Yes |

## Repository contents

| Path | Contents |
|---|---|
| [`docs/`](docs/) | Architecture, business model, sources |
| [`pitch/`](pitch/) | Pitch deck (PDF to view on GitHub, PPTX original) |
| [`src/`](src/) | Prototype code |

## Team

- **Mohammed Bani** · [LinkedIn](#)
- **Koussay Ben Salem** · [LinkedIn](#)
- **Youssef Besbes** · [LinkedIn](#)

---

*Every drop counts, and now every farmer can count it, just by talking.*
