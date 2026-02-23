# Claude Cowork: Building Your First AI Workflow
## Learning Page Outline — Step-by-Step Structure

**Page title:** Building Your First AI Workflow
**Subtitle:** Graduate from Claude Chat to Claude Cowork. Build a content repurposing system — and learn to manage AI like a project.
**Layout:** Three-column (rail + main + no sidebar). No target mockup sidebar — this tutorial's visual artifacts are generated *inside* Cowork during the experience.

---

## STEP 0: Welcome — You're Ready for This
**Rail label:** Start
**Title:** Building Your First AI Workflow
**Subtitle:** Graduate from Claude Chat to Claude Cowork. Build a content repurposing system — and learn to manage AI like a project.

### Content

Opening paragraph: You've used Claude Chat. You've uploaded files to a Claude Project. You've seen how giving Claude more context produces better work. Now it's time to graduate. You're going to build a system — not just send prompts.

**Dark card:**
> "You already know how to manage AI. You've been practicing."
> Every time you uploaded a brand guide to a Claude Project, you were building context. Every time you set project instructions, you were writing steering documents. Cowork is the same skill set — with no walls.

**Compare split — "Claude Projects vs. Claude Cowork":**

| Claude Projects (where you've been) | Claude Cowork (where you're going) |
|---|---|
| Upload files manually | Claude reads and writes files directly |
| Flat file list, no subfolders | Full directory structure — nested folders, hierarchy |
| Limited number of project files | Work with as many files as you need |
| Can't edit uploaded files in place | Claude edits files directly — saves updates automatically |
| Chat-only interface | Chat + file system + tool access |
| Great for learning the principles | Ready for real workflows |

Callout (green): "If you've never used Claude Projects, that's fine too. This tutorial teaches the principles from scratch — Cowork just lets you apply them at full scale."

**Three-window setup diagram:**
Unlike the previous tutorials (two windows), this one uses THREE:

```
┌─────────────────┬─────────────────┬─────────────────┐
│  Claude Cowork  │   This Guide    │  File Explorer   │
│                 │                 │                  │
│  Where you talk │  Follow along   │  Watch files     │
│  to Claude      │  step by step   │  appear in       │
│                 │                 │  real time        │
└─────────────────┴─────────────────┴─────────────────┘
```

Labels:
- **Left:** Claude Cowork — where you have conversations and Claude does the work
- **Center:** This guide — follow along step by step
- **Right:** File Explorer / Finder — watch the directory build in real time

**Action box — Set up your workspace:**
1. Create a folder on your Desktop called `content-workflow`
2. Open Claude Cowork at claude.com/cowork (requires Pro, Max, Team, or Enterprise subscription)
3. Point Cowork at your `content-workflow` folder — this gives Claude read/write access to that directory
4. Open File Explorer (Windows) or Finder (Mac) and navigate to the `content-workflow` folder
5. Arrange all three windows side by side on your screen

Callout (blue): "What is Claude Cowork? Claude Cowork is a mode in the Claude desktop app that gives Claude native access to a folder on your computer. Unlike Claude Chat (where you upload files one by one), Cowork can read, create, and edit files directly — like a teammate who has access to the shared drive. You don't need to configure anything technical. Just point it at a folder and start talking."

---

## STEP 1: The Onboarding Conversation
**Rail label:** Onboard
**Title:** The Onboarding Conversation
**Subtitle:** Before building anything, define the project through conversation. Claude asks; you answer.

### Content

Opening: When you onboard a new team member, you don't hand them a task on day one. You have a conversation. You explain the project, the goals, who the audience is, what success looks like. Claude is your new team member. Let's onboard it.

The key insight: **You don't have to write all the documentation yourself.** You have a conversation with Claude about what you want, and Claude drafts the documentation based on what you tell it. Your job is to talk about your project — Claude's job is to turn that into structured project docs.

**Dark card:**
> "Talk first. Document second."
> The best steering documents come from conversations, not from sitting down and writing a spec from scratch. Tell Claude what you're trying to do. Let it ask you questions. Then have it crystallize your answers into files.

**Action box — Prompt #1: Start the onboarding conversation**

