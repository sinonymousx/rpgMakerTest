# RPG Maker MV Collaboration Project

A Git repository for collaborating on an RPG Maker MV game development project.

## About

This repository is set up for team collaboration on RPG Maker MV game development. It includes proper version control configurations and guidelines to help multiple developers work together effectively.

## Getting Started

### Prerequisites

- [RPG Maker MV](https://www.rpgmakerweb.com/products/rpg-maker-mv) installed on your computer
- Git installed for version control
- A text editor for editing JSON and JavaScript files

### Setting Up Your Local Environment

1. Clone this repository:
   ```bash
   git clone https://github.com/sinonymousx/rpgMakerTest.git
   cd rpgMakerTest
   ```

2. Open the project in RPG Maker MV:
   - Launch RPG Maker MV
   - Click "Open Project"
   - Navigate to and select the cloned repository folder

## Project Structure

Once the RPG Maker MV project is initialized, the typical structure will be:

```
rpgMakerTest/
├── audio/          # Background music and sound effects
├── data/           # Game database files (JSON)
├── fonts/          # Custom fonts
├── icon/           # Game icon files
├── img/            # Graphics and images
├── js/             # JavaScript files and plugins
├── movies/         # Video files
├── save/           # Save game files (not tracked in git)
├── Game.rpgproject # RPG Maker MV project file
├── index.html      # Game entry point
├── package.json    # Project metadata
└── README.md       # This file
```

## Collaboration Guidelines

### Before You Start Working

1. **Always pull the latest changes** before starting work:
   ```bash
   git pull origin main
   ```

2. **Create a new branch** for your feature or changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```

### While Working

1. **Commit frequently** with clear, descriptive messages:
   ```bash
   git add .
   git commit -m "Add new character sprite for protagonist"
   ```

2. **Test your changes** in RPG Maker MV before committing

3. **Avoid working on the same maps/events simultaneously** with other team members to prevent conflicts

### Best Practices for RPG Maker MV with Git

- **Communicate with your team** about what you're working on
- **Use descriptive branch names**: `feature/`, `bugfix/`, `content/`
- **Keep commits focused**: One feature or fix per commit when possible
- **Don't commit save files**: The `/save/` directory is ignored by git
- **Be careful with binary files**: Images and audio files should be final before committing
- **Test before pushing**: Always playtest your changes before pushing to the repository

### Handling Conflicts

RPG Maker MV stores most data in JSON files. If you encounter merge conflicts:

1. **For small conflicts**: Manually resolve them in a text editor
2. **For large conflicts**: Coordinate with your team to determine which version to keep
3. **For map files**: It's often easier to recreate changes than merge conflicting map data

### Submitting Your Work

1. **Push your branch** to the repository:
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Create a Pull Request** on GitHub for review

3. **Wait for review** and address any feedback

4. **Merge** once approved

## Common Tasks

### Adding New Content

- **Maps**: Create in RPG Maker MV, commit the updated map JSON files in `/data/`
- **Events**: Edit in RPG Maker MV, commit the changes to map files
- **Database Items**: Use RPG Maker MV's database editor, commit updated database JSON files
- **Plugins**: Add JavaScript files to `/js/plugins/`, update plugin configuration
- **Assets**: Add images to `/img/`, audio to `/audio/`, commit the new files

### Plugin Management

If your project uses custom plugins:

1. Add plugin files to `/js/plugins/`
2. Document the plugin purpose and usage in comments or a separate PLUGINS.md file
3. Update plugin parameters in the RPG Maker MV editor
4. Commit both the plugin file and updated configuration

## Troubleshooting

### "My changes aren't showing up"

- Make sure you've saved in RPG Maker MV
- Close and reopen RPG Maker MV to refresh the project
- Check if your changes were actually committed: `git status`

### "I have merge conflicts in a map file"

- Coordinate with your team to determine which version to keep
- Consider using one person's version and re-applying the other's changes manually in RPG Maker MV

### "The game won't run after pulling changes"

- Try closing and reopening the project in RPG Maker MV
- Check if there are any error messages in the console (F8 during playtest)
- Verify all required plugins are present in `/js/plugins/`

## Resources

- [RPG Maker MV Documentation](https://www.rpgmakerweb.com/support/products/rpg-maker-mv)
- [RPG Maker Forums](https://forums.rpgmakerweb.com/)
- [Git Documentation](https://git-scm.com/doc)

## License

Specify your project's license here.

## Contributors

List your team members and contributors here.
