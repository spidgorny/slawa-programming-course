# Speaker Prep — "From Electrons to Apps"

A practical cheat sheet for presenting this talk, aimed at a first-timer.
Not a script — a set of memory hooks, timing checkpoints, and a "tough
question" bank so being grilled doesn't catch you off guard.

## Before Tuesday

- [ ] Do at least **one full run-through out loud**, alone, with a timer.
      Reading slides in your head is not the same as saying them.
- [ ] Time yourself per section once (see table below) — you'll likely
      run long the first time. That's normal; cut detail, not sections.
- [ ] Know your **3 "if I forget everything else" takeaways** (below) cold.
- [ ] Decide your **cut list** in advance if you're running out of time
      (see plan.md: Cloud bonus first, then C/higher-level languages detail).
- [ ] Rehearse in **presenter view** (see below) — it shows the next slide
      and your notes (bridge text, jokes, activity hints).
- [ ] Check the room has **internet** for the logic-gate video; open the
      link in a browser tab beforehand. No internet → skip the video and
      explain the gate symbols on the slide instead.
- [ ] **Confirm licences** of the presenter-provided images
      (see `images/CREDITS.md`) before sharing the deck publicly.
- [ ] Glance through the "tough questions" bank once — you don't need
      perfect answers, you need to not freeze.

## Presenter view

Open `slides.html` in a browser and press **P**. A second window opens with
the current slide, a preview of the **next slide**, a timer, and the speaker
notes. Every slide's notes start with "Next: <title>" so you can prepare the
transition; section-divider notes hold the full bridge explanation, and 😄
notes hold optional jokes (keep the punchline off-screen). Put the presenter
window on your laptop screen and the main window on the projector.

To embed notes in the PDF as well: `npx @marp-team/marp-cli slides.md
--pdf --pdf-notes --allow-local-files`.

## General public-speaking tips (first-timer focused)

- **Pause, don't fill.** Silence for 2 seconds feels like 10 to you, like
  nothing to the audience. It beats "uhh, so, like..."
- **Breathe before you answer a question.** You're allowed one full breath
  before speaking — it looks like thoughtfulness, not hesitation.
- **"I don't know" is a complete, respectable answer.** Follow with "let's
  figure it out" or "great question, I'll look into it" — never fake it.
- **Repeat the question before answering** (especially tough ones). Buys
  you thinking time and makes sure everyone heard it.
- **Pick one friendly face** in the room to glance at when nervous, then
  widen out — don't lock eyes with the toughest questioner the whole time.
- **Slow down on purpose.** Nerves speed you up more than you think;
  deliberately talk ~20% slower than feels natural.
- **It's OK to say "let's park that and come back after the break/at the
  end"** if a question threatens to derail your timing.

## Your 3 "unforgettable" takeaways

If you remember nothing else to say, say these:

1. **Computing is a tower of abstraction layers** — electrons → bits →
   logic gates → machine code → C → high-level languages → OS → apps —
   each layer hides the complexity of the one below it.
2. **Every layer is just a translation step.** Nothing magical happens
   anywhere — compilers, interpreters, and OSes are all just programs
   translating one representation into another.
3. **"The cloud" is just someone else's computer**, running the exact
   same stack you just learned, somewhere else, that you reach over a
   network.

## Timing checkpoints (cumulative, out of ~65 min)

Use these as pacing checkpoints — if you're past the target by more than
~2 min, speed up or trim the current section's detail.

| By minute | You should be finishing... |
|---|---|
| 4 | Hook & Roadmap |
| 11 | Floor 1 — Electrons & Transistors |
| 17 | Floor 2 — Bits & Bytes |
| 23 | Floor 3 — Logic Gates → CPU |
| 30 | Floor 4 — Machine Code & Assembler |
| 37 | Floor 5 — C |
| 43 | Floor 6 — Higher-Level Languages |
| 51 | Floor 7 — Operating Systems |
| 56 | Floor 8 — User Applications |
| 62 | Bonus — The Cloud |
| 65 | Recap + Q&A buffer |

## Section-by-section cues

