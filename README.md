# Block blockadblock

A simple [uBlock origin](https://github.com/gorhill/uBlock) fix to block the script distributed to block add blockers from [blockadblock](https://blockadblock.com/). The repository contains the script that is distributed as well as an unobfuscated script.


## The fix 

Add the following to ```My filters``` in the uBlock origin dashboard

```
example.com##^script:has-text(eval)
```

Change ```example.com``` to the domain that is executing the blockadblock script.

This simply blocks the initial call to eval - which is a [probably good thing to block in general](https://stackoverflow.com/questions/86513/why-is-using-the-javascript-eval-function-a-bad-idea)!

## License

[GPLv3](LICENSE)
