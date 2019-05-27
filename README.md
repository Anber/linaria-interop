# `babel-plugin-linaria-interop`

This plugin allows to interpolate Linaria components inside styled-components and Emotion:
```javascript
import styled from 'styled-components';
import { Title } from './Title.styled'; // Linaria component

const Article = () => { /* … */ };

export default styled(Article)`
  & > ${Title} {
    color: green;
  }
`;

```

## Quick start

Install the plugin first:

```
npm install --save-dev babel-plugin-linaria-interop
```

Then add `linaria-interop` to your babel configuration *before* `styled-components`:

```JSON
{
  "plugins": [
    ["linaria-interop", { "library": "styled-components" }],
    "styled-components"
  ]
}
```
