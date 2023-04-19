# TypeScript Monorepo Example

This is an example project demonstrating the setup of a basic monorepo for multiple TypeScript projects, with shared common modules.

## tsconfig.json

The `tsconfig.json` files in each module refer back to the base `tsconfig.base.json` file in the root of the repo. This base file uses configuration presets to apply the settings required:

- @tsconfig/esm
- @tsconfig/node18"
- @tsconfig/strictest

## Packages vs. Apps

Packages are modules that will never be independently built, and will instead be built as part of an application. Apps are modules that will be built and (usually) deployed. This means Apps have a `src` and `dist` folder, but Packages do not.
