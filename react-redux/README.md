# React and Redux

If you are not familiar with linters, read [root level README](../README.md).

## Set-up GitHub Actions

Please do the following **steps in this order**:

1. In the first commit of your feature branch create a `.github/workflows` folder and add a copy of [`.github/workflows/linters.yml`](.github/workflows/linters.yml) to that folder.
   - **Remember** to use the file linked above
   - **Remember** that `.github` folder starts with a dot.
2. **Do not make any changes in config files - they represent style guidelines that you share with your team.**
   - If you think that change is necessary - open a [Pull Request in this repository](../README.md#contributing).
3. When you open your first pull request you should see the result of the GitHub actions checks:

![gh-actions-html-css-checks](https://user-images.githubusercontent.com/120318564/222532514-faffbc4c-1635-4842-b2a6-f39462afaeee.png)


Click on the `Details` link of each action to see the full output and the errors that need to be fixed:

![gh-actions-html-css-failing-checks](https://user-images.githubusercontent.com/120318564/222532976-598f5d71-ff8c-4a0a-ad64-38a214879756.png)

## Set-up linters in your local env

**Note**: The `npm` package manager is going to create a `node_modules` directory to install all of your dependencies. You shouldn't commit that directory. To avoid that, you can create a [`.gitignore`](https://git-scm.com/docs/gitignore) file and add `node_modules` to it:

```
# .gitignore
node_modules/
```

### [Stylelint](https://stylelint.io/)

A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.

1. Run

   ```
   npm install --save-dev stylelint@13.x stylelint-scss@3.x stylelint-config-standard@21.x stylelint-csstree-validator@1.x
   ```

   *not sure how to use npm? Read [this](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).*

2. Copy [.stylelintrc.json](./.stylelintrc.json) to the root directory of your project.
3. **Do not make any changes in config files - they represent style guidelines that you share with your team.**
   - If you think that change is necessary - open a [Pull Request in this repository](../README.md#contributing).
4. Run `npx stylelint "**/*.{css,scss}"` on the root of your directory of your project.
5. Fix linter errors.
6. **IMPORTANT NOTE**: feel free to research [auto-correct options for Stylelint](https://stylelint.io/user-guide/usage/options) if you get a flood of errors but keep in mind that correcting style errors manually will help you to make a habit of writing a clean code!

### [ESLint](https://eslint.org/)

1. Run 
   ```
   npm install --save-dev eslint@7.x eslint-config-airbnb-base@14.x eslint-plugin-import@2.x babel-eslint@10.x
   ``` 
   *not sure how to use npm? Read [this](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).*

2. Copy [.eslintrc.json](./.eslintrc.json)and and [.babelrc](./.babelrc) to the root directory of your project.
3. **Do not make any changes in config files - they represent style guidelines that you share with your team.**
    - If you think that change is necessary - open a [Pull Request in this repository](../README.md#contributing).
4. Run `npx eslint .` on the root of your directory of your project.
5. Fix linter errors.
6. **IMPORTANT NOTE**: feel free to research [auto-correct options for Eslint](https://eslint.org/docs/latest/user-guide/command-line-interface#fixing-problems) if you get a flood of errors but keep in mind that correcting style errors manually will help you to make a habit of writing a clean code!
