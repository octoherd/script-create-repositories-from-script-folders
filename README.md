# create-repositories-from-folder

> An [octoherd](https://github.com/octoherd) script that creates new repositories from folders

This script is specific to the needs of a one-time migration for [@octoherd](https://github.com/octoherd). But it might be a good starting point if you need to create a script to eject a monorepo setup yourself.

## Usage

Minimal usage

```
$ npx @octoherd/script-create-repositories-from-script-folders \
  --path-to-folders "scripts"
```

Pass all options as CLI flags to avoid user prompts

```
$ npx @octoherd/script-create-repositories-from-script-folders \
  --path-to-folders "scripts" \
  -T ghp_0123456789abcdefghjklmnopqrstuvwxyzA \
  -R "octoherd/repository-with-script-folders"
```

## Options

| option                       | type             | description                                                                                                                                                                                                                                 |
| ---------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `--path-to-folders`          | string           | **Required.** Relative path to where the folders are located                                                                                                                                                                                |
| `--octoherd-token`, `-T`     | string           | A personal access token ([create](https://github.com/settings/tokens/new?scopes=repo)). Script will create one if option is not set                                                                                                         |
| `--octoherd-repos`, `-R`     | array of strings | One or multiple space-separated repositories in the form of `repo-owner/repo-name`. `repo-owner/*` will find all repositories for one owner. `*` will find all repositories the user has access to. Will prompt for repositories if not set |
| `--octoherd-bypass-confirms` | boolean          | Bypass prompts to confirm mutating requests                                                                                                                                                                                                 |

## License

[ISC](LICENSE.md)
