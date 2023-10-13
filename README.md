# action-smallstep-ca-bootstrap

This GitHub Action bootstraps your CA on your GitHub action with `step` CLI on Linux and MacOS. You can choose to bootstrap with our without a `step` CLI context.

## Usage

You can use this action by adding the following to your workflows. Please note that you need to have [step CLI](https://smallstep.com/docs/step-cli/) installed in order to use this workflow. We have made [smallstep/action-install-step-cli](https://github.com/smallstep/action-install-step-cli) which can do this for you. Please see that project's README for more information.

Install the latest version:

```yaml
- uses: smallstep/action-install-step-cli@v1
- uses: smallstep/action-smallstep-ca-bootstrap@v1
  with:
    smallstep-ca-url: https://<your_ca_slug>.<your_team>.ca.smallstep.com
    smallstep-ca-fingerprint: <your CA fingerprint>
```

Install with a specific version:

```yaml
- uses: smallstep/action-install-step-cli@v1
- uses: smallstep/action-smallstep-ca-bootstrap@v1
  with:
    smallstep-ca-url: https://<your_ca_slug>.<your_team>.ca.smallstep.com
    smallstep-ca-fingerprint: <your CA fingerprint>
    smallstep-cli-context: mycontext
```

## License

MIT License

Copyright (c) 2023 Smallstep Labs, Inc

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
