# Claude Code Agents

A collection of custom agents for Claude Code, designed to enhance development workflows and automate common tasks.

## Author

**rizzo**  
GitHub: [@samuelrizzo](https://github.com/samuelrizzo)

## Repository

[https://github.com/samuelrizzo/cc-agents](https://github.com/samuelrizzo/cc-agents)

## Available Agents

### 🔍 CodeRabbit Review Handler

**File**: `.claude/agents/coderabbit-review-handler.md`  
**Model**: Sonnet

Analyzes CodeRabbit pull request reviews and implements fixes or provides technical justifications.

**Features:**

- Evaluates validity of AI-generated code review feedback
- Creates implementation plans for valid feedback
- Provides technical justifications for invalid feedback
- Follows a structured decision framework
- References project documentation (CLAUDE.md) for context

### 🔧 Lint Fixer

**File**: `.claude/agents/lint-fixer.md`  
**Model**: Sonnet  
**Color**: Blue

Automatically identifies and fixes linting errors in codebases.

**Features:**

- Scans and categorizes linting violations
- Creates KISS (Keep It Simple, Stupid) fix plans
- Executes systematic fixes (auto-fixable first)
- Validates changes don't break functionality
- Supports ESLint, Prettier, TypeScript, React/Next.js standards

### ✅ Pre-Commit Reviewer

**File**: `.claude/agents/pre-commit-reviewer.md`  
**Model**: Sonnet

Reviews code changes before committing to ensure project guideline compliance.

**Features:**

- Reads project guidelines from `/.cursor/rules` and `/CLAUDE.md`
- Auto-fixes linting issues before manual review
- Analyzes TypeScript, React/Next.js, Tailwind CSS compliance
- Checks architecture patterns, accessibility, security practices
- Creates correction plans when issues are found

## Repository Structure

```
cc-agents/
├── .claude/
│   └── agents/
│       ├── coderabbit-review-handler.md
│       ├── lint-fixer.md
│       └── pre-commit-reviewer.md
└── README.md
```

## Usage

1. Clone this repository to your development environment
2. Agents will be automatically available in Claude Code
3. Use agents as needed in your workflow:
   - **CodeRabbit Review Handler**: After receiving CodeRabbit reviews
   - **Lint Fixer**: When encountering linting errors
   - **Pre-Commit Reviewer**: Before making important commits

## Contributing

Feel free to submit issues and enhancement requests!
