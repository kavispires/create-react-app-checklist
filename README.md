# Create React App Checklist

## Initialize App
* `create-react-app APP_NAME`
* Create github repository
* `cd APP_NAME`
* `git init`

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
  




