# Home-Assistant

This repository contains code and automations for [Home Assistant](https://www.home-assistant.io/), an open-source platform for smart home automation.

## 📂 Structure

- `Blueprints/`
  - `open_window_energy_ward.yaml` – A reusable automation blueprint for energy-saving window monitoring.

---

## 🪟 Open Window Energy Guard Blueprint

**Purpose:**  
This blueprint helps you save energy by monitoring a window sensor and taking action if a window is left open in a heated room. It sends tiered alerts and can automatically turn off heating if needed.

**Features:**
- **Level 1 Alert:** Notifies you after the window has been open for a set time.
- **Level 2 Alert:** Escalates if the window stays open longer or if the room temperature drops below the heating setpoint, and turns off the heating.
- **Window Closed Actions:** Optional actions when the window is closed again.

**Customizable:**  
You can set the alert times, temperature thresholds, and actions for each stage.

---

### Quick Add

[![Add to Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fadviest%2FHome-Assistant%2Fmain%2FBlueprints%2Fopen_window_energy_ward.yaml)

--- 

### Usage

1. Go to **Settings > Automations & Scenes > Blueprints** in Home Assistant.
2. Click the **"Import Blueprint"** button or use the button above.
3. Configure the blueprint with your window sensor, climate entity, and desired actions.

---

## License

This repository is for personal and community use with Home Assistant.

---