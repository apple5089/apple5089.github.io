# Daily Work Plan Memo

A zero-dependency, pure frontend daily work plan management tool that supports drag-and-drop sorting, Excel import and export, and offline use.

## 🚀 Quick Start

1. Simply open the `index.html` file to use it
2. No need to install any software or dependencies
3. Support offline usage, with data saved in the browser's local storage

## 📋 Functional Features

### Core functions
- **Weekly View Management**: Monday through Sunday, with three time slots: morning, afternoon, and evening
- **Task lifecycle**: creation, editing, completion, deletion, and drag-and-drop sorting
- **Recurring Tasks**: Supports single occurrence, daily, and weekly recurrence types, with intelligent scheduling
- **Local storage**: Automatically saved, no loss upon page refresh
- **CSV Import and Export**: Supports the .csv format, including information on recurring tasks

### Interactive operation
- **Drag and sort**: Tasks can be sorted up or down within the same time slot
- **Drag and drop scheduling**: Drag tasks from the task pool to specific time slots
- **Double-click to edit**: Click on the task card to edit its details
- **Keyboard shortcuts**:
  - `Ctrl+N`: New task
  - `Ctrl+S`: Manual save
  - `Ctrl+E`: Export to Excel

## 🎯 User Guide

### Create Task
1. **Method 1**: Click the "+" button in the task pool, create a task, and then drag it to the designated time slot
2. **Method 2**: Click the "+" button in any time slot cell to directly create to that time slot
3. **Method 3**: Double-click on an empty area to create a task

### Task Management
- **Completed**: Click the checkbox before the task
- **Edit**: Click anywhere on the task card (excluding the checkbox and delete button)
- **Delete**: Click the × button in the top right corner of the task
- **Move**: Drag and drop tasks to any time slot or task pool

### Excel import and export

#### Export to CSV
1. Click the "📊 CSV Export" button at the top
2. The file will be downloaded automatically in the format of `weekly_plan_YYYY-MM-DD.csv`
3. Include all task information: week, time slot, title, time, priority, completion status, remarks, recurrence type, selected week

#### Import CSV
1. Click the "📥 CSV Import" button at the top
2. Select CSV file for uploading
3. Confirm the import after previewing the number of tasks
4. Importing will overwrite all current tasks, and support the identification and restoration of duplicate tasks

#### CSV Template Format

| Column Name | Description | Example |
|------|------|------|
| Column A - Day | Monday to Sunday | Monday |
| Column B - Time Period | Morning/Afternoon/Evening/Recurring Task | Morning |
| Column C - Task Title | Task Name | Project Meeting |
| Column D - Start Time | HH:mm format | 09:00 |
| Column E - End Time | HH:mm format | 10:00 |
| F column - Priority | High/Medium/Low | High |
| Column G - Completed or Not | Yes/No | No |
| Column H - Remarks | Task Details | Discuss Project Progress |
| Column I - Recurrence Type | Single/Daily/Weekly | Weekly |
| Column J - Selected Weeks | Comma-separated Weeks | Monday, Wednesday, Friday |

### Reuse of repeated tasks
- **Add Task**: Click the "+ Add Task" button and select the recurrence type (once/daily/weekly)
- **Weekly repetition**: When selecting "Weekly", you can specify the specific day of the week for execution
- **One-click Scheduling**: Click the "One-click Scheduling" button, and the system will intelligently allocate tasks to corresponding time slots based on task time and recurrence type
- **Priority Sorting**: When scheduling with one click, high-priority tasks will be arranged first

## 🎨 Theme Settings

Support three themes:
- **Light Theme**: The default theme, suitable for daily use
- **Dark Theme**: Eye-protection mode, suitable for night use
- **Eye-friendly green theme**: Green color scheme, providing greater comfort for prolonged use

## 📱 Mobile adaptation

- **Responsive design**: Automatically adapts to different screen sizes
- **Mobile gestures**: Task cards can be swiped left or right to complete or delete them
- **Floating Button**: Display the sidebar toggle button on mobile devices

## 💾 Data Storage

- **Local storage**: All data is saved in the browser's localStorage
- **Auto Save**: Automatically save after each operation
- **Manual save**: Press Ctrl+S or click the relevant button
- **Clear Data**: Click "Clear This Week" to reset all tasks

## 🔧 Technical Features

- **Zero dependencies**: Implemented purely with HTML/CSS/JavaScript
- **Single file**: All functions are integrated into index.html
- **Offline usage**: Supports PWA, can be added to the home screen
- **Compatibility**: Supports Chrome 88+、Edge 88+、Safari 14+
- **File size**: < 500KB

## 📊 Data Model

```json
{
  "id": "Unique identifier for the task",
  "title": "Task Title",
  "start": "Start time (HH:mm)",
  "end": "End time (HH:mm)",
  "priority": 1|2|3,
  "done": true|false,
  "doneAt": "Completion timestamp",
  "weekday": 1-7,
  "slot": "AM|PM|EVENING|POOL",
  "note": "Task Notes"
}
```

## 🚨 Precautions

1. **Data backup**: It is recommended to regularly export Excel files to back up important data
2. **Browser Compatibility**: It is recommended to use a modern browser for the best experience
3. **Privacy Protection**: All data is stored locally and will not be uploaded to the server
4. **Storage Limit**: The browser localStorage has a storage limit (usually 5-10MB)

## 🆘 Common Issues

**Q: Will the data be lost? **
A: The data is saved in the browser's local storage, and it will be retained unless the browser data is cleared or the app is uninstalled.

**Q: How do I migrate to another device? **
A: Use the export function in Excel and import it on the new device.

**Q: Does it support multi-person collaboration? **
A: Currently, it is a standalone version and does not support multiplayer collaboration. Tasks can be shared through Excel files.

**Q: How to reset all data? **
A: Click the "Clear This Week" button, or clear the 'weeklyTasks' data in the browser's localStorage.

## 📞 Contact Support

If you have any questions or suggestions, please contact us through the following ways:
- Submit an issue to the project repository
- Send an email for feedback

---

**Version**: v1.0.0
**Updated Date**: 2024
**License**: MIT