```
I'm starting a new project. I want to build a content repurposing system. Here's the idea:

I regularly create content — blog posts, meeting notes, project updates, long-form writing. Right now, each piece of content gets used once and forgotten. I want a system where I can drop a piece of source content into this folder, and you help me turn it into multiple outputs: social media posts, an email newsletter section, a summary brief, and a key quotes collection.

Before we build anything, I want you to understand the project fully. Ask me questions about:
- Who my audience is across these different channels
- What tone and voice I use (or want to use)
- What platforms I post on and their constraints
- What a good output looks like for each format
- How I want to review and approve outputs before they go live

Ask me 3-5 questions to start. We'll go back and forth until you have a clear picture.
```

Callout (purple): "Notice what's happening. You're not asking Claude to produce anything yet. You're starting a *conversation* — the same way you'd sit down with a new hire over coffee and explain the project. Claude's questions will surface details you might not have thought to include. That's the value."

Paragraph: Claude will ask you questions. Answer them naturally — use your own voice, your own brand, your own audience. There's no wrong answer. The point is to surface the details Claude needs to build a system tailored to *your* work.

Callout (amber): "Take your time with this conversation. Go back and forth 3-4 rounds. The more Claude understands now, the less you'll need to correct later. This conversation *is* the foundation of the whole system."

---

## STEP 2: Crystallize the Conversation into Documents
**Rail label:** Docs
**Title:** Crystallize the Conversation
**Subtitle:** Turn your onboarding conversation into persistent steering documents Claude can reference every time.

### Content

Opening: You've had the conversation. Claude now understands your project. But if you closed this chat and started a new one, Claude would forget everything. Let's fix that. We're going to ask Claude to take everything it learned and write it down — as real files in your folder.

Paragraph: Watch your file explorer as you send this prompt. You're about to see the folder go from empty to populated.

**Action box — Prompt #2: Generate the steering documents**

```
Great, I think you have a solid understanding of my project now. I'd like you to create the following documentation files in this workspace. Base everything on our conversation — don't use generic placeholders.

1. Create a `docs/` folder and inside it create:
   - `project-overview.md` — What this project is, who it's for, what we're trying to achieve. This is the north star document.
   - `brand-guidelines.md` — My voice, tone, style across channels. What I sound like, what I never say, and how I adapt for different platforms.
   - `process.md` — Step-by-step instructions for how you should process a new piece of source content. What to read first, what to produce, in what order, and where to save outputs.

2. Create a `CLAUDE.md` file in the root of the workspace that references all of these docs. This should contain:
   - A one-paragraph project summary
   - Rules for how you work in this project (always read process.md first, always follow brand guidelines, etc.)
   - References to each doc with @docs/filename.md syntax

Save everything as real files. I want to see them in my file explorer.
```

### PAUSE MOMENT — Understanding what just happened

Callout (purple — key concept): "Look at your file explorer right now. A moment ago, that folder was empty. Now it has a structure — folders, documents, a project configuration file. You didn't write any of those documents by hand. You had a conversation, and Claude turned it into a workspace. **The conversation was the work. The documents are the output.**"

**Folder tree component** showing the current state:
```
content-workflow/
├── CLAUDE.md              ← Project instructions. Claude reads this first, every time.
├── docs/
│   ├── project-overview.md  ← What we're building and why
│   ├── brand-guidelines.md  ← Voice, tone, style rules
│   └── process.md           ← How Claude should process content
```

Paragraph: Open each file. Read them. These are *your* documents — written in *your* voice, based on *your* answers. If something doesn't sound right, we'll fix it in a moment. But first, let's understand why this structure matters.

---

## STEP 3: Why the Directory Structure Matters
**Rail label:** Structure
**Title:** Your Directory Is the System
**Subtitle:** The folder structure isn't just organization — it's the workflow, the memory, and the interface between you and Claude.

### Content

Opening: This step has no prompt to copy. It's a pause. Because the directory structure you just created is the most important thing in the entire project, and most people blow right past it. Let's not.

**Dark card:**
> "The folder is three things at once."
> It's Claude's workspace. It's your map. It's the iteration surface. If you understand the folder, you can debug any problem, improve any output, and scale the system indefinitely.

### The folder is Claude's workspace

Paragraph: Claude needs to know where to find things — inputs, instructions, outputs. A flat folder with 30 files is chaos. Claude will grab the wrong context, overwrite things, or lose track of state. A well-structured directory is like a well-organized kitchen: everything has a place, and the chef can move fast because they're not searching for ingredients.

### The folder is your map

Paragraph: When something goes wrong — and it will — you need to trace the problem. "The newsletter tone is off" becomes a solvable problem when you can say: "Claude read brand-guidelines.md, then source-content.md, then wrote to outputs/newsletter.md. The issue is in brand-guidelines.md — it doesn't mention that we're casual in email but professional on LinkedIn." Without the directory structure, debugging is "I don't know, it just sounds wrong."

