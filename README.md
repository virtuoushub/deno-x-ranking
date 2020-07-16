# deno-x-ranking
[![(Deno)](https://img.shields.io/badge/deno-v1.1.3-green.svg?style=flat-square&logo=deno)](https://deno.land)
![gh-pages](https://github.com/yoshixmk/deno-x-ranking/workflows/gh-pages/badge.svg)
[![nest badge](https://nest.land/badge.svg)](https://nest.land/package/ranking)  

🦕 Deno Third Party Modules Ranking 👑    
https://deno.land/x/ranking

## Ranking Page
https://yoshixmk.github.io/deno-x-ranking

## Get Started

### Github API Tokens
Prepare an access token for Github public access permission only from the following URL. When public access setting permissions, you can leave all check boxes cleared.  
https://github.com/settings/tokens/new

### Tsv output
```Shell
$ deno run --allow-net --allow-write https://deno.land/x/ranking/mod.ts -u <github username> -t <github token> -f tsv
```

### Console output
```Shell
$ deno run --allow-net https://deno.land/x/ranking/mod.ts -u <github username> -t <github token> -f table
```

### Markdown output
```Shell
$ deno run --allow-net --allow-write --allow-read https://deno.land/x/ranking/mod.ts -u <github username> -t <github token> -f markdown
```

### Help
```Shell
$ deno run https://deno.land/x/ranking/mod.ts -h
```

## Ranking Logic
After processing according to the ranking logic below, limit to only the necessary data for each output format, and output at the end.
1. Ranking GitHub Star count.  
1. Sorted by GitHub Star.  
1. If same GitHub Star count, continue to check rank using forks count, watchers count, subscribers count.

## Sample
[./examples/ranking_result.tsv](./examples/ranking_result.tsv)

## Plan
- [x] `"type": "github"` support  
- [ ] `"type": "npm"` support  
- [ ] `"type": "deno_std"` support  
- [x] real-time ranking page update