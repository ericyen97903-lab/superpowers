---
name: brainstorming
description: "You MUST use this before any creative work - creating features, building components, adding functionality, modifying behavior, or planning anything new, in software or out of it (a talk, a business, a renovation). HQ 路由（客製 2026-10-13）：影片、廣告片、動態圖像等影像創作一律走 hq-video，它自帶問答與八欄分鏡表，不寫設計文件、不接 writing-plans。只想把想法想清楚、不產出程式碼或設計文件的，走 grilling。商業策略走 ceo-office-hours。本 skill 保留給軟體專案與需要留設計文件的案子。"
---

# Brainstorming

You are very good at building. You build what you believe your human
partner wants, and that belief is usually thinner than it feels. This
skill is for finding out what they actually want, and why, before
anything gets built.

People often haven't finished working out what they want. Good questions
help them think it through. When you understand the why, you make the
hundred decisions they never mention the way they would have made them.

## First: What Do You Actually Know?

Before you reply, ask yourself: what do I know about what they want, and
why?

- **Everything that matters is in the request** ("make the icon cornflower
  blue"). This is a quick, clear task. Do it, and say what you did.
- **Something non-trivial is missing.** Start the conversation.

**霧濃度分流（HQ 客製 2026-09-05；2026-10-13 隨 v7.0.0 重建移植，語意不變）**：進入本 skill 前，若任務是一團霧（新領域或沒聽過的工具、Eric 說「看到才知道」「我沒概念」、創作方向還沒定調、接手外部工具或 repo、要動的東西沒 spec 也沒記憶），先走 `explore-unknowns` 的四象限走法，地圖貼回對話並落檔後，再進本 skill 的提問、Size the Work 與核准閘；地圖上的決策帳逐條當設計文件的既定條件，OPEN 項在文件標「待決」。判準正本：`docs/institution/judgment-rubrics.md` R9。「能不能做」永遠先跑最便宜的決定性測試（spike），不走四象限。

## Your First Message

Your first message is two things, in this order:

1. One line letting them know that if they'd rather skip the questions and
   have you just start, they can say so. If they take you up on it, this
   skill is done: state any significant how-it-gets-made choice
   (platform, language, medium) in one plain line, then do what they
   asked through the normal workflow.
2. One open question that gets them describing. Ask about a real moment
   or a concrete picture: "What's the moment you find yourself wishing
   this existed?" or "Tell me about the people who'll be in the room."

That's the whole message.

## The Conversation

Each message ends with one question: a single sentence with no list of
example answers hanging off it. Use plain language, pitched just a little
above where your human partner is. Match their vocabulary; never use
process jargon.

**提問協議（HQ 客製 2026-08-14；2026-10-13 Eric 拍板「分階段混用」方案，隨 v7.0.0 重建定稿）：開場照 v7，之後改用 grilling 的輪次制，每輪後回放**

上面那條「每則訊息只問一題、不附選項」修的是「選單牽著人走、人沒真的思考」。Eric 8 月的客製修的是另一個失敗：太慢，而且沒有可驗證的收斂判準（「我覺得懂了」就往下走，正是誤開工的破口）。兩個失敗都要堵，所以分階段：

1. **開場照 v7**：第一則訊息只有「可跳過提問」那一行加一個開放式問題，不給選單、不附推薦答案，讓 Eric 用自己的話描述。他的話帶出的意圖，選單帶不出來。
2. **第二則起，凡是 Size the Work 會判成 small change 或 project 的任務，提問改用 `grilling` skill 的 frontier 輪次制**：把設計畫成決策樹，一輪問完整個 frontier（所有前置條件已定案、現在就能答的題），編號並每題附上推薦答案，等 Eric 一次回完。答案取決於本輪其他題的，排到下一輪。推薦答案若是我的推測，要標明是推測，不要包成既定事實（2026-10-01 AI廣告13 的「延續上一支風格」教訓）。
3. **每輪答完先回放再問下一輪**（v7 的 Play It Back）：用兩三百字講我聽到的這一部分，只有 Eric 說過的才寫成他的，我猜的標成我的猜測，結尾問他哪裡錯、哪裡漏。回放被糾正就重算 frontier。
4. **需要查環境才能答的**（檔案、版本、既有實作）派 subagent 自己去查，不准問 Eric；下方「Offer recon」保留給範圍較大的探勘（整個 codebase、網路調研）。
5. **收斂判準是機械式的**：frontier 清空，且最後一段回放 Eric 沒有再糾正，才算問完。不是「我覺得懂了」。

本客製只換掉**提問方式**。其餘照 v7 且優先：Size the Work 尺寸判定、設計文件產出、Builder check、HARD-GATE 核准閘、終點只能交給 writing-plans。quick, clear task 與 spike 不套用（它們本來就只要兩三句拿個點頭）。

Eric 用平常的口語提需求即可，不需要指名任何 skill。詳見 memory `feedback_grilling_to_superpowers_bridge`。

Be clear and concise. Lead with what matters. Avoid jargon. When you
report what you found, give them the most important findings and offer
the rest.

**Get them describing.** Open questions come first. Their own words carry
intent that your options can't. Offer a short menu only when they're
stuck. When they say "just guess" or "what do you think?", propose
something concrete.

**How it gets made.** Every project rests on choices about medium, tools,
materials, and resources: the platform, programming language, and
libraries for an app; the medium for a piece of art. Find out early which
of those choices they want to make, which they're handing to you, and what
they already have to work with. Someone with strong views or skills will
want to talk it through. Someone counting on you needs sensible defaults,
said in plain words. When there's existing work, build on what it already
uses. Any choice you make goes in the design as your call, never as
something they agreed to.

**Ground to cover.** This is territory, not a script. Never read these
out as questions:

- what kind of thing this is, and what makes it special
- why now, and what success looks like to them
- goals, non-goals, and anti-goals (what would make this a failure even
  if it technically works)
- prior art: what they've seen elsewhere, loved or hated
- current state: what exists now, what they've tried
- the details they care about

**Questions that work** anchor in specifics: "Walk me through the last
time...", "If it could only do one of these well, which?", "What would
make you wince if I got it wrong?" A guess they can correct ("I'm
guessing this is because X keeps biting you?") often beats a question.

**Offer recon.** Once you have a bit of grounding and looking would help,
offer to go look: their codebase or project, their own files and data,
or the web. Say what you'd look for. They decide whether you go.

**Think wide privately.** Before you propose anything, come up with
several ideas and drop the weak ones, including any that fight what
they've told you about why. Show the comparison only when it helps them
decide.

**Show, don't tell.** Offer the visual companion (below) whenever seeing
would help more than reading:

- something they'll look at: a screen, a page, a printout, a sign
- a layout or arrangement: of a screen, a room, a schedule
- a flow or a sequence of steps
- options that would look different from each other
- a structure that's easier to see than read: a diagram, a timeline, a map

Once they've accepted, use it for mockups to react to, side-by-side
options, and throwaway prototypes they can click.

**Spike to feel things out.** Agentic work is waterfall, but very, very
fast. A quick throwaway build is often the cheapest way to learn what
they want or whether something works. Offer one when it would help.
When they just want to spike, get out of the way. Spikes get no tests
or minimal ones, aren't bulletproof, and skip the plan, implementation,
and review process. Bring what the spike taught you back into the
conversation.

## Play It Back

Play back as you go. As soon as you understand one part well enough to
describe it (what it's for and who it serves, say, or how one piece
behaves), describe that part back in about 200-300 words, then return to
questions about the next part. Playback and questions alternate through
the whole conversation; the last chunk covers whatever is left.

Mark anything you're guessing as your guess; only what they said goes in
as theirs. End each chunk by asking what's wrong or missing.

Before you send a chunk, check it: does it describe something they'll
look at, like a page, a screen, a schedule, or a printout? If so, and
they haven't seen the visual companion offer yet, send the offer instead
(its own message, below) and hold the chunk for the next message. Once
they've accepted, put a mockup next to the description.

## Size the Work

Once you understand what they want, pick a size and say it in plain
words. They can override it.

| Size | The full description | Then |
|------|----------------------|------|
| A quick, clear task | the request itself | do it |
| A small change | in chat | build it through the normal workflow |
| A project with a written design | a written design document | a full plan (for software: superpowers:writing-plans) |

If it grows mid-task, stop, say so, and step up a size.

If this is really several independent projects, say so, agree on an
order, and brainstorm them one at a time.

## The Written Design

For a project, write a plain document a talented builder in the domain
could plan from without going back to your human partner. Cover:

- intent and the why
- goals, non-goals, anti-goals
- constraints
- the parts of the how they decided, as they decided them
- what's left to the builder

**Where it goes:** in a software repo,
`docs/superpowers/specs/YYYY-MM-DD-<topic>-design.md`, committed.
Otherwise, ask. Your human partner's preferences override both.

**Builder check:** dispatch a fresh subagent with
`builder-check-prompt.md` in this directory. When you tell your human
partner you're writing it up, say a reviewer will read it first and you
may come back once with a few questions. Don't hand over the document
until the check is back. Sort what the builder asks into three piles:

- **Answered already** by the conversation or the project: put the answer
  in the document.
- **Minor:** a sensible builder could settle it without changing what gets
  built. Settle it yourself and mark it in the document as your call.
- **Theirs:** only your human partner can answer it, and the answer changes
  what gets built.

Bring the "theirs" pile in one message, most important first. Update the
document with their answers, then hand it over with a short list of the
calls you made so they can check those while reading. That's the only
round of questions the check produces. Without a subagent tool, read the
document as that builder yourself.

<HARD-GATE>
Nothing gets built until your human partner approves the full
description: in chat for a small change, the document for a project.
Building includes writing product code, scaffolding, installing
dependencies, creating projects, and invoking an implementation skill.
Reading and exploring are fine.

Two exceptions. If they opted out of the questions, the skill is done
and the gate goes with it. A spike they said yes to may be built; it
stays labeled throwaway, and keeping what it produced is a new request
that comes back through this gate.

After a project's document is approved, the next step is the plan. For
software, invoke superpowers:writing-plans and no other skill.
</HARD-GATE>

## Red Flags

| Thought | Reality |
|---------|---------|
| "I'll offer options to save them effort" | Options steer. Ask them to describe it first. |
| "I'll fill in sensible defaults" | Good. Say them out loud. A default they never heard is one they couldn't reject. |
| "I should explain the process first" | Ask your question. The process shows itself. |
| "They said 'sounds good' to the idea" | Approval covers what you showed them. A description you haven't written isn't approved. |
| "The spike works, I'll keep building on it" | Keeping it is a new request. Back through the gate. |

## Visual Companion

A browser tab for showing mockups, diagrams, and prototypes. It's a
tool, not a mode: accepting it doesn't send every question to the
browser.

**Offer it just-in-time.** Offer it the first time one of the moments
above comes up, never upfront. The offer is its own message with nothing
else in it:

> "This might be easier if I show you. Want me to open a browser tab with some mockups?"

If they decline, stay in text and don't offer again unless they raise it.

**Per question, ask: would they understand this better by seeing it?**
Mockups, layouts, diagrams, and side-by-side designs go in the browser.
Requirements, scope, tradeoffs, and conceptual choices stay in text. A
question about a UI topic isn't automatically a visual question.

If they accept, read `visual-companion.md` in this directory before
starting the server.
