# rootdump

[![PyPI version](https://badge.fury.io/py/rootdump.svg)](https://badge.fury.io/py/rootdump)
[![Python Versions](https://img.shields.io/pypi/pyversions/rootdump.svg)](https://pypi.org/project/rootdump/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A Python library for dumping directory contents into a single organized text file. Perfect for code reviews, documentation, and project analysis.

## Features

✨ **Tree Structure** - Displays directory structure in a tree format  
📝 **Content Dump** - Dumps the content of all text files  
🔍 **Extension Filtering** - Filter files by extension  
⚡ **Binary Detection** - Automatically excludes binary files  

## Installation

```bash
pip install rootdump
```

## Quick Start

### Command Line Usage

Basic usage:
```bash
rootdump /path/to/source output.txt
```

With options:
```bash
# Exclude binary files
rootdump /path/to/source output.txt --exclude-binary

# Include only specific extensions
rootdump /path/to/source output.txt --extensions .py .txt .md

# Skip directory tree structure
rootdump /path/to/source output.txt --no-tree
```

### Python API

```python
from rootdump import dump_directory

# Basic usage
dump_directory("source_dir", "output.txt")

# With options
dump_directory(
    "source_dir",
    "output.txt",
    exclude_binary=True,
    include_extensions=[".py", ".txt"],
    show_tree=True
)
```

## Output Example

```
# Directory structure:
# .
# ├── src/
# │   ├── __init__.py
# │   └── main.py
# ├── tests/
# │   └── test_main.py
# └── README.md

## src/__init__.py

[content here]

## src/main.py

[content here]
```

## Contributing

Contributions are welcome! Feel free to:

- Report issues
- Suggest features
- Submit pull requests

## Acknowledgments

This project was inspired by [uithub.com](https://uithub.com)'s project structure visualization.

## License

This project is licensed under the MIT License - see the LICENSE file for details.