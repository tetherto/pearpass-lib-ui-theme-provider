# pearpass-lib-ui-theme-provider

A React theme provider library for Pearpass applications that supplies consistent colors, themes and styling capabilities across both Desktop and React Native projects.

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

1. To ensure the security and integrity of your projects, please note that official PearPass packages are distributed exclusively through our GitHub organization.
2. Any packages with similar names found on the npm registry or other third-party package managers are not affiliated with PearPass and should be strictly avoided. We recommend installing directly from this repository to ensure you are using the verified, open-source version.

## Installation

```bash
npm install git+https://github.com/tetherto/pearpass-lib-ui-theme-provider.git
```

## Usage Examples

### React Web
```jsx
import React from 'react';
import { ThemeProvider } from '@tetherto/pearpass-lib-ui-theme-provider';
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
import { ThemeProvider } from '@tetherto/pearpass-lib-ui-theme-provider/native';
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

- [@tetherto/pearpass-app-mobile](https://github.com/tetherto/pearpass-app-mobile) - A mobile app for PearPass, a password manager
- [@tetherto/pearpass-app-desktop](https://github.com/tetherto/pearpass-app-desktop) - A desktop app for PearPass, a password
- [@tetherto/pearpass-lib-ui-react-native-components](https://github.com/tetherto/pearpass-lib-ui-react-native-components) - A library of React Native UI components for PearPass
- [@tetherto/pearpass-lib-ui-react-components](https://github.com/tetherto/pearpass-lib-ui-react-components) - A library of React UI components for PearPass
- [@tetherto/tether-dev-docs](https://github.com/tetherto/tether-dev-docs) - Documentations and guides for developers

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](./LICENSE) file for details.