# Git Automation Tools

A collection of intelligent Git automation commands that streamline common version control workflows with smart commit message generation and best practices enforcement.

## 🚀 Features

- **Smart Commit Messages**: Automatically generates Conventional Commits compliant messages based on code changes
- **One-Command Workflow**: Stage, analyze, and commit changes with a single command
- **Change Detection**: Intelligently categorizes changes (feat, fix, docs, style, refactor, etc.)
- **Multi-language Support**: Works with Chinese and English commit messages
- **Safety Checks**: Prevents accidental commits of sensitive files and large binaries
- **Split Commit Suggestions**: Detects mixed change types and suggests atomic commits

## 📋 Available Commands

### `/git:gcmsg` - Smart Git Commit

Automatically stages changes, analyzes code modifications, and generates appropriate commit messages following Conventional Commits specification.

**Usage:**
```
/git:gcmsg [optional-prefix]
```

**Examples:**
- `/git:gcmsg` - Auto-generate commit message for all changes
- `/git:gcmsg "fix: resolve null pointer exception"` - Use custom commit message
- `/git:gcmsg "chore: initialize project"` - Project initialization

### `/git:gcmsg-emoji` - Emoji Git Commit

Similar to gcmsg but with emoji prefixes for more visual commit history.

## 🎯 Smart Detection Rules

The tool automatically categorizes changes based on:

- **Documentation changes** → `docs: 更新文档`
- **Test files** → `test: 补充测试`
- **Bug fixes** (contains fix/bug/修复) → `fix: 修复问题`
- **New features** (contains feat/feature/新增) → `feat: 新增功能`
- **Code formatting** → `style: 调整格式`
- **Refactoring** → `refactor: 重构代码`
- **Performance improvements** → `perf: 性能优化`
- **Other changes** → `chore: 代码维护`

## 🔧 Installation

1. Clone this repository
2. Add the commands to your Claude Code configuration
3. Ensure Git is installed and configured

## 📁 Project Structure

```
.
├── git/
│   ├── gcmsg.md          # Documentation for gcmsg command
│   └── gcmsg-emoji.md    # Documentation for emoji variant
├── .gitignore
└── README.md
```

## 🛡️ Safety Features

- **Sensitive File Detection**: Warns about potential secrets or private keys
- **Large File Prevention**: Prevents accidental commits of large binaries
- **Empty Repository Check**: Ensures proper .gitignore for initial commits
- **Mixed Change Detection**: Suggests splitting commits when multiple types are detected

## 🤝 Contributing

This project is designed to improve Git workflows. Feel free to:
- Suggest new detection patterns
- Report issues or edge cases
- Propose additional commands

## 📄 License

This project is part of the Claude Code workflow tools collection.

---

**Note**: These commands are designed to work within Claude Code environment and follow specific formatting requirements for commit messages.