### The folder is the iteration surface

Paragraph: When you want to improve the system, you're not rewriting prompts — you're editing files in specific folders. Want better social posts? Edit docs/brand-guidelines.md. Want a different process order? Edit docs/process.md. The directory structure tells you *where to make changes* — which is half the battle.

**Action box — Comprehension check:**

> Before we continue, test yourself. For each folder in your workspace, answer these three questions:
> - **What goes in here?** (inputs, outputs, instructions, templates, tracking)
> - **Who puts things here?** (you, Claude, or both)
> - **When does this folder get used?** (at the start, during processing, at the end, ongoing)
>
> If you can't answer those three questions for a folder, it shouldn't exist yet. And if you *can* answer them — you understand how Claude will navigate your system.

---

## STEP 4: Expand the Workspace — Let Claude Help Design It
**Rail label:** Expand
**Title:** Expand the Workspace
**Subtitle:** Ask Claude to build out the full directory structure — inputs, outputs, templates, and tracking.

### Content

Opening: Your workspace has steering documents, but it doesn't have places for the actual work to happen yet. There's no input folder, no output folder, no place for templates or tracking. Let's have Claude design the rest.

**Action box — Prompt #3: Let Claude propose the full structure**

```
Now I want to build out the full directory structure for this project. Right now we have docs/ with our steering documents. But we need places for:
- Source content I'll drop in for processing
- Outputs organized by type (social posts, newsletters, summaries, etc.)
- Templates for each output type (so outputs are consistent)
- A tracking system so we know what's been processed and what's pending review

Propose a complete directory structure. Create all the folders and add a brief README.md inside each folder explaining what goes there and who manages it (me or you). Also create an initial task-tracker.md in the tracking folder.

After you create everything, show me an artifact that visualizes the complete directory structure — like a map of the workspace. For each folder, show its purpose and whether I manage it or you manage it.
```

Callout (blue): "Notice that last line — 'show me an artifact.' This is a key Cowork pattern. The raw files are the system of record, but **artifacts are your review surface**. You'll see a visual representation of your workspace rendered right in the conversation, while the actual files appear in your file explorer simultaneously."

### PAUSE MOMENT — Trace the path

**Dark card:**
> "Follow the content, not the code."
> Before we run anything, let's trace how a piece of content will flow through your directory.

Expandable card — "Trace: the journey of a blog post through your system":
1. You drop a blog post into `inputs/`
2. Claude reads it from `inputs/`
3. Claude reads `docs/process.md` to know what to do
4. Claude reads `docs/brand-guidelines.md` to know how to sound
5. Claude reads `templates/` to know the format for each output
6. Claude writes analysis to `outputs/analysis/`
7. Claude writes social posts to `outputs/social/`
8. Claude writes newsletter draft to `outputs/email/`
9. Claude writes key quotes to `outputs/quotes/`
10. Claude updates `tracking/task-tracker.md` with what was produced
11. Anything flagged for your review goes to `review/`

Callout (purple): "You should be able to point to every folder in your file explorer right now and say what role it plays in that journey. The directory is the assembly line. Each folder is a station. Content moves through stations, and at each one, either you or Claude does something to it."

---

## STEP 5: Preview Before You Run
**Rail label:** Preview
**Title:** Preview Before You Run
**Subtitle:** Before committing to a full pipeline run, see what the outputs will look like. Iterate on the instructions, not the output.

### Content

Opening: A good manager doesn't let a new team member ship their first deliverable without a review. Before we run the full pipeline on real content, let's see a preview — and calibrate the system.

**Action box — Prompt #4: Drop in source content and ask for a preview**

