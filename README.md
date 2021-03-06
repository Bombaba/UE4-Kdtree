# UE4 Plugin: kd-tree

This is a UE4 plugin to provide utility functions for building kd-tree as Blueprint Function Library.


## Supported Environment

This plugin is tested on the below environment.

* UE4 Version: 4.22 
* OS: Windows/Mac


## Installation

#### 1. Download source codes

Download whole project's source codes from [GitHub](https://github.com/nutti/UE4-Kdtree/archive/master.zip) and unzip them.


#### 2. Copy the plugin source codes

Copy the plugin source codes (`Kdtree` directory) into the plugin directory (`Plugin` directory) on your UE4 project.


#### 3. Generate a project file for each IDE

Generate a project file for Visual Studio (Windows) or XCode (Mac).


#### 4. Build

Build whole source codes including plugin source codes.


#### 5. Launch UE4 editor and enable plugin

Launch .uproject file and enable plugin via *Settings* > *Plugins* > *Project* > *Other* > *kd-tree*.


## Features / Tutorials

### Build kdtree and radius search

1. `Build Kdtree` builds a kd-tree (`Kdtree` object in Blueprint) from `Vector` objects.
   * `Dump Kdtree to Console` outputs the internal information of `Kdtree` object to the console for debugging.
   * `Validate Kdtree` checks the `Kdtree` object and halts the game play if there is a incorrect in it. 
2. `Collect from Kdtree` collects `Vector` objects in the sphere (center location is `Center`, radius is `Radius`). `Collect from Kdtree` also returns indicies of list that is input argument of `Build Kdtree`.
3. If you don't use `Kdtree` any more, you can destroy `Kdtree` object and free memories by `Clear Kdtree`.

![](docs/images/kdtree.png)


### Build kdtree and radius search (Async version)

Async version is also provided by this plugin.

1. `Build Kdtree Async` is an asynchronous version of `Build Kdtree`.
   * All synchronous versions (`Collect from Kdtree`, `Dump Kdtree to Console`, `Validate Kdtree` and `Clear Kdtree`) can be applicatable to `Kdtree` object after `Build Kdtree Async` is completed.
2. `Collect from Kdtree Async` is an asynchronous version of `Collect from Kdtree`.

![](docs/images/kdtree_async.png)
