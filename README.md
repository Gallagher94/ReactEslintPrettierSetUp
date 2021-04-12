# Getting Started with Eslint - Prettier in a Create React App

Watch this video https://www.youtube.com/watch?v=GedOLszVOo4

Eslint Prettier Create React App VSCode Best Configuration Setup

Have you ever wanted to configure Eslint to work correctly with Prettier and your Create React App? If so in this video you will learn the best settings to do that.

Steps:
1. Install Eslint Globally
npm i -g eslint

2. Open your create-react-app react project or create one by typing
npx create-react-app name-of-project
(needs npm 5.2+)

3. Initiate Eslint in your project:
eslint --init
(answer the questions)

4. Confirm installation of eslint-plugin-react

5. Leave this in your ESlint config:
 "env": {
  "browser": true,
  "es6": true
 },
 "extends": ["eslint:recommended"],
 "plugins": ["react"],
 "parserOptions": {
  "ecmaVersion": 2018
 },
 "rules": {}

6.  Install eslint-config-react-app peer dependencies:
npx install-peerdeps --dev eslint-config-react-app

7. Install prettier dependencies:
npm i -D eslint-config-prettier eslint-plugin-prettier prettier

8. Configure Prettier through ESlint example: 
{
  "env": {
    "browser": true,
    "es6": true
  },
  "extends": ["react-app", "prettier"],
  "plugins": ["react", "prettier"],
  "parserOptions": {
    "ecmaVersion": 2018
  },
  "rules": {
    "prettier/prettier": [
      "error",
      {
        "printWidth": 80,
        "trailingComma": "es5",
        "semi": false,
        "jsxSingleQuote": true,
        "singleQuote": true,
        "useTabs": true
      }
    ]
  }
}

9. Change your VScode settings 
"eslint.autoFixOnSave": true

10. Check for conflicting rules with the following:
{
  "scripts": {
    "eslint-check": "eslint --print-config path/to/main.js | eslint-config-prettier-check"
  }
}

# ReactEslintPrettierSetUp
