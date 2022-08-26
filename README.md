# Starknet Interface Checker

Check whether your contract interfaces match the actual contract implementations. Don't let them go out of sync.

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
