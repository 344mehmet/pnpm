# 344mehmet/pnpm

> [!NOTE]
> Bu depo, **pnpm** projesinin güncel bir çatallamasıdır (fork). TDK standartlarına uygun Türkçe dokümantasyon ve yerel geliştirmeler içermektedir.

## 🇹🇷 Türkçe Özet (TDK Uyumlu)
pnpm, disk alanından tasarruf sağlayan ve kurulumları hızlandıran gelişmiş bir **Paket Yöneticisidir**.

**Özellikler:**
*   **Hızlı:** Alternatiflerinden 2 kata kadar daha hızlıdır.
*   **Verimli:** `node_modules` içindeki dosyalar içerik adresli tek bir depodan bağlanır, disk alanından tasarruf sağlar.
*   **Monorepo Desteği:** Çoklu paket içeren depolar için mükemmel destek sunar.
*   **Katı:** Paketler sadece `package.json` dosyasında belirtilen bağımlılıklara erişebilir.
*   **Kararlı:** `pnpm-lock.yaml` dosyası ile deterministik kurulum sağlar.
*   **Node.js Sürüm Yöneticisi:** `pnpm env use` komutu ile Node.js sürümlerini yönetebilir.

---

[简体中文](https://pnpm.io/zh/) |
[日本語](https://pnpm.io/ja/) |
[한국어](https://pnpm.io/ko/) |
[Italiano](https://pnpm.io/it/) |
[Português Brasileiro](https://pnpm.io/pt/)

<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://i.imgur.com/qlW1eEG.png">
  <source media="(prefers-color-scheme: dark)"  srcset="https://i.imgur.com/qlW1eEG.png">
  <img src="https://i.imgur.com/qlW1eEG.png" alt="pnpm">
</picture>

Fast, disk space efficient package manager:

* **Fast.** Up to 2x faster than the alternatives (see [benchmark](#benchmark)).
* **Efficient.** Files inside `node_modules` are linked from a single content-addressable storage.
* **[Great for monorepos](https://pnpm.io/workspaces).**
* **Strict.** A package can access only dependencies that are specified in its `package.json`.
* **Deterministic.** Has a lockfile called `pnpm-lock.yaml`.
* **Works as a Node.js version manager.** See [pnpm env use](https://pnpm.io/cli/env).
* **Works everywhere.** Supports Windows, Linux, and macOS.
* **Battle-tested.** Used in production by teams of [all sizes](https://pnpm.io/users) since 2016.
* [See the full feature comparison with npm and Yarn](https://pnpm.io/feature-comparison).

To quote the [Rush](https://rushjs.io/) team:

> Microsoft uses pnpm in Rush repos with hundreds of projects and hundreds of PRs per day, and we’ve found it to be very fast and reliable.

[![npm version](https://img.shields.io/npm/v/pnpm.svg?label=latest)](https://github.com/pnpm/pnpm/releases/latest)
[![OpenCollective](https://opencollective.com/pnpm/backers/badge.svg)](https://opencollective.com/pnpm)
[![OpenCollective](https://opencollective.com/pnpm/sponsors/badge.svg)](https://opencollective.com/pnpm)
[![X Follow](https://img.shields.io/twitter/follow/pnpmjs.svg?style=social&label=Follow)](https://x.com/intent/follow?screen_name=pnpmjs&region=follow_link)
[![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/badges/StandWithUkraine.svg)](https://stand-with-ukraine.pp.ua)

## Platinum Sponsors

<table>
  <tbody>
    <tr>
      <td align="center" valign="middle">
        <a href="https://bit.dev/?utm_source=pnpm&utm_medium=readme" target="_blank"><img src="https://pnpm.io/img/users/bit.svg" width="80" alt="Bit"></a>
      </td>
    </tr>
  </tbody>
</table>

## Gold Sponsors

<table>
  <tbody>
    <tr>
      <td align="center" valign="middle">
        <a href="https://sanity.io/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/sanity.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/sanity_light.svg" />
            <img src="https://pnpm.io/img/users/sanity.svg" width="120" alt="Sanity" />
          </picture>
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://discord.com/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/discord.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/discord_light.svg" />
            <img src="https://pnpm.io/img/users/discord.svg" width="220" alt="Discord" />
          </picture>
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://vite.dev/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <img src="https://pnpm.io/img/users/vitejs.svg" width="42" alt="Vite">
        </a>
      </td>
    </tr>
    <tr>
      <td align="center" valign="middle">
        <a href="https://serpapi.com/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/serpapi_dark.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/serpapi_light.svg" />
            <img src="https://pnpm.io/img/users/serpapi_dark.svg" width="160" alt="SerpApi" />
          </picture>
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://coderabbit.ai/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/coderabbit.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/coderabbit_light.svg" />
            <img src="https://pnpm.io/img/users/coderabbit.svg" width="220" alt="CodeRabbit" />
          </picture>
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://workleap.com/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/workleap.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/workleap_light.svg" />
            <img src="https://pnpm.io/img/users/workleap.svg" width="190" alt="Workleap" />
          </picture>
        </a>
      </td>
    </tr>
    <tr>
      <td align="center" valign="middle">
        <a href="https://stackblitz.com/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/stackblitz.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/stackblitz_light.svg" />
            <img src="https://pnpm.io/img/users/stackblitz.svg" width="190" alt="Stackblitz" />
          </picture>
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://nx.dev/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/nx.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/nx_light.svg" />
            <img src="https://pnpm.io/img/users/nx.svg" width="50" alt="Nx" />
          </picture>
        </a>
      </td>
    </tr>
  </tbody>
</table>

## Silver Sponsors

<table>
  <tbody>
    <tr>
      <td align="center" valign="middle">
        <a href="https://uscreen.de/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/uscreen.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/uscreen_light.svg" />
            <img src="https://pnpm.io/img/users/uscreen.svg" width="180" alt="u|screen" />
          </picture>
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://leniolabs.com/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <img src="https://pnpm.io/img/users/leniolabs.jpg" width="40" alt="Leniolabs_">
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://depot.dev/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/depot.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/depot_light.svg" />
            <img src="https://pnpm.io/img/users/depot.svg" width="100" alt="Depot" />
          </picture>
        </a>
      </td>
    </tr>
    <tr>
      <td align="center" valign="middle">
        <a href="https://devowl.io/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/devowlio.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/devowlio.svg" />
            <img src="https://pnpm.io/img/users/devowlio.svg" width="100" alt="devowl.io" />
          </picture>
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://cerbos.dev/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/cerbos.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/cerbos_light.svg" />
            <img src="https://pnpm.io/img/users/cerbos.svg" width="90" alt="Cerbos" />
          </picture>
        </a>
      </td>
      <td align="center" valign="middle">
        <a href="https://oomol.com/?utm_source=pnpm&utm_medium=readme" target="_blank">
          <picture>
            <source media="(prefers-color-scheme: light)" srcset="https://pnpm.io/img/users/oomol.svg" />
            <source media="(prefers-color-scheme: dark)" srcset="https://pnpm.io/img/users/oomol_light.svg" />
            <img src="https://pnpm.io/img/users/oomol.svg" width="90" alt="OOMOL Studio" />
          </picture>
        </a>
      </td>
    </tr>
  </tbody>
</table>

Support this project by [becoming a sponsor](https://opencollective.com/pnpm#sponsor).

## Background

pnpm uses a content-addressable filesystem to store all files from all module directories on a disk.
When using npm, if you have 100 projects using lodash, you will have 100 copies of lodash on disk.
With pnpm, lodash will be stored in a content-addressable storage, so:

1. If you depend on different versions of lodash, only the files that differ are added to the store.
  If lodash has 100 files, and a new version has a change only in one of those files,
  `pnpm update` will only add 1 new file to the storage.
1. All the files are saved in a single place on the disk. When packages are installed, their files are linked
  from that single place consuming no additional disk space. Linking is performed using either hard-links or reflinks (copy-on-write).

As a result, you save gigabytes of space on your disk and you have a lot faster installations!
If you'd like more details about the unique `node_modules` structure that pnpm creates and
why it works fine with the Node.js ecosystem, read this small article: [Flat node_modules is not the only way](https://pnpm.io/blog/2020/05/27/flat-node-modules-is-not-the-only-way).

💖 Like this project? Let people know with a [tweet](https://r.pnpm.io/tweet)

## Getting Started

- [Installation](https://pnpm.io/installation)
- [Usage](https://pnpm.io/pnpm-cli)
- [Frequently Asked Questions](https://pnpm.io/faq)
- [X](https://x.com/pnpmjs)
- [Bluesky](https://bsky.app/profile/pnpm.io)

## Benchmark

pnpm is up to 2x faster than npm and Yarn classic. See all benchmarks [here](https://r.pnpm.io/benchmarks).

Benchmarks on an app with lots of dependencies:

![](https://pnpm.io/img/benchmarks/alotta-files.svg)

## License

[MIT](https://github.com/pnpm/pnpm/blob/main/LICENSE)

