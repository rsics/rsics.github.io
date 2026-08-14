# rsics

Personal GitHub Pages site built with [Hugo](https://gohugo.io/).

## Structure

- **`content/_index.md`** — Home page
- **`layouts/`** — Hugo templates (`baseof.html`, `home.html`, `page.html`, `section.html`, `taxonomy.html`, `term.html`)
- **`public/`** — Static output deployed to GitHub Pages
- **`hugo.toml`** — Site config (baseURL set to `https://rsics.github.io/rsics/`)

The site uses the [Tella](https://github.com/opera7133/tella) Hugo theme (Tailwind-based, responsive). It's a starting point for linking to external projects and presentations (e.g., the DRI Slidev presentation in `dri-2026`).

## Hugo Setup for Local Development

### Linux (Debian/Ubuntu)

```bash
# Install Hugo (latest extended edition)
sudo apt update
sudo apt install hugo

# Or download a specific version from https://github.com/gohugoio/hugo/releases
wget https://github.com/gohugoio/hugo/releases/download/v0.145.0/hugo_extended_0.145.0_linux-amd64.tar.gz
tar -xzf hugo_extended_0.145.0_linux-amd64.tar.gz
sudo mv hugo /usr/local/bin/
```

### macOS

```bash
# Using Homebrew
brew install hugo

# Or using MacPorts
sudo port install hugo
```

### Run Dev Server

```bash
cd rsics
hugo server -D   # -D includes draft content
```

The site will be available at `http://localhost:1313/rsics/`.

### Build for Production

```bash
hugo
```

Output goes to `public/`, which can be pushed to GitHub Pages.
