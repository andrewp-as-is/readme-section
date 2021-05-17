[![](https://img.shields.io/pypi/v/readme-section.svg?maxAge=3600)](https://pypi.org/project/readme-section/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/readme-section/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/readme-section/actions)

### Installation
```bash
$ pip install readme-section
```

### Pros
+   **auto headings**
+   **native**, **minimalistic**, **fast** - only markdown files and shell script

### How it works
1.  make README sections files
2.  make a shell script to build the README.md file

### Examples
`README.md.sh`
```bash
#!/usr/bin/env bash

[ -e setup.py ] && echo "badges ..." && cat <<EOF
### Installation
pip install name
EOF

readme-section ".readme/pros.md"
readme-section ".readme/how.md" "How it works"
readme-section ".readme/examples.md"
readme-section ".readme/links.md"               # optional. empty if file not exists
```

```bash
$ bash -l README.md.sh > README.md
```
```markdown
badges ...

### Installation
pip install name

### Features
features.md content ...

### How it works
how.md content ...
```

