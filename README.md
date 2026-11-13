# Toch Omot - Week 07 Project
## JavaScript Best Practices - To-Do List Refactor

## Live Demo
https://tochomot385-hash.github.io/iyf-s12-week-07-tochomot385-hash/

## Collaboration
- My PR (refactor/modules): PASTE_YOUR_PR_LINK_HERE
- Partner PR I reviewed: PASTE_PARTNER_PR_LINK_HERE
- Reviewer: [Partner Name + GitHub]

## Features
- Same as Week 5 + survives refresh (tasks + filter in localStorage)
- Does not crash if saved data is missing or broken JSON
- Modules: state, storage, todo-logic (pure), ui, app
- Tests: `npm test` passes, Lint: `npm run lint` clean

## Technologies
- HTML, CSS, ES Modules, Node 22/24, ESLint 9, Prettier, node:test

## What I Learned
- Splitting into modules made bugs easier to find. Before, one big app.js meant a storage bug looked like a UI bug. Now todo-logic has no DOM, so I can test it with `npm test` without a browser.
- Immutability prevents sneaky bugs. I first used `tasks.push()` and my tests failed because the original array changed. Returning `[...tasks, newTask]` fixed it.
- Broken localStorage must not crash the app. When I put invalid JSON in localStorage, the app went blank. Wrapping `JSON.parse` in try/catch and falling back to `[]` fixed it.

## How to Run
npm install
npm test
npm run lint
# Then open with Live Server