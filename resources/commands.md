# Useful Console Commands

Open command by pressing `~`

## Start/Stop all trains

start

```lua
/c for k,t in pairs(game.player.force.get_trains()) do t.manual_mode = false end
```
stop

```lua
/c for k,t in pairs(game.player.force.get_trains()) do t.manual_mode = true end
```


## Research Minining Productivity

```lua
/c game.player.force.technologies['mining-productivity-4'].level = 170
```

[# of miners] = [desired output] / ( [miner base speed] * (1 + [speed module boost]*[number of speed modules]) * ( 1 + 0.1 * [mining research level]) )

Note a vanilla miner's base speed is 0.5, so not really a variable unless using modded miners.

Plugging some numbers in: how many miners with 3@Speed3 modules and level 170 mining productivity does it take to fill 1/2 a blue belt (22.5 items/s)?:

22.5/(0.5 * (1 + 0.5*3)*(1 + 0.1*170) ) = 1