# Junior International Law Scholars Association

Website for JILSA, built with Jekyll and hosted on GitHub Pages.

## Local Development

### Prerequisites

**Ruby 3.3** is required (matches GitHub Pages).

Install via Homebrew:
```bash
brew install ruby@3.3

# Add to shell config (~/.zshrc or ~/.bashrc):
echo 'export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# Verify
ruby --version  # Should be 3.3.x
```

### Setup
```bash
# Use local vendor directory for gems
bundle config set --local path 'vendor/bundle'

# Install dependencies
bundle install
```

### Run locally
```bash
bundle exec jekyll serve
```

Then open http://localhost:4000 in your browser.

### Build for production
```bash
bundle exec jekyll build
```

Output goes to `_site/` directory.

## Deployment

Pushes to `main` automatically deploy to GitHub Pages via the workflow in `.github/workflows/jekyll.yml`.
