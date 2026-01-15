# Proposed Plugins

Plugins need to be 4.21-4.27 compatible (do not propose here any ue5 only plugins).

This document serves as a summary of plugins to be added to the engine repo, and for a list of others to keep as common use, but not to be added to the Repo directly.

Already integrated Plugins are located in: Engine\Plugins\Runtime\VitePlugins
![Plugins1.png](Plugins1.png)

General guidelines:

For Engine Repo: Represents core functionality and native runtime (low in size/comp times)

“Staples”: Represents relevant plugins for general game production, often used in AAA productions, and represents major functionality.

“Common use”: Represents non-essential/High Level tooling (such as BP extensions)

## Pending to be added to the engine repo

### FSR 4 and Anti Lag 2

[https://gpuopen.com/fidelityfx-super-resolution-4/](https://gpuopen.com/fidelityfx-super-resolution-4/)
[https://gpuopen.com/anti-lag-2/](https://gpuopen.com/anti-lag-2/)

### Blast (PhysX 3)

## Staple Plugins

### PhysX InstancedSubsystem [] (free)
PhysX Instanced Subsystem is an Unreal Engine plugin that provides a world subsystem + instanced actor workflow for managing large amounts of PhysX-backed instanced bodies.

Instead of spawning thousands of separate AActor / UPrimitiveComponent objects, you keep one (or a few) instanced mesh actors for rendering, while the subsystem creates and updates per-instance PhysX rigid bodies and writes their poses back into ISM/HISM-style instance transforms.

[PhysXInstancedSubsystem](https://github.com/Dragomirson/PhysXInstancedSubsystem)

[Demo Project](https://drive.google.com/file/d/1NulunBP2Qre5vLyYnkiqywovsycNuWdQ/view)

### Houdini [Added] (commercial/free use)

Powerful and flexible procedural workflow into Unreal Engine through Houdini Digital Assets. Artists can interactively adjust asset parameters inside the editor and use Unreal assets as inputs. Houdini's procedural engine will then "cook" the asset, and the results will be available in the editor without the need for baking.

[sideeffects/HoudiniEngineForUnreal at Houdini20.0-Unreal4.27](https://github.com/sideeffects/HoudiniEngineForUnreal/tree/Houdini20.0-Unreal4.27)

### Confetti FX (commercial/free use)

Proprietary particle system used in several AAA titles (Blizzard titles/racing games). 2.18.6 is the latest fully compatible ver with UE 4.27. Features better GPU perf than Niagara.

[PopcornFX/UnrealEnginePopcornFXPlugin: PopcornFX plugin for Unreal Engine 5](https://github.com/PopcornFX/UnrealEnginePopcornFXPlugin) </br>
Direct download: [https://github.com/PopcornFX/UnrealEnginePopcornFXPlugin/archive/refs/tags/v2.18.6.zip](https://github.com/PopcornFX/UnrealEnginePopcornFXPlugin/archive/refs/tags/v2.18.6.zip)

Patched Version (fixes a compile error, by bunnyofficial): [https://drive.google.com/file/d/1hckpY_1zSLsW6mBqBlDeEgPVSijg9Z_y/view?usp=drive_link ](https://drive.google.com/file/d/1hckpY_1zSLsW6mBqBlDeEgPVSijg9Z_y/view?usp=drive_link)

### Azure Playfab (commercial/free use)
Azure PlayFab is a comprehensive backend platform for building and operating live games, providing managed services for player authentication, data storage, matchmaking, multiplayer networking, analytics, and live operations (LiveOps) like events and A/B testing, all powered by Microsoft Azure's global infrastructure
![Plugins2.png](Plugins2.png)
[PlayFab/UnrealMarketplacePlugin: Source code for the PlayFab Marketplace Plugin for Unreal](https://github.com/PlayFab/UnrealMarketplacePlugin)

### Wwise (commercial/free use)
With hundreds of titles shipped, Wwise is the leading audio solution and trusted standard for the gaming and interactive audio industry.
[Wwise Unreal Integration](https://www.audiokinetic.com/en/public-library/2025.1.3_9039/?source=UE4&id=index.html)

### Downgrader Plugin  (Paid)
Asset Downgrader will downgrade assets to 5.6.1, 5.5.4, 5.4.4, 5.3.2, 5.2.1, 5.1.1, 5.0.3, 4.27, 4.26 . It works by first upgrading the assets to Source Version (5.6), and then applying various patches to the .uasset files in order to make them compatible with the TargetVersion, just without the newer data (i.e. nanite data is removed for a 4.27 downgrade). Do note that features of the newer unreal versions (like nanite on masked materials, new material nodes, new niagara modules) can't be ported to the old versions.

Ciprian Stanciu (downgrader creator) is on Vite Discord 
![CiprianStanciu.png](CiprianStanciu.png)

![AssetDwongrader.png](AssetDwongrader.png)

### Motion Symphony [Added] (Ubisoft-based Motion Matching)

Documentation:
[https://www.wikiful.com/@AnimationUprising/motion-symphony/motion-matching](https://www.wikiful.com/@AnimationUprising/motion-symphony/motion-matching)

Sample Project (Vite compatible):
[https://github.com/Animation-Uprising/MotionSymphony_ExampleProject/tree/main ](https://github.com/Animation-Uprising/MotionSymphony_ExampleProject/tree/main )

### HTN  (FAB/Paid)
Battle-tested Unreal rendition of HTN AI Framework: The strategy is built with a goal-driven approach by separating ‘what’ to do and ‘how’ to do it. [HTN plugin for Unreal Engine](https://maksmaisak.github.io/htn/front.html)

1.18.3 has been recently backported for 4.27
![HTN.png](HTN.png)

## Common use Plugins

### FFMPEG Media Player
[bakjos/FFMPEGMedia: Unreal FFMPEG Plugin to support more video formats and alpha videos](https://github.com/bakjos/FFMPEGMedia)

### UI Navigation  (Blueprints)
[https://github.com/goncasmage1/UINavigation/tree/4.27_3.0](https://github.com/goncasmage1/UINavigation/tree/4.27_3.0)

### Multiplayer Movement Plugin  (Blueprints)
[https://github.com/Reddy-dev/SMN2/tree/master(deprecated)](https://github.com/Reddy-dev/SMN2/tree/master(deprecated)) , supported up to ue4.26 but can be compiled and used on ue4.27 and also it is possible to additionally extend functionality.

### Root Motion (Blueprints)
[https://github.com/VJien/RootMotionSource](https://github.com/VJien/RootMotionSource)
this is fully functional pugin for ue4.26 and ue4.27. you have details here [https://supervj.top/2022/03/24/RootMotionSource/?highlight=root+motion+source](https://supervj.top/2022/03/24/RootMotionSource/?highlight=root+motion+source) and also mutch more for ue4. its almost same as motion warping for ue5. in ue4 we have this as root motion source but it is correct network functional only trough gas. this plugin override that and give us fully funcionality for root motion source directly in blueprints. i have partial testing this in real network with lag and if we folow some cmc logic with this it give perfect results without jittering and corrections from server side during root motion animations.
![Plugins3.png](Plugins3.png)

