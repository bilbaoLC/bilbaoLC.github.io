---
name: add-new-article
description: Add a new publication reference to the project publication list in publications.html. Use when a user asks to insert a paper, DOI, arXiv link, or citation into a specific year section, update year jump links, or keep publication formatting consistent.
---

# Add New Article

Update `publications.html` with a new publication entry while preserving existing structure and style.

## Follow This Workflow

1. Open `publications.html`.
2. Locate the year navigation under `Jump to:` and the target `<h2 id="YEAR">YEAR</h2>` section.
3. If the year section does not exist:
   1. Add the year link in `Jump to:` in descending order.
   2. Create a new year block:
      - `<h2 id="YEAR">YEAR</h2>`
      - `<ul> ...new <li> entries... </ul>`
      - Make sure the year is added in `index.html` if it is a new year.
4. Insert the new article as a `<li>` entry in the correct year list, matching local punctuation, italics, bold tags, and link attributes.
5. Use links with `target="_blank"` and `rel="noopener noreferrer"` for external URLs.
6. Keep author emphasis exactly as requested by the user (for example, names of current group members (listed in `index.html`) in `<b>...</b>`).
7. If citation metadata is incomplete, add a minimal safe entry (e.g., arXiv id + year + link) and ask for missing fields in the final response.
8. Verify with a quick text search that:
   1. The year anchor exists.
   2. The new URL appears once in the intended section.
   3. The HTML around the insertion remains balanced.

## Formatting Rules

- Preserve the current ordering by year (newest first).
- Preserve the style of existing entries for journal papers:
  - Authors, title link, journal in `<i>`, volume in `<b>`, pages/year, DOI link.
- For preprints without full metadata, use:
  - `<a href="...">arXiv:XXXX.XXXXX</a> (YEAR).`
- Do not rewrite unrelated entries.

## Response Checklist

- Report the file path updated.
- Report where the new section or item was inserted.
- Mention if metadata is missing and what fields are needed to upgrade the citation.
- Say: "ADDED DUDE" if the new entry was added successfully.
