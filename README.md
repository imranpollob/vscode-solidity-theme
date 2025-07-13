# Solidity Theme for VS Code

Enhanced Solidity Theme for Visual Studio Code with improved syntax highlighting and language support.

## Features

- **Enhanced Override Function Highlighting**: Functions with `override` keyword are visually distinguished with underline styling
- **Security-focused Syntax Highlighting**: Special highlighting for security-relevant Solidity constructs
- **Multiple Theme Options**: Dark and light themes optimized for Solidity development
- **Comprehensive Language Support**: Full Solidity language grammar support

## Installation

### From VS Code Marketplace
1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Search for "Solidity Theme"
4. Click Install

### Manual Installation
1. Download the `.vsix` file from releases
2. Open VS Code
3. Press `Ctrl+Shift+P`
4. Type "Extensions: Install from VSIX"
5. Select the downloaded `.vsix` file

## Usage

1. Open a Solidity file (`.sol`)
2. The syntax highlighting will automatically apply
3. Functions with `override` keyword will be underlined and specially highlighted

## Themes Included

- **Solidity Visual Developer Dark** - Dark theme optimized for security auditing
- **Solidity Visual Developer Solarized Light** - Light theme with solarized colors
- **Solidity Visual Developer Light** - Clean light theme

## Features Showcase

### Override Function Highlighting
```solidity
contract Parent {
    function virtualFunc() public virtual returns (uint) {
        return 1;
    }
}

contract Child is Parent {
    // This function will be underlined and highlighted
    function virtualFunc() public override returns (uint) {
        return 2;
    }
}
```

## Development

### Building from Source
```bash
git clone https://github.com/imranpollob/vscode-solidity-theme.git
cd vscode-solidity-theme
npm install -g vsce
vsce package
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Based on the original work by [tintinweb](https://github.com/tintinweb/vscode-solidity-language)
- Enhanced with override function highlighting and improved themes

## Changelog

### 1.0.0
- Initial release
- Added override function highlighting
- Enhanced syntax highlighting for security constructs
- Multiple theme options


## Theme: Solidity Visual Developer Light (VSCode)

<img width="1364" alt="theme_light_vs" src="https://user-images.githubusercontent.com/2865694/61187576-6b1ca500-a673-11e9-8770-ff8b47d716ee.png">


## Theme: Solidity Visual Developer Dark

**Simple DAO**

<img width="981" alt="screenshot 2019-02-09 at 12 30 30" src="https://user-images.githubusercontent.com/2865694/52521879-58deab00-2c7e-11e9-9621-1afc73c918d8.png">

**Vulnerable Contract**

![highlight](https://user-images.githubusercontent.com/2865694/52523502-4bcbb700-2c92-11e9-9ef1-085e3a244cda.png)


## Theme: Solidity Visual Developer Solarized Light

**Simple DAO**

<img width="970" alt="screenshot 2019-02-11 at 21 52 11" src="https://user-images.githubusercontent.com/2865694/52592696-5c715e00-2e47-11e9-99f4-32332e308ec3.png">

