---
name: 📝 Pull Request
about: Create a pull request to contribute to CS Professor Technical Agent Team
title: '[PR TYPE] <brief description>'
labels: ''
assignees: ''
---

## 📝 Description

A clear and concise description of the changes in this pull request.

## 🎯 Type of Change

Select the type of change your PR introduces:

- [ ] 🐛 **Bug fix** - Non-breaking change which fixes an issue
- [ ] ✨ **New feature** - Non-breaking change which adds functionality
- [ ] 💥 **Breaking change** - Fix or feature that would cause existing functionality to not work as expected
- [ ] 📚 **Documentation** - Documentation only changes
- [ ] ♻️ **Refactoring** - Code change that neither fixes a bug nor adds a feature
- [ ] ⚡ **Performance** - Performance improvement
- [ ] ✅ **Test** - Adding or updating tests
- [ ] 🔧 **Chore** - Changes to build process or auxiliary tools
- [ ] 🎨 **Style** - Changes that don't affect code meaning (whitespace, formatting, etc.)
- [ ] ♿️ **CI/CD** - Changes to CI/CD pipeline or automation

## 📸 Screenshots (if applicable)

If your changes affect the UI or generate visual output, include screenshots to demonstrate the changes:

| Before | After |
|--------|-------|
| [Screenshot 1] | [Screenshot 2] |
| [Screenshot 3] | [Screenshot 4] |

## 🔧 Changes Made

### Code Changes
- List the main files modified
- Briefly describe what each change accomplishes
- Note any refactoring or structural changes

### Documentation Changes
- List documentation files updated
- Describe documentation improvements
- Note any new documentation added

### Testing Changes
- List test files added or modified
- Describe test coverage improvements
- Note any new test cases

## 🧪 Testing

### Manual Testing
Describe any manual testing performed:
- Test case 1: Description and results
- Test case 2: Description and results
- Test case 3: Description and results

### Automated Testing
- [ ] All existing tests pass
- [ ] New tests added for new functionality
- [ ] Tests cover edge cases and error conditions
- [ ] Test coverage is maintained or improved

### Testing Environment
- **OS**: [e.g., macOS 14.2, Ubuntu 22.04, Windows 11]
- **Node.js Version**: [e.g., 18.19.0, 20.10.0]
- **Bun Version** (if applicable): [e.g., 1.0.25]
- **OpenCode CLI Version**: [e.g., 1.0.213]

## 📋 Related Issues

Does this pull request address any existing issues?

- Closes #123
- Fixes #456
- Related to #789
- Part of #1011

## 📊 Breaking Changes

### API Changes
Are there any breaking changes to the API or interfaces?
- [ ] No breaking changes
- [ ] Yes - Describe breaking changes below:

  - Change 1: Description and migration path
  - Change 2: Description and migration path

### Configuration Changes
Are there any changes to configuration or agent behavior?
- [ ] No configuration changes
- [ ] Yes - Describe configuration changes below:

  - Change 1: Description and how to handle
  - Change 2: Description and how to handle

## 📚 Documentation Updates

- [ ] README.md updated if needed
- [ ] CHANGELOG.md updated with changes
- [ ] New documentation added
- [ ] Existing documentation updated
- [ ] Inline code comments added/updated
- [ ] API documentation updated (if applicable)

### Documentation Links
- [Link to updated documentation]
- [Link to new documentation]
- [Link to API changes documentation]

## 🎯 Checklist

### Code Quality
- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings

### Testing
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published in downstream modules

### Agent-Specific Checks
- [ ] Agent YAML frontmatter is valid and complete
- [ ] Agent description is clear and concise
- [ ] Agent tools configuration is appropriate
- [ ] Agent temperature setting is appropriate
- [ ] Agent expertise sections are complete
- [ ] Pedagogical annotations are included (if applicable)
- [ ] Quality standards are documented

### Commit Messages
- [ ] Commits follow Conventional Commits specification
- [ ] Commit messages are clear and descriptive
- [ ] Commit history is clean and logical
- [ ] No merge commits or messy history

### Documentation
- [ ] README.md is updated if user-facing changes were made
- [ ] CHANGELOG.md includes an entry for this PR
- [ ] Documentation is clear, accurate, and up-to-date
- [ ] Examples are provided where appropriate
- [ ] API changes are documented (if applicable)

## 🔍 Code Review Focus

Please highlight any specific areas you'd like reviewers to focus on:

- **Area 1**: Description of why this needs extra attention
- **Area 2**: Description of why this needs extra attention
- **Area 3**: Description of why this needs extra attention

## 💭 Additional Context

Add any other context, screenshots, or examples about the pull request here.

### Implementation Notes
- Note 1: Any implementation details worth mentioning
- Note 2: Design decisions and trade-offs
- Note 3: Alternative approaches considered

### Performance Impact
- [ ] No performance impact
- [ ] Performance improvement: [Describe improvements]
- [ ] Performance regression: [Explain why it's acceptable]

### Security Considerations
- [ ] No security implications
- [ ] Security changes: [Describe security improvements or considerations]

### Known Limitations
Are there any known limitations or issues with this PR?
- Limitation 1: Description and plan to address
- Limitation 2: Description and plan to address

## 🚀 Deployment Notes

Any special considerations for deployment?

- **Migration needed**: [Yes/No] - If yes, describe migration steps
- **Configuration changes**: [Yes/No] - If yes, describe changes
- **Rollback plan**: Describe how to rollback if needed
- **Deployment order**: Any specific order for deployment steps

## 📞 After Merge

What should happen after this PR is merged?

- [ ] Create follow-up issue for remaining work
- [ ] Update related issues
- [ ] Notify stakeholders
- [ ] Schedule release (if applicable)
- [ ] Update documentation website (if applicable)

## 🙏 Acknowledgments

Who helped with this PR? Who should be credited?

- [ ] Mentored by @username
- [ ] Code review by @username
- [ ] Inspired by @username
- [ ] Thanks to @username

---

Thank you for your contribution! 🎉

**Note**: After submitting, please:
1. Ensure all CI/CD checks pass
2. Respond to review feedback promptly
3. Update the PR description if changes are needed
4. Be patient with the review process