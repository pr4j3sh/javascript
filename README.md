# Javascript NPM Package/Library

This is a javascript npm package starter template.

It provides both package scenarios:

- library
- binary

## Usage

- Clone using `@pr4j3sh/frames`

```bash
npm create @pr4j3sh/frames@latest javascript mypkg
```

- Run using

```bash
npm run dev
```

### Transitioning to `module`

By default `javascript` package is of type `commonjs`

- Add `"type":"module"` to `package.json`
- Change contents of `esbuild.config.js` to

```js
import esbuild from "esbuild";

try {
  await esbuild.build({
    entryPoints: ["index.js"],
    bundle: true,
    minify: true,
    platform: "node",
    packages: "external",
    outfile: "dist/bundle.js",
  });
  console.log("Build successful!");
} catch (err) {
  console.error("Build failed:", err);
  process.exit(1);
}
```

- Use `imports` instead of `require`

## Reference

- [NodeJS Documentation](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs)
- [NPM Documentation](https://docs.npmjs.com/)
- [@pr4j3sh/frames](https://pr4j3sh.github.io/frames/)
