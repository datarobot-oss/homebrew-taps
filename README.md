# DataRobot OSS Homebrew Tap

A Homebrew tap repository for DataRobot's open source software packages.

## Installation

You can install any cask from this tap using:

```bash
brew install datarobot-oss/taps/<cask>
```

For example, if there was a cask called `example-tool`, you would install it with:

```bash
brew install datarobot-oss/taps/example-tool
```

## Available Casks

Currently, this tap contains the following formulas:

- dr-cli - The DataRobot CLI

## For Developers: Adding New Casks

This tap follows the standard Homebrew tap guidelines. To add a new cask:

1. **Create a new Cask file** in the `Cask/` directory
2. **Name the file** using the pattern `<cask-name>.rb`
3. **Follow Homebrew formula conventions** - see the [Adding Software to Homebrew guide](https://docs.brew.sh/Adding-Software-to-Homebrew)

### Quick Start for New Casks

1. Use `brew create <url>` to generate a cask template:
   ```bash
   brew create https://github.com/your-org/your-software/archive/v1.0.0.tar.gz
   ```

2. Move the generated cask to this tap's `Casks/` directory

3. Edit the cask to follow DataRobot standards and test thoroughly

4. Submit a pull request with your new cask

### Resources

- [How to Create and Maintain a Tap](https://docs.brew.sh/How-to-Create-and-Maintain-a-Tap)
- [Adding Software to Homebrew](https://docs.brew.sh/Adding-Software-to-Homebrew)

## Testing

Before submitting a cask, please test it locally:

```bash
# Test the formula installation
brew install --build-from-source ./Casks/<formula-name>

# Run audit to check for common issues
brew audit --strict --online ./Casks/<formula-name>

# Test uninstallation
brew uninstall <formula-name>
```
