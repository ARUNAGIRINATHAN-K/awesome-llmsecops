# Contributing to Awesome LLMSecOps

First off, thank you for considering contributing to Awesome LLMSecOps! 🎉

This is a community-driven resource, and every contribution helps make it more valuable for security engineers, AI practitioners, and researchers worldwide.

## Table of Contents

- [How Can I Contribute?](#how-can-i-contribute)
- [Submission Guidelines](#submission-guidelines)
- [Quality Standards](#quality-standards)
- [Pull Request Process](#pull-request-process)
- [Style Guide](#style-guide)
- [Reporting Issues](#reporting-issues)

## How Can I Contribute?

### 🔗 Add a New Resource

The most common contribution is adding a new tool, paper, framework, or resource to the list.

1. **Fork** the repository
2. **Create a branch** (`git checkout -b add/resource-name`)
3. **Add your resource** following the [style guide](#style-guide)
4. **Submit a Pull Request** with a clear description

### 🐛 Report a Broken Link

Found a dead link? Please [open an issue](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/issues/new?template=broken_link.yml) or submit a PR with the fix.

### 📂 Suggest a New Category

Think we're missing an important category? [Open a discussion](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/discussions) to propose it.

### ✏️ Improve Descriptions

Better descriptions help everyone. If you can improve an existing description to be more accurate or informative, please submit a PR.

### 🔍 Review Pull Requests

Help us maintain quality by reviewing open PRs and providing feedback.

## Submission Guidelines

### For Tools & Frameworks

Your submission should meet **all** of the following criteria:

- [ ] **Open source** or has a **free tier/community edition**
- [ ] **Actively maintained** — commits or releases within the last 12 months
- [ ] **Directly relevant** to LLMSecOps (security of LLM/GenAI systems)
- [ ] **Well-documented** — has a README, documentation site, or usage guide
- [ ] **Not already listed** — check the existing list first
- [ ] **Proven quality** — meaningful community adoption (stars, contributors, citations)

### For Research & Papers

- [ ] **Published** or available as a preprint on recognized platforms (arXiv, ACL, NeurIPS, USENIX, IEEE, etc.)
- [ ] **Relevant** to LLM/GenAI security (not general ML or unrelated security)
- [ ] **Accessible** — freely available or has an open-access version
- [ ] **Impactful** — introduces novel concepts, techniques, or significant findings

### For Standards & Frameworks

- [ ] **From a recognized body** (OWASP, NIST, ISO, MITRE, etc.) or widely adopted by industry
- [ ] **Currently active** — not deprecated or superseded
- [ ] **Freely accessible** — the standard document or summary is publicly available

## Quality Standards

### We Accept ✅

- Open-source tools with active maintenance and clear documentation
- Peer-reviewed or preprint research papers on LLM security topics
- Industry standards and frameworks from recognized organizations
- High-quality blog posts from reputable security researchers and organizations
- Educational resources (courses, books, tutorials) with verifiable quality

### We Don't Accept ❌

- Promotional or marketing content without technical substance
- Proprietary tools with no free tier or community edition
- Resources not updated in 24+ months (unless clearly foundational/seminal)
- Duplicate entries covering the same tool or concept already listed
- Broken, paywalled, or inaccessible links
- Vague descriptions that don't explain what the resource does
- Resources unrelated to LLM/GenAI security

## Pull Request Process

### 1. Title Format

Use a clear, descriptive title:

```
Add [Resource Name] to [Category Name]
```

Examples:
- `Add PyRIT to Red Teaming & Adversarial Testing`
- `Update NeMo Guardrails description`
- `Fix broken link for MITRE ATLAS`

### 2. Description

Include in your PR description:

- **What**: Brief description of the resource
- **Why**: Why it's valuable to the LLMSecOps community
- **Where**: Which category/subsection it belongs in
- **Verification**: Confirm you've checked it meets the submission guidelines

### 3. Review Process

- PRs are reviewed within **7 days** of submission
- Maintainers may request changes or additional context
- Once approved, PRs are merged within **48 hours**
- All links are validated before merging

## Style Guide

### Resource Format

Every resource entry should follow this format:

```markdown
- [Resource Name](https://link) - Brief 1-2 sentence description explaining what it does and why it's relevant to LLMSecOps
```

### Rules

1. **Descriptions must start with a capital letter** and end with no period for single sentences
2. **Descriptions should be actionable** — explain what the tool/paper does, not just what it is
3. **Links should point to the primary source** — GitHub repo for tools, arXiv/conference page for papers
4. **Alphabetical ordering** within subsections is preferred but not required
5. **No referral links, tracking parameters, or URL shorteners**
6. **Use HTTPS** links wherever possible

### Examples

**Good** ✅
```markdown
- [Garak](https://github.com/NVIDIA/garak) - LLM vulnerability scanner with 50+ probe types covering prompt injection, data leakage, hallucination, and toxicity
```

**Bad** ❌
```markdown
- [Garak](https://github.com/NVIDIA/garak) - A great tool for LLM security.
```

## Reporting Issues

### Broken Links

If you find a broken link, please include:
- The resource name and current link
- The section where it's located
- A suggested replacement link (if available)

### Incorrect Information

If a description is inaccurate:
- Explain what's wrong
- Provide the correct information with sources
- Suggest updated text

### General Feedback

For general suggestions, questions, or discussions, please use [GitHub Discussions](https://github.com/ARUNAGIRINATHAN-K/awesome-llmsecops/discussions).

---

Thank you for helping make Awesome LLMSecOps a valuable resource for the community! 🛡️
