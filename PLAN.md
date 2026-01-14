# Marketing Command Center

## Overview
An interactive, real-time dashboard for tracking marketing operations across three buckets (Production, Presence, Push) with team visibility, deadline tracking, and workload management.

**Live Dashboard:** https://nsn-aaron.github.io/mkt-command-center/marketing_dashboard.html

---

## The Dashboard

### Three Views

#### 1. Timeline View
**Swimlane Timeline + Capacity Heatmap**

**Timeline Section:**
- 3 horizontal swimlanes (Production, Presence, Push)
- 8-week timeline with week labels
- Tasks positioned by deadline
- Color coding: Red (deadline risk), Yellow (dependencies), Green (on track)
- Drag tasks horizontally to change deadlines
- Collision detection prevents overlap (max 3 rows per lane)
- Fixed 90px height for compact viewing

**Capacity Heatmap:**
- 4 rows for DRIs: Aaron, Ingrid, Shaun, Jarod
- 3 metrics: Total tasks, In Progress, At Risk
- Color-coded workload: Red (5+), Yellow (3-4), Green (1-2), Gray (0)
- Instant visibility of team balance

#### 2. Kanban View
**Workflow Management**

**Features:**
- 4 status columns: Backlog → In Progress → Review → Done
- Drag and drop cards between columns to change status
- Sort by: Priority, Deadline, Has Dependency
- Task count per column
- Bucket color-coded borders
- Delete button (trash icon) on each card

#### 3. DRI Dos View
**Personal To-Do Lists**

**Features:**
- 4 columns (one per DRI)
- Checkbox to mark tasks done/incomplete
- Drag tasks between DRIs to reassign
- Sort by: Priority, Deadline, Has Dependency
- Completed tasks shown with reduced opacity and strikethrough
- Task count: incomplete/total

---

## Interactive Features

### Drag and Drop
**Timeline:** Drag tasks horizontally to adjust deadlines - date auto-calculates from position
**Kanban:** Drag cards between status columns to change workflow stage
**DRI Dos:** Drag tasks between DRI columns to reassign ownership

### Sorting
**Kanban & DRI Dos:** Sort tasks by Priority (High→Low), Deadline (earliest first), or Has Dependency (Yes→No)

### Task Management
- **Click any task** to view/edit full details in modal
- **Checkbox (DRI Dos)** to quickly toggle done/incomplete
- **Delete button** (trash icon) to remove tasks
- **Add Task button** generates markdown to paste into `marketing_projects.md`

### Auto-Refresh
- Checks markdown file every 5 seconds for changes
- Auto-reloads all views when file updated
- No page refresh needed

---

## Data Source

### Markdown Format
Tasks stored in `marketing_projects.md` using this structure:

```markdown
## Production Bucket

### Category Name
- **Task**: Task description
- **Status**: In Progress
- **DRI**: Aaron
- **Priority**: High
- **Impact**: High
- **Deadline**: 2025-01-31
- **Dependency**: None
- **Notes**: Additional context

## Presence Bucket
...

## Push Bucket
...
```

### Task Fields
- **Task** - Task name/description
- **Status** - Backlog, In Progress, Review, Done
- **DRI** - Aaron, Ingrid, Shaun, Jarod
- **Priority** - High, Medium, Low
- **Impact** - High, Medium, Low
- **Deadline** - YYYY-MM-DD format
- **Dependency** - Task dependencies or "None"
- **Notes** - Free-form notes

---

## How to Use

### Viewing Tasks
1. Open: https://nsn-aaron.github.io/mkt-command-center/marketing_dashboard.html
2. Switch between Timeline, Kanban, DRI Dos views using top buttons
3. Click any task to see full details
4. Use sort dropdowns to organize tasks

### Making Changes (In Browser)
**Note:** Changes only persist in browser memory - they reset on page refresh. To save permanently, update the markdown file.

1. **Drag and drop** to change dates, status, or assignment
2. **Check boxes** to mark tasks complete
3. **Click tasks** to edit details
4. **Sort** to organize by priority, deadline, or dependencies

