# Create React App Checklist

## Initialize App
* `create-react-app APP_NAME`
* Create github repository
* `cd APP_NAME`
* `git init`
* Link repo to project with: `git remote add origin https://github.com/USER_NAME/APP_NAME.git`
* Add "homepage" to package.json with link to live website

## Add Linters
* `npm install --save-dev eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react`
* `touch .eslintrc.json .eslintrc.js
* Add code to .eslintrc.json
```
{
    "extends": "airbnb"
}
```
* Add code to .eslintrc.js
```
module.exports = {
  "extends": "airbnb",
  "plugins": [
    "react",
    "jsx-a11y",
    "import"
    ],
    "rules": {
      "react/jsx-filename-extension": [1, { "extensions": [".js", ".jsx"] }]
    }
};
```

## Add SASS
* `npm install --save node-sass-chokidar`
* Add to package.json:
```
"scripts": {
    "build-css": "node-sass-chokidar --include-path ./src --include-path ./node_modules src/ -o src/",
    "watch-css": "npm run build-css && node-sass-chokidar --include-path ./src --include-path ./node_modules src/ -o src/ --watch --recursive"
}
```
* Add to .gitignore
```
# CSS
src/**/*.css

## Except
!src/**/index.css
```
* `mkdir src/stylesheets`
  




