### Steps

- Fork either of these repos `https://github.com/Yog9/SnapShot` OR `https://github.com/AssaultKoder95/test-gh-pages`
- remove the original `.git` folder
- Initialize the repo with git again `git init`
- Create a repo on github name `deploy-static-website-pavo-<your name>`
- Add the remote url to the local repo using the following commands `git remote add origin <your repo link>`
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

- Run the following command : `npm run deploy`
- That's it, you should be able to see your website at `https://assaultkoder95.github.io/test-gh-pages`