### Updating Data (Permanent)
1. Edit `marketing_projects.md` in your local repository
2. Make changes to any task field
3. Run: `git add marketing_projects.md`
4. Run: `git commit -m "Update tasks"`
5. Run: `git push origin main`
6. Dashboard auto-updates in 5-30 seconds

### Adding New Tasks
1. Click "+ Add Task" button
2. Fill out the form
3. Click "Generate Markdown"
4. Click "Copy to Clipboard"
5. Paste into `marketing_projects.md` under the correct bucket
6. Commit and push to Git

---

## Design

### Visual Theme
**Dark theme inspired by financial dashboards (Nansen)**

- Background: Deep blue-black (#0a0e14)
- Cards: Dark gray (#151a21)
- Accent: Teal/cyan (#00d4aa)
- Text: White and light gray
- Font: Inter (Google Fonts)

### Color Coding

**Buckets:**
- Production: Blue (#3b82f6)
- Presence: Purple (#8b5cf6)
- Push: Teal (#00d4aa)

**Deadline Risk:**
- Red: Overdue or at risk
- Yellow: Dependencies blocking
- Green: On track

**Workload:**
- Red: 5+ tasks (overloaded)
- Yellow: 3-4 tasks (busy)
- Green: 1-2 tasks (good)
- Gray: 0 tasks (available)

---

## Technology

### Stack
- **HTML/CSS/JavaScript** - Single self-contained file
- **No frameworks** - Pure vanilla JS
- **No database** - Markdown file as data source
- **GitHub Pages** - Free hosting with HTTPS
- **Git** - Version control

### Why This Approach?
- ✅ Simple - One HTML file
- ✅ Fast - No build process
- ✅ Portable - Works anywhere
- ✅ Free - Zero monthly costs
- ✅ Maintainable - All code visible
- ✅ Version controlled - Full history in Git

---

## Deployment

### GitHub Pages Hosting
**Repository:** https://github.com/nsn-aaron/mkt-command-center
**Live URL:** https://nsn-aaron.github.io/mkt-command-center/marketing_dashboard.html

### Update Process
1. Edit files locally
2. Commit changes: `git commit -m "message"`
3. Push to GitHub: `git push origin main`
4. GitHub Pages auto-deploys in 1-2 minutes

---

## Key Features Summary

✅ **Three specialized views** - Timeline, Kanban, DRI Dos
✅ **Drag and drop everywhere** - Change dates, status, assignment
✅ **Smart sorting** - Priority, deadline, dependencies
✅ **Auto-refresh** - Live updates every 5 seconds
✅ **Capacity visibility** - See team workload at a glance
✅ **Deadline tracking** - Color-coded urgency indicators
✅ **Collision detection** - No overlapping tasks in timeline
✅ **Quick actions** - Checkboxes, delete buttons, inline editing
✅ **Professional design** - Dark theme, smooth animations
✅ **Zero cost** - Free hosting on GitHub Pages

---

## Current Limitations

- **No persistence** - In-browser changes (drag/drop, checkboxes) reset on refresh
- **Manual updates** - Must edit markdown and push to Git to save permanently
- **No authentication** - Dashboard is public (anyone with URL can view)
- **No collaboration** - Team members must push/pull Git for updates
- **No history** - No audit log of changes

### Why These Limitations Exist
Browser security prevents JavaScript from writing files. To add persistence, would need:
- Backend server with GitHub API integration
- Authentication system
- Database to store changes

Current approach keeps everything simple and free while giving full control over data.

---

## Team Benefits

- **Transparency** - Everyone sees the same data in real-time
- **Accountability** - DRI ownership clearly visible
- **Planning** - Timeline shows what's happening when
- **Workload Balance** - Capacity heatmap prevents overload
- **Flexibility** - Three views for different use cases
- **Speed** - Quick actions (drag/drop, checkboxes) for fast updates
- **Visibility** - At-a-glance status across all marketing operations

---

*Last Updated: 2026-01-14*
