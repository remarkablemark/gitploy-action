# gitploy-action

[![version](https://badgen.net/github/release/remarkablemark/gitploy-action)](https://github.com/remarkablemark/gitploy-action/releases)
[![test](https://github.com/remarkablemark/gitploy-action/actions/workflows/test.yml/badge.svg)](https://github.com/remarkablemark/gitploy-action/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

🚀 GitHub Action to deploy a directory to a remote Git branch.

> [!NOTE]
>
> If you see the error:
>
> ```
> remote: Permission to ... denied to ....
> fatal: unable to access 'https://github.com/...': The requested URL returned error: 403
> ```
>
> Enable **Settings** > **Actions** > **General** > **Workflow permissions** > **Read and write permissions**

## Quick Start

```yaml
on: push
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      # insert build step
      # ...

      - name: Deploy to GitHub Pages
        uses: remarkablemark/gitploy-action@v1
        with:
          directory: build
```

## Usage

See [action.yml](https://github.com/remarkablemark/gitploy-action/blob/master/action.yml)

**Basic:**

```yaml
- uses: remarkablemark/gitploy-action@v1
```

## Inputs

### `directory`

**Required**: The directory of the build files.

```yaml
- uses: remarkablemark/gitploy-action@v1
  with:
    directory: build
```

### `branch`

**Optional**: The remote Git branch to deploy to. Defaults to `gh-pages`:

```yaml
- uses: remarkablemark/gitploy-action@v1
  with:
    directory: build
    branch: gh-pages
```

## Contributions

Contributions are welcome! 👋

## License

[MIT](https://github.com/remarkablemark/gitploy-action/blob/master/LICENSE)
