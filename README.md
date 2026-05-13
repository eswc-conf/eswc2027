# 2027 ESWC Conference

## Configuration

### Creating content
Create content at `/content` by creating an index file.
- in a new subsection: `/content/section/new-subsection/index.md`
- directly at a section: `content/section/index.md`

Documentation on the structure of every section follows.

### Modify the Navbar
The navbar is loaded from `layouts/partials/navbar` AND `layouts/partials/mobile-navbar`. Every change to the items in the main level of the navbar should be performed at both files.

#### Adding elements to the subnavbar
Items displayed on the second level of the navbar are added as list items and follow the following structure:
```
<ul class="nav-submenu">
  <li class="nav-submenu-item">
    <a href="${URL}" class="nav-submenu-item--link">
      ${TITLE_DISPLAYED}
    </a>
  </li>
  [...]
</ul>
```
- `${URL}`: url, relative to the site's base URL
- `${TITLE_DISPLAYED}`: text displayed in the subnavbar

### Modify the schedule
The schedule is modified at `data/schedule.yaml`. See the existing data structures for reference.

## Installation
1. Clone the repository
2. [Install Hugo](https://gohugo.io/installation/)
3. Run the server:
   ```bash
   hugo server --bind -p 1313
   ```
4. Open your browser and go to `http://localhost:1313/`

> **Note:** The theme (`themes/tum-hugo`) is a customized fork of [ls1intum/tum-hugo-theme](https://github.com/ls1intum/tum-hugo-theme) and is committed directly in the repository.

## About
This is the source code of the website for the 24th European Semantic Web Conference (ESWC 2027). The website is built using [Hugo](https://gohugo.io/) and the [TUM Hugo Theme](https://github.com/ls1intum/tum-hugo-theme).

## TODO
- [ ] Call for contributions: define important dates
- [ ] Home rework
- [ ] Set organizing committee
- [ ] Review template