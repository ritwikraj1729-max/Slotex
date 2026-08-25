# Slotex – Study Planner Web App

Slotex is a lightweight, self-contained single-page application for planning study sessions and managing tasks within time slots. It runs entirely in the browser, using local storage for persistence and requiring no backend.

## Features

- **Study slots**: Create, edit, and delete time-based study sessions (e.g., Mathematics, 08:00–10:00).
- **Tasks**: Add, check off, edit, delete, and drag-and-drop tasks between slots.
- **Productivity labels**: Mark slots as High, Medium, or Low productivity.
- **Dashboard**: Overview of today's slots, total tasks, completed/remaining tasks, focus score, and total study time.
- **Stats view**: Aggregate statistics, overall task completion progress bar.
- **Filters**: Filter slots by productivity level or completion status.
- **Dark / Light theme**: Toggle between themes; preference is saved.
- **Notifications**: Browser notifications for upcoming slots (within 10 minutes) and in-app toasts.
- **Import / Export JSON**: Backup or transfer your data.
- **Keyboard shortcuts**: `Ctrl/Cmd + N` to create a new slot, `Esc` to close modals.
- **Responsive design**: Works on desktop and mobile.

## How to Use

1. Open the HTML file in any modern web browser.
2. Use the **Add slot** button (or `Ctrl+N`) to create a study slot with a name, start/end time, productivity level, and optional notes.
3. Inside each slot card, add tasks using the input field. Check them off as you complete them.
4. Drag tasks between slots to reorganize.
5. Use the sidebar to switch between Dashboard, Stats, Settings, Import/Export.
6. Click the **Filter** button to filter slots by productivity or completion status.
7. Toggle dark/light mode from the sidebar or Settings.

## Data Storage

All data is stored in your browser's `localStorage` under the key `studyPlannerData`. No data is sent to any server.

## Technical Overview

- **Pure HTML/CSS/JavaScript** – no external dependencies.
- **State management**: Simple global `STATE` object holding slots and theme.
- **Rendering**: Dynamic DOM rendering on every state change.
- **Icons**: Inline SVGs, no emoji or external icon fonts.
- **Notifications**: Uses the Web Notifications API (permission requested on load).
- **Export/Import**: JSON file download/upload.

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + N` | Create new slot |
| `Esc` | Close modal / popover / mobile sidebar |

## File Structure

The entire application is contained in a single HTML file:

```
slotex.html
```

No build process or server required.

## Browser Compatibility

Works in all modern browsers (Chrome, Firefox, Safari, Edge) that support ES6 and localStorage.

## License

Free to use and modify for personal or educational purposes.
