# Contributing to RPG Maker MV Project

Thank you for contributing to this RPG Maker MV project! This guide will help you contribute effectively.

## Getting Started

1. Fork the repository (if you don't have write access)
2. Clone your fork or the main repository
3. Create a new branch for your work
4. Make your changes
5. Test thoroughly in RPG Maker MV
6. Submit a pull request

## Branching Strategy

Use descriptive branch names with prefixes:

- `feature/` - New game features, characters, maps, etc.
  - Example: `feature/add-forest-dungeon`
- `bugfix/` - Bug fixes
  - Example: `bugfix/fix-door-event`
- `content/` - Content additions (dialogue, items, etc.)
  - Example: `content/add-npc-dialogue`
- `asset/` - New assets (images, audio, etc.)
  - Example: `asset/add-battle-music`

## Commit Message Guidelines

Write clear, descriptive commit messages:

### Good Examples
```
Add forest dungeon map with puzzle events
Fix door event not triggering on Map003
Update protagonist sprite with new design
Add battle background music track
```

### Bad Examples
```
Update
Fixed stuff
Changes
asdf
```

### Commit Message Format

```
<type>: <short description>

<optional longer description>
<optional references to issues>
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `content`: Content addition/modification
- `asset`: Asset addition/modification
- `docs`: Documentation changes
- `refactor`: Code refactoring
- `test`: Test additions/changes

## Working with RPG Maker MV Files

### JSON Files (Data)

- RPG Maker MV stores game data in JSON files in the `/data/` directory
- These files are text-based and can be version controlled
- **Warning**: Be careful when manually editing JSON files - syntax errors can break your game

### Map Files

- Each map is stored as a separate JSON file (e.g., `Map001.json`)
- **Important**: Avoid multiple people editing the same map simultaneously
- If you must work on the same map, communicate closely and merge changes carefully

### Database Files

Common database files include:
- `Actors.json` - Character/actor definitions
- `Classes.json` - Character classes
- `Skills.json` - Skills and abilities
- `Items.json` - Items and equipment
- `Enemies.json` - Enemy definitions
- `Troops.json` - Enemy troop formations
- `States.json` - Status effects
- `Animations.json` - Animation definitions
- `System.json` - Game system settings
- `CommonEvents.json` - Common events

### Binary Files (Assets)

- Images, audio, and video files are binary and harder to merge
- Ensure assets are final before committing when possible
- Use descriptive filenames for assets
- Document asset sources and licenses if applicable

## Code Review Process

1. **Self-review**: Test your changes thoroughly before submitting
2. **Create Pull Request**: Provide a clear description of your changes
3. **Address Feedback**: Respond to review comments promptly
4. **Testing**: Ensure changes don't break existing functionality
5. **Approval**: Wait for approval from maintainers
6. **Merge**: Maintainers will merge approved changes

## Testing Checklist

Before submitting a pull request, verify:

- [ ] Game launches without errors
- [ ] New content works as intended
- [ ] Existing content still works correctly
- [ ] No console errors (press F8 during playtest)
- [ ] All events trigger properly
- [ ] Plugin compatibility is maintained
- [ ] Save/load functionality works
- [ ] Changes are committed and pushed

## Communication

- **Announce your work**: Let the team know what you're working on
- **Ask questions**: If unsure, ask before making major changes
- **Report issues**: Use GitHub Issues for bug reports and feature requests
- **Be respectful**: Treat all contributors with respect

## Asset Guidelines

### Images

- Use appropriate image formats (PNG for most game assets)
- Maintain consistent art style with existing assets
- Optimize image sizes when possible
- Name files descriptively: `hero_walk_01.png` not `img1.png`

### Audio

- Use OGG format for music (better compression)
- Use M4A/OGG for sound effects
- Normalize audio levels
- Keep file sizes reasonable
- Name files descriptively: `battle_theme_01.ogg` not `music1.ogg`

### Fonts

- Only include fonts you have the license to use
- Document font licenses in a FONTS.txt file

## Plugin Development

If developing custom plugins:

1. Follow RPG Maker MV plugin conventions
2. Include clear documentation in plugin header comments
3. Test thoroughly with other plugins
4. Document any plugin dependencies
5. Version your plugins
6. Consider backward compatibility

### Plugin Template

```javascript
//=============================================================================
// PluginName.js
//=============================================================================

/*:
 * @plugindesc Brief description of what your plugin does
 * @author Your Name
 *
 * @param ParameterName
 * @desc Description of this parameter
 * @default default_value
 *
 * @help
 * Longer description and usage instructions here.
 */

(function() {
    // Your plugin code here
})();
```

## Conflict Resolution

### Preventing Conflicts

- Pull latest changes before starting work: `git pull origin main`
- Work on separate maps/features when possible
- Communicate with team about overlapping work
- Commit and push regularly

### Resolving Conflicts

If you encounter merge conflicts:

1. **Simple text conflicts**: Resolve manually in a text editor
2. **Complex JSON conflicts**: 
   - Coordinate with the other contributor
   - Choose one version as base
   - Manually re-apply changes from the other version in RPG Maker MV
3. **Asset conflicts**: Usually safe to keep both and rename one
4. **When in doubt**: Ask for help from maintainers

## Questions?

If you have questions or need help:

- Check existing documentation
- Search closed issues for similar problems
- Ask in pull request comments
- Contact project maintainers

Thank you for contributing to our RPG Maker MV project!
