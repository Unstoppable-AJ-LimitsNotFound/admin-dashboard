# Admin Dashboard

A dashboard layout recreated from The Odin Project's reference design, built with HTML and CSS. Almost everything is CSS Grid, with grids nested inside grids. It's the final project of the Intermediate HTML and CSS course.

- 🔗 [Live demo](https://unstoppable-aj-limitsnotfound.github.io/admin-dashboard/)
- 📂 [Repo](https://github.com/Unstoppable-AJ-LimitsNotFound/admin-dashboard)

## Features

- **Sidebar:** branding at the top, then two navigation groups (Home, Profile, Messages, History, Tasks, Communities; Settings, Support, Privacy)
- **Header:** search bar, notification bell and user info on top; user greeting and New / Upload / Share buttons below, with a shadow separating it from the content
- **Main content:** a grid of six project cards, an announcements panel and a trending list
- **Icons and fonts:** 15 inline SVG icons plus one externally linked SVG, Roboto from Google Fonts, and self-hosted Norse Bold for the brand heading

## Built with

- HTML
- CSS3
- [Material Design Icons](https://pictogrammers.com/library/mdi/) (SVG)
- Google Fonts (Roboto)
- [Norse Bold](https://www.joelcarrouche.com/fonts/norse) font by Joël Carrouché, self-hosted for the brand heading
- Josh Comeau's custom CSS reset as a starting point

## What I Learned

### Technical skills practised

- **Grid vs Flexbox, felt rather than read.** The brief said to lean on Grid, so I used it everywhere, and that made the difference concrete. Grid fits when the layout is decided *before* the content: you define the tracks and the content fills them. Flexbox fits when the *content* should decide, with items sized by their own intrinsic size and spaced around each other. In places where I wanted elements to spread out around their natural sizes, Grid meant guessing how much room they'd need, and I kept wishing for Flexbox. They solve different problems, and one doesn't replace the other.
- **Nested Grid layouts.** Sidebar, header and main are one grid. Inside them, the branding, nav, search bar, user info, project cards and trending list are each their own grid.
- **Two ways to use SVGs.** Inline SVGs in the HTML for icons I wanted to restyle (for example changing their fill colour with CSS), and an externally linked SVG for the logo.
- **Two ways to load web fonts.** Roboto through Google Fonts, and a downloaded font self-hosted with `@font-face`.
- **CSS reset and box shadows.** Revised a reset as a consistent starting point, and used shadows to layer the header and cards over the page.

### Development practices

- **Built outside-in.** Containers first, then each section's layout (sidebar, header, main), then the content, and assets and typography last. I used dummy content and placeholders for layout work and deliberately left icons and fonts until the structure was done.
- **Commits at meaningful checkpoints, not at tutorial steps.** I stopped matching commits to the brief's instructions. For example, the header's top row got its own commit while the bottom row was still unfinished, because it was a coherent milestone on its own.
- **Atomic commits.** One commit is one coherent change, which can include HTML and CSS together, such as the header's grid setup and the positioning of its contents. It doesn't mean one commit per element or per property. The payoff is a history that's easier to read, easier to trace a bug through, and safer to undo one change from without touching unrelated work.
- **Commit messages.** Imperative, capitalised subjects with no full stop, around 50 characters as a guide rather than a hard limit. A body only when the subject isn't enough, which I used in the final commit to document the two SVG and two font approaches. I drafted each message myself first, then refined it against what the change actually did.
- **Good to know:** `git revert` undoes an earlier commit by adding a new one, so later history stays intact. I haven't needed it yet.

## Odin requirements checklist

- [x] Git repository set up, HTML and CSS linked
- [x] Layout built with Grid: sidebar, header and main-content containers
- [x] Nested grids for sidebar branding and navigation
- [x] Nested grids for the header search bar, user info and buttons
- [x] Nested grids for projects, announcements and trending items
- [x] SVG icons from Material Design Icons
- [x] Fonts chosen and loaded (Roboto via Google Fonts)
- [x] Pushed to GitHub and published with GitHub Pages
- [ ] Responsive project cards (optional in the brief, not implemented)

## Known limitations and future ideas

- **Desktop only.** Responsiveness was optional in the brief, and the layout uses fixed sizes, so it doesn't adapt when the window is resized.
- **Sidebar and header aren't fixed.** Making them sticky so they stay put while the content scrolls is a planned polish.
- **Accessibility wasn't a focus.** Navigation items aren't links, so keyboard users can only reach the search box and buttons.
- **Static content.** Buttons and search are visual only, and all text is placeholder.
- **Grid-only by design.** Some spots would be simpler with Flexbox.

## Running locally

```bash
git clone https://github.com/Unstoppable-AJ-LimitsNotFound/admin-dashboard.git
cd admin-dashboard
```

Then open `index.html` in your browser. There's no build step.