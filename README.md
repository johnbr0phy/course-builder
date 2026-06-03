# Course Builder

A **Claude Code skill** that turns a topic or some source material into a complete,
hands-on, instructor-led course — and, optionally, a live homepage.

It packages a proven pattern: **Claude Code is the instructor, learners learn by
doing, every concept ties to one real thing the learner brings, and each session
ends in an 8-question quiz.** Point it at any subject and it builds the whole
thing in minutes.

🌐 **Landing page:** https://johnbr0phy.github.io/course-builder/
▶️ **A course it built (demo):** https://johnbr0phy.github.io/Workflows-course/

---

## What it generates

```
<topic>-course/
├── README.md          overview & quick start
├── CLAUDE.md          the instructor (runs sessions, grades quizzes)
├── LESSONS.md         full session plans (real content, not stubs)
├── SOURCE.md          canonical source of truth
├── index.html         browsable homepage (optional)
└── templates/
    ├── user.json
    ├── progress.json
    ├── PROGRESS.md
    └── MY_THING.md    the learner's running example → capstone
```

- **An instructor, not a document** — `CLAUDE.md` runs sessions, waits for the
  learner, and grades quizzes.
- **Personalized throughout** — every exercise runs on the one real example the
  learner brings; the capstone ships it.
- **Hands-on by design** — learning happens in the real environment.
- **Ships a website** — a data-driven homepage you can deploy live in one push.

## Install

Copy the skill folder into your Claude Code skills directory:

```bash
git clone https://github.com/johnbr0phy/course-builder.git
cp -r course-builder/course-builder ~/.claude/skills/   # personal (all projects)
# — or, to scope it to one project —
cp -r course-builder/course-builder /path/to/your/repo/.claude/skills/
```

## Use

In Claude Code, just ask:

```
Build a course on <your topic> for <your audience>.
```

Claude runs a short intake, proposes an outline, you confirm, and it builds the
course — then offers to put up the homepage. It stops there; the generated course
is what teaches.

## Repo layout

```
course-builder/                 (this repo)
├── README.md
├── docs/index.html             # the landing page (served by GitHub Pages)
└── course-builder/             # the installable skill — copy this into .claude/skills/
    ├── SKILL.md
    ├── reference/              # course-anatomy, homepage, deploy-pages recipes
    ├── assets/                 # config-driven homepage shell + Pages workflow
    └── templates/              # scaffolds for every generated course file
```
