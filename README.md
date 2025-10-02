# DataRobot OSS Homebrew Tap

A Homebrew tap repository for DataRobot's open source software packages.

## Installation

You can install any formula from this tap using:

```bash
brew install datarobot-oss/taps/<formula>
```

For example, if there was a formula called `example-tool`, you would install it with:

```bash
brew install datarobot-oss/taps/example-tool
```

## Available Formulas

Currently, this tap contains the following formulas:

- dr - The DataRobot CLI

Note: There is an `example-formula.rb.template` file in the `Formula/` directory that serves as a template for creating new formulas. Remove this template when adding your first real formula.

## For Developers: Adding New Formulas

This tap follows the standard Homebrew tap guidelines. To add a new formula:

1. **Create a new formula file** in the `Formula/` directory
2. **Name the file** using the pattern `<formula-name>.rb`
3. **Follow Homebrew formula conventions** - see the [Adding Software to Homebrew guide](https://docs.brew.sh/Adding-Software-to-Homebrew)

### Quick Start for New Formulas

1. **Use the provided template**: Start with the `Formula/example-formula.rb.template` file as a reference

2. Use `brew create <url>` to generate a formula template:
   ```bash
   brew create https://github.com/your-org/your-software/archive/v1.0.0.tar.gz
   ```

3. Move the generated formula to this tap's `Formula/` directory

4. Edit the formula to follow DataRobot standards and test thoroughly

5. Submit a pull request with your new formula

### Resources

- [How to Create and Maintain a Tap](https://docs.brew.sh/How-to-Create-and-Maintain-a-Tap)
- [Adding Software to Homebrew](https://docs.brew.sh/Adding-Software-to-Homebrew)
- [Formula Cookbook](https://docs.brew.sh/Formula-Cookbook)
- [Homebrew Acceptable Formulae](https://docs.brew.sh/Acceptable-Formulae)

## Testing

Before submitting a formula, please test it locally:

```bash
# Test the formula installation
brew install --build-from-source ./Formula/<formula-name>.rb

# Run audit to check for common issues
brew audit --strict --online ./Formula/<formula-name>.rb

# Test uninstallation
brew uninstall <formula-name>
```
