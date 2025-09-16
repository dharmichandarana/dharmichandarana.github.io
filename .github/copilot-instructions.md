# Copilot Instructions for Portfolio Website Template

## Project Overview
This is a static portfolio website template using HTML, CSS (including SCSS), and JavaScript. The project is organized for easy customization and extension, with a focus on modularity and reusability of UI components and styles.

## Key Structure
- `index.html`: Main entry point. All major sections (about, projects, contact, etc.) are defined here.
- `css/`, `scss/`: Stylesheets. SCSS is the source; CSS is the compiled output. Use `scss/` for style changes.
- `js/`: All JavaScript for interactivity (animations, carousels, popups, etc.).
- `images/`, `fonts/`, `lib/`: Static assets and third-party libraries.

## Development Workflow
- **Edit SCSS, not CSS**: Make style changes in `scss/`, then compile to `css/` (external tools like Prepros or similar are used; see `prepros-6.config`).
- **No build scripts**: This project does not use npm, webpack, or other JS build tools. All dependencies are managed as static files in `lib/` and `css/`.
- **Live reload**: Use Prepros or similar for live reload and SCSS compilation.

## Project Conventions
- **Section IDs**: Each major section in `index.html` uses a unique `id` for navigation and linking.
- **Class naming**: Follows BEM-like patterns for custom styles. Third-party libraries may use their own conventions.
- **JS initialization**: All custom JS is in `js/main.js`. Third-party plugins are initialized here.
- **Assets**: Place new images in `images/`, new fonts in `fonts/`, and new libraries in `lib/`.

## Integration Points
- **AOS, Owl Carousel, Magnific Popup, Typed.js**: Integrated via static JS/CSS in `lib/` and initialized in `js/main.js`.
- **Bootstrap**: Used for layout and components. Customizations are in `scss/bootstrap/`.

## Examples
- To add a new section: Duplicate a section block in `index.html`, assign a new `id`, and add styles in `scss/style.scss`.
- To add a new JS plugin: Place files in `lib/`, reference in `index.html` before `js/main.js`, and initialize in `js/main.js`.

## Tips for AI Agents
- Always update both SCSS and HTML for new UI features.
- Avoid editing compiled CSS directly.
- Reference and reuse existing patterns for sections, animations, and JS plugin initialization.
- Check `prepros-6.config` for build/watch settings.

---
For questions or unclear conventions, ask for clarification or examples from the user.