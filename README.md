# assetgen-assets

> 🌈 A showcase of spec files and AI-generated game art produced with [`assetgen`](https://github.com/hangovergames/assetgen).

This repo is **only example content**—think of it as a gallery + reference for
anyone learning to write spec files or evaluating assetgen’s output quality.
Each sub-folder is a self-contained sample project:

| Folder | What it contains | Run-cost* |
|--------|------------------|-----------|
| [`citygame`](./citygame) | 32 top-down road, car and building sprites (for a SimCity-style prototype) | ≈ $5.48 |

\*Costs are what we paid to the OpenAI Images API when the assets were generated.  
Actual prices may differ if you re-generate with new models or larger sizes.

### Using these samples

1. **Clone with submodules** (if you embedded this repo into a larger project):

   ```bash
   git submodule add https://github.com/hangovergames/assetgen-assets.git assets
   git submodule update --init
   ```

2. **Inspect the spec**—each project has an `Assetgenfile` describing the
   global prompt, per-asset prompts and any per-run configuration.

3. **Re-generate** (optional):

   ```bash
   # inside the project folder (e.g. citygame/)
   assetgen -n 10 Assetgenfile
   ```

4. **Optimise** (optional): after generation we run `optipng -o7 *.png`
   to squeeze the PNGs a bit.

### Contributing samples

Have a cool spec you want to share?

1. Fork the repo, create a new folder (e.g. `space-shooter/`).
2. Commit your `Assetgenfile`, the generated images and a small README
   noting the API cost.
3. Open a pull request 🚀

### Licence

All sample specs and generated images are released under the **MIT License** –
see [LICENSE](./LICENSE).  
You may use them in your own prototypes or games, though we recommend
re-generating graphics for production so you can pick the quality / style you
need.
