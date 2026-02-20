# Todo List App - Specification

## Project Overview
- **Project Name**: Todo List App
- **Type**: Single-page web application
- **Core Functionality**: A clean, interactive todo list application that allows users to add, complete, and delete tasks
- **Target Users**: Anyone needing a simple task management tool

## UI/UX Specification

### Layout Structure
- Single page application
- Centered card layout (max-width: 480px)
- Sections: Header, Input area, Todo list, Footer stats
- Responsive: Works on mobile (320px+) and desktop

### Visual Design

#### Color Palette
- **Background**: `#1a1a2e` (deep navy)
- **Card Background**: `#16213e` (dark blue)
- **Primary Accent**: `#e94560` (coral red)
- **Secondary Accent**: `#0f3460` (midnight blue)
- **Text Primary**: `#eaeaea` (off-white)
- **Text Secondary**: `#a0a0a0` (gray)
- **Success**: `#4ecca3` (mint green)
- **Danger**: `#ff6b6b` (soft red)

#### Typography
- **Font Family**: 'Poppins', sans-serif
- **Header**: 28px, font-weight: 600
- **Body**: 16px, font-weight: 400
- **Small**: 14px, font-weight: 300

#### Spacing
- Card padding: 32px
- Item spacing: 12px
- Border radius: 12px (card), 8px (inputs/buttons)

#### Visual Effects
- Box shadow on card: `0 8px 32px rgba(0, 0, 0, 0.3)`
- Hover transitions: 0.2s ease
- Strikethrough animation on complete
- Fade-in animation for new todos

### Components

#### Header
- App title "My Tasks"
- Subtitle showing pending tasks count

#### Input Area
- Text input field with placeholder "Add a new task..."
- Add button with "+" icon

#### Todo Item
- Checkbox (circle style) for completion
- Task text
- Delete button (trash icon) on hover
- States: default, completed (strikethrough + muted), hover

#### Footer Stats
- Shows "X of Y tasks completed"
- Progress bar showing completion percentage

## Functionality Specification

### Core Features
1. **Add Task**: Enter text and press Enter or click Add button
2. **Complete Task**: Click checkbox to toggle completion
3. **Delete Task**: Click delete button to remove task
4. **Persistence**: Store todos in localStorage
5. **Stats Display**: Real-time update of completed/total tasks

### User Interactions
- Pressing Enter in input adds the task
- Empty input shows subtle shake animation (validation)
- Completed tasks show strikethrough effect
- Delete button appears on task hover

### Data Handling
- Todos stored as JSON array in localStorage
- Each todo: { id: timestamp, text: string, completed: boolean }
- Auto-save on every change

### Edge Cases
- Empty task text: show validation, don't add
- Very long text: truncate with ellipsis
- No tasks: show "No tasks yet" message

## Acceptance Criteria
- [ ] App loads without errors
- [ ] Can add new tasks via input + button or Enter key
- [ ] Can mark tasks as complete/incomplete
- [ ] Can delete tasks
- [ ] Tasks persist after page refresh
- [ ] Stats update in real-time
- [ ] Responsive design works on mobile
- [ ] Visual effects (hover, animations) work smoothly
