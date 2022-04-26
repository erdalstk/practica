# Contributing to Practica.js - The short guide

## You belong with us

We are in an ever-going quest for better software practices. If you reached down to this page, you probably belong with us 💜. 

Note: This is a shortened guide that suits those are willing to quickly contribute. Once you deepen your relations with Practica.js - It's a good idea to read the [full guide](https://github.com/practicajs/practica/blob/main/CONTRIBUTING.md)

## 3 things to consider

- Our philospophy is all about minimalism and simplicity - We strive to write less code, rely on existing and reputable libraries, stick to Node/JS standards and avoid adding our own abstractions
- Popular vendors only - Each technology and vendor that we introduce must super popular and reliable. For example, a library must one of the top 5 most starred and downloaded in its category. See [full vendor choose instructions here](./vendor-pick-library.MD)
- 

## The internals in a nutshell

Practica is divided into two main worlds:

**- The code generator - Code and CLI to get the user preferences and copy the right code to her computer**

Here you will find CLI, UI, and logic to generate the right code. We use a templating library to go through the code-template files and filter out parts/files based on the user preferences. For example, should she ask NOT to get a github action file - The generator will remove this file from the output

**- The code templates - The output of our program: An example Microservice and libraries**

Here you will the generated code that we will selectivelly copy to the user's computer. This files are not pure TS/JS files rather template files, to code with these files, you must first generate aside code for yourself, then you'll receive valid TS files which you can run and modify. 

To generate a working folder with real code, do the following:

1. Install dependencies

```
nvm use && npm i
```

2. Bind the CLI command to our code

```
cd .dist && npm link
```

3. Generate the code to your preferred working folder

```
cd {some folder like $HOME}
generate generate --install-dependencies
```

4. Now you can work on the generated code. Later on, once your tests pass and you're happy - copy the chages back to ~practica/src/code-templates


## Workflow

1. Idea
2. Optional: Design
3. PR

## Development machine setup

✅ Ensure Node, Docker and [NVM](https://github.com/nvm-sh/nvm#installing-and-updating) are installed

✅ Configure GitHub and npm 2FA!

✅ Close the repo if you are a maintainer, or fork it if have no collaborators permissions

✅ With your terminal, ensure the right Node version is installed:

```
nvm use
```

✅ Install dependencies:


```
nvm i
```

✅ Ensure all tests pass:

```
npm t
```

✅ You can safely start now: Code, run the test and vice versa