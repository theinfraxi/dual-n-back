Since you're aiming to build this as a **professional portfolio project** (not just a simple assignment), I recommend following the same workflow used by frontend developers in industry.

Below is the complete roadmap from **idea → finished website → deployment**.

---

# Dual N-Back Website Development Roadmap

## Phase 1 — Planning (UI/UX)

### Goal

Know exactly what you're building before writing code.

### Tasks

* [ ] Research Dual N-Back mechanics
* [ ] Decide website color theme
* [ ] Decide typography
* [ ] Decide animation style
* [ ] Sketch rough wireframe on paper
* [ ] Create UI in Figma
* [ ] Decide responsive layouts
* [ ] Finalize component list

---

## Deliverables

You should have pages for

```
Configuration Screen

↓

Game Screen

↓

Results Screen
```

---

# Phase 2 — Prepare Development Environment

## Install

* [ ] VS Code
* [ ] Node.js
* [ ] Git
* [ ] GitHub Desktop (optional)

Extensions

* [ ] Live Server
* [ ] Prettier
* [ ] ESLint
* [ ] HTML CSS Support
* [ ] Auto Rename Tag

---

## Create Project

```
dual-n-back/
```

Initialize

```
npm create vite@latest
```

Choose

```
Vanilla
JavaScript
```

Install

```
npm install
```

Run

```
npm run dev
```

---

# Phase 3 — Professional Folder Structure

Inside `src`

```
src/

assets/

components/

styles/

utils/

audio/

game/

data/

main.js
```

---

Inside `game`

```
GameManager.js

GameState.js

StimulusGenerator.js

ScoreManager.js

InputManager.js

RoundManager.js
```

---

Inside `audio`

```
Speech.js

Letters.js
```

---

Inside `utils`

```
Random.js

Timer.js

Storage.js
```

---

Inside `styles`

```
base.css

layout.css

components.css

animations.css

responsive.css
```

---

# Phase 4 — Figma Design

Design everything first.

---

## Configuration Screen

Contains

* Title

* Description

* N selector

* Round selector

* Volume

* Speed

* Theme

* Start button

---

## Game Screen

Contains

```
Trial Counter

Current N

3×3 Grid

Current Spoken Letter

Match Position Button

Match Audio Button

Pause Button
```

---

## Results Screen

Contains

```
Score

Accuracy

False Alarms

Misses

Hits

Reaction Time

Play Again
```

---

# Phase 5 — HTML Layout

Create

```
Header

Main

Footer
```

Inside Main

```
Configuration

Game

Results
```

Initially

Only Configuration is visible.

---

# Phase 6 — CSS

Build

Dark theme

Responsive layout

Modern spacing

Rounded corners

Glassmorphism

Smooth transitions

Animations

Hover effects

Button feedback

Grid highlight effect

Mobile layout

Tablet layout

Desktop layout

---

# Phase 7 — Game Engine

Create variables

```
Current N

Current Trial

Current Position

Current Letter

Position History

Letter History

Score

Hits

Misses

False Alarms
```

---

Create Game State

```
Idle

Playing

Paused

Finished
```

---

# Phase 8 — Random Generator

Need

Random Grid Position

```
0–8
```

Random Letter

```
A

B

C

D

E

F

G

H
```

Avoid repeating too often if desired.

---

# Phase 9 — Speech Engine

Use

```
window.speechSynthesis
```

Create

```
Speak()

Stop()

Change voice

Volume

Speed
```

---

# Phase 10 — Stimulus Engine

Every

```
3 seconds
```

Do

Generate position

Generate letter

Store histories

Highlight square

Speak letter

Update UI

Wait

Repeat

---

# Phase 11 — History System

Store

```
PositionHistory[]

LetterHistory[]
```

Example

```
Position

1

5

7

2

5

```

Letter

```
A

D

F

A

C
```

Always compare

```
Current

vs

Current - N
```

---

# Phase 12 — Input System

Buttons

