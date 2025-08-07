---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Integration Testing for Real-World React Apps
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
seoMeta:
  # By default, Slidev will use ./og-image.png if it exists,
  # or generate one from the first slide if not found.
  ogImage: auto
  # ogImage: https://cover.sli.dev
---

# Confidence Over Coverage

Integration Testing for Real-World React Apps

Sibasish Mohanty

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: slide-up
level: 2
---

# What We are Told vs What We Do

⚠️ The goal: Ship with confidence, not follow dogma.

| Conventional Wisdom                       | The Reality                              |
| ----------------------------------------- | ---------------------------------------- |
| Test Driven Development                   | "We wrote it after 3 prod bugs"          |
| 100% Coverage                             | "We test the scary stuff first"          |
| Pure Functions = Unit Tests = Good Design | "The test broke, but the feature worked" |

---
transition: slide-up
level: 2
---

# What Makes a Test Worth It?

❌ Tests that:

- Know too much about the internals
- Break because of renames or DOM changes
- Exist “just for coverage”

✅ Tests that:

- Mirror real user behavior
- Are resilient to internal refactors
- Save you from introducing regressions
- Guide better component/API design

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---

# Testing Philosophy in Practice

> “The more your tests resemble how your software is used, the more confidence they can give you.”

- Kent C. Dodds

> “Focus on testing what Redux-connected components render and do — not their internals.”

- Mark Erikson

<br/>
<br/>

So we:

- Avoid testing Redux logic in isolation
- Use `renderWithProviders` and `MSW`
- Write tests after the component is useful, not before

<!--
Notes can also sync with clicks

[click] This will be highlighted after the first click

[click] Highlighted with `count = ref(0)`

[click:3] Last click (skip two clicks)
-->

---
layout: center
class: text-center
---

# How We Test Our Components

Live coding and examples

---

# When (Not) to Test

💡 Think Cost vs Benefit and Test code you want to protect.

High ROI:

- Core flows: login, checkout, dashboard
- Bug regressions
- Anything you’re scared to change

Low ROI:

- Pure CSS/layout tweaks
- Very early prototype UIs
- Internals you plan to delete soon

---

# What We Gained

💡 Testing = documentation + confidence + courage

✅ Fewer regressions in business-critical flows

✅ Ability to refactor with confidence

✅ Cleaner APIs (because tests exposed bad ones)

✅ Onboarding is faster — tests show usage clearly

<!--
Your Next Steps
Pick a flow you're scared to touch — write a test for it

Start with one meaningful integration test

Invest in renderWithProviders or setup() utils

Share flaky tests with the team — kill them together
-->

---
layout: center
class: text-center
---

# Thank you

Ask me anything. Or show me your flakiest test.
