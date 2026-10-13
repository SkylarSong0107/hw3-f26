# HW3 CSS Grid validation

Checked and published on 2026-10-13.

- `bank.html` remains the entry file. The original HTML class and ID names and all three starter CSS filenames are unchanged.
- Browser widths checked: 320, 375, 700, 824, 825, and 1000 px. No horizontal page overflow was observed. The layout uses five grid columns below 825 px and seven from 825 px upward.
- The 700 px and 1000 px layouts were compared with the supplied full-page reference images.
- The skip link moves keyboard focus to `main`. The long text panel can be focused and scrolled with a keyboard at 375 px and 1000 px.
- Nu Html Checker: no HTML or CSS errors. HTML Validate: no errors. Axe Core: no violations at 375, 700, or 1000 px.
- A WAVE screenshot supplied after the initial commit showed the hero text overlapping later content. Simulating an injected element before `.overview` in Chrome reproduced the collapse: the `:first-child` rule no longer selected the hero. The hero now uses an explicit `.overview` selector and grid row. With the simulated injected element, hero width, position, and text containment match the unmodified page at 320, 375, 560, 590, 600, 620, 640, 660, 700, 824, 825, 1000, and 1166 px. No horizontal overflow was detected at these widths.
- Axe Core found no violations on a clean page. Inserting WAVE-like icons directly inside the five lists reproduced the five `list` violations shown when Axe DevTools and WAVE were run together; those nodes came from the WAVE extension, not `bank.html`. WAVE alone was not rerun after the hero fix.
- The user accepted the browser-tested version on 2026-10-13. The iOS Simulator could not boot (`launchd_sim could not bind to session`).
- GitHub Pages publishes from `main` at `/` and serves `https://skylarsong0107.github.io/hw3-f26/bank.html`. The public page returned HTTP 200 and loaded with its CSS and images. Canvas submission remains pending.
