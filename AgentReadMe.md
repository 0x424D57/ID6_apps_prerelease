# AgentReadMe

## Select the apps

Ask the owner for their choice of **MHD+ Suite** or **Bootmod3 Suite**, and whether they want **xDrive Control**. Install only the selected tuning menu. Install xDrive Control only when selected. BoostDeck, ShiftDeck, and Engine Fault Codes are independent apps.

## Identify the car

1. Confirm the installation is authorized and the car is parked, with iDrive awake. Connect wired ENET and identify the computer's ENET address, diagnostic gateway address, and head-unit SSH address.
2. Use an unlock tool that supports the exact unit, such as [Bavarian SSH Client](https://ssh.bavarian-aa.uk/). Verify the SSH host key and use locally supplied credentials.
3. Read the exact NBTevo software code, the active panel resolution (LayerManager screen 0), and SHA-256 hashes of both files under /opt/hmi/ID5/lib. Use the [read-only capture utility](source/tools/capture_headunit.py) when you need a structured report.

The packaged build is for **NBTevo_N18032I**, **1280 × 480**, with this framework pair.

| File | SHA-256 |
| --- | --- |
| libAppFramework.A.so | 93f4c7ab7e59c0adf7923b9b491de06165ba9d97bbe7412292e7ddc418ca2123 |
| libCoreFramework.A.so | 64ba154c68c772f9ca779fc18507f5b34715be58ded4a198b8a62b90d16c3ee0 |

Check the gateway used by the payload, 169.254.21.3. If the firmware, frameworks, resolution, or gateway differ, use the [porting workflow](source/docs/PORTING.md) and build for the actual target. Native changes need the QNX SDP 6.5 Linux host tools and ARM GCC 4.4.2. Matching packaged binaries and compatible layout resource changes do not need QNX on the ENET computer.

## Stage and verify

Download and extract the selected packages from [packages/](packages/). The dashboard ZIP contains BoostDeck, ShiftDeck, EngineCodes, and MhdMaps. Include MhdMaps only for the MHD choice. Bootmod3Suite and XDriveControl are separate ZIPs. Read their package notes for module and tune constraints. Install neither when the owner declines them.

Inventory /var/opt/hmi/data/ID5/Plugins for conflicting names and connector IDs. Back up any prior version being replaced to a separate directory outside Plugins. Stage complete app folders outside Plugins, upload over confirmed SSH, set the workers executable, and compare each readback with its local file before moving the folders into Plugins. Verify the final paths and bytes, and tell the owner where backups were saved. If anything fails, restore the previous folders before restarting. Do not add a second copy of an app.

After verification, have the owner hold the volume knob until iDrive goes dark, then check the selected menus while parked. Check live readings and settings. Menu installation alone does not verify an engine or drivetrain command. Get the owner's authorization before testing a command that changes ECU or drivetrain state.