One-line reminder of the *point* of each section (say this in your own
words, don't read slides verbatim) plus the one bridge-idea to land.

| Section | Core point to land | Bridge to next |
|---|---|---|
| Electrons & Transistors | Electricity can represent on/off; a transistor is a switch controlled by electricity | Humans agree to call on/off "1" and "0" (glass-of-water aside) |
| Bits & Bytes | A bit is one on/off; a byte (8 bits) can represent 256 things — numbers, letters, anything | Storing bits is nice — transistors wired into gates can *compute* with them |
| Logic Gates → CPU | Millions of gates wired together = a CPU; add a clock + memory and you get a general-purpose machine | The CPU needs instructions to do anything useful |
| Machine Code & Assembler | Machine code is raw binary instructions; assembler just gives them readable names, 1:1 | Assembly is CPU-specific and tedious — we want portability |
| C | C adds structure (vars/functions/loops) and a compiler makes it portable across CPUs | C is still low-level (manual memory, verbose) |
| Higher-Level Languages | Python/JS/Java trade some speed/control for much less tedium and more safety | These languages still run *inside* an OS |
| Operating Systems | The OS shares one machine safely between many running programs (processes, files, drivers) | The OS runs the apps you actually interact with |
| User Applications | Everything you click on is, underneath, the entire stack — down to electrons | What if the stack runs on a machine you've never touched? |
| The Cloud (bonus) | Cloud = the same tower, just physically somewhere else, reached over a network | Full circle — recap the whole ladder |

## Self-rehearsal drill (works solo, no partner needed)

Since you may be rehearsing alone: for each section, cover the "answer"
column below, read only the question out loud, pause 2 full seconds,
then answer out loud as if a real person just interrupted you. Only
then reveal the suggested answer and compare. Repeat for every section
in one sitting — it takes ~15 minutes and is the single highest-value
prep activity here.

## "Grill me" — anticipated tough questions

Use these for the drill above. You don't need the perfect textbook
answer — aim for "confident, honest, and roughly right," and it's fine
to simplify further or admit the limit of your knowledge.

**Electrons & Transistors**
- *Q: Why specifically silicon? Why not some other material?*
  A: Silicon is a semiconductor — it can be made to conduct or block
  current depending on tiny impurities ("doping"), which is exactly
  the on/off switch behavior we need. It's also cheap and abundant.
  (If pushed further: "That's genuinely deep materials-science territory,
  happy to not go further down that hole today.")
- *Q: Isn't a transistor just a tiny relay, like 1900s telephone switches?*
  A: Conceptually yes — a relay is also a switch controlled by current.
  Transistors just do the same job with no moving parts, at nanometer
  scale, millions of times a second, with no mechanical wear.

**Bits & Bytes**
- *Q: Why 8 bits in a byte and not some other number?*
  A: Mostly historical/practical convention (it comfortably covers the
  Latin alphabet + punctuation + control codes with room to spare, and
  is a convenient power of two for memory addressing). Not a law of
  nature — some historic machines used different word sizes.
- *Q: You said bits represent "everything" — how do bits become a color
  or a sound, not just numbers and text?*
  A: Everything is first turned into numbers (a color as RGB values, a
  sound as thousands of amplitude samples per second), and those numbers
  are then just bytes — so "is it a color" is purely a matter of which
  program interprets those bytes and how.

**Logic Gates → CPU**
- *Q: How does the CPU know what "instruction" to run next — who tells it?*
  A: A special register (the "program counter") holds the memory address
  of the next instruction; after each instruction the CPU automatically
  bumps it to the next one (or jumps elsewhere for loops/branches).
- *Q: Is a CPU core literally just millions of these adders wired up?*
  A: Adders are one example; there are many other circuit blocks (for
  comparisons, memory access, control logic) — but yes, it's fundamentally
  "lots of logic gates wired together for different jobs," plus a clock.

**Machine Code & Assembler**
- *Q: You said mixing up data and instructions causes freezes — is that
  also how computer viruses/hacking works?*
  A: Often, yes — many classic exploits (like buffer overflows) work by
  tricking a program into treating attacker-supplied data as instructions
  and executing it. It's a real, historically important class of bug.
- *Q: Do people still write assembly by hand today?*
  A: Rarely, and mostly in tiny niches — OS boot code, embedded/driver
  code, performance-critical inner loops, or compiler output inspection.
  Compilers write better assembly than humans for almost everything else.

**C**
- *Q: If C is "portable," why do some C programs only work on Linux?*
  A: The *language* is portable, but programs often call OS-specific
  functions (files, networking, GUIs) that differ between Windows/Linux/
  macOS — that's the part that isn't portable, not the C language itself.
- *Q: What exactly does "manual memory management" mean, concretely?*
  A: In C, you explicitly ask the OS for a chunk of memory and must
  explicitly give it back when done; forgetting causes a "memory leak,"
  and giving it back twice or using it after freeing causes crashes/bugs.

**Higher-Level Languages**
- *Q: If higher-level languages are slower, why doesn't everyone just use C?*
  A: Development speed and safety usually matter more than raw performance
  for most software (a web app doesn't need to be as fast as a game engine
  or OS kernel) — it's a trade-off, not a strict downgrade.
- *Q: What's actually happening when Python code "interprets" instead of
  compiles?*
  A: Roughly: the interpreter reads your code line by line (or a compiled
  intermediate form of it) and does the corresponding machine-level work
  on the fly, instead of producing a separate standalone binary upfront.

**Operating Systems**
- *Q: If two programs both want the CPU at the same time, what actually
  happens?*
  A: The OS rapidly switches between them (context switching) — giving
  each a tiny time slice, often milliseconds — fast enough that it looks
  simultaneous to us, even on one core.
- *Q: Is Android really "Linux"? It doesn't look anything like it.*
  A: Yes — Android uses the Linux kernel underneath for exactly the core
  jobs (processes, drivers, memory); everything you *see* is a completely
  different user interface layer built on top.

**User Applications**
- *Q: When I update an app, does it really go through this whole stack again?*
  A: Yes — new source code gets recompiled (or re-interpreted), produces
  new instructions, and the OS runs the new version as a new/updated
  process next time you launch it.

**The Cloud**
- *Q: If it's "just someone else's computer," why can't I just rent one
  server and do it myself?*
  A: You can! Cloud providers mostly add convenience on top: they handle
  the physical machines, networking, power, and let you add/remove
  capacity in seconds instead of buying and racking hardware yourself.
- *Q: Is my data actually safe "in the cloud"?*
  A: It's as safe as the provider's security practices and your own
  configuration — "the cloud" doesn't inherently mean more or less secure,
  it's still ordinary computers, which can be configured well or badly.

## If you genuinely get stuck

A safe, honest holding pattern:
> "That's a great question and I want to give you a correct answer rather
> than guess — let me note it down and follow up / let's dig into that
> together after the talk."

That's a completely normal, professional answer — and arguably better
training for real public speaking than memorizing every possible answer.
