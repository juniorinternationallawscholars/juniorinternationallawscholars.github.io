# Junior International Law Scholars Association

Website for JILSA, built with Jekyll and hosted on GitHub Pages.

## Ownership & Handoff

The domain was originally registered by **Haley S. Anderson**. She cannot provide IT support or respond to requests about this site. **After 2026, do not contact her about this website.**

When responsibility for the site changes hands, the outgoing owner should pass along:

1. Credentials for the shared email account (`juniorinternationallawscholars@gmail.com`)
2. Access to this GitHub repository

GitHub credentials are currently stored in **1Password**. Haley holds the original passkey.

All changes to the website should be made through GitHub — never edit the live site directly.

## Editing the Website (No Coding Experience Needed)

You can make changes entirely in your web browser. You do not need to install anything.

### One-time setup

1. Create a free account at [github.com](https://github.com).
2. Ask the current site owner to add you as a collaborator on this repository.
3. Accept the invitation email from GitHub.

### Making a change

1. Go to the repository on github.com and find the file you want to edit:
   - **`index.md`** — the homepage text (About, Contact, etc.)
   - **`_config.yml`** — site title and basic settings
   - **`assets/`** — images and styles
   - **`_layouts/default.html`** — the page template (header, footer, layout)
2. Click the file name to open it.
3. Click the pencil icon (✏️) in the top-right to edit.
4. Make your changes in the browser.
5. Scroll down to **Commit changes**.
   - Add a short description of what you changed (e.g. "Update contact email").
   - Choose **Commit directly to the `main` branch**.
   - Click **Commit changes**.
6. Wait 1–2 minutes. The site will rebuild automatically and your change will appear at the live URL.

### How to know it worked

- Go to the **Actions** tab on the repository. You'll see a workflow running. A green checkmark means the site updated successfully. A red X means something went wrong — open the failed run to see the error.
- Then refresh the live site in your browser.

### If you make a mistake

Every change is saved in the history. To undo:

1. Go to the **Commits** view of the repository.
2. Find the change that caused the problem.
3. Click the commit, then click **Revert** at the top right.
4. Confirm. This creates a new commit that undoes the bad one.

## Local Development (For Developers)

If you want to preview changes on your computer before publishing, you'll need Ruby installed.

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
