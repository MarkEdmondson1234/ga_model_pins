# ga_model_pins
ga_models that can be fetched with library(pins)

See https://github.com/MarkEdmondson1234/googleAnalyticsR/issues/280

```r
library(pins)

board_register_github(repo = "MarkEdmondson1234/ga_model_pins", branch = "main")

# repeat for each model to pin
m <- ga_model_example("decomp_ga_advanced.gamr")
pin(m, name = "decomp_ga_advanced", description = m$description, board = "github")
```

To use:

```r
ga_model(81416156, pin_get("decomp_ga", board = "github"))
ga_model(81416156, pin_get("decomp_ga_advanced", board = "github"), frequency = 7)
```
