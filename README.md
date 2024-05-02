# docusaurus-docsite

# Installation

### Requirements
- Node.js

### Create scaffold project website
`npx create-docusaurus@latest [WEBSITE-NAME] classic`
Run the command in an empty repository and it will create a new directory containing the scaffold files

### Run development server
```npm
cd [WEBSITE-NAME]
npm run start
```

### Build 
```npm
npm run build
```

### Test Build 
```npm
npm run serve
```

[Click on the link to learn more](https://docusaurus.io/docs/installation)

# Add SearchBar
The searchbar that i have implemented is by using a Local Search plugin that is provided in [the list](https://docusaurus.io/community/resources#search)

The plugin used is [@easyops-cn/docusaurus-search-local](https://github.com/easyops-cn/docusaurus-search-local)

### Installation
`npm install --save @easyops-cn/docusaurus-search-local`
Run the command within the website directory

Once the installation is completed, add the plugin with the `docusaurus.config.js` file
```docusaurus.config.js
import {themes as prismThemes} from 'prism-react-renderer';

/** @type {import('@docusaurus/types').Config} */
const config = {
  plugins: [
    [require.resolve("@easyops-cn/docusaurus-search-local"),
    {hashed: true}
    ],
  ],
  title: 'My Site',
  tagline: 'This site is only for testing purposes',
  favicon: 'favicon.ico',
```