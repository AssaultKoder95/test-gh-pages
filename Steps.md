### Steps

- Install `gh-pages` package using `npm install gh-pages --save-dev`
- Add `homepage` property in your package.json file

```js
// package.json
{
    "version": "0.1.0",
    "private": true,
    "homepage": "https://assaultkoder95.github.io/test-gh-pages",
    "dependencies": {
        "@testing-library/jest-dom": "^4.2.4",
        "@testing-library/react": "^9.3.2",
        "@testing-library/user-event": "^7.1.2",
        "axios": "^0.19.2"
    }
}
```

- Inside `scripts` property add the following scripts

```js
   "scripts": {
        //.... other properties
        "predeploy": "npm run build",
        "deploy": "gh-pages -d build"
   }
```
