# AIDLC Boilerplate: AI-Driven Development Template

A production-ready boilerplate for building software projects with **AI-assisted development using Claude Code**. This template establishes safety guardrails, architectural patterns, and best practices to enable efficient, scalable development workflows powered by Claude AI.

---

## 🎯 Purpose

This boilerplate provides a foundational structure for projects built using [Claude Code](https://claude.com/claude-code) and the [Claude Agent SDK](https://github.com/anthropics/claude-agent-sdk). It codifies essential guardrails, context modes, and execution discipline to ensure:

- **Safety**: Secure handling of credentials and sensitive data
- **Quality**: Consistent code patterns and architecture
- **Scalability**: Clear progression from greenfield to brownfield development
- **Efficiency**: AI-assisted workflows with defined decision points

---

## 🚀 Key Features

### 🔒 Safety & Security Guardrails
- Prevents accidental exposure of secrets (API keys, tokens, credentials)
- Enforces secure data handling practices
- Validates destructive operations before execution
- Protects codebase integrity through migration discipline

### 🧭 Dual-Mode Development
- **GREENFIELD**: Build from scratch with clear architectural foundations
- **BROWNFIELD**: Maintain existing systems with minimal, incremental changes
- Automatic mode detection based on codebase state

### 🧠 AI-Assisted Execution
- Structured prompting for consistent AI behavior
- Skill-based task workflows (debugging, features, refactoring)
- Guardrail-enforced decision-making
- Output constraints for minimal, focused diffs

### ⚖️ Execution Discipline
- Explicit approval gates for risky operations
- Plan-first methodology for complex tasks
- Clear priority ordering (Safety > Guardrails > Context > Intent)
- Anti-pattern prevention

---

## 📋 Project Structure

```
aidlc-boilerplate/
├── CLAUDE.md              # AI execution guardrails & context modes
├── README.md              # This file
├── LICENSE                # MIT License
└── .git/                  # Git repository
```

### What Goes Where

When extending this template:

```
your-project/
├── CLAUDE.md              # Copy & customize guardrails for your project
├── src/                   # Application source code
│   ├── components/        # Reusable modules
│   ├── services/          # Business logic & abstraction layers
│   ├── utils/             # Utilities & helpers
│   └── types/             # Type definitions
├── tests/                 # Test suites
├── docs/                  # Project documentation
├── .env.example           # Environment variable template (NO SECRETS!)
├── package.json           # Dependencies (language-specific)
└── README.md              # Project-specific documentation
```

---

## 🌱 GREENFIELD Mode: Starting Fresh

### When to Use
- Building a new application from scratch
- Establishing foundational architecture
- No existing codebase constraints

### Best Practices

1. **Define Structure First**
   ```
   ✅ Establish folder hierarchy (3-5 levels max)
   ✅ Define core abstractions (services, models, utilities)
   ✅ Choose widely-accepted patterns
   ```

2. **Build Incrementally**
   ```
   ✅ Start with MVP scope
   ✅ Add features in layers (core → extended)
   ✅ Refactor as you learn, not speculatively
   ```

3. **Avoid Over-Engineering**
   ```
   ❌ Don't build for hypothetical future requirements
   ❌ Don't add abstraction layers before they're needed
   ❌ Don't optimize prematurely
   ```

### Example Workflow

```bash
# 1. Create project from this template
cp -r aidlc-boilerplate my-project
cd my-project

# 2. Customize CLAUDE.md for your project
# - Update technology stack details
# - Add domain-specific guardrails
# - Define architectural patterns

# 3. Set up git & initial structure
git init
mkdir -p src/components src/services src/utils
touch src/index.ts

# 4. Begin development with Claude Code
# - Run: claude code .
# - AI will follow CLAUDE.md guardrails automatically
```

---

## 🏗️ BROWNFIELD Mode: Existing Systems

### When to Use
- Working within an established codebase
- Integrating new features into existing architecture
- Maintaining system consistency

### Best Practices

1. **Respect Existing Patterns**
   ```
   ✅ Follow existing naming conventions
   ✅ Reuse established services & abstractions
   ✅ Match surrounding code style
   ```

2. **Make Minimal Changes**
   ```
   ✅ Scope changes to the task at hand
   ✅ Avoid unrelated refactors
   ✅ Prefer incremental diffs over rewrites
   ```

3. **Maintain Compatibility**
   ```
   ✅ Test against existing code paths
   ✅ Keep migrations forward-only
   ✅ Don't bypass abstraction layers
   ```

### Example: Adding a Feature

```bash
# 1. Examine existing patterns
grep -r "service pattern" src/services/
git log --oneline | head -10

# 2. Create isolated changes
# - Add feature in existing folder structure
# - Use same naming & patterns as surrounding code

# 3. Test compatibility
npm test
npm run lint

# 4. Commit with context
git commit -m "Add X feature following [existing pattern]"
```

---

## 🔐 CLAUDE.md: The AI Execution Manifesto

The `CLAUDE.md` file is the core of this template—it defines how Claude AI should behave in your project:

### Key Sections

#### 🚨 Global Guardrails
- Safety & security (secrets, logging)
- Destructive action gates
- Codebase integrity rules
- Architecture boundaries
- Output constraints

#### 🧭 Context Modes
- **GREENFIELD**: Build foundations cleanly
- **BROWNFIELD**: Preserve and extend
- Auto-detection based on codebase state

#### 🧠 Skill Usage Policy
- Task-specific workflows
- Debugging, feature development, refactoring patterns
- Integration with Claude Code superpowers

#### ⚖️ Priority Order
1. Safety & Security
2. Guardrails
3. Context Mode
4. User Intent
5. Skill Workflow
6. Optimization

### Customizing for Your Project

```markdown
# CLAUDE.md Template
---

# 🚨 GLOBAL GUARDRAILS (adapt these to your needs)

## 🔒 Safety & Security
* [Your project-specific secret handling rules]
* [Database access controls]
* [API key management]

## ⚠️ Destructive Actions
* [Your specific approval gates]
* [Environmental safety checks]

## 📦 Codebase Integrity
* [Your migration strategy]
* [Generated file handling]
* [Dependency approval process]

## 🧱 Architecture Boundaries
* [Your core abstractions]
* [Service layer patterns]
* [Module boundaries]

---

# 🧭 CONTEXT MODE

## 🌱 GREENFIELD MODE
* [Your initial architecture setup]
* [Core services to build first]
* [Scalability considerations]

## 🏗️ BROWNFIELD MODE
* [Existing patterns to follow]
* [Architecture you won't change]
* [Integration points]

---

# 🧠 SKILL USAGE POLICY

* [Your testing strategy]
* [Code review process]
* [Deployment workflow]

---

# 🧾 RESPONSE STYLE

* [Communication preferences]
* [Documentation expectations]
* [Code comment standards]
```

---

## 🛠️ Getting Started

### Prerequisites
- [Claude Code CLI](https://claude.com/claude-code) installed
- Git initialized
- Node.js / Python / Your language runtime

### Quick Setup

```bash
# 1. Clone or copy this template
git clone <this-repo> my-new-project
cd my-new-project

# 2. Customize for your needs
# - Update CLAUDE.md with your project specifics
# - Create initial folder structure
# - Add package.json or language-specific config

# 3. Initialize git & first commit
git add .
git commit -m "Initial commit: AIDLC boilerplate setup"

# 4. Start development
claude code .
```

---

## 💡 Usage Examples

### Example 1: Building a REST API (GREENFIELD)

```bash
# 1. Your CLAUDE.md includes:
# - API design patterns (REST vs GraphQL)
# - Authentication approach
# - Error handling standards

# 2. Claude Code will:
# - Create folder structure: routes/, middleware/, models/
# - Generate schemas and service layers
# - Follow your guardrails automatically

# 3. Prompt Claude Code:
"Build a REST API for user management following CLAUDE.md patterns"
# → Gets architecture blueprint + implementation
```

### Example 2: Adding Auth to Existing App (BROWNFIELD)

```bash
# 1. Your CLAUDE.md includes:
# - Current authentication pattern
# - Services not to modify
# - Integration points

# 2. Claude Code will:
# - Examine existing auth middleware
# - Create minimal new files
# - Integrate with existing abstractions
# - Follow established patterns

# 3. Prompt Claude Code:
"Add JWT refresh token support to existing auth"
# → Gets targeted changes, preserves system stability
```

### Example 3: Debugging Test Failures

```bash
# 1. Run /code-review to understand issues
/code-review

# 2. Claude Code will:
# - Identify root causes
# - Follow guardrails for test data handling
# - Suggest fixes aligned with CLAUDE.md

# 3. Use /verify to confirm changes work
/verify
```

---

## 🎓 Best Practices for AI-Assisted Development

### ✅ Do's

- **Ask before risky actions**: Destructive operations, deployments, migrations
- **Provide context**: Link issues, PRs, documentation in your prompts
- **Verify changes**: Run tests and manually confirm behavior
- **Iterate incrementally**: Small changes, frequent testing
- **Review guardrails**: Keep CLAUDE.md up-to-date as you learn

### ❌ Don'ts

- **Don't assume**: Always clarify ambiguous requirements
- **Don't skip guardrails**: They exist to prevent mistakes
- **Don't over-commit**: Batch related changes, not everything
- **Don't bypass safety**: Never skip security checks for speed
- **Don't ignore errors**: Investigate and fix root causes

---

## 🔄 Development Workflow

```
┌─────────────────────────────────────────────────┐
│  1. Define in CLAUDE.md                         │
│     (guardrails, patterns, context mode)        │
└─────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────┐
│  2. Prompt Claude Code                          │
│     (clear requirements + context)              │
└─────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────┐
│  3. Review Generated Changes                    │
│     (guardrails enforced automatically)         │
└─────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────┐
│  4. Test & Verify                               │
│     (/verify, manual testing, git diff)         │
└─────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────┐
│  5. Commit & Deploy                             │
│     (guardrails approve safe operations)        │
└─────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────┐
│  6. Update CLAUDE.md (as needed)                │
│     (learn + refine guardrails)                 │
└─────────────────────────────────────────────────┘
```

---

## 📚 Learn More

### Claude Code Resources
- [Claude Code Documentation](https://claude.com/claude-code)
- [Claude Agent SDK](https://github.com/anthropics/claude-agent-sdk)
- [Claude API Docs](https://docs.anthropic.com)

### Development Concepts
- [Guardrails for AI Safety](https://en.wikipedia.org/wiki/AI_safety)
- [GREENFIELD vs BROWNFIELD Development](https://en.wikipedia.org/wiki/Greenfield_project)
- [Incremental Development](https://en.wikipedia.org/wiki/Iterative_and_incremental_development)

### Example Projects
- This boilerplate can be extended for:
  - Web apps (Next.js, React, Vue)
  - APIs (Node.js, Python, Go)
  - CLI tools
  - Data pipelines
  - Mobile apps

---

## 📝 License

This boilerplate is licensed under the [MIT License](LICENSE).

```
Copyright (c) 2026 TheTechnologyTribe

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 🤝 Contributing

This is a template repository. To improve it:

1. **Fork & Customize**: Create your own version for your organization
2. **Document Learnings**: Update CLAUDE.md as you discover patterns
3. **Share Improvements**: Contribute back guardrails that helped your project
4. **Refine Context Modes**: Add domain-specific GREENFIELD/BROWNFIELD guidance

---

## 🆘 Support & Feedback

- **Issues & Questions**: Check Claude Code documentation first
- **Guardrail Issues**: Review CLAUDE.md and git history for context
- **Template Improvements**: Fork and customize for your needs
- **AI Behavior**: Adjust CLAUDE.md to steer Claude Code appropriately

---

## 🎯 Quick Reference

### Key Files
| File | Purpose |
|------|---------|
| `CLAUDE.md` | AI execution guardrails & patterns |
| `README.md` | Project documentation |
| `LICENSE` | MIT license |

### Common Commands
```bash
# Start development
claude code .

# Review changes
/code-review

# Verify implementation
/verify

# Simplify code
/simplify

# Run tests
npm test

# Commit with context
git commit -m "Feature: [description]"
```

### CLAUDE.md Priority Order
1. 🔒 Safety & Security
2. 🚨 Guardrails
3. 🧭 Context Mode (GREENFIELD/BROWNFIELD)
4. 👤 User Intent
5. 🧠 Skill Workflow
6. ⚡ Optimization

---

## 🚀 Next Steps

1. **Customize CLAUDE.md** for your project's tech stack and architecture
2. **Create initial folder structure** for your use case
3. **Define guardrails** specific to your domain (database, APIs, security)
4. **Start building** with Claude Code and let AI accelerate your workflow
5. **Refine patterns** as you discover what works best for your team

---

**Built with ❤️ for AI-assisted software development**
