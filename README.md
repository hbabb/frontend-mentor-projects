# Frontend Mentor Projects

A comprehensive collection of Frontend Mentor challenges focusing on mastering fundamental web development skills through practical, real-world projects.

## 🎯 Repository Purpose

This repository serves as a dedicated workspace for Frontend Mentor challenges, emphasizing:

- **Fundamental Mastery**: Focusing on core HTML, CSS, and JavaScript skills rather than relying on frameworks
- **Progressive Learning**: Documenting growth and problem-solving approaches across projects
- **Code Maintenance**: Centralized repository for better version control and code reuse
- **Portfolio Development**: Showcasing technical progression and attention to detail

## 🏗️ Project Structure

Each project follows a consistent structure for maintainability and clarity:

```
project-name/
├── assets/
│   ├── fonts/          # Local font files (GDPR-compliant)
│   └── images/         # Project images and assets
├── css/
│   ├── global/         # Modular CSS architecture
│   │   ├── fonts.css
│   │   ├── reset.css
│   │   └── variables.css
│   └── style.css       # Main stylesheet
├── index.html          # Project entry point
└── README.md           # Project-specific documentation
```

## 📋 Current Projects

### Completed Challenges

| Project                                           | Difficulty | Technologies            | Live Demo                                                                      | Status      |
| ------------------------------------------------- | ---------- | ----------------------- | ------------------------------------------------------------------------------ | ----------- |
| [07 - Testimonials Grid](./07-testimonials-grid/) | Newbie     | HTML, CSS Grid, Flexbox | [Demo](https://hbabb.github.io/frontend-mentor-projects/07-testimonials-grid/) | ✅ Complete |

### Planned Projects

- Additional Frontend Mentor challenges (TBD)
- Previous projects to be migrated into this repository structure

## 🛠️ Development Approach

### Technology Stack

- **Languages**: HTML5, CSS3, JavaScript (ES6+)
- **Methodologies**: Mobile-first design, Progressive enhancement
- **Package Manager**: pnpm (fast, efficient package management)
- **IDE**: Visual Studio Code

### Development Tooling & Code Quality

#### Linting & Formatting

- **ESLint**: [@antfu/eslint-config](https://github.com/antfu/eslint-config) - Modern, opinionated ESLint configuration
- **ESLint Stylistic**: Integrated formatting solution (Prettier alternative)
- **Multi-language Support**: ESLint validation for HTML, CSS, JavaScript, TypeScript, Vue, and more
- **VS Code Integration**: Project-specific settings for consistent development experience

**Why @antfu/eslint-config over ESLint + Prettier?**

Traditional ESLint + Prettier setups suffer from conflicting opinions between the two tools, requiring careful configuration management to avoid conflicts. The antfu configuration solves this by integrating ESLint Stylistic, providing:

- **Unified Tooling**: Single tool handles both code quality and formatting
- **Conflict-Free Setup**: No more fighting between ESLint and Prettier rules
- **Enhanced VS Code Integration**: Automatic project configuration and intelligent rule silencing
- **Comprehensive Language Support**: Out-of-the-box support for modern web technologies

<details>
<summary>View ESLint Configuration</summary>

```javascript
// eslint.config.mjs
import antfu from "@antfu/eslint-config";

export default antfu({
  type: "app",
  vue: true,
  typescript: true,
  formatters: true,
  stylistic: {
    indent: 2,
    semi: true,
    quotes: "double",
    objectCurlySpacing: "always",
    arrowParens: "always",
    linebreaks: "unix",
  },
  ignores: [".pnpm-store/**", "node_modules/**", "**/migrations/*"],
}, {
  rules: {
    "vue/max-attributes-per-line": ["error", {
      singleline: { max: 2 },
      multiline: { max: 1 },
    }],
    "ts/consistent-type-definitions": ["error", "type"],
    "no-console": ["warn"],
    "perfectionist/sort-imports": ["error", {
      tsconfigRootDir: ".",
    }],
    "unicorn/filename-case": ["error", {
      cases: { camelCase: true, kebabCase: true },
      ignore: ["README.md"],
    }],
  },
});
```

**VS Code Workspace Settings:**

```json
{
  // Disable Prettier, use ESLint for formatting
  "prettier.enable": false,
  "editor.formatOnSave": false,

  // Auto-fix on save with ESLint
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit"
  },

  // Silent stylistic rules in IDE (auto-fix without noise)
  "eslint.rules.customizations": [
    { "rule": "style/*", "severity": "off", "fixable": true },
    { "rule": "format/*", "severity": "off", "fixable": true }
  ],

  // Enable ESLint for all supported languages
  "eslint.validate": [
    "javascript",
    "typescript",
    "vue",
    "html",
    "css",
    "scss",
    "json",
    "markdown"
  ]
}
```

</details>

#### Git Workflow & Automation

- **Husky**: Git hooks for automated quality checks
- **lint-staged**: Pre-commit linting on staged files only
- **Automated Scripts**:
  ```bash
  pnpm lint       # Run ESLint on entire project
  pnpm lint:fix   # Auto-fix ESLint issues where possible
  ```

#### Project Maintenance Philosophy

- **ESLint over Prettier**: Personal preference for ESLint's comprehensive approach to code quality
- **Pre-commit Quality Gates**: Every commit automatically linted to maintain consistent code standards
- **Modular CSS Architecture**: Organized stylesheets for maintainability and cross-project reuse
- **Local Font Management**: GDPR-compliant font implementation avoiding external API calls

### Deployment Strategy

- **Automatic Deployment**: GitHub Actions workflow deploys to GitHub Pages on main branch merge
- **Individual Project Pages**: Each challenge accessible via unique subdirectory
- **Landing Page**: Central navigation hub for all completed projects
- **Portfolio Integration**: Selected projects featured in personal Nuxt portfolio

## 📚 Learning Documentation

### Current Focus Areas

- **CSS Grid & Flexbox Mastery**: Building intuitive understanding of modern layout systems
- **Semantic HTML**: Developing accessibility-first markup practices
- **Vanilla CSS Proficiency**: Achieving framework-independent styling skills
- **Responsive Design**: Mobile-first methodology and fluid typography

### Future Documentation Plans

- `docs/` directory for learning journal and progression tracking
- Problem-solving methodologies and breakthrough moments
- Cross-project learning applications and skill transfers
- Technical decision rationale and alternative approaches considered

## 🔗 Links & Resources

### Project Links

- **Live Site**: [GitHub Pages](https://hbabb.github.io/frontend-mentor-projects/)
- **Repository**: [GitHub](https://github.com/hbabb/frontend-mentor-projects)
- **Portfolio Integration**: [heath-babb.dev](https://heath-babb.dev) _(selected projects)_

### External Profiles

- **Frontend Mentor**: [@hbabb](https://www.frontendmentor.io/profile/hbabb)
- **Twitter**: [@Heath2420](https://x.com/Heath2420)
- **Codewars**: [@hbabb](https://www.codewars.com/users/hbabb)

## 🎨 Design Philosophy

This repository represents a deliberate return to fundamentals after extensive framework experience. The goal is to achieve native-level fluency with core web technologies, treating HTML and CSS with the same intuitive comfort as spoken language.

Each project emphasizes:

- **Clean, semantic markup**
- **Maintainable, modular CSS architecture**
- **Progressive enhancement principles**
- **Accessibility-first approach**
- **Performance optimization**

## 🚀 Getting Started

### Prerequisites

- Node.js (for development tools)
- pnpm (package manager)
- Modern web browser for testing

### Local Development

1. Clone the repository:

   ```bash
   git clone https://github.com/hbabb/frontend-mentor-projects.git
   cd frontend-mentor-projects
   ```

2. Install development dependencies:

   ```bash
   pnpm install
   ```

3. **VS Code Setup** (recommended):
   - Open the project in VS Code
   - Install recommended extensions when prompted (see `.vscode/extensions.json`)
   - Extensions include ESLint, Live Server, HTML/CSS tools, and productivity enhancements

4. Run code quality checks:

   ```bash
   pnpm lint        # Check for linting issues
   pnpm lint:fix    # Auto-fix issues where possible
   ```

5. Navigate to any project directory and open `index.html` in your browser or use Live Server

6. Development workflow:
   - Make changes to project files
   - Stage changes with `git add`
   - Pre-commit hooks automatically run linting on staged files
   - Commit and push - GitHub Actions handles deployment

### Contributing to Learning

While this is a personal learning repository, feedback and suggestions are welcome through:

- GitHub Issues for technical discussions
- Twitter DMs for casual learning conversations
- Frontend Mentor community interactions

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

---

**About the Developer**: Heath Babb | HB Consultants, LLC (DBA TechSolvd) | Building mastery one challenge at a time
