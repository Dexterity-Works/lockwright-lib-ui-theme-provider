# lockwright-lib-ui-theme-provider

A React theme provider for Lockwright. Colors and themes for desktop and React Native.

Site: [lockwright.dexterity.works](https://lockwright.dexterity.works)

Community fork of PearPass (Apache 2.0). Not affiliated with or endorsed by Tether Data or the Pears project.

## Table of Contents

- [Features](#features)
- [Security Notice](#security-notice)
- [Installation](#installation)
- [Usage Examples](#usage-examples)
- [Dependencies](#dependencies)
- [Related Projects](#related-projects)

## Features

- Support for both React and React Native applications
- Easy-to-use ThemeProvider component
- Color class with multiple variant support
- Styled-components integration

## Security Notice

The package name is `lockwright-lib-ui-theme-provider`.

## Installation

```bash
npm install git+https://github.com/Dexterity-Works/lockwright-lib-ui-theme-provider.git
```

## Usage Examples

### React Web
```jsx
import React from 'react';
import { ThemeProvider } from 'lockwright-lib-ui-theme-provider';
import styled from 'styled-components';

const StyledComponent = styled.div`
    background-color: ${props => props.theme.colors.primary400.mode1};
    color: ${props => props.theme.colors.white.mode1};
`;

function App() {
    return (
        <ThemeProvider>
            <StyledComponent>
                This component uses the theme colors
            </StyledComponent>
        </ThemeProvider>
    );
}
```

### React Native
```jsx
import React from 'react';
import { ThemeProvider } from 'lockwright-lib-ui-theme-provider/native';
import styled from 'styled-components/native';

const StyledComponent = styled.View`
    background-color: ${props => props.theme.colors.primary400.mode1};
`;

const StyledText = styled.Text`
    color: ${props => props.theme.colors.white.mode1};
`;

function App() {
    return (
        <ThemeProvider>
            <StyledComponent>
                <StyledText>This component uses the theme colors</StyledText>
            </StyledComponent>
        </ThemeProvider>
    );
}
```

## Dependencies
- [styled-components](https://www.npmjs.com/package/styled-components) - peer dependency

## Related Projects

- [lockwright-app-mobile](https://github.com/Dexterity-Works/lockwright-app-mobile) - Lockwright for mobile
- [lockwright-app-desktop](https://github.com/Dexterity-Works/lockwright-app-desktop) - Lockwright for desktop
- [lockwright-lib-ui-react-native-components](https://github.com/Dexterity-Works/lockwright-lib-ui-react-native-components) - Lockwright UI kit
- [tether-dev-docs](https://github.com/Dexterity-Works/tether-dev-docs) - Documentations and guides for developers

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](./LICENSE) file for details.