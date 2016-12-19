c2e:src/main.js

```js
// main.js
#!/usr/bin/env node
import { getTextFromFile, writeFileFromText } from './file'
import { convertLinesToContexts } from './converter'
const README = getTextFromFile(`./README.md`)
const lines = README.split('\n')
const newContexts = convertLinesToContexts(lines)
const newDocs = newContexts.join('\n')
writeFileFromText(newDocs, './README.md')
```
