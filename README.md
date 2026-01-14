# Marketing Command Center 🚀

An interactive, real-time dashboard for tracking marketing operations across Production, Presence, and Push initiatives. Built with vanilla JavaScript and a sleek dark theme inspired by modern analytics platforms.

## 🌐 Live Dashboard

**[View Dashboard](https://nsn-aaron.github.io/mkt-command-center/marketing_dashboard.html)**

## ✨ Features

### Three Powerful Views

#### 🫧 Bubble Map
- Organic bubble chart visualization with intelligent collision detection
- Bubble sizes reflect task priority (High, Medium, Low)
- Color-coded by status with gradient effects
- Floating animations for visual engagement
- Group by bucket: Production, Presence, Push

#### 📋 Kanban Board
- Drag-and-drop task cards between status columns
- Five status stages: Backlog → Planning → In Progress → Review → Done
- Visual priority and deadline indicators
- Bucket color coding for quick identification
- Real-time task counts per column

#### 📅 Timeline View
- Chronological deadline tracking
- Visual urgency indicators (Overdue, Upcoming, Future)
- Days-until-deadline countdown
- Sortable by date and bucket
- Quick deadline scanning

### 🎨 Design

- **Dark Theme**: Professional crypto/finance aesthetic inspired by Nansen
- **Auto-Refresh**: Updates every 5 seconds when markdown file changes
- **Responsive**: Works on desktop, tablet, and mobile
- **Interactive**: Click any task to view full details
- **Smooth Animations**: Polished hover effects and transitions

### 📊 Task Management

Track these properties for each task:
- Task name
- Status (Backlog, Planning, In Progress, Review, Done)
- Owner
- Priority (High, Medium, Low)
- Deadline
- Dependencies
- Notes

## 🚀 Quick Start

### View the Dashboard

Simply visit the [live dashboard](https://nsn-aaron.github.io/mkt-command-center/marketing_dashboard.html) - no installation required!

### Update Tasks

1. Edit `marketing_projects.md`
2. Commit and push changes:
   ```bash
   git add marketing_projects.md
   git commit -m "Update tasks"
   git push
   ```
3. Dashboard auto-updates within 5 seconds

## 📝 Task Format

Tasks are organized in `marketing_projects.md` using this structure:

```markdown
## Production Bucket

### Category Name
- **Task**: Task description
- **Status**: In Progress
- **Owner**: [Team Member Name]
- **Priority**: High
- **Deadline**: 2025-01-31
- **Dependencies**: None
- **Notes**: Additional context

## Presence Bucket
...

## Push Bucket
...
```

### Available Statuses
- `Backlog` - Not yet started
- `Planning` - Being planned
- `In Progress` - Currently being worked on
- `Review` - Under review
- `Done` - Completed

### Priority Levels
- `High` - Large bubble (130px), red badge
- `Medium` - Medium bubble (100px), yellow badge
- `Low` - Small bubble (75px), gray badge

## 🛠 Technical Details

### Stack
- **Pure JavaScript** - No frameworks or dependencies
- **HTML5 & CSS3** - Modern web standards
- **Markdown** - Simple, version-controlled task storage

### Key Features
- Collision detection algorithm for bubble positioning
- Real-time markdown parsing
- File change detection via Last-Modified headers
- Drag-and-drop API for kanban functionality
- CSS animations for smooth interactions

### Browser Support
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)

## 🎨 Color Scheme

| Bucket | Color | Hex |
|--------|-------|-----|
| Production | Blue | #3b82f6 |
| Presence | Purple | #8b5cf6 |
| Push | Teal | #00d4aa |

### Status Colors
- **Backlog**: Gray gradient
- **Planning**: Blue gradient
- **In Progress**: Orange gradient
- **Review**: Purple gradient
- **Done**: Green gradient

## 📁 Project Structure

```
mkt-command-center/
├── marketing_dashboard.html    # Interactive dashboard
├── marketing_projects.md       # Task data source
├── nansen-dashboard.png        # Design reference
└── README.md                   # This file
```

## 🔄 Workflow

1. **Add Tasks** - Update `marketing_projects.md` with new tasks
2. **Commit** - Push changes to GitHub
3. **Auto-Update** - Dashboard refreshes automatically
4. **Track Progress** - Monitor tasks across three views
5. **Stay Aligned** - Team sees real-time updates

## 🤝 Contributing

To add new features or fix bugs:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally (use `python3 -m http.server 8000`)
5. Submit a pull request

## 📄 License

MIT License - feel free to use and modify for your needs.

## 🙏 Credits

Built with Claude Sonnet 4.5 for efficient marketing operations tracking.

---

**Need Help?** Open an issue or reach out to the team.

**Live Dashboard:** https://nsn-aaron.github.io/mkt-command-center/marketing_dashboard.html
