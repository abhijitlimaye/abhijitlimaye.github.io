---
layout: single
title: "Vibe Coding, Anyone?"
date: 2025-09-06
categories: [development, coding, AI]
tags: [vibe coding, chatGPT, flutter, productivity]
---

# Vibe Coding, Anyone?

If you can’t code yourself, you won’t get too far with vibe coding!

Let me start the blog from the “lessons learned” and some “pro tips” before diving into my experience of vibe-coding. If you are short on time (or attention span), just the points below are a good starting point.

---

## The Biggest Challenge

The biggest challenge of vibe coding is to get the AI to come out of what I call the:

**“Self-Destruct Loop of Regressions” (SDLR)**  
*(should I trademark this term? 🙂)*

My take is this: you need some experience of coding to really get around these challenges.

---

## Pro Tips for Vibe Coding

- Start by clearly defining and explaining the role to AI.  
  For example: *“You are a senior developer building apps to solve customer problems.”*

- Give clear instructions on how you want the code to be:  
  *“You will suggest code that is well-designed, extensible, modular, and maintainable.”*

- Explain the feature you want to implement to AI, and ask it to repeat its understanding.

- For UI features, you can ask AI to generate a **text-based wireframe**. Try it — it’s good!

- Make sure that it doesn’t dump a ton of code on you.  
  My go-to instruction became:  
  *“Do not generate code first. First give me your design thinking on how you will structure the code.”*

- Ask for **surgical fixes** with precise code and step-by-step instructions.

- Watch out for regressions. AI often suggests contradictory code compared to what it gave earlier. Point it out clearly, ask it to drop its current line of thinking, and make it *“think differently.”*

- Whenever you hit compile or runtime errors, dump the debug output or error message to AI. It usually suggests quick fixes.

- Try to understand the **logic** behind the code. Don’t blindly trust AI — I had to ask for refactors when the generated code was poorly structured.

- Pick up one feature addition at a time after reaching a working baseline / MVP.  
  Keep a fully working copy separate — or better, use Git with feature branches.

- As interactions grow, AI will “forget” what you were doing. Ask it to summarize the context before proceeding.

- Keep an eye on SDLR:  
  when new code breaks old code, and its “fix” breaks something else.  

- ChatGPT once suggested I start a new chat because responses were slowing down.  
  But when I did, the new chat lacked full context!

- When I hit SDLR badly, I switched to Gemini. It required more context, but eventually worked. This is where being an **experienced coder** really helps.

---

## My Experience: Building a Task App in Flutter

I decided to build a simple task-keeping app using Flutter, without knowing a thing about it.  
Well, what better challenge than to use “vibe coding,” that’s all en vogue these days!

### Setup

- Installed VS Code, Android SDK, Java SDK, Flutter SDK, Android Debug Bridge, and Android Emulator.  
- Took ~2.5–3 hours without Android Studio (which would’ve been easier).  
- AI pointed me to some reference videos. Instructions were okay, with a few hiccups.  

With the Flutter extension in VS Code, creating a new app gives you boilerplate code and a working home screen.

### First Steps

I described my feature set to ChatGPT.  
It gave clear instructions on files, folder hierarchy, and key configs (`pubspec.yaml`, `AndroidManifest.xml`).  
I built and tested the app on the local emulator successfully.

Some feature additions went smoothly:

- Switching between card view and list view  
- Replacing default table layout with a styled version (header row, color bands)

### Hitting the SDLR

As the code grew, chat interactions ballooned. Eventually, ChatGPT responses slowed and regressed.  
At one point, I realized I was working in *“slave mode”* — blindly following AI.

I changed my approach.  
I became the **master**, trusted my developer instinct, and switched to Gemini.  
I gave it full context (file names, class names, features).  
Then I picked the cleanest code between ChatGPT and Gemini and **rebuilt my app manually**.  

Painful? Yes.  
But it got me to a good working state.

---

## Most Frustrating Parts

- Fixing compile and runtime errors  
- Debugging a **Contacts-picker crash**:  
  - Connected my phone via USB  
  - Enabled USB debugging  
  - Ran a debug build  
  - Captured crash logs with ADB  
  - Gemini finally pinpointed the issue  

- Flutter UI code (Scaffold, Build methods) felt **tedious and fragile**  
- Syntax quirks: brackets everywhere, commas/semicolons unclear (coming from C/C++)  
- Code aesthetics — often painful for someone who likes clean structure

---

## The End Result

A fully functional task app with these features:

- Add new tasks  
- Home screen toggle: Card view ↔ List view  
- Filters: hide completed / show today’s tasks  
- Contacts picker to assign tasks to people  
- Share a task via Android’s standard share popup  
- App lock for added security  

---

If you need more details, feel free to contact me.  

Until then,  
**Happy Vibe-coding!** 🎉

