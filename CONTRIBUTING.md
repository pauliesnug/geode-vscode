# Contrubuting

## Steps

1. Fork and clone the repository.
2. Open the `Extensions` tab of VSCode.
3. Search for `@recommended`.
4. Make sure to install the `TypeScript + Webpack Problem Matchers` extension.
5. Run `ni` (or `pnpm i`) in terminal.
6. Press <kbd>F5</kbd> or `Code -> Run -> Start Debugging` to start debuging.

## Troubleshooting

### Task Error

**Error messages:**

- In `OUTPUT` panel of VSCode 👇.

```jsonc
Error: the description can't be converted into a problem matcher:
{
    "base": "$ts-webpack-watch",
    "background": {
        "activeOnStart": true,
        "beginsPattern": "Build start",
        "endsPattern": "Build success"
    }
}
```

- A popup like this 👇.

```bash
The task 'npm: dev' cannot be tracked. Make sure to have a problem matcher defined.
```

**Solution:**

Please make sure you follow the steps above and install the recommended extension. This extension provides the `$ts-webpack-watch` problem matcher required in `.vscode/tasks.json`.

### Terminal Starting Error

After pressing <kbd>F5</kbd>, if there isn't a new terminal named `Task` autostart in the `TERMINAL` panel of VS Code, and recommended extension is installed correctly, it may because VS Code doesn't load your `.zshrc` or other bash profiles correctly.

**Error message:**

- An error tip in the bottom right corner like this 👇.

```bash
The terminal process "/bin/zsh '-c', 'pnpm run dev'" terminated with exit code: 127.
```

**Solutions:**

- Run `pnpm run dev` (or `nr dev`) manually.
- Quit out of VSCode and restart it from your terminal app by running the `code` command.
