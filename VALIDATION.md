# HW3 CSS Grid validation

Checked on 2026-10-13 before GitHub Pages publication.

- `bank.html` remains the entry file. The original HTML class and ID names and all three starter CSS filenames are unchanged.
- Browser widths checked: 320, 375, 700, 824, 825, and 1000 px. No horizontal page overflow was observed. The layout uses five grid columns below 825 px and seven from 825 px upward.
- The 700 px and 1000 px layouts were compared with the supplied full-page reference images.
- The skip link moves keyboard focus to `main`. The long text panel can be focused and scrolled with a keyboard at 375 px and 1000 px.
- Nu Html Checker: no HTML or CSS errors. HTML Validate: no errors. Axe Core: no violations at 375, 700, or 1000 px.
- A WAVE screenshot supplied after the initial commit showed the hero text overlapping later content. Simulating an injected element before `.overview` in Chrome reproduced the collapse: the `:first-child` rule no longer selected the hero. The hero now uses an explicit `.overview` selector and grid row. With the simulated injected element, hero width, position, and text containment match the unmodified page at 320, 375, 560, 590, 600, 620, 640, 660, 700, 824, 825, 1000, and 1166 px. No horizontal overflow was detected at these widths.
- WAVE's own interface was not rerun against this private repository. The iOS Simulator still fails to boot with `launchd_sim could not bind to session`. Manual review of the public GitHub Pages URL and Canvas submission remain pending.
