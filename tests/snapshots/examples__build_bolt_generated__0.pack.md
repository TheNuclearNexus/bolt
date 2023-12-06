# Lectern snapshot

## Data pack

`@data_pack pack.mcmeta`

```json
{
  "pack": {
    "pack_format": 26,
    "description": ""
  }
}
```

### demo

`@function demo:foo`

```mcfunction
say 123
```

`@function demo:generated`

```mcfunction
execute if score #smithed.core load.status matches 1 run function demo:0
```

`@function demo:0`

```mcfunction
data merge storage smithed:log {message: '["Could not find ",{"text":"#smithed.prevent_aggression 0.0.1","color":"red"}]', type: "ERROR"}
function #smithed:core/pub/technical/tools/log
```
