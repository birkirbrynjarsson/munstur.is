# Munstur og Menning — munstur.is

Website for **Munstur og Menning**, a small Icelandic publishing operation run by Jenný Karlsdóttir of Akureyri. The site showcases republished Icelandic traditional craft books and documents a long-running research project cataloguing church altar cloths (*altarisdúkar*) across Iceland.

## Pages

| Page | URL | File | Description |
|------|-----|------|-------------|
| Heim | `/` | `index.html` | Front page with slideshow |
| Bækurnar | `/portfolio` | `portfolio.html` | Book catalogue |
| Altarisdúkar | `/altarisdukar` | `altarisdukar.html` | Altar cloth research project |
| Altarisdúkamunstur | `/altarisdukamunstur` | `altarisdukamunstur.html` | Altar cloth embroidery patterns |
| Munstur.is | `/munstur` | `munstur.html` | About the publisher |

### Book sub-pages (`/baekur/`)

`/baekur/hannyrdir`, `/baekur/vefnadur`, `/baekur/utsaumur`, `/baekur/jurtalitun`, `/baekur/gomul_mynstur`, `/baekur/milliverk`, `/baekur/munsturbekkir`, `/baekur/stafabaekur`, `/baekur/utskurdarmynstur`, `/baekur/utsogunarmynstur`, `/baekur/tuskudyr`, `/baekur/smidakver`

## Tech Stack

- **Caddy** — Web server with URL rewriting for clean URLs
- **HTML + Go Templates** — Go template syntax for shared partials
- **jQuery** + **prettyPhoto** — Image lightbox galleries
- **Custom CSS** — `style.css`, `css/style3.css`

## Project Structure

```
index.html               # Front page
portfolio.html           # Book catalogue
altarisdukar.html        # Altar cloth research
munstur.html             # About page
baekur/                  # Individual book pages (.html files)
templates/               # Shared template partials
  ├── header.html        # Page header with stylesheets
  ├── footer.html        # Page footer
  ├── navigation.html    # Main navigation menu
  ├── sidebar.html       # Content sidebar
  └── sidebar-contact.html  # Alternative contact sidebar
images/                  # Site images
prettyPhoto/             # Lightbox library
js/                      # JavaScript files
css/                     # Stylesheets
Caddyfile                # Production web server config
Caddyfile.local          # Local development config
```

## Development

### Prerequisites

- Caddy v2+
- Python 3.x (for template preprocessing)

### Local Setup

1. **Install Caddy**
   ```bash
   brew install caddy
   ```

2. **Start local server**
   ```bash
   caddy run --config Caddyfile.local
   ```
   Opens at `http://localhost:3000`

3. **Test URLs**
   - Clean URLs: `http://localhost:3000/portfolio`, `http://localhost:3000/baekur/hannyrdir`
   - Backwards compat: `http://localhost:3000/portfolio.php` (redirects to `/portfolio`)

## Template System

Shared components live in `/templates/`:
- Pages use `{{ include "/templates/header.html" }}` to load partials

### Backwards Compatibility

Old PHP URLs (`.php` extensions) automatically redirect to clean URLs via Caddy URL rewriting.

## Contact

**Jenný Karlsdóttir**  
Víkurgili 19, 600 Akureyri  
jenny@munstur.is  
S: 860-4933 / 462-5869
