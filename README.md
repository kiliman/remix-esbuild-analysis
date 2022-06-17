# Remix esbuild bundle analysis patch

This patch will add the [`--metafile`](https://esbuild.github.io/api/#metafile) option to the esbuild compiler. It generates a _meta.json_ file in the output directory for both client and server builds. You can upload the _meta.json_ file to [Bundle Buddy](https://bundle-buddy.com).

It also generates the _bundle-analsys.txt_ file which shows how modules were bundled and the size contributed to the final file.

## 🛠 Installation

```bash
npm install -D patch-package
```

Copy one of the patch files from the `patches` folder to your project `patches` folder. Choose the correct Remix version for your patch.

Apply the patch

```bash
npx patch-package
```

Update your _package.json_ file to include the following postinstall script. This will ensure your patch is automatically applied when you checkout you project.

```json
"scripts": {
  "postinstall": "patch-package"
}
```
