# ButterSus AstroCore Repository

A personalized fork of the [AstroNvim Core](https://github.com/AstroNvim/astrocore) with my custom configurations, enhancements, and contributions.

<div align="center">
  <img src="https://astronvim.com/logo/astronvim.svg" width="110" height="100" />
</div>

## Repository Structure

This repository is organized with the following branch structure:

- `personal` (default): My customized version with personal settings and enhancements
- `main`: Mirror of the upstream AstroNvim/astrocore repository

## Using This Repository

### In Your AstroNvim Config

To use my personal branch of the astrocore repository instead of the official one, modify your `lua/plugins/astrocore.lua` file:

```lua
return {
  "ButterSus/astrocore", -- Use my fork instead of the official repo
  -- Default branch is 'personal' so no need to specify
  opts = {
    -- Your core configuration options here
  },
}
```

If you want to specifically use the personal branch (though it's the default):

```lua
return {
  { "ButterSus/astrocore", branch = "personal" },
  opts = {
    -- Your core configuration options here
  },
}
```

### Custom Features

This fork includes:

- Enhanced core functionality
- Custom configurations and overrides for the AstroNvim core
- Core settings optimized for my personal workflow
- Additional utilities and helper functions

## Git Workflow

### For Maintaining This Repository

I maintain this repository using the following git workflow:

1. **Syncing with upstream**:

   ```bash
   git checkout main
   git fetch upstream
   git merge upstream/main
   git push origin main

   # Update personal branch with changes from main
   git checkout personal
   git rebase main
   git push -f origin personal  # Force push as rebase rewrites history
   ```

2. **Contributing to upstream**:

   ```bash
   # Create feature branch from main (not personal)
   git checkout main
   git checkout -b feature/new-core-feature

   # Make changes and commit
   git add .
   git commit -m "Add new core feature: feature-name"

   # Push to fork
   git push origin feature/new-core-feature

   # Create PR to upstream through GitHub interface
   ```

3. **Adding personal customizations**:
   ```bash
   git checkout personal
   # Make core changes or enhancements
   git commit -m "Add personal customization for core functionality"
   git push origin personal
   ```

### For Contributors

If you want to contribute to my personal fork:

1. Fork this repository
2. Create a branch for your feature from the `personal` branch
3. Submit a pull request to the `personal` branch of this repository

## Initial Setup

If you want to set up a similar workflow for your own fork:

```bash
# Clone your fork
git clone https://github.com/yourusername/astrocore.git
cd astrocore

# Add upstream remote
git remote add upstream https://github.com/AstroNvim/astrocore.git

# Create personal branch
git checkout -b personal

# Set personal as default branch (in GitHub settings)

# Push to your fork
git push -u origin personal
```

## Questions or Issues?

Feel free to open an issue if you have any questions or encounter problems using my fork.
