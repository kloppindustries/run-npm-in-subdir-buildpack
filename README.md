The actual build component (`compile`) is just changing into a specific directory, and running an `npm` invocation to compile the SPA into a new location as an artifact rather than a VCS changeset.

There's nothing of note in either `detect` or `release`, though the assumption is that there is a buildpack providing `node` and `npm` higher up in the chain...

That is, the entire thing is:

```bash
cd to-directory
npm run my-cool-command
```

🤨😮‍😮‍💨

Don't forget to use [shellcheck](https://www.shellcheck.net/) if you make changes to this.