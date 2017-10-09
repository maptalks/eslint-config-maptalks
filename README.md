# eslint-config-maptalks
An ESLint config for MapTalks javascript projects

## Install
```bash
npm install eslint eslint-config-maptalks --save-dev
```
Then add a following .eslintrc file in the repo root:
```javascript
{
  "extends": "maptalks"
}
```
## Usage

### CLI

```bash
npm install eslint eslint-config-maptalks -g
eslint src/**/*.js
```
Simple errors like indentation or quotes can be fixed automatically by 
```bash
eslint src/**/*.js --fix
```

### With gulp-eslint
```javascript
var eslint = require('gulp-eslint');
gulp.task('lint', function() {
  gulp.src('src/**/*.js')
      //the parameter of eslint is optional
      //used to override the default rules
      .pipe(eslint({
          extends: 'maptalks',
          globals: {
              'Z':true
          }
      }))
      .pipe(eslint.format())
      .pipe(eslint.failAfterError())
});
```

### In package.json
```javascript
"scripts": {
  "lint": "eslint src/**/*.js",
  "pretest": "npm run lint"
}
```
Run in terminal and enjoy thousands of errors:
```bash
npm run lint
```
## Config
Can be extended by .eslintrc file
```javascript
{
  extends: 'maptalks',
  globals: {
      'Z':true
  }
}
```

## Credits
based on [mourner](https://github.com/mourner)'s [eslint-config-mourner](https://github.com/mourner/eslint-config-mourner)
