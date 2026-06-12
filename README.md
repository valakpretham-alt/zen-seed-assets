# ZEN SEED Assets Repository

3D assets for the **ZEN SEED** meditation app - a Three.js powered experience.

## Asset Pack

**Source:** KayKit - Forest Nature Pack (FREE)  
**License:** CC0 - Free to use commercially  
**Format:** glTF 2.0 (optimized for Three.js)

## Contents

```
gltf/
├── Trees (20 models)
│   ├── Leafy trees (Tree_1 through Tree_4)
│   └── Bare trees (seasonal variations)
├── Rocks (43 models)
│   └── 3 base types with multiple variants (A-R)
├── Bushes (22 models)
│   └── 4 base types with variations
├── Grass (20 models)
│   ├── Double-sided (for richness)
│   └── Single-sided (for mobile performance)
└── Textures
    └── forest_texture.png (shared by all models)
```

**Total Assets:** 100+

## Quick Start

### Loading Assets in Three.js

```javascript
import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader.js';

const ASSET_BASE_URL = 'https://valakpretham-alt.github.io/zen-seed-assets/gltf/';

const loader = new GLTFLoader();
loader.load(
  `${ASSET_BASE_URL}Tree_1_A_Color1.gltf`,
  (gltf) => {
    const tree = gltf.scene;
    scene.add(tree);
  }
);
```

### Asset Manifest

See `manifest.json` for:
- Complete asset listing
- Model IDs and filenames
- Category organization
- Loading recommendations

## Performance Tips

1. **Lazy load assets** - Load models only when needed, not all at once
2. **Cache textures** - The texture is shared; load once, reuse
3. **Mobile optimization** - Use single-sided grass variants on mobile
4. **CDN delivery** - Assets are served via GitHub Pages (fast delivery)

## Integration with ZEN SEED

Assets are organized to support garden progression:
- **Early stages:** Simple trees, minimal vegetation
- **Growth stages:** Add bushes, rocks for complexity
- **Full bloom:** Dense grass, multiple tree types

See the main project repo for progression logic.

## License

All assets are **CC0** - Public Domain. Free to use commercially without attribution.

**Creator:** KayKit by Kay Lousberg

---

**Last Updated:** 2026-06-12  
**Repository:** github.com/valakpretham-alt/zen-seed-assets
