# Munstur og Menning — munstur.is

Website for **Munstur og Menning**, a small Icelandic publishing operation run by Jenný Karlsdóttir of Akureyri. The site showcases republished Icelandic traditional craft books and documents a long-running research project cataloguing church altar cloths (*altarisdúkar*) across Iceland.

## Pages

| Page | File | Description |
|------|------|-------------|
| Heim | `index.php` | Front page with slideshow |
| Bækurnar | `portfolio.php` | Book catalogue |
| Altarisdúkar | `altarisdukar.php` | Altar cloth research project |
| Altarisdúkamunstur | `altarisdukamunstur.php` | Altar cloth embroidery patterns |
| Munstur.is | `munstur.php` | About the publisher |

### Book sub-pages (`baekur/`)

Hannyrðir, Vefnaður, Hvítar Útsaumsgerðir, Jurtalitun, Gömul Mynstur, Milliverk, Munsturbekkir, Stafabækur, Útskurðarmynstur, Útsögunarmynstur, Tuskudýr, Smíðakver.

## Tech Stack

- **PHP** — `include_once` templating with shared header, navigation, and footer fragments
- **jQuery** + **prettyPhoto** — image lightbox galleries
- **Custom CSS** — `style.css`, `css/style3.css`

## Project Structure

```
index.php             # Front page
portfolio.php         # Book catalogue
altarisdukar.php      # Altar cloth research
munstur.php           # About page
baekur/               # Individual book pages
images/               # Site images
prettyPhoto/          # Lightbox library
js/                   # JavaScript files
css/                  # Stylesheets
```

## Contact

**Jenný Karlsdóttir**  
Víkurgili 19, 600 Akureyri  
jenny@munstur.is  
S: 860-4933 / 462-5869
