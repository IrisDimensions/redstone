# Redstone

Redstone is a minimal Iris dimension pack for high-throughput redstone and build testing. It generates a level, two-block-deep white-concrete work surface at world Y 2, with bedrock at Y 0 and a normal Overworld environment.

The dimension uses `SUPERFLAT` mode so Iris runs only its terrain and biome stages. Decoration, objects, custom mob generation, caves, mantle work, and Iris structure placements are intentionally absent. Its native-structure policy denies the entire `minecraft:` namespace, so no vanilla or Minecraft-namespaced datapack structures generate in new chunks.

Iris structure policies match namespace prefixes rather than supporting a global wildcard. A server that installs structures under another namespace must add that namespace prefix to `importedStructures.disabled` to preserve the structure-free contract.

## Install and validate

Copy this directory as `redstone` under the Iris packs root:

- Bukkit, Paper, or Folia: `plugins/Iris/packs/redstone/`
- Fabric, Forge, or NeoForge: `config/irisworldgen/packs/redstone/`

On Bukkit-family servers, validate and create a disposable world with:

```text
/iris pack validate pack=redstone
/iris create name=redstone-test type=redstone seed=1337
```
