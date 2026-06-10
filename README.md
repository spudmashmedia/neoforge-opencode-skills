# NeoForge Modding OpenCode Skills Bundle
<p align="center">
   <img src="docs/img/icon_256.png" alt="NeoForge Modding OpenCode Skills Bundle" />
</p>

This repository contains a modular bundle of OpenCode skills designed to assist with building, testing, and developing Minecraft mods using the NeoForge framework.

## Content Included
* **`SKILL.md`**: The main orchestration manifest that manages context.
* **`mod-conventions.md`**: Strict coding standards, naming rules, and patterns.
* **`item-creation.md`**: Guidelines for item, block, and data generation.
* **`build-and-testing.md`**: Environment setup and Gradle compile rules.

## Installation
To use these skills globally with OpenCode on your local machine, clone this repository and symlink the bundle into your configuration directory:

```bash
# Clone the repository
git clone https://github.com
cd neoforge-opencode-skills

# Create the global directory if it doesn't exist
mkdir -p ~/.config/opencode/skills/

# Symlink the skill bundle
ln -s "$(pwd)/skills/neoforge-modding" ~/.config/opencode/skills/neoforge-modding
```

## License
This project is licensed under the MIT License - see the front matter in `SKILL.md` for details.
