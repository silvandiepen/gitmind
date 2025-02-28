<picture>
  <source srcset="https://github.com/user-attachments/assets/fbf3f128-e0e6-4ff6-b05c-315521b89749" media="(prefers-color-scheme: dark)">
  <img src="https://github.com/user-attachments/assets/90aa081c-4cce-41fa-9c9b-03bd908a8b20" alt="Logo" width="200">
</picture>

# GitSage

An intelligent Git commit message generator powered by OpenAI's GPT-4. This tool analyzes your staged changes and automatically generates meaningful, conventional commit messages.

## Features

- 🤖 AI-powered commit message generation
- 📝 Conventional commit format support
- 🔍 Smart change analysis and grouping
- ✨ Interactive commit message selection
- 🛠️ Easy configuration and setup
- 🔄 Interactive fixup for commit amendments
- 📋 AI-powered PR content generation

## Quick Start

You can use gitsage directly without installation using npx:

```bash
npx gitsage
```

### Optional Installation

If you prefer, you can install the package globally:

```bash
npm install -g gitsage
```

## Configuration

Before using gitsage, you'll need to configure your OpenAI API key. The tool will prompt you for the key on first use, or you can set it up manually:

1. Get your API key from [OpenAI's platform](https://platform.openai.com/)
2. The tool will automatically store your API key securely for future use

## Usage

1. (Optional) Stage your changes using git add:
```bash
git add <files>
```

2. Run gitsage:
```bash
gitsage
```

3. Review and confirm the generated commit messages

Note: If no changes are staged, gitsage will automatically help you select which files to stage through an interactive interface. This makes the staging process optional and more user-friendly.

### Using Pull Request Generation

To generate a pull request with AI-powered content:

```bash
gitsage pr
```

This will:
1. Detect your Git platform (GitHub/Bitbucket)
2. Analyze the changes between your current branch and target branch
3. Generate a well-structured PR description including:
   - Title and description
   - Problem statement
   - Solution overview
   - List of changes
   - Testing details
4. Create the PR using the platform's CLI tool (gh/bb)

Requirements:
- GitHub CLI (gh) for GitHub repositories
- Bitbucket CLI (bb) for Bitbucket repositories

### Using Fixup

The fixup command allows you to amend changes to a previous commit:

```bash
gitsage fixup
```

This will:
1. Show your current changes
2. Let you select a commit to fixup into
3. Create a fixup commit and automatically rebase

It's useful when you want to:
- Add forgotten changes to a previous commit
- Fix bugs in earlier commits
- Keep your commit history clean and organized

## How It Works

1. Analyzes staged Git changes
2. Splits large diffs into manageable chunks
3. Uses GPT-4 to analyze changes and generate appropriate commit messages
4. Groups related changes together
5. Presents commit suggestions for your approval
6. Creates commits using conventional commit format

## Commit Types

The tool generates commits following the conventional commits specification:

- `feat`: New features
- `fix`: Bug fixes
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes using the tool itself! (`gitsage`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Powered by OpenAI's GPT-4
- Inspired by conventional commits
- Built with TypeScript and Node.js
