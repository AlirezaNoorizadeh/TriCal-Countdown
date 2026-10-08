# TriCal Countdown ⏳

A modern, fully offline countdown tracker for birthdays, anniversaries, holidays, and recurring reminders. It supports **Jalali (Persian), Gregorian, and Hijri (Islamic)** calendars, comes with a Persian (RTL) interface, and runs from a single HTML file. All data stays on your device.

---
## 🖼️ Preview

| 1. Overview | 2. Add New Occasion | 3. Preset Occasions |
|:---:|:---:|:---:|
| ![Overview](./assets/preview-overview.jpg) | ![Add New Occasion](./assets/preview-add-occasion.jpg) | ![Preset Occasions](./assets/preview-presets.jpg) |

## 🚀 Getting Started

### Single File Structure
```
trical-countdown/
└── trical-countdown.html    # Complete standalone app (HTML+CSS+JS)
```

## Installation
### Running the App:

#### Option 1: Direct File Access (Simplest)
1. Double-click the HTML file in your file explorer
2. Opens directly in browser (file:// protocol)

#### Option 2: With Local Server (Recommended)
Use any local server method:
- VS Code Live Server
- Python http.server
- Node.js http-server

```bash
# Example with Python:
python -m http.server 8000
```
Then open: `http://localhost:8000/trical-countdown.html`

> **Note:** An internet connection is only needed to load the Vazirmatn font from Google Fonts. Without it, the app still works fully and falls back to the browser's default sans-serif font.

---

## 🌟 Core Features

### Countdowns
- ⏳ Days remaining until each occasion, sorted from nearest to farthest
- 🕐 Optional time of day, with an "hours and minutes left" display on the day itself
- 📊 Progress bar on every card showing how far along the current cycle is
- 🔥 Urgent highlight for occasions within the next 7 days
- 📁 Past one-time occasions are moved to a collapsible "Past occasions" section

### Calendars & Recurrence
- 📅 Three calendar systems: **Jalali**, **Gregorian**, and **Hijri**
- 🔁 One-time or recurring events with four frequencies:
  - **Yearly**: same date every year
  - **Monthly**: same day every month
  - **Weekly**: same weekday every week
  - **Daily**: every day
- 🔍 Expandable cards that preview upcoming occurrences of recurring events
- 🗓️ Smart handling of edge cases such as Feb 29 in non-leap years

### Preset Occasions
- 🎁 38 ready-made occasions you can add with one tap, in five categories:
  - Professions (e.g. Engineer, Programmer, Teacher, Nurse)
  - Family (e.g. Mother's Day, Father's Day)
  - National and ancient (Jalali), e.g. Nowruz, Yalda Night
  - Religious (Hijri), e.g. Eid al-Fitr, Eid al-Adha, Ashura
  - World (Gregorian), e.g. New Year, Christmas, Earth Day
- ✅ Already-added presets are marked so you never add duplicates

### Data Management
- 💾 Export all events to a JSON file (optionally including past events)
- 📥 Import events from a JSON file, with a preview of new, duplicate, and invalid entries before confirming
- ☑️ Multi-select mode with bulk delete
- 🧹 One-click full data reset, with confirmation

---

## 🛠️ Technical Implementation

### Architecture
- **Self-contained** single HTML file
- **Vanilla JavaScript** with no frameworks or dependencies
- **Modern CSS** with CSS variables for theming
- **Responsive design** for mobile/desktop
- **Built-in calendar conversion** between Jalali, Gregorian, and Hijri (tabular Islamic calendar), no external libraries
- **Custom dropdown components** for consistent look across browsers
- **Fault-tolerant rendering**: malformed events are flagged with a warning card and can be deleted instead of crashing the app

### Data Storage
- Events are saved in the browser's `localStorage` under the key `countdown_events_v2`
- Nothing is sent to any server
- Data is per browser and per device; use Export/Import to move it elsewhere

### Default Configuration
- Persian (RTL) interface
- Dark theme with gold and teal accents
- Jalali calendar selected by default
- Year pickers cover roughly 80 years back and 30 years ahead

---

## 🎮 How to Use

1. Tap **"Add new occasion"** to open the form
2. Enter a title, choose one-time or recurring, and pick a calendar and date
3. *(Optional)* Enable a specific time of day
4. Tap **"Add to list"** to see your countdown
5. Or tap **"Add from presets"** to add a built-in occasion instantly
6. Tap the ▾ arrow on a recurring card to see its upcoming dates
7. Use ✕ to delete a single event, or **"Multi-select"** to delete several at once

---

## ⚙️ Features Overview

Access via the buttons on the main screen:

- **Add new occasion**:
  - Title, recurrence type, calendar type, and date
  - "Today" shortcut for the date and "Now" shortcut for the time
  - Optional time of day

- **Add from presets**: Browse categorized occasions and add the variant you want (e.g. Iranian or international version)

- **Multi-select**: Select individual events or all of them, then delete in bulk

- **Export (JSON)**: Download a backup named `countdown-events.json`

- **Import file**: Load a previously exported JSON file; duplicates are skipped automatically

- **Full data reset**: Permanently erases all events from this device

---

## 🔮 Future Development

TriCal Countdown is just getting started. My plan is to grow it from a single HTML file into a proper mobile experience. Planned directions include:

- 📱 **Home screen widgets** on mobile, so your next occasions are visible without opening the app
- 📲 **Installable app**: making it installable on phones (for example as a Progressive Web App, and possibly native wrappers for Android and iOS)
- 🔔 **Notifications and reminders** before an occasion arrives
- 🌐 **Multi-language interface** (English UI alongside Persian)
- 🌓 **Light theme** and further customization options
- ☁️ **Optional backup and sync** while keeping privacy as a priority
- 📆 **More preset occasions** and community-contributed lists

These are goals, not promises, and the order may change as the project evolves. Ideas and suggestions are very welcome!

---

## 🤝 Contributing

Contributions are warmly welcome, and I'd be genuinely happy to see anyone help move the project forward, especially with the mobile widget and installable-app work described above.

Ways you can help:
- 💡 Suggest features or improvements by opening an issue
- 🐞 Report bugs, including wrong date conversions or holiday dates
- 🛠️ Submit a pull request for any item in the Future Development list
- 🌍 Help with translations or add new preset occasions
- 📝 Improve documentation

To get started:
1. Fork the repository
2. Create a branch for your change (`git checkout -b feature/your-feature`)
3. Commit your changes and push the branch
4. Open a pull request describing what you changed and why

If you're planning something big, such as the widget or native app work, please open an issue first so we can discuss the approach together.

---

## 📜 License [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This project is licensed under the MIT License.

---

## 🙏 Credits

Thanks to:
- Vazirmatn font for beautiful Persian typography
- Web standards communities for CSS/JS features
- Open source developers for inspiration

---

> TriCal Countdown: a complete, polished occasion countdown in a single portable HTML file, with multi-calendar support, recurring events, and full privacy.
