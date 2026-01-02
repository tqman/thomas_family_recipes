# CLAUDE.md

If a file named @CLAUDE.local.md exists in this directory, read it first. Any instructions there take precedence.

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal recipe collection for the Thomas family. All recipes are stored as plain text files (.txt) with a few markdown files for meal planning.

## Repository Structure

- **Root directory**: Individual recipe files (e.g., `pizza.txt`, `chicken_tikka_masala.txt`)
- **`meal_plans/`**: Weekly meal planning documents organized by date (YYYYMMDD.md format)
- **`thanksgiving/`**: Thanksgiving dinner menus, timelines, and shopping lists organized by year
- **`christmas/`**: Christmas meal planning organized by year
- **`high_altitude_notes.txt`**: Important baking adjustments for high-altitude cooking (~5,200 feet in northern Colorado)

## File Format Conventions

Recipe files are plain text with a loose structure:
- Recipes often include revision dates in YYYYMMDD format, but this predates being tracked in git and should not be continued with new files.
- Many recipes include source URLs or cookbook references
- Some recipes contain notes from previous iterations, but again this predates git and should not be continued in new recipes
- Meal plans for major holidays include "after-action reports" to improve next year's performance (yes this repository is SEI SMM Level 4!)
- High-altitude adjustments may be noted within individual recipes or refer to `high_altitude_notes.txt`

Meal planning files use markdown with day-of-week headers listing planned meals.

Holiday planning files (thanksgiving/, christmas/) include:
- Complete menus with serving times
- Detailed timelines with specific start times
- Shopping lists and ingredient quantities
- After-action reports with improvements for next year

## Common Tasks

### Finding a recipe
Use Grep to search recipe contents or Glob to find files by pattern:
```
grep -i "pattern" **/*.txt
```

### Viewing meal plans
Meal plans are in `meal_plans/` with YYYYMMDD.md naming convention. The most recent ones show the current meal planning style.

### Working with holiday menus
Thanksgiving and Christmas directories contain year-specific planning files. Recent years (2023, 2024) contain the most detailed timelines and after-action reports for planning future events.

## Notes
- Git is used for version control but many new recipes remain uncommitted (see git status)
- Recipe format is intentionally informal and personal
- No build, test, or lint commands needed - this is a text-based recipe collection

## Creating new recipes or converting from text to markdown
- This original collection dates from 2002 and was originally text files
- Recently have begun converting files to markdown so they display better on GitHub

## Converting text files to markdown
- When converting a text file to markdown, see [TEMPLATE.md](TEMPLATE.md) for rough formatting guidance, but use your judgement if a more complicated recipe doesn't fit within that format perfectly
- When converting a text file to markdown, it's important to preserve the checkin history. So:
  1. Edit the existing text file in place and make it so that it is internally markdown
  2. Ensure to keep ALL of the data in the original. Do not drop any information because it doesn't fit into the template; make a place for it. It is better to violate the template than to lose information.
  3. `git mv` the `.txt` file to `.md`.
  4. At this point the process is complete; there is no need to verify anything or preform diffs with GitHub.