```
I'm going to give you a piece of source content. Before you process it through the full pipeline, I want you to show me a PREVIEW of what each output would look like. Don't save anything to the output folders yet — just show me as artifacts so I can review.

Here's the source content:
[PASTE YOUR OWN BLOG POST, MEETING NOTES, OR ANY WRITING HERE — or use this sample if you want:]

---
Title: Why We Moved Our Team Standup to Async

Last month, our team made a small change that had a big impact. We replaced our daily 15-minute standup meeting with an async update in Slack. Here's what happened.

The problem wasn't the standup itself — it was the timing. With team members across three time zones, our 10am EST call meant 7am for the West Coast folks and 11pm for our colleague in Tokyo. Nobody was at their best.

We switched to a simple Slack template: What I did yesterday. What I'm doing today. Any blockers. Everyone posts by their own morning. The whole team reads the thread when they're ready.

The results surprised us. Updates got more detailed (people write better than they talk at 7am). Blockers got flagged faster (people read the thread throughout the day). And we got 75 minutes back per week — per person.

The downside? We lost some of the spontaneous conversation. To fix that, we added a weekly 30-minute "coffee chat" with no agenda. It's optional, it's casual, and it's become the highlight of the week.

Would we go back? Not a chance.
---

Show me what each output would look like:
1. The LinkedIn post
2. The Twitter/X thread
3. The email newsletter section
4. The summary brief
5. The key quotes

Render each one as it would appear on the actual platform — LinkedIn in a LinkedIn-style frame, tweets in a tweet-style frame, etc.
```

Callout (amber): "Important: you told Claude 'don't save anything yet.' This is your review checkpoint. You're looking at what the system *would* produce — not committing to it. If the previews look off, you fix the steering documents, not the output."

Paragraph: Look at the previews Claude generated. For each one, ask yourself:
- Does this sound like me?
- Is the tone right for this platform?
- Is it the right length?
- Would I actually post this?

If something's off — that's perfect. That's the whole point of previewing. Let's fix it.

**Action box — Prompt #5: Give feedback and iterate**

```
Here's my feedback on the previews:

[GIVE YOUR ACTUAL FEEDBACK — for example:]
- The LinkedIn post is too formal. I write more conversationally on LinkedIn — shorter sentences, more personal.
- The Twitter thread is good but the first tweet needs a stronger hook. Something that makes people stop scrolling.
- The email newsletter section is way too long. I want it to be 2-3 sentences max with a link to the full post.
- The summary brief is great as-is.

Based on this feedback, do two things:
1. Show me updated previews so I can see the changes
2. Update docs/brand-guidelines.md to capture these preferences so you get it right automatically next time. I don't want to have to give this feedback again.
```

**Dark card:**
> "Iterate on the system, not the deliverable."
> You didn't fix the LinkedIn post. You fixed the brand guidelines that *generate* LinkedIn posts. Every future LinkedIn post will now be better — not just this one. That's the difference between doing work and building a system.

Callout (green): "Look at your file explorer. The brand-guidelines.md file just changed. Open it — you'll see your feedback has been incorporated into the document. The system just got smarter. This is the compounding effect: every round of feedback permanently improves all future outputs."

---

## STEP 6: Run the System
**Rail label:** Run
**Title:** Run the Full Pipeline
**Subtitle:** Let Claude process your content through the complete workflow. Watch the directory fill up in real time.

### Content

Opening: The steering documents are calibrated. The previews look right. Now let's run it for real. This is where it gets exciting — and where having three windows open pays off.

Callout (blue): "Arrange your windows: Cowork on the left, this guide in the center, and your file explorer on the right. You're going to watch Claude work — and see files appear in your directory in real time."

**Action box — Prompt #6: Execute the pipeline**

```
I'm happy with the previews. Now run the full content repurposing pipeline:

1. Read the source content from inputs/
2. Follow the process defined in docs/process.md
3. Apply the brand guidelines from docs/brand-guidelines.md
4. Use the templates in templates/ for each output format
5. Save all outputs to the appropriate folders in outputs/
6. Update tracking/task-tracker.md with what was processed

When you're done, show me a summary artifact — a visual dashboard showing what was created, where it lives, and what's ready for my review.
```

Callout (purple — key concept): "Watch your file explorer right now. See the files appearing? Each one is a real file on your computer — you can open it, edit it, share it, copy it to another tool. The directory is the system of record. The artifact Claude shows you is just a view into that record."

### What Claude is doing under the hood

Expandable card — "What's actually happening":
> When Claude runs a multi-step task like this, it's orchestrating a sequence of operations:
> 1. Read docs/process.md to understand the workflow
> 2. Read docs/brand-guidelines.md to understand the constraints
> 3. Read the source content from inputs/
> 4. Read templates/ to understand the output formats
> 5. Generate each output — some in sequence (analysis first, then derivatives), some in parallel (social posts and newsletter can be written simultaneously)
> 6. Write each output to the correct folder
> 7. Update the tracking file
>
> **The steering documents are the choreography.** Claude didn't need you to tell it the order of operations in this prompt — it read process.md and followed it. That's the power of the directory structure: the instructions live in the files, not in your head.

