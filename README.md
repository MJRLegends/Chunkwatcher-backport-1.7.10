# ChunkWatcher
ChunkWatcher is a lightweight mod able to block force chunkloading of specified mods.

## Features
* Configurable blacklist for mods
* In-game commands
* Reloadable at runtime
* See what mods keeps chunks loaded in a certain world, and how many.

## Commands
* `/chunkwatcher`<br>
shows available commands
* `/chunkwatcher block <mod name>`<br>
Blocks forcing chunks for a mod (Case insensitive).
* `/chunkwatcher allow <mod name>`<br>
Re-enables forcing chunks for a mod (Case insensitive).
* `/chunkwatcher reload`<br>
Reload the config.
* `/chunkwatcher show <mod name> [dimension ID]`<br>
Shows coordinates of the loaded chunks, for the specified mod.
* `/chunkwatcher list [dimension ID]`<br>
Provides a summary of total forced chunks per-mod.
   ##### Example:<br>
  `/chunkwatcher list` shows the forced chunks in your current world.<br>
  `/chunkwatcher list 0` shows the forced chunks in the overworld.<br>
  `/chunkwatcher list 1` shows the forced chunks in the end.<br>
  `/chunkwatcher list -1` shows the forced chunks in the nether.<br>
  > Note: As console, you __must__ always provide a dimension ID.


## How it works
ChunkWatcher listens for mods that request to force a chunk.
When that happens, ChunkWatcher checks the mod's name against the configurable blacklist. If there's a match, the chunk will be unloaded immediately.

## Benefits
* Server performance!
* Disabling unnecessary chunkloading by mods. Potentially allowing you to un-ban some items related to chunk loading!
* Prevent illegal chunk loading.

## Limitations
Not all mods are written equally, some mods may require a chunk to be loaded in order to function at all. In most cases, though: it should work.