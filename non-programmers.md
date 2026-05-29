# Non-Programmers: Best Practices for AI Usage

If you're not a programmer, your AI usage can also benefit from concepts and approaches in the programming space:

1. \*One shotting\* (getting a good result from a single prompt without back and forth) is possible! But only if you provide the complete details. Examples of bad and good prompts:

❌ Write a marketing post about vibe coding

✅ Write marketing post about vibe coding, incl. what vibe coding is (for non-technical people), whether learning fundamentals is a waste of time (it's not), why learning fundamentals is not a waste of time, common downsides with AI-generated code

If you don't know what details to write after "incl." in 1. above, continue to 2.

2. \*Plan mode\* Some AI tools for programming have a "plan mode" which allows you to refine your idea before prompting AI.

You can follow the same approach by writing a prompt to refine your idea, like:

✅ give me 10 subtopics about "vibe coding" for a marketing post. reply with terse, short bullet point list. each point should be 1-9 words

3. \*Less is more\* Write fewer lines and words of text, but compress your meaning by using terse, high-density language. This not only makes the AI more efficient, but also makes humans reading and editing it more efficient.

❌ Writing prompts with perfect English which include repetition and filler words ("a", "the", "actually"), vague words ("dynamic", "seamless"), direction words ("help me", "please"), but which miss the key details

✅ Writing prompts without perfect English, dropping repetition, filler and vague and direction words, but using abbreviations ("incl.", "approx.", "re.", "wks", "reqs", "para")

Examples:

- ❌ Write a really engaging and impactful LinkedIn post about our innovative new course.  
  ✅ linkedin post for new js course in amsterdam - beginners, 12 wks, evening classes, apps open now, friendly tone, not too corp., approx. 120 words

- ❌ Create a seamless and intuitive landing page for our product.  
  ✅ landing page copy for time tracking app - audience = small agencies, incl. headline, subheading, 3 benefits, CTA, mention billable hrs, team reports, invoice export, tone clear + practical

- ❌ Make this email more dynamic, compelling, and professional.  
  ✅ rewrite email for existing customers re: 20% sale until sunday - incl. subject line + preview text, warm tone, a bit premium, not too salesy, max 90 words

- ❌ Write a robust and strategic plan for launching this project.  
  ✅ 6 wk launch plan for online coding bootcamp - cover landing page, ads, webinar, email seq., follow-up, reqs = concrete steps + timeline, not generic fluff

- ❌ Make this paragraph more powerful and streamlined.  
  ✅ rewrite paragraph w/ less repetition, clearer msg, stronger intro, keep main point, audience = B2B founders, max 70 words, no vague biz buzzwords

4. \*Less is more\* also applies to drafts and working copies:

❌ Draft with 10-20 paragraphs of AI-generated text (often filled with unnecessary fluff, maybe even "AI slop")

✅ Draft with 5 bullet points showing the high-level plan, in terse detail

Examples:

```txt
❌ Title: Chrome extension for customized PWA installs

Description:

Chrome extension for installing tested, refined PWA variants of supported websites, with optional manual customization.

Ship hardcoded verified presets, similar in flavor to Refined GitHub, Refined Gmail and Better-X extensions. Each preset defines a known-good custom manifest for a specific website: `start_url`, `name`, `icons`, `display`, `theme_color` and explicit `id`.

User flow:
- detect supported websites and suggest matching presets
- choose a verified website preset
- prefill editable manifest fields from the preset
- allow changes before install
- allow fully custom manifest overrides for unsupported websites
- apply the custom manifest to the current page where possible
- guide users into Chrome's native PWA install prompt

Constraints:
- not silent install, Chrome still owns final install confirmation
- presets must be tested and marked verified per website
- `start_url` must stay valid for the manifest/app origin, otherwise Chrome may fall back to the install page URL
- explicit manifest `id` avoids `start_url` accidentally becoming app identity
- injection can fail when the page already has a manifest, CSP blocks inline/data manifests or Trusted Types blocks DOM mutation
- fallback path should document when Local Overrides or manual install steps are still required

UI should show current state clearly: unsupported, supported preset found, installable, patched, blocked by CSP, blocked by existing manifest or blocked by browser behavior.
```

```txt
✅ Title: Chrome extension for customized PWA installs

Chrome extension for customized PWA installs.

- popup with form fields: `start_url`, `name`, `icons`, `display`, `theme_color`, explicit `id`
- maintained, tested presets for supported websites, kind of like a PWA-only version of [`refined-github`](https://github.com/refined-github/refined-github) or [`refined-gmail`](https://github.com/karlhorky/refined-gmail-userscript)
  - prefills fields only, editable before install
- failure handling for existing manifest conflicts, CSP blocks, Trusted Types blocks and fallback to Local Overrides / manual install steps
- possibly required install safety checks?
  - `start_url` must stay valid for the manifest/app origin, otherwise Chrome may fall back to the install page URL 
  - explicit `id` avoids `start_url` accidentally becoming app identity
```

Drafts are often not close to the final version, so they should be optimized for quick review, editing and deletion. Long drafts take a long time to read and are hard to edit - editing often involves not only the overall structure and order and message, but also the word-by-word minutiae and phrasing. Short bullet-point drafts are easy to read, quick to reorder and edit, and each point is also easy to delete.

Keep edits to working copies constrained and surgical, using diffs:

- ❌ Add market data to the quotes in this working copy case study
  ✅ para 3: add market data to quotes in this working copy case study. keep edits surgical. show me a diff

To further constrain and review AI changes, consider setting up version control tools like Git.
