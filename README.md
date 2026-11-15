# NBT Evo ID6 apps

Connect your parked car to a computer over wired ENET. Open an AI agent with terminal access on that computer and give it this repository and [AgentReadMe.md](AgentReadMe.md). The agent identifies your head unit, checks compatibility, and installs your chosen apps under **My Vehicle**.

If your head unit needs temporary SSH access, use [Bavarian SSH Client](https://ssh.bavarian-aa.uk/) when your agent asks. Check that the client supports your exact head unit and firmware.

## Tell your agent what to install

Choose **MHD+ Suite** or **Bootmod3 Suite**. Also say **yes or no to the xDelete-style xDrive menu**. Bootmod3 and xDrive Control are beta packages. xDrive Control is still being tested, with no guarantee of compatibility or operation.

> My car is parked, iDrive is awake, and this computer is connected over wired ENET. Follow the AgentReadMe to install BoostDeck, ShiftDeck, and Engine Fault Codes. My tuning menu choice is **[MHD+ Suite / Bootmod3 Suite]**. My xDrive Control choice is **[yes / no]**. Verify firmware, framework hashes, and display resolution before uploading. Ask me when temporary SSH or a parked restart is needed.

[Quick Start](Quick%20Start.md) · [Change notes](CHANGELOG.md) · [Native source](source/)

## Features

- **BoostDeck** has faster gauge updates and a new bar layout. It displays boost, AFR, ignition timing, intake air temperature, transmission temperature, rail pressure, oil pressure, coolant temperature, and Active Ethanol. Press **OPTIONS** for gauge colors, including Multicolor, and to switch between PSI and Fahrenheit or bar and Celsius.
- **ShiftDeck** displays live speed, an RPM bar, and shift lights with a selectable RPM threshold. Press **OPTIONS** to switch between mph and km/h. This update includes performance improvements.
- **MHD+ Suite** offers four map slots, exhaust flap control, and Max Cooling on compatible MHD+ tunes.
- **Bootmod3 Suite** is a new beta control menu for compatible CustomROM tunes. It offers four map slots, exhaust flap control, Active Sound, and burble presets.
- **xDrive Control** is an xDelete-style beta menu for temporarily selecting rear-wheel drive on supported DSC versions. It is still being tested, with no guarantee of compatibility or operation.
- **Engine Fault Codes** reads engine/DME fault codes and shows descriptions when available. It can read codes even when the DME refuses to clear them.

## Photo Showcase (Old UI)

<table>
  <tr>
    <td><img src="images/01_boostdeck_daylight.jpg" alt="BoostDeck in daylight" width="300"></td>
    <td><img src="images/02_boostdeck_closeup.jpg" alt="BoostDeck close-up" width="300"></td>
  </tr>
  <tr>
    <td><img src="images/05_shiftdeck.jpg" alt="ShiftDeck" width="300"></td>
    <td><img src="images/06_boostdeck_night.jpg" alt="BoostDeck at night" width="300"></td>
  </tr>
  <tr>
    <td><img src="images/07_boostdeck_ambient.jpg" alt="BoostDeck with ambient lighting" width="300"></td>
    <td><img src="images/08_mhd_maps.jpg" alt="MHD Maps" width="300"></td>
  </tr>
</table>

Earlier HUD prototype photos

<table>
  <tr>
    <td><img src="images/03_hud_white.jpg" alt="HUD prototype in white" width="300"></td>
    <td><img src="images/04_hud_orange.jpg" alt="HUD prototype in orange" width="300"></td>
  </tr>
</table>