---

## STEP 7: Review Outputs Without Leaving the Conversation
**Rail label:** Review
**Title:** Claude Is Your Interface
**Subtitle:** Don't open raw files. Ask Claude to show you the outputs the way your audience will see them.

### Content

Opening: Your output folders now have real files in them. You *could* open each one in a text editor — but let's do something better. Claude can render your outputs as visual artifacts, showing you exactly how each piece of content would appear on the actual platform. The raw files are the system of record. Claude is the interface.

**Action box — Prompt #7: View outputs as visual artifacts**

```
Show me the outputs you just created. For each one, render it as it would appear on the actual platform:
- The LinkedIn post in a LinkedIn-style frame
- The tweets in a Twitter-style thread
- The email newsletter section in an email layout
- The summary brief as a clean formatted document

I want to review them here in the conversation and give you feedback before I copy them anywhere.
```

Paragraph: This is the pattern: the files live in the folder, but you review them in the conversation. Why? Because Claude can render them visually — styled, formatted, in context. A markdown file in a folder is hard to evaluate. A LinkedIn post in a LinkedIn-shaped frame is easy to evaluate.

**Action box — Prompt #8: Give feedback and update**

```
The LinkedIn post needs work — [give your feedback]. Update it and save the changes back to the outputs folder.

Also, whatever you changed — if it reflects a general preference and not a one-off edit, update the brand guidelines too.
```

Callout (green): "**The directory is the warehouse. Claude is the showroom.** Files persist between sessions. Artifacts are ephemeral views you summon when you need them. This separation is powerful: your data is always organized, portable, and searchable. Your views are always tailored to what you need right now."

### The generative UI concept

**Dark card:**
> "Claude doesn't have a fixed interface. The interface is whatever you need it to be."
> Traditional software gives you one view. Claude generates any view you ask for — from the same underlying data.

Paragraph: Try these to see the pattern:
- *"Show me everything you produced today as a visual summary"*
- *"Compare the LinkedIn post to the tweets side by side"*
- *"Show me the project status — what's been created, what's pending review, what's finalized"*

Callout (purple): "The directory is the database. Claude is the query engine that returns visual results instead of rows. The better your folder structure, the more ways Claude can slice and present your data."

---

## STEP 8: Debug the System
**Rail label:** Debug
**Title:** When Something's Off — Trace It
**Subtitle:** Don't guess. Diagnose. The directory structure is your diagnostic tool.

### Content

Opening: Something in your outputs probably isn't perfect. That's normal — and it's an opportunity to learn the most important long-term skill: debugging a system, not just fixing an output.

**Action box — Prompt #9: Diagnose an issue**

```
Show me the [LinkedIn post / newsletter / whichever output feels off] alongside the brand guidelines you used to write it. Display them side by side so I can see where the gap is.
```

Paragraph: Look at the side-by-side. The gap between what you wanted and what you got is now visible. It's in one of three places:

Expandable card — "Three places a problem can live":
1. **The source content** — Was the original clear enough? Did it have the information Claude needed? → Check `inputs/`
2. **The instructions** — Did the brand guidelines cover this case? Did the process describe the right steps? → Check `docs/`
3. **A one-off preference** — Maybe the output is fine and you just have a preference for this specific piece. → Fix the output directly, don't change the system.

Callout (purple — key concept): "This is the most important skill in managing AI systems. You're not guessing what went wrong — you're checking specific files in specific folders. Every fix you make to a steering document permanently improves all future outputs. Every fix you make to an individual output helps only that output. **Always fix the system when you can.**"

**Action box — Prompt #10: Fix and document**

```
I found the issue — [describe it]. Update [the relevant doc] to fix this, and log what we changed in tracking/decisions-log.md so we have a record of why.

Then reprocess just the [affected output] using the updated guidelines.
```

Callout (green): "You just completed the feedback loop: Run → Review → Diagnose → Fix docs → Re-run. This is the loop that makes the system compound over time. Every cycle makes the system smarter."

---

## STEP 9: Your Project Dashboard
**Rail label:** Dashboard
**Title:** The View From Above
**Subtitle:** Ask Claude for a project dashboard — a living view of your workspace, generated on demand.

### Content

Opening: You've built a working content repurposing system. You've run it, reviewed outputs, debugged issues, and improved the steering documents. Now let's build the view that ties it all together.

**Action box — Prompt #11: Generate the management dashboard**

