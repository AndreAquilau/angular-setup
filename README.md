## Create Project In Angular
```bash
ng new <name:project>
```

#### Migrating and configuring Eslint with Angular 11
Primary install convert-tslint-to-eslint.
> With ng install @angular-eslint/schematics
```bash
// Execute in Project 

ng add @angular-eslint/schematics
```
> Execute Convertion For Eslint
```bash
// Execute in Project

ng g @angular-eslint/schematics:convertion-tslint-to-eslint <name:project>

// exemple

$ ng g @angular-eslint/schematics:convert-tslint-to-eslint angular-cod3r
CREATE .eslintrc.json (1084 bytes)
UPDATE angular.json (3470 bytes)
```
> Create file .eslintignore
```bash
touch .eslintignore
```
```.eslintignore
node_modules
dist
e2e
build
/*.js
```
#### Action On Save Execute Eslint in VSCode
> Create folder .vscode and settings.json
```.json
// .vscode/settings.json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```
#### Configuration Prettier Format with Eslint
```bash
yarn add prettier eslint-plugin-prettier eslint-config-prettier
```

#### Create File .prettierrc
```.prettierrc
{
  "tabWidth": 2,
  "useTabs": true,
  "printWidth": 80,
  "semi": true,
  "singleQuote": true,
  "quoteProps": "as-needed",
  "trailingComma": "none",
  "bracketSpacing": true,
  "arrowParens": "avoid",
  "overrides": [
      {
          "files": "*.component.html",
          "options": {
              "parser": "angular"
          }
      },
      {
          "files": "*.html",
          "options": {
              "parser": "html"
          }
      }
  ]
}
```
> create .prettierignore
```.prettierignore
node_modules
dist
e2e
build
/*.js
```
#### Configuration extensions, plugin, rule in .eslintrc.json
```.json
+++
 "extends": [
        "eslint:recommended",
        "plugin:@typescript-eslint/recommended",
        "plugin:prettier/recommended",
        "prettier/standard",
        "prettier/@typescript-eslint",
        "prettier/@typescript-eslint",
      ],
  +++
  "rules": {
    "prettier/prettier": "error"
  }
```
##### References Configuration
[References Eslint + Prettier + Angular]()