```
Match Position

Match Audio
```

Keyboard

```
A

L
```

Allow

One response each trial.

---

# Phase 13 — Match Detection

Visual

```
Current Position

==

PositionHistory[current-N]
```

Audio

```
Current Letter

==

LetterHistory[current-N]
```

---

# Phase 14 — Scoring

Track

Visual

```
Correct Hits

Misses

False Alarm
```

Audio

Same.

Calculate

```
Accuracy

%

Precision

Recall
```

---

# Phase 15 — Results

Show

```
Visual Accuracy

Audio Accuracy

Total Score

Hits

Misses

False Alarms

Reaction Time
```

---

# Phase 16 — Animations

Square flash

Fade

Scale

Glow

Buttons

Press animation

Page transition

Progress animation

---

# Phase 17 — Mobile Optimization

Support

320px

375px

768px

1024px

1440px

---

# Phase 18 — Accessibility

Keyboard only

Focus ring

ARIA labels

Screen reader

Color contrast

---

# Phase 19 — Local Storage

Remember

Theme

N Level

Volume

Best Score

Statistics

---

# Phase 20 — Statistics

Show

Games Played

Average Accuracy

Highest N

Longest Streak

Best Score

---

# Phase 21 — Testing

Test

* N=1
* N=2
* N=3
* N=4
* N=5

Test

100+ rounds

Spam buttons

Resize browser

Mute audio

Pause

Resume

Restart

---

# Phase 22 — Bug Fixes

Ensure

No timer overlap

No duplicated speech

No duplicated scoring

No memory leaks

No skipped trials

---

# Phase 23 — Code Cleanup

Rename variables

Add comments

Split functions

Remove duplicate code

Format with Prettier

---

# Phase 24 — GitHub

```
git init

git add .

git commit
```

Push

GitHub Repository

---

# Phase 25 — Deploy

Deploy to

* GitHub Pages
* Netlify
* Vercel

Test

Desktop

Tablet

Mobile

---

# Phase 26 — Future Improvements (Version 2)

Once Version 1 is complete, you can add:

* Adaptive N-Level (automatically increase/decrease difficulty based on performance).
* Multiple themes (Dark, Light, AMOLED).
* Additional stimulus types (e.g., colors, shapes).
* Detailed performance graphs and statistics.
* Sound effects and background music.
* User accounts with cloud save.
* Daily training challenges.
* Leaderboards.
* Progressive Web App (PWA) support for offline play.
* Internationalization (multiple languages).

---

# Overall Progress Checklist

Use this checklist to track your progress:

* ☐ Phase 1 — Planning & Requirements
* ☐ Phase 2 — Development Environment Setup
* ☐ Phase 3 — Project Structure
* ☐ Phase 4 — Figma UI Design
* ☐ Phase 5 — HTML Layout
* ☐ Phase 6 — CSS Styling
* ☐ Phase 7 — Game State & Engine
* ☐ Phase 8 — Random Stimulus Generator
* ☐ Phase 9 — Speech Synthesis
* ☐ Phase 10 — Stimulus Timing Loop
* ☐ Phase 11 — History Arrays
* ☐ Phase 12 — User Input
* ☐ Phase 13 — Match Detection Logic
* ☐ Phase 14 — Scoring System
* ☐ Phase 15 — Results Screen
* ☐ Phase 16 — Animations
* ☐ Phase 17 — Responsive Design
* ☐ Phase 18 — Accessibility
* ☐ Phase 19 — Local Storage
* ☐ Phase 20 — Statistics Dashboard
* ☐ Phase 21 — Testing
* ☐ Phase 22 — Bug Fixing
* ☐ Phase 23 — Code Cleanup
* ☐ Phase 24 — GitHub Repository
* ☐ Phase 25 — Deployment
* ☐ Phase 26 — Version 2 Enhancements

Following this roadmap will take you from a blank project to a polished, production-ready Dual N-Back web application while helping you learn professional frontend development practices along the way.
