# Laser Juice
ILDA laser abstract generator built with TouchDesigner. https://laserjuice.xyz/

![screen shot](https://github.com/tgreiser/laser-juice/blob/master/laser-juice-screen.png?raw=true)

## About

Laser Juice is donationware project of Prim8 Technology Consulting, LLC. If you need assistance, making a donation is a good way to request some of our time.

- Paypal - tim [ at ] prim8.net
- ETH - 0x48Ae5C3E0e561E099b9A332B0C4e51390837E4be
- BCH - qpz8p7lh8etrhwa7enymk5px87rwkctkwqt44ja56v

## System Requirements

- TouchDesigner 099 - build 18580+ - https://derivative.ca/download
- For laser output: Ether Dream (v1 or 2) or Helios DAC.
- GPU: 1gb GPU memory and Nvidia GeForce 600 series, AMD HD 7000 series, Intel HD4000 or better.

## Safety Reminder

Pressing the space bar will effectively stop any laser signal from Laser Juice. It is expected the owner and operator of the laser has taken the proper safety precautions necessary when operating any laser. For basic laser safety information, visit the ILDA website at http://www.ilda.com/safety-basics.htm. The creators of Laser Juice are not liable for personal injuries or damage to equipment when using this program.

## Ether Dream DAC

For full function of the Ether Dream, you need to connect to it via Cat 5/6 ethernet cable. You should open on any firewall inbound UDP port 7654. In addition, Mac OS may require manual IP configuration in order to connect. Refer to the Ether Dream diagnostic tool - https://ether-dream.com/downloads-ed2.html

You should also attempt to set the queue time as low as possible without getting any flicker. Having excessive queue time can introduce latency into the system.

## Calibration

In settings, ‘scale freq’ will scale your maximum frequency downwards. If your scanners are making a lot of noise, or your laser image is distorted from the preview, reduce the ‘scale freq’ value until undesired behavior stops. BasicLissajous is a good preset for testing frequency calibration. If one end of the laser pattern sticks out in an asymmetrical manner, then your scanners are distorting and you may wish to reduce the frequency.

This is also a good time to look at the blanking value. If there is a "laser tail" connecting the start of the line and the end of the line, you probably need to slighly increase your blanking. 5-10% is probably enough on most scanners to eliminate the tails.

## Help, My Laser Cuts Out Randomly!

This is most likely because either the sample rate and Ether Dream queue time are not balanced, or the computer CPU is too slow. See “Calibration” to check the former. If you experience flickers or dropouts when clicking on dropdown menus, it is likely the computer CPU that is too slow. Here are some ways to decrease the load on the CPU:

-	Close the System Settings window
-	Disable Audio Out if not in use (“Activate Laser”)
-	Disable Audio In if not in use (“React Active”)
-	Disable Ether Dream if not in use (“Activate Laser”)
-	Disable “Display Graphs”
-	Lower Sample Rate
