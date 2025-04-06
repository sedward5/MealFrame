# MealFrame

**Plan meals. Track your history. Generate grocery lists. Self-hosted simplicity.**

MealFrame is an open-source Hugo-based tool for planning meals by the week. It’s built to support flexible planning (including multiple dishes per day), generate helpful grocery lists, and archive meal history in a way that’s easy to browse. You can host your own recipes or import others using structured JSON-LD. Everything runs statically — no databases, no servers.

---

## Table of Contents

- [Project Goals](#project-goals)
- [How It Works](#how-it-works)
- [Key Features](#key-features)
- [File Structure](#file-structure)
- [Roadmap](#roadmap)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)

---

## Project Goals

MealFrame is designed to solve a real-world problem: how to easily plan meals week by week, track what you’ve cooked before, and make grocery shopping a breeze — all with the option of using your own recipes or pulling from trusted blogs.

It’s also meant to be:

- **Open-source and extendable**: Contributions welcome!
- **Self-hosted**: Static-site powered by [Hugo](https://gohugo.io).
- **Structured**: Machine-readable data, ready for automation.
- **Pragmatic**: Designed for real-life use — Sunday planning sessions, weekday cooking, and Friday fridge clean-outs.

---

## How It Works

MealFrame uses Hugo and Markdown to generate a static site that contains:

- A **weekly planner view**: see what’s for dinner each day.
- **Recipe pages**: either written in Markdown or imported from external blogs using [JSON-LD](https://developers.google.com/search/docs/appearance/structured-data/recipe).
- A **grocery list generator**: pulls ingredients from planned recipes and consolidates them.
- A **recipe archive**: your personal cooking history, searchable and taggable.

### Under the Hood

- Weekly meal plans are defined in front matter or data files.
- Recipes live in `/content/recipes/`, with support for:
  - Markdown-based recipes
  - Imported recipes (via script or plugin that parses JSON-LD)
- Hugo shortcodes or layouts render plans, lists, and history.
- GitHub Actions (or your CI of choice) builds and deploys the site.

---

## Key Features

- Plan by the week: Sunday through Saturday
- Track full meals (main + side + veg + etc.)
- Generate consolidated shopping lists
- Host your own recipes
- Import from other blogs using structured data
- Browse meal history
- Mobile-friendly layout
- Easy to deploy (GitHub Pages, Netlify, etc.)

---

## 📁 File Structure

```
MealFrame/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── feature_request.yml
│   │   └── config.yml
│   └── workflows/
│       └── deploy.yml               # GitHub Actions deploy script (optional but useful)
├── archetypes/
│   └── default.md
├── content/
│   ├── _index.md
│   └── recipes/                     # Markdown-based recipe content
├── data/
│   └── mealplans/                   # Where weekly plans can live as .yaml or .json
├── layouts/
│   └── _default/                    # (Optional) overrides for Ananke layout
├── static/
│   └── images/
├── themes/
│   └── ananke/                      # Submodule
├── .gitignore
├── config.toml                      # Hugo config
├── hugo.toml                        # Optional alternate config for environments
├── LICENSE
├── README.md
└── DEPLOY.md                        # Deployment documentation
```

---

## Roadmap

Check out the [GitHub Projects board](https://github.com/YOUR_USERNAME/MealFrame/projects) for current issues and feature planning.

Planned upcoming features:

- [ ] Shopping list export (PDF / plain text)
- [ ] Recipe tagging and filtering
- [ ] GitHub Action deployment setup
- [ ] UI theming / custom CSS support
- [ ] Reorderable meals within days

---

## Getting Started

MealFrame is still in early development. Here's how to get involved:

### 1. Clone the repo

```bash
git clone https://github.com/YOUR_USERNAME/MealFrame.git
cd MealFrame
```

### 2. Install Hugo

Follow the [official Hugo install guide](https://gohugo.io/getting-started/installing/).

### 3. Serve the site locally

```bash
hugo server
```

### 4. Start planning meals!

Check out the `/content/` and `/data/` directories for how meal plans and recipes are structured.

---

## Contributing

Contributions are welcome! This is a solo-used tool with community aspirations.

### Ways to help:

- Add new features (see [feature requests](https://github.com/YOUR_USERNAME/MealFrame/issues))
- Improve the layout or theme
- Write documentation or sample recipes
- Report bugs or suggest UX improvements

### To contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/some-feature`)
3. Commit your changes
4. Open a Pull Request

See the [CONTRIBUTING.md](CONTRIBUTING.md) file for details (coming soon).

---

## License

MIT License — see [`LICENSE`](LICENSE) for details.

---

> *MealFrame is still in alpha. The fridge is full, but the site is half-baked — join in and help cook it up!*
