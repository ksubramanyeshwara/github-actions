# Shared Actions

- It is a reusable github actions that can be accessed within the same repo, across repos in an org, or publicly from the GitHub Marketplace.

## GitHub Marketplace

[GitHub Marketplace Actions](https://github.com/marketplace?type=actions)

- It is a place where you can find ready made actions that you can use in your workflows

### Example from marketplace:

`actions/checkout@v4` : pulls your repo code into the runner

## How it works

1. Create an action inside the repo
   ```
   my-org/
   └── terraform-action/
     ├── action.yml
     └── script.sh
   ```
2. Then use it:
   ```
   - uses: my-org/terraform-action@v1
   ```
