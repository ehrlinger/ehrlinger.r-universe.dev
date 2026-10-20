# ehrlinger.r-universe.dev

The registry for the HVTI R package family on [R-universe](https://ehrlinger.r-universe.dev): `packages.json` lists every member, and R-universe builds each from its GitHub repository into a CRAN-style repository. Studies then install the family by package name, without the GitHub API and without personal tokens.

```r
install.packages("hvtiR", repos = c("https://ehrlinger.r-universe.dev", getOption("repos")))
```

**`boostmtree` is the CCF fork**, built from `ehrlinger/boostmtree_src` (subdirectory `boostmtree`) at the tag `ggBoostedTrees` pins in its `Remotes:`. CRAN also has a `boostmtree`; R installs whichever carries the higher version, so the fork's version must stay ahead of CRAN's. When `ggBoostedTrees` moves its pin, move `branch` here to the same tag.

Members and their repositories match `hvtiR::members()`, plus `hvtiR` itself. Scope and risks: `ehrlinger/hvtiR` `dev/specs/2026-10-20-r-universe-scope.md`.
