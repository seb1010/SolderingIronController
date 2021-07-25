# Temperature Controller for Hakko 936 Clone

## Overview
 * PID type controller for regulating the temperature of a soldering iron
 * Control done with lm324 quad opamp
 * Heating element switched with back to back mosfets

## Implementation

### Switching
 * The Sources of the MOSFETs were connected together
 * This node was also the cicuit ground
   * This made it very easy to switch mosfets
 * The advantages of using MOSFETs
   * Easy to control
   * Low voltage drop results in high efficiency and no need for heat sinking
 * Used a SQ4946AEY Dual MOSFET

<img src="images/switchSCH.png" width="80%" />

### Power Supply for Control Circuitry
 * Shunt Zener Regulator
  * used a current source in place of usual resitor due to issues caused by 60 Hz ripple on supply rail
 * avoided electrolytic capacitors bc case can get quite warm

<img src="images/powerSupplySCH.png" width="80%" />
 
