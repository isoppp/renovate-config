## Usage

Create a file in `.github/renovate.json5` , your work repository.

```json5
{
  // import this config
  "extends": [
    "github>isoppp/renovate-config"
  ],
  
  // enable specific managers(recommend)
  "enabledManagers": ["npm", "github-actions"],
}
```

## Note

To test config:

```bash
LOG_LEVEL=debug \
RENOVATE_BASE_BRANCHES=main \
GITHUB_TOKEN=********* \
RENOVATE_CONFIG_FILE=.github/renovate.json5 \
  npx renovate \
    --token=$GITHUB_TOKEN \
    --schedule="" \
    --require-config=ignored \
    --dry-run=full username/repository-name
```