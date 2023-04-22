# node-npm-typescript-prettier-eslint-jest-hotreload-hooks

Spike to create a Node project built with TypeScript + Prettier + ESLint + Jest + Hotreload + Git Hooks

---

This repo presents a spike done to create a barebones Node.js project that is built with TypeScript and uses:

- `npm` to manage dependencies and act as a build tool;
- `eslint` to enforce coding style with linting rules;
- `prettier` to format source files using present linting rules;
- `jest` to describe and execute unit tests;
- `tsup` to compile and bundle project for types (`.d.ts`), CommonJS (`.cjs`), transpiled JS (`.js`) and source-maps (`.map`);
- `nodemon` to provide a way to mantain a lifecycle of the program execution, reloading and applying changes automatically;
- `swc` to compile and run the program in a fast manner;
- `git-hooks` to prevent pushing files that are not formatted.

Each step was documented via git commits, so you can follow the process from start to finish via `git log`.

---

## Scripts

- `npm run build` to transpile and bundle files in `.cjs`, `.js`, `.d.ts` and respective source-maps
- `npm run start` to run the project in a "traditional manner" (compiles with `tsc` and then run the transpiled file)
- `npm run start:hot` to run the project with hot-reload enabled
- `npm run start:swc` to run the project in a "ultra fast manner" (compiçes with `swc` and then run the transpiled file)
- `npm run test` to run the unit tests
- `npm run lint` to analyze and lint the project
- `npm run format` to format the project based on lint feedback

## Acknowledgements

I would like to thank Khalil Stemmler for his [Node.js + TypeScript started project article](https://khalilstemmler.com/blogs/typescript/node-starter-project), as well as @mattpocock for introducing me to `tsup` tool and other TypeScript things! Here's Matt video on it:

[![Watch the video](https://img.youtube.com/vi/eh89VE3Mk5g/hqdefault.jpg)](https://youtu.be/eh89VE3Mk5g)

---

If you found this spike useful, you can generate a custom project that uses the same tools for building programs and libraries. Find out more at https://github.com/dart-pacotes/.bricks/tree/master/pacote_web
