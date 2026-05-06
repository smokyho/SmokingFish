# AGENTS.md - MiroFish Project Agent Guidelines

This document defines the rules and best practices for AI agents (such as Kilo) working on the MiroFish project codebase. All agents must follow these guidelines to ensure consistency, quality, and adherence to the project's vision.

## Project Overview
MiroFish is a swarm intelligence engine for multi-agent simulations, enabling predictions of real-world events through digital parallel worlds. The codebase includes:
- **Frontend**: Vue.js application with internationalization support
- **Backend**: Python FastAPI application with multi-agent simulation logic
- **Architecture**: Multi-agent system using LLMs for autonomous behavior simulation

## General Rules

### 1. Code Language and Localization
- **All code comments, docstrings, and internal strings must be written in English**
- **User-facing text must use the i18n system** (`locales/en.json`, `locales/zh.json`)
- Do not hardcode Chinese or English text in code; use translation keys
- When adding new user-facing strings, add entries to both locale files

### 2. Coding Standards
- **Python**: Follow PEP 8 style guide, use type hints, maintain 88-character line limits
- **JavaScript/Vue**: Follow Vue.js style guide, use ESLint configuration, maintain consistent formatting
- **Commit Messages**: Write clear, concise English commit messages following conventional commits format
- **Documentation**: Write technical documentation in English with bilingual README support

### 3. Architecture Compliance
- Maintain separation between frontend (Vue) and backend (Python/FastAPI)
- Follow the established multi-agent architecture patterns
- Preserve the simulation workflow: Graph Building → Environment Setup → Simulation → Report Generation → Deep Interaction
- Do not modify core simulation logic without thorough testing

### 4. Security and Best Practices
- Never commit sensitive information (API keys, credentials) to version control
- Validate all user inputs and API responses
- Implement proper error handling with English error messages
- Follow Docker best practices for containerization

### 5. Testing and Quality Assurance
- Write unit tests for new functionality
- Run existing test suites before committing changes
- Ensure cross-platform compatibility (Windows/Linux/macOS)
- Test both English and Chinese locales for UI changes

### 6. Git Workflow
- Create feature branches for new work
- Use meaningful branch names (e.g., `feature/add-simulation-metrics`, `fix/locale-loading-bug`)
- Keep commits atomic and focused on single changes
- Rebase feature branches before merging to main

### 7. Internationalization (i18n)
- Use Vue i18n plugin for frontend localization
- Backend API responses should support language parameters when appropriate
- Maintain consistency between `en.json` and `zh.json` locale files
- Test locale switching functionality

### 8. Agent Communication
- Provide clear, technical responses without conversational fluff
- Use tools efficiently to gather information before making changes
- Create todo lists for complex multi-step tasks
- Suggest code reviews only after completing substantial implementation work

### 9. Environment and Dependencies
- Respect the established development environment (Node.js 18+, Python 3.11-3.12)
- Use `uv` for Python dependency management as specified
- Follow the setup scripts and Docker configuration
- Do not modify build/deployment scripts without coordination

### 10. Ethical Guidelines
- Respect user privacy and data protection
- Ensure simulation outputs are clearly marked as AI-generated predictions
- Maintain neutrality in political/social simulations
- Follow responsible AI practices in multi-agent behavior modeling

## Task-Specific Guidelines

### Code Translation Tasks
When translating code from Chinese to English:
1. Identify all Chinese comments, docstrings, and hardcoded strings
2. Translate accurately while preserving technical meaning
3. Replace with appropriate English equivalents
4. Test that functionality remains intact after translation
5. Update any related documentation

### Feature Implementation
1. Understand the multi-agent simulation context
2. Ensure changes align with the swarm intelligence paradigm
3. Add comprehensive tests for new features
4. Update documentation and locale files as needed

### Bug Fixes
1. Reproduce the issue in both development and production environments
2. Implement minimal, targeted fixes
3. Add regression tests
4. Verify fixes work across all supported platforms

## Emergency Procedures
- If critical security issues are discovered, immediately notify project maintainers
- For breaking changes, create detailed migration guides
- In case of data loss risks, backup before destructive operations

All agents confirm they have read and will follow these guidelines in all future tasks on the MiroFish project.</content>
<parameter name="filePath">D:\GitHub\SmokingFish\AGENTS.md