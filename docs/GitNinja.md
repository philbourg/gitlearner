# Git Ninja - Interactive Git Learning Platform

## Project Overview

Git Ninja is an interactive web application designed to help developers learn Git commands through a gamified experience. The platform uses visual feedback and progressive challenges to make learning Git intuitive and engaging.

## Core Features

1. **Authentication System**

   - Firebase authentication
   - GitHub OAuth integration
   - User profile management
   - Progress tracking

2. **Interactive Learning System**

   - Real-time Git tree visualization using Mermaid.js
   - Command-line interface simulation
   - Progressive difficulty levels
   - Visual feedback for each command
   - Achievement/badge system

3. **Game Mechanics**
   - Level-based progression
   - Challenge completion tracking
   - Points/badges system
   - Visual progress indicators

## Technical Stack

- **Frontend Framework**: React + Vite
- **Styling**:
  - Tailwind CSS
  - shadcn/ui components
  - Retro gaming theme
- **Authentication/Database**: Firebase
- **Visualization**: Mermaid.js
- **State Management**: React hooks

## Project Structure

```
git-ninja/
├── src/
│   ├── components/
│   │   ├── GitVisualizer/
│   │   ├── CommandLine/
│   │   ├── Achievements/
│   │   └── Auth/
│   ├── hooks/
│   ├── context/
│   ├── pages/
│   └── utils/
└── firebase/
```

## Implementation Phases

### Phase 1: Project Setup

1. Initialize React + Vite project
2. Set up Tailwind CSS and shadcn/ui
3. Configure Firebase
4. Set up project structure
5. Install required dependencies:
   ```bash
   npm install firebase mermaid-js @shadcn/ui lucide-react
   ```

### Phase 2: Core Components

1. **Git Visualizer Component**

   - Implement Mermaid.js integration
   - Create git tree visualization
   - Add real-time updates

2. **Command Line Interface**

   - Create terminal-like interface
   - Implement command parsing
   - Add command history
   - Implement basic Git commands:
     - git init
     - git branch
     - git checkout
     - git commit
     - git merge

3. **Authentication System**
   - Implement Firebase auth
   - Create login/signup forms
   - Add GitHub OAuth
   - Create protected routes

### Phase 3: Game Mechanics

1. **Level System**

   ```javascript
   const levels = [
     {
       id: 1,
       title: "Git Basics",
       challenges: [
         {
           id: "init-repo",
           description: "Initialize your first repository",
           commands: ["git init"],
           hints: ["Use git init to create a new repository"],
         },
         // More challenges...
       ],
     },
     // More levels...
   ];
   ```

2. **Achievement System**
   - Define achievements/badges
   - Create progress tracking
   - Implement reward system

### Phase 4: User Interface

1. **Theme Implementation**

   - Apply retro gaming style
   - Create responsive layout
   - Add animations/transitions

2. **Components to Create**
   ```jsx
   // Main game components
   -LevelSelector -
     Challenge -
     CommandPrompt -
     GitVisualizer -
     AchievementPanel -
     UserProfile;
   ```

## Git Commands to Implement

```javascript
const supportedCommands = {
  init: "Create new repository",
  add: "Stage changes",
  commit: "Create commit",
  branch: "Create branch",
  checkout: "Switch branches",
  merge: "Merge branches",
  push: "Push changes",
  pull: "Pull changes",
  status: "Check status",
  log: "View history",
};
```

## Levels Structure

1. **Level 1: Basics**

   - Git initialization
   - Basic commits
   - Understanding staging

2. **Level 2: Branching**

   - Creating branches
   - Switching branches
   - Basic merging

3. **Level 3: Advanced**
   - Merge conflicts
   - Rebasing
   - Cherry picking

## Firebase Structure

```javascript
{
  "users": {
    "userId": {
      "profile": {
        "name": String,
        "email": String,
        "avatar": String
      },
      "progress": {
        "currentLevel": Number,
        "completedChallenges": Array,
        "achievements": Array
      }
    }
  },
  "levels": {
    "levelId": {
      "title": String,
      "description": String,
      "challenges": Array,
      "requiredCommands": Array
    }
  }
}
```

## Development Steps with Cursor IDE

1. Initialize project with Vite

   ```bash
   npm create vite@latest git-ninja -- --template react
   ```

2. Install dependencies

   ```bash
   npm install @shadcn/ui tailwindcss firebase mermaid-js lucide-react
   ```

3. Set up Firebase

   - Create Firebase project
   - Add authentication
   - Set up Firestore

4. Create core components one by one:

   - Start with GitVisualizer
   - Add CommandLine interface
   - Implement authentication
   - Add game mechanics

5. Test and deploy:
   - Unit testing
   - Integration testing
   - Firebase deployment

## Prompting Tips for Cursor

1. Break down tasks into small, specific components
2. Use clear, detailed descriptions
3. Include example code snippets
4. Specify exact dependencies and versions
5. Request step-by-step implementation

Remember to use Git throughout development to track changes and enable collaboration.
