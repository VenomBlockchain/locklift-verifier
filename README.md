# Locklift Verification plugin

<p align="center">
    <p align="center">
        <a href="/LICENSE">
            <img alt="GitHub" src="https://img.shields.io/badge/license-Apache--2.0-orange" />
        </a>
        <a href="https://www.npmjs.com/package/locklift-verifier">
            <img alt="npm" src="https://img.shields.io/npm/v/locklift-verifier">
        </a>
    </p>
</p>

<p align="center">
  <a href="https://github.com/venom-blockchain/developer-program">
    <img src="https://raw.githubusercontent.com/venom-blockchain/developer-program/main/vf-dev-program.png" alt="Logo" width="366.8" height="146.4">
  </a>
</p>



## Install
Inside the locklift project
```shell
npm i locklift-verifier
```

Inside the locklift.config.ts
```typescript
import "locklift-verifier";

const config: LockliftConfig = {
    verifier: {
        verifierVersion: "latest", // contract verifier binary, see https://github.com/broxus/everscan-verify/releases
        apiKey: "APIKEY",
        secretKey: "SECRET",
       // license: "AGPL-3.0-or-later", <- this is default value and can be overrided
    },
  ///////////////////
}
```

## Usage
```shell
npx locklift verify
```
Example output
```text
✅ Verified contracts:

╭────────────────────────────────┬──────────────────────────────────────────────────────────────────╮
│ Contract path                  ┆ Code hash                                                        │
╞════════════════════════════════╪══════════════════════════════════════════════════════════════════╡
│ /app/contracts/src/Sample.tsol ┆ a47ca4e6f055804482d01eeb65bc4a4d6aff83fd3cb703da3ff3569480b3c6e1 │
╰────────────────────────────────┴──────────────────────────────────────────────────────────────────╯
```



