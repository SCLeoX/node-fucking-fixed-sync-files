This is a fork of [byteclubfr/node-sync-files](https://github.com/byteclubfr/node-sync-files). They are basically the same thing except this fork is fucking fixed, so it actually works on frequently changed files and doesn't give you one billion npm security warnings when you use it.

P.S. Command is still called `sync-files`, but you can use `fucking-fixed-sync-files` alternatively if you want to.

# node-fucking-fixed-sync-files

Synchronize files or folders locally, with a watch option

## Install

Locally:

```sh
npm install fucking-fixed-sync-files
```

Globally:

```sh
npm install --global fucking-fixed-sync-files
```

## Usage

![](help-screen.png)

### In your `package.json`

You may have some build script in your package.json involving mirroring folders (let's say, static assets), that's a good use-case for `sync-files`:

```js
// Before
{
  "scripts": {
    "build": "cp -rf src/images dist/",
    "watch": "???"
  }
}

// After
{
  "devDependencies": {
    "sync-files": "^1.0.3"
  },
  "scripts": {
    "build": "sync-files src/images dist/images",
    "watch": "sync-files --watch src/images dist/images"
  }
}
```

## Sample

![](sample-screen.png)
