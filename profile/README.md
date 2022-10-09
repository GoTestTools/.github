## Go Test Tools

Go Test Tools is a project by two Go developers, [@engelmi](https://github.com/engelmi) and [@janosdebugs](https://github.com/janosdebugs). We aim to make writing and maintaining tests easier for Go projects.

### gotestfmt: go test output for humans

Are you tired of scrolling through endless Golang test logs in GitHub Actions (or other CI systems)?

![An animation showcasing that gotestfmt transforms a text log into an interactive log with folding sections.](https://raw.githubusercontent.com/GoTestTools/.github/main/gotestfmt.svg)

Then this is the tool for you. Run it locally, or in any CI system with the following command line like this:

```bash
set -euo pipefail
go test -json -v ./... 2>&1 | tee /tmp/gotest.log | gotestfmt
```

Tadam, your tests will now show up in a beautifully formatted fashion. Plug it into your CI and you're done.

[Read more »](https://github.com/GoTestTools/gotestfmt)

---

### limgo: Don't let your test coverage drop

Do you need to guard your Go test coverage and make sure it doesn't drop below a limit? Then [limgo](https://github.com/GoTestTools/limgo) is the right tool for you.

Simply install it and get started:

```
go install github.com/GoTestTools/limgo@latest
go test ./... -coverprofile=cov.out
limgo -coverfile=cov.out -config=.limgo.json -v=1
```

[Read more »](https://github.com/GoTestTools/gotestfmt)