```
Build me a project dashboard that shows the current state of everything in this workspace. Include:

- **Workspace map** — Visual directory tree showing all folders and their purposes
- **Pipeline status** — What content has been processed, what outputs were created, what's pending review
- **Output gallery** — Thumbnails or previews of each output, organized by type
- **Recent changes** — What documents were updated and when
- **System health** — Are all steering docs current? Any known gaps or TODOs?

Make it something I can ask you to regenerate anytime I check in. This is my control panel for the project.
```

Paragraph: This dashboard isn't a static file. It's generated fresh every time you ask for it, pulling from the real state of your folder. Next week, when you've processed more content, the same prompt gives you an updated dashboard. The system is alive because the folder is alive.

Callout (purple): "You've been seeing this pattern the whole tutorial. Every artifact Claude built for you — the directory map, the flow diagram, the output previews, this dashboard — was a generated view into your folder. The folder is the source of truth. Claude is the interface. You decide what view you need."

---

## STEP 10: What You Built — And What's Next
**Rail label:** Done
**Title:** You're Managing AI Like a Project
**Subtitle:** A workspace, a workflow, a feedback loop. Here's what you built and where it goes from here.

### Content

**Dark card:**
> "You didn't learn to write better prompts. You learned to build systems."
> The skill isn't prompting — it's management. Define the workspace. Create the instructions. Run the system. Review the outputs. Fix the docs. Repeat. Everything else scales from there.

### What you built

Folder tree component — final state of the complete workspace with hover tooltips.

### The principles behind it

Recap list:
1. **The folder is the memory.** Claude doesn't remember between sessions. Your folder does.
2. **Conversations become documents.** You don't write specs from scratch — you talk through the project and Claude crystallizes it.
3. **Structure creates workflow.** Each folder is a station in the assembly line. Content flows through them.
4. **The directory is the interface.** Claude generates any view you need from the organized data.
5. **Iterate on the system, not the output.** Fix the steering docs, and all future outputs improve.
6. **The system compounds.** Every feedback loop makes it permanently smarter.

### Where this goes next

**Next-steps grid (2x2):**

| Card | Description |
|------|-------------|
| **Add more content types** | Drop different kinds of source content — meeting notes, project updates, research findings. The same system processes them all. |
| **Connect external tools** | Add MCP connectors to post to LinkedIn, send newsletters via Mailchimp, or pull feedback from Slack. The folder stays the hub. |
| **Graduate to Claude Code** | When your workflows get more complex — automated scheduling, data processing, multi-step pipelines — Claude Code gives you full programming power. Same folder, same principles, more capability. |
| **Build another system** | Apply this same approach to any project: client reporting, research workflows, project management. The pattern is always the same: folder → documents → system → outputs. |

**Success card:**
> You're a systems builder now.
> You took an empty folder and turned it into a working content repurposing pipeline — complete with steering documents, a processing workflow, output management, and a feedback loop. That's not prompting. That's project management. And the same approach works for anything you want to build with AI.

---

## Design Notes

### Components used across steps:
- **Dark cards** — For key mental model shifts (steps 0, 2, 3, 5, 7, 10)
- **Action boxes** — For all prompts (every step except 3 and 10)
- **Callouts** — Purple for key concepts, blue for context, green for success/progress, amber for warnings
- **Folder tree** — Steps 2, 4, 10 (growing each time)
- **Compare split** — Step 0 (Projects vs Cowork)
- **Expandable cards** — Steps 4, 6, 8 (deeper explanations)
- **Recap list** — Step 10
- **Next grid** — Step 10
- **Success card** — Step 10

### No context meter
Unlike the context-engineering tutorial, this page doesn't use a context meter. Instead, the progress visual is the **growing directory** — the folder tree component appears at steps 2, 4, and 10, each time showing more folders and files. The directory *is* the progress bar.

### Three-window setup
The setup diagram needs to show three windows instead of two. Update the desktop mockup from previous tutorials to include a third panel for the file explorer.

### No target sidebar
This tutorial doesn't have a target mockup like the vibe coding or context engineering pages. The "target" is the working system itself — and the visual artifacts Claude generates during the tutorial serve as the progress confirmation.

### Key teaching pauses
Steps 3 and 8 are dedicated teaching/reflection steps with no prompt to copy. They exist to slow the learner down and make sure they understand *why* things work, not just *how* to do them. Step 3 (directory structure) and Step 8 (debugging) are the two skills that separate casual AI users from effective AI managers.
