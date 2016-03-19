# eslint-config-maptalks
An ESLint config for MapTalks javascript projects

##Usage
```bash
npm install eslint eslint-config-maptalks --save-dev
```
CLI:
```bash
npm install eslint eslint-config-maptalks -g
eslint src/**/*.js
```
Simple errors like indentation or quotes can be fixed by 
```bash
eslint src/**/*.js --fix
```

##Config
Can be extended by .eslintrc file
```javascript
{
  extends: 'maptalks',
  globals: {
      'Z':true
  }
}
```

##Credits
based on [mourner](https://github.com/mourner)'s [eslint-config-mourner](https://github.com/mourner/eslint-config-mourner)
