# Contributing to CS Professor Technical Agent Team

Thank you for your interest in contributing to the CS Professor Technical Agent Team! This document provides guidelines and instructions for contributing to this project.

## Table of Contents

- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Code Standards](#code-standards)
- [Agent Structure](#agent-structure)
- [Testing](#testing)
- [Documentation](#documentation)
- [Pull Request Process](#pull-request-process)
- [Code of Conduct](#code-of-conduct)

## Getting Started

### Ways to Contribute

We welcome contributions in many forms:

- **New Specialized Agents**: Create agents for new technical domains
- **Agent Enhancements**: Improve existing agent capabilities and prompts
- **Bug Fixes**: Correct issues and improve reliability
- **Documentation**: Improve or add documentation
- **Examples**: Add new usage examples and scenarios
- **Testing**: Improve test coverage and quality
- **Performance**: Optimize agent responses and coordination

### Before You Start

1. **Check Existing Issues**: Browse [open issues](https://github.com/yourusername/cs-prof-agents/issues) to find something to work on
2. **Open an Issue**: If you're planning significant changes, discuss them first
3. **Fork the Repository**: Create your own fork to work on
4. **Read the Docs**: Familiarize yourself with the project structure and existing agents

## Development Setup

### Prerequisites

- Node.js 18+ or Bun 1.0+
- OpenCode CLI (latest version)
- Git 2.20+
- Text editor with YAML and Markdown support (VS Code, etc.)

### Clone and Setup

```bash
# Fork the repository on GitHub, then clone your fork
git clone https://github.com/YOUR_USERNAME/cs-prof-agents.git
cd cs-prof-agents

# Add the original repository as upstream
git remote add upstream https://github.com/ORIGINAL_OWNER/cs-prof-agents.git

# Install dependencies
bun install
# or
npm install

# Verify OpenCode installation
opencode doctor

# Start the development environment
opencode start
```

### Development Workflow

```bash
# Create a new branch for your work
git checkout -b feature/your-feature-name
# or
git checkout -b fix/your-bug-fix

# Make your changes
# ... edit files ...

# Test your changes
opencode test

# Commit your changes
git add .
git commit -m "feat: add new agent for database optimization"

# Push to your fork
git push origin feature/your-feature-name

# Create a pull request on GitHub
```

### Keeping Your Fork Synced

```bash
# Fetch upstream changes
git fetch upstream

# Merge upstream main into your current branch
git merge upstream/main

# Or rebase your branch on top of upstream main
git rebase upstream/main

# Resolve any conflicts, then push
git push origin feature/your-feature-name --force-with-lease
```

## Code Standards

### Commit Message Conventions

We follow [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that don't affect code meaning (whitespace, formatting, etc.)
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `perf`: Performance improvement
- `test`: Adding or updating tests
- `chore`: Changes to the build process or auxiliary tools
- `ci`: CI/CD changes

**Examples:**

```
feat(web-developer): add React 18 concurrent mode support

Add support for React 18's concurrent features including:
- Suspense for data fetching
- Concurrent rendering mode
- Transition API for smooth UI updates

Closes #123
```

```
fix(algorithm-specialist): correct Dijkstra's algorithm implementation

The priority queue was not being updated correctly when
relaxing edges, leading to suboptimal paths.

Fixes #456
```

### Code Style

- **YAML Frontmatter**: All agent files must have valid YAML frontmatter
- **Markdown Formatting**: Use proper Markdown syntax with headers, lists, code blocks
- **Code Blocks**: Use proper syntax highlighting for all code examples
- **Line Length**: Keep lines under 100 characters for readability
- **Indentation**: Use 2 spaces for indentation (standard for Markdown)

### Agent File Standards

All agent files must follow this structure:

```yaml
---
description: <concise description of agent's purpose>
mode: <subagent or primary>
model: <model name, typically GLM-4.7>
temperature: <0.1-0.3, depending on agent type>
tools:
  write: <true/false>
  edit: <true/false>
  bash: <true/false>
---

<agent introduction and core mission>

## Core Expertise

<list of technical domains and capabilities>

## Quality Standards

<standards for code, implementation, and best practices>

## Pedagogical Approach

<how the agent provides educational value>

[Additional sections as needed for the agent domain]
```

## Agent Structure

### Required Sections

1. **Frontmatter**: YAML metadata with required fields
2. **Introduction**: Brief description of agent's role and expertise
3. **Core Expertise**: List of technical domains and capabilities
4. **Quality Standards**: Standards for code quality and best practices
5. **Pedagogical Approach**: How the agent provides educational value

### Recommended Sections

- **Technology Stack Recommendations**: Recommended tools and frameworks
- **Common Scenarios**: Example use cases with expected responses
- **Anti-Patterns**: Common mistakes to avoid
- **Best Practices Checklist**: Checklist for development/implementation
- **Resources and References**: Links to documentation, books, papers

### Creating a New Agent

When creating a new specialized agent:

1. **Choose a Descriptive Name**: Clear, concise name that describes the specialty
2. **Write a Compelling Description**: 1-2 sentences explaining the agent's purpose
3. **Set Appropriate Mode**: `primary` for coordinator, `subagent` for specialists
4. **Configure Tools**: Enable write/edit/bash as appropriate for the domain
5. **Define Core Expertise**: List 8-12 key technical areas
6. **Establish Quality Standards**: Reference industry best practices
7. **Include Pedagogical Approach**: How the agent provides educational value
8. **Add Examples**: 3-5 common scenarios with expected outputs
9. **Provide Resources**: Links to documentation, books, papers
10. **Test Thoroughly**: Verify agent responds appropriately to various inputs

### Example Agent Template

```yaml
---
description: New Specialist - Concise description of specialty
mode: subagent
model: GLM-4.7
temperature: 0.2
tools:
  write: true
  edit: true
  bash: true
---

You are a New Specialist agent specializing in [domain] with expertise spanning [areas]. You provide solutions that combine [quality standard 1] with [quality standard 2], suitable for [context 1] and [context 2].

## Core Expertise

### [Domain Area 1]
- **[Skill 1]**: [description]
- **[Skill 2]**: [description]
- **[Skill 3]**: [description]

### [Domain Area 2]
- **[Skill 4]**: [description]
- **[Skill 5]**: [description]
- **[Skill 6]**: [description]

[Continue with more domain areas...]

## Quality Standards

### [Standard Category 1]
- Follow [Industry Standard/Guideline]
- Implement [Best Practice 1]
- Apply [Principle 1]
- Use [Tool/Framework 1]

### [Standard Category 2]
- [Standard description]
- [Standard description]
- [Standard description]

[Continue with more standards...]

## Pedagogical Approach

### Teaching-Ready Solutions
- Provide [pedagogical technique 1]
- Include [pedagogical technique 2]
- Explain [pedagogical technique 3]
- Show [pedagogical technique 4]

### Educational Annotations
- **Learning objectives** for each [concept]
- **Key principles** and their [application]
- **Common misconceptions** and how to address them
- **Real-world applications** from [industry/research]

[Continue with more pedagogical content...]

## Common Scenarios

### [Scenario 1]
```
Request: "[example request]"
Response includes:
- [Response element 1]
- [Response element 2]
- [Response element 3]
```

[Continue with more scenarios...]

## Resources and References

### Documentation
- [Link 1] - [Description]
- [Link 2] - [Description]

### Books
- "[Book Title]" (Author)

### Learning Resources
- [Link 1] - [Description]
- [Link 2] - [Description]

[Continue with more resources...]

Provide solutions that demonstrate [quality principle 1] while maintaining standards suitable for [context].
```

## Testing

### Testing Your Changes

Before submitting a pull request, ensure:

```bash
# Run the test suite
opencode test

# Test specific agent
opencode test --agent .opencode/agent/subagents/your-agent.md

# Lint and validate YAML
opencode lint

# Run integration tests
opencode test --integration
```

### Manual Testing Checklist

- [ ] Agent responds correctly to typical requests in its domain
- [ ] Agent provides appropriate educational explanations
- [ ] Agent follows established quality standards
- [ ] Agent coordinates properly with other agents
- [ ] Agent handles edge cases gracefully
- [ ] Code blocks are properly formatted with syntax highlighting
- [ ] Examples work as documented
- [ ] Documentation is clear and accurate
- [ ] No typos or grammatical errors
- [ ] All links in references are valid

### Test Cases to Consider

When testing an agent, verify it handles:

1. **Simple requests**: Basic questions in the agent's domain
2. **Complex scenarios**: Multi-part, detailed requests
3. **Edge cases**: Unusual or boundary conditions
4. **Educational requests**: Requests that require explanations
5. **Production requests**: Requests for production-quality code
6. **Cross-domain requests**: Requests that might need coordination
7. **Ambiguous requests**: Unclear or incomplete specifications
8. **Multi-language requests**: Requests involving multiple programming languages

## Documentation

### Documentation Standards

- **Clarity**: Write in clear, concise language
- **Completeness**: Include all necessary information
- **Accuracy**: Ensure all information is correct and up-to-date
- **Tone**: Use professional, educational tone
- **Structure**: Use clear headings and logical organization
- **Examples**: Provide concrete examples for complex concepts

### Updating Documentation

When making changes that affect documentation:

1. Update relevant sections in affected agent files
2. Update the main README if adding/removing agents
3. Add examples to `usage-examples.md` if applicable
4. Update any relevant technical documentation
5. Consider adding a changelog entry for significant changes

### Writing Examples

When adding usage examples:

- Use realistic scenarios professors might encounter
- Include both simple and complex examples
- Show expected response structure
- Explain the pedagogical value
- Reference relevant learning objectives
- Connect to industry practices where appropriate

## Pull Request Process

### Before Submitting

1. **Check the PR Template**: Use the provided pull request template
2. **Test Your Changes**: Ensure all tests pass
3. **Update Documentation**: Include documentation updates
4. **Clean Commits**: Use descriptive commit messages
5. **Sync with Upstream**: Ensure your branch is up to date

### Pull Request Template

```markdown
## Description
[Brief description of changes]

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update
- [ ] Performance improvement
- [ ] Code refactoring

## Related Issues
Fixes #(issue number)
Related to #(issue number)

## How Has This Been Tested?
[Describe how you tested your changes]

## Checklist:
- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published in downstream modules
```

### PR Review Process

1. **Automated Checks**: All CI/CD checks must pass
2. **Code Review**: At least one maintainer must review and approve
3. **Feedback Addressed**: Address all review comments before merge
4. **Test Coverage**: Maintain or improve test coverage
5. **Documentation**: Ensure documentation is up to date

### After Your PR is Merged

- Celebrate! 🎉
- Watch for any follow-up issues
- Consider contributing again
- Help new contributors get started

## Code of Conduct

### Our Pledge

In the interest of fostering an open and welcoming environment, we as contributors and maintainers pledge to making participation in our project and our community a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, gender identity and expression, level of experience, nationality, personal appearance, race, religion, or sexual identity and orientation.

### Our Standards

Examples of behavior that contributes to creating a positive environment include:

- Using welcoming and inclusive language
- Being respectful of differing viewpoints and experiences
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

Examples of unacceptable behavior by participants include:

- The use of sexualized language or imagery and unwelcome sexual attention or advances
- Trolling, insulting/derogatory comments, and personal or political attacks
- Public or private harassment
- Publishing others' private information, such as a physical or electronic address, without explicit permission
- Other conduct which could reasonably be considered inappropriate in a professional setting

### Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable behavior and are expected to take appropriate and fair corrective action in response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or reject comments, commits, code, wiki edits, issues, and other contributions that are not aligned to this Code of Conduct, or to ban temporarily or permanently any contributor for other behaviors that they deem inappropriate, threatening, offensive, or harmful.

### Scope

This Code of Conduct applies both within project spaces and in public spaces when an individual is representing the project or its community. Examples of representing a project or community include using an official project e-mail address, posting via an official social media account, or acting as an appointed representative at an online or offline event. Representation of a project may be further defined and clarified by project maintainers.

### Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be reported by contacting the project team at [maintainer@example.com]. All complaints will be reviewed and investigated and will result in a response that is deemed necessary and appropriate to the circumstances. The project team is obligated to maintain confidentiality with regard to the reporter of an incident. Further details of specific enforcement policies may be posted separately.

### Attribution

This Code of Conduct is adapted from the [Contributor Covenant][homepage], version 1.4, available at [https://www.contributor-covenant.org/version/1/4/code-of-conduct.html](https://www.contributor-covenant.org/version/1/4/code-of-conduct.html)

[homepage]: https://www.contributor-covenant.org

## Getting Help

If you need help contributing:

- **Documentation**: Check the project documentation
- **Issues**: Search existing [GitHub issues](https://github.com/yourusername/cs-prof-agents/issues)
- **Discussions**: Start a [GitHub discussion](https://github.com/yourusername/cs-prof-agents/discussions)
- **Email**: Contact maintainers at [maintainer@example.com]

## Acknowledgments

Thank you for contributing to the CS Professor Technical Agent Team! Your contributions help make computer science education better for everyone.

---

**Built with ❤️ by the CS education community**