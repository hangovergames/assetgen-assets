# City-Game Asset Pack

A collection of **32** top-down sprites—roads, buildings and vehicles—designed
to drop into a tile-based city builder or traffic sim.

| Category  | Files | Preview |
|-----------|-------|---------|
| Roads     | 12 PNG | `road_straight_ns.png`, `road_corner_ne.png`, … |
| Buildings | 14 PNG | `building_gas_station.png`, `building_office_block.png`, … |
| Vehicles  | 6 PNG  | `car_taxi.png`, `van_delivery.png`, … |

*(Browse the folder to see thumbnails in GitHub.)*

### Generation details

* **Spec file:** [`instructions.md`](./instructions.md)
* **Model:** `gpt-image-1`
* **Size:** `1024 × 1024`
* **Cost:** **$ 5.48** in OpenAI usage (April 2025 pricing)
* **Post-processing:** `optipng -o7 *.png` after generation

### Re-create the set

```bash
# From repo root
cd citygame
rm *.png
assetgen instructions.md -c 32          # or smaller batches with -c 5
```

The script will skip images that already exist, so you can experiment with new
models or parameters without overwriting the originals—just point the output
to a new directory.

Enjoy building your virtual metropolis! 🏙️
