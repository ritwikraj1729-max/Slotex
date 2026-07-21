# ⏱️ Slotex

**Slotex** is a premium, distraction‑free study slot planner built with pure HTML, CSS, and JavaScript. It helps you structure your day by creating timed study/work slots, managing tasks inside each slot, and tracking your progress — all wrapped in a beautiful glass‑morphism interface.

---

## ✨ What it does

- **Create Slots** – Add unlimited study slots with a name, start/end time, productivity level (High/Medium/Low), subject, and optional notes.
- **Manage Tasks** – Inside each slot, add unlimited tasks. Mark them complete, edit names, or delete them. Progress bars update automatically.
- **Dashboard** – At a glance, see today's slots, completed/remaining tasks, total study time, and focus score.
- **Current Slot Highlight** – The timeline automatically highlights the slot that matches the current time with a "Now" badge.
- **Dark / Light Theme** – Toggle between themes; your preference is saved.
- **Export / Import** – Backup your entire planner as a JSON file, or restore it later.
- **Auto‑Save** – All changes are saved to localStorage instantly. Close the app and come back — your data is still there.
- **Responsive** – Works beautifully on desktop, tablet, and mobile.

---

## 🛠️ Tech Stack

- **HTML5** – semantic structure
- **CSS3** – custom properties, glass‑morphism, animations, responsive layout
- **Vanilla JavaScript (ES6)** – modular, clean, and well‑commented

No frameworks, no libraries — just pure frontend code.

---

## 🚀 Getting Started

1. **Download or clone** this repository.
2. **Open `index.html`** in your browser (no server required).
3. Start by clicking the **＋** floating button to create your first study slot.
4. Add tasks, track your progress, and plan your day!

---

## 📂 Architecture

- **Slots** – each slot has an `id`, `name`, `date`, `startTime`, `endTime`, `productivity`, `subject`, `notes`, and `tasks[]`.
- **Tasks** – each task has an `id`, `name`, `completed` flag, `priority`, and optional `notes`.
- **localStorage** – all data is serialized to JSON and stored under the key `studyPlannerData`.
- **Rendering** – the timeline updates reactively after every change; the dashboard stats recalculate automatically.
- **Current Slot Detection** – `getCurrentSlot()` compares the current time against each slot's start/end times for today.

---

## 🎨 Customization

You can easily adjust the look and feel by editing the CSS variables in the `:root` section inside `index.html`:

```css
--bg-primary: #f0f4ff;
--accent-1: #6c5ce7;
--accent-2: #00b894;
--font: 'Inter', ...;
--radius-md: 18px;
