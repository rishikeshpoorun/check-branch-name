# Branch naming rules
<img alt="GitHub Actions status" src="https://github.com/deepakputhraya/action-branch-name/workflows/main/badge.svg">

Github action to enforce naming convention on branch names

## Usage

See [action.yml](./action.yml)

```yaml
steps:
- uses: rishikesh.poorun/check-branch-name@master
  with:
    regex: '([a-z])+\/([a-z])+' # Regex the branch should match. This example enforces grouping
    allowed_prefixes: 'feature,stable,fix' # All branches should start with the given prefix
    ignore: master,develop # Ignore exactly matching branch names from convention
    min_length: 5 # Min length of the branch name
    max_length: 20 # Max length of the branch name
```