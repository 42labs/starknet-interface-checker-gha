# Starknet Interface Checker

The starknet-interface-checker let's you check whether the contract interface matches the contract implementation. This helps you catch when your files go out of sync.

## Usage

It assumes interfaces Assumes convention that if contract is called `Contract.cairo` then interface is `IContract.cairo`.

See the [Empiric repo](https://github.com/42labs/Empiric) for a real world example.

### Inputs

| input | required | description |
| ----- | -------- | ----------- |
| `cairo-path` | yes | Path to Cairo files, used to search for files to check and for relative imports when compiling. |

### Example

In the following example our Cairo files are in the `contracts` folder.

```yaml
- uses: 42labs/starknet-interface-checker-gha@main
  with:
    cairo-path: 'contracts'
```
