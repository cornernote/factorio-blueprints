# Useful Console Commands

Open command by pressing `~`

## Start/Stop all trains

start

```
/c for k,t in pairs(game.player.force.get_trains()) do t.manual_mode = false end
```
stop

```
/c for k,t in pairs(game.player.force.get_trains()) do t.manual_mode = true end
```