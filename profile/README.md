## We're fed up with leetcode bullsh*t 😤

Look, we've all been there. Grinding leetcode problems that have ZERO connection to actual software engineering. When's the last time you reversed a binary tree at work? Never? Exactly.

**The real problem:** Most coding practice platforms teach you to solve puzzles, not build actual software. You end up great at optimizing algorithms nobody uses but terrible at building real systems that people actually need.

## What we're building instead

A coding platform that teaches you to build **real sh*t**:
- TCP servers (like the ones powering your favorite apps)
- HTTP parsers (because the web runs on this stuff)
- Database engines (yes, the actual storage layer)
- Compilers (how your code becomes machine code)

No more "find the missing number in an array" garbage. Build the tools that power the internet.

## Why this exists

- **Real projects** - Build actual systems, not toy problems
- **Affordable** - We're not trying to buy a yacht off your subscription
- **Learn by doing** - Write code that actually runs and does useful things
- **No algorithm gymnastics** - If it doesn't exist in production, we don't teach it


## CHANGELOG

#### Frontend
- Built a `progress.tsx` page that dynamically fetches and displays:
  - User's current level
  - Challenge name
  - Username
- Integrated real-time updates using **Supabase subscriptions** to reflect progress changes instantly.

#### Backend
- Created a `/fork` endpoint to fork a GitHub repository.
- Added a `/api/submission_webhook` endpoint to:
  - Handle webhook payloads from the CI/CD pipeline
  - Update user progress in Supabase

#### CI/CD Workflow
- Configured a **GitHub Actions** workflow to:
  - Run tests for each level
  - Unlock the next level if tests pass
  - Notify the backend via a webhook about the user's progress

#### Pending Task

- The `/api/submission_webhook` is **not yet functional** in the CI/CD workflow due to pointing to `localhost`.

**Solution:**  
Deploy the backend to a public server or use tunneling tools like **Ngrok** or **Localtunnel** to expose it temporarily for testing.

---

**Got ideas for challenges?** Drop them in issues. We're always looking for more real-world systems.

---
*For engineers who want to build real software, not solve riddles* 🛠️
