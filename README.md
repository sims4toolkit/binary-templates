# Binary Templates

"Binary templates" are the documentation that EA provides for binary resources such as SimData and object definitions. You can find a list containing most of them [here](https://forums.thesims.com/en_US/discussion/858947/maxis-info-index#latest).

We do not have binary templates for all of the game's resources, and some of the ones that we do have have some errors in them. So, this repo contains binary templates that are either entirely modder-made (in the `custom` folder), or ones that were originally by EA, but were fixed by a modder (in the `fixed` folder).

In order to use binary templates, you must download [010 Editor](https://www.sweetscape.com/010editor/). It is paid software ($50 USD), but there is a generous free trial period (based on usage rather than time) that does not require a credit card.

## Index of Binary Templates

### Custom

**Object Definition (0xC0DB5AE7)**: Based on S4PE's implementation of object definition files. Their source code can be found [here](https://github.com/s4ptacle/Sims4Tools/blob/fff19365a12711879bad26481a393a6fbc62c465/s4pi%20Wrappers/CatalogResource/ObjectDefinitionResource.cs).

### Fixed

**Combined Tuning (0x62E94D38)**: There was a bug in EA's SimData/Combined Tuning binary template that prevented combined tuning from being parsed correctly. This bug is on line 374 (of the file in this repository). That line does not need to be there, and simply commenting it out makes the template work for both SimData and Combined Tuning. This is the [implementation that Sims 4 Toolkit is currently using](https://github.com/sims4toolkit/models/blob/main/src/lib/resources/abstracts/data-resource.ts), and there have been no issues so far.
