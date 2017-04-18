# Raspberry Pi Model Zero

## About rpi0_gadget_ethernet

This is a custom Nerves System Raspberry Pi Zero and Raspberry Pi Zero W. It differs
slightly from the Base Nerves Pi Zero System.

For the official Pi Zero and Pi Zero W Nerves System, see 
https://github.com/nerves-project/nerves_system_rpi0.

## Custom System Details:

In addition to gadget serial (provided in the base system), it adds gadget ethernet,
dnsmasq, and it remaps the uart so that the header pins gets the full uart and
the Bluetooth chip gets the mini-uart.

The purpose of this system is to push the envelope on what the OTG port can do and
provide a system that allows the hardware to serve as a DHCP server over the usb
networking device. For an example of a Nerves firmware that utilizes this, see 
https://github.com/tmecklem/nerves_pi_sandbox.

## Installation

Add `rpi0_gadget_ethernet` to your list of dependencies in mix.exs:

```
  def deps do
    [{:rpi0_gadget_ethernet, "~> 0.12.0", github: "tmecklem/rpi0_gadget_ethernet"}]
  end
```
