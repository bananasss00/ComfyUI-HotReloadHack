# ComfyUI-HotReloadHack
Hot reloading for custom node developers

This is a very hacky way to get hot reloading of custom nodes, but has worked very well on all workflows tested.

## Features
* Watches files in `ComfyUI/custom_nodes/`
* Automatically reloads new code for any repo changed
* Clears the Comfy execution cache so Comfy will rerun nodes in changed repo
* Automatically loads in new repos that you download without the need to restart ComfyUI

## Installation
After git cloning the repo into your `custom_nodes/` you only need to install watchdog.
```
python -m pip install watchdog
```

## How to Use

HotReloadHack automatically watches files in your `custom_nodes/` directory and when one changes reloads the node repo it belongs to. 

It does not use a file dependency graph (yet), so all nodes in the changed repo will run on the next Comfy execution.

## Examples

![example_without_hrh](https://github.com/user-attachments/assets/7f29fd52-410d-48fe-8f1a-64b6d5e122f3)

![example_with_hrh](https://github.com/user-attachments/assets/a13f6e4f-a081-43bd-89b8-e6a98483f52f)
