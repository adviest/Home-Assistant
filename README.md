# Home-Assistant

This repository contains code and automations for [Home Assistant](https://www.home-assistant.io/), an open-source platform for smart home automation.

## 📂 Structure

- `Blueprints/`
  - `open_window_energy_guard.yaml` – A reusable automation blueprint for energy-saving window monitoring.

---

## 🪟 Open Window Energy Ward Blueprint

**Purpose:**  
This blueprint helps you save energy by monitoring a window sensor and taking action when a window is left open in a heated room. It uses tiered alerts and can automatically turn off heating when a window is open and the room starts cooling. When the window closes, heating is restored only if the blueprint was the one that turned it off.

**Features:**
- **Level 1 Alert:** Notifies you after the window has been open for a set time.
- **Level 2 Alert:** Escalates after a longer open duration or if the room temperature drops by a configured amount since opening. At Level 2, the heating switch is automatically turned OFF.
- **Window Closed Actions:** Optional actions when the window is closed again, including smart heating restoration.
- **Temperature snapshot on open:** The blueprint records the temperature when the window opens and uses that as the baseline for the Level 2 temp drop trigger.
- **Smart suppression:** Alerts/actions only run if the configured heating switch is ON (avoids redundant notifications when heating is already off).
- **Heating restoration:** On window close, heating is turned back on only if the blueprint turned it off (and it's still off), preventing interference with manual user actions.

**Requirements:**
- A window binary sensor (open/closed)
- A temperature sensor
- A zone heating switch
- **An input_number helper** (per zone) to store the "temperature at open" snapshot (range -10 to 40, step 0.1)
- **An input_boolean helper** (per zone) to track if the blueprint turned off the heating

**Customizable:**  
You can set alert times, the temperature drop threshold, and the actions for each stage (Level 1, Level 2, and window-closed).
### Quick Add

[![Add to Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fadviest%2FHome-Assistant%2Fmain%2FBlueprints%2Fopen_window_energy_guard.yaml)

--- 

### Usage

1. Go to **Settings > Automations & Scenes > Blueprints** in Home Assistant.
2. Click the **"Import Blueprint"** button or use the button above.
3. Configure the blueprint with your window sensor, climate entity, and desired actions.

---

## License

This repository is for personal and community use with Home Assistant.

---