# ideas

## Flexible ROM Indexer Thingie

Problem: 
Emulators and front-ends like RetroArch or MAME are updated often and can require manual reconfiguration for updated versions, synchronisation of databases for thumbnails etc. 

It'd be nice to have a tool that rapidly indexed the NTFS MFT for known ROMs and auto-configured / created configurations for MAME / RetroArch based upon their latest available romset metadata.

The tool could be maybe written in PowerShell where the databases for each emulator are imported, as well as the MFT dump for any path containing ROMs and a cross-reference is checked to create a ready made config file for the emulator.

An optional extra would be to enforce checksumming of ROMs, making rapid assumptions of ROM content based on their proximity to other well known ROMs, as well as generating custom configurations for putting on external drives or devices like Raspberry Pis. Stuff like Thumbnails, metadata etc should be sorted at the same time.

Going further, it could be an idea to have it fill in gaps in sets by downloading missing files from archive.org or IPFS, however this may be problematic from a legal standpoint. 

## Demoscene downloader tool

Problem:
There is no way to rapidly download / organise demoscene productions.

It'd be nice to have a tool to sort of package manage demoscene productions so they can be run easily from a local machine.

Something like:
demo-get --platform windows --all

Supplemental metadata could be added to the package definition to hint if the production has compatibility issues (nvidia-only, ati-only, requires-dotnet46, requires-windows10, virus-prompt) etc.

The metadata could be populated from demozoo and tags can be pushed back to demozoo to smooth things out.
