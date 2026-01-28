# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Flashcards and practice tests for high school computing revision. This is one of several subject repositories linked from the main hub at [5tedes.github.io](https://5tedes.github.io).

## Site Architecture

**Hub-and-spoke model:**
- Main hub: `5tedes.github.io` repo contains term index pages (year-one-term-one.html, etc.)
- Subject repos: Each subject has its own repo (`subject-computing`, `subject-maths`, etc.)
- Published URL: `https://5tedes.github.io/subject-computing/y1s1/flashcards-components.html`

When adding new content, update the corresponding term page in the main hub repo to link to it.

## Tech Stack

- Pure HTML5 with embedded vanilla JavaScript and CSS
- No build tools, frameworks, or dependencies
- Static files deployed via GitHub Pages

## File Organization

```
y1s1/                          # Year 1, Semester 1
├── flashcards-{topic}.html    # Flashcard sets
├── practice-test-{topic}.html # Practice tests (future)
└── practice-exam-{n}.html     # Practice exams (future)
y1s2/                          # Year 1, Semester 2 (future)
```

Each HTML file is self-contained with embedded styles, scripts, and data.

## Flashcard Data Structure

Flashcards are stored as a JavaScript array within the HTML file:
```javascript
const flashcards = [
    { topic: "Category", question: "Question text", answer: "Answer text" },
    // ...
];
```

## UI Features to Maintain

- 3D card flip animation (CSS transform-style: preserve-3d)
- Keyboard navigation (Arrow keys, Space/Enter to flip)
- Responsive design with 768px mobile breakpoint
- Disabled navigation buttons at first/last card boundaries
