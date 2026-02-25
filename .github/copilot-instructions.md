# Copilot Instructions for 7heknight (GitHub Profile README)

## Repository Purpose
This is a **GitHub profile README** repository (`7heknight/7heknight`). The sole deliverable is `README.md`, which renders as the landing page on [github.com/7heknight](https://github.com/7heknight).

## Architecture & Key Components
- **`README.md`**: Profile page using raw HTML inside Markdown; contains GitHub Stats widgets (via `github-readme-stats.vercel.app`) and social badge links
- **No build system, tests, or runtime dependencies** — this is a static Markdown/HTML file served directly by GitHub

## Content Structure in `README.md`
- **Header**: Animated typing SVG via `readme-typing-svg.demolab.com` — cycles through greeting lines, centered
- **Profile views**: Counter badge via `komarev.com/ghpvc/` with `flat-square` style
- **Stats row**: Two `<img>` tags inside a `<kbd>` wrapper — general stats + top languages, both from `github-readme-stats` API
- **Streak stats row**: GitHub streak card via `streak-stats.demolab.com` inside a `<kbd>` wrapper, themed to match
- **Social links row**: Shield.io badge links (Facebook, LinkedIn, GitHub) using `style=for-the-badge` with colored backgrounds
- **Styling approach**: Inline HTML with `align="center"` on `<p>` tags; transparent backgrounds (`bg_color=00000000`) and GitHub blue text (`text_color=58a6ff`, `#58A6FF`)

## Project-Specific Patterns & Conventions
- All layout uses raw HTML (`<p>`, `<h1>`, `<kbd>`, `<a>`, `<img>`) rather than native Markdown — preserve this pattern when editing
- Stats widget URLs use query params for theming: `bg_color`, `text_color`, `hide_border`, `disable_animations` — keep these consistent across widgets
- Social badges use `img.shields.io` with `style=for-the-badge` and colored backgrounds (e.g., `Facebook-1877F2`) — follow this pattern for any new links
- Username reference is `7heknight` (lowercase 'h') everywhere in URLs

## Notes for AI Agents
- **No build/test/deploy steps exist** — changes are live on push to `main`
- When adding new stats widgets, use the same transparent-background theme params: `bg_color=00000000&text_color=58a6ff&hide_border=true&disable_animations=true`
- Streak stats use different param names but the same color: `ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff&sideLabels=58a6ff&dates=8b949e&hide_border=true`
- Typing SVG uses `color=58A6FF` (uppercase hex) and `font=Fira+Code` — keep font/color consistent if editing
- GitHub renders profile READMEs with limited HTML support — avoid `<style>`, `<script>`, `<iframe>`, or CSS classes (they are stripped)
- The `<kbd>` tag around stats images adds a subtle border effect — this is intentional styling
- Keep the file concise; GitHub truncates long profile READMEs with a "Read more" fold
