# uniCorne Build Guide

## Materials Needed: 
- Common parts

  | **Component**        | **Quantity** | **Description**                                      |
  |---                   |---:          | ---                                                  |
  | PCB                  | 2            | Left and right side                                  |
  | Switches             | 36           | Mechanical switches (e.g., Cherry MX, Kailh Choc)    |
  | Keycaps              | 36           | Keycaps compatible with your switches                |
  | Hotswap Sockets      | 36           | Hotswap sockets compatible with your switches        |
  | 1N4148W SOD-123      | 36           | Diodes for each switch                               |
  | Tactile Push Button  | 1            | SMD 2x4x3.5mm                                        |
  | Top Plate            | 1            | Case compatible with uniCorne-3x5 PCB                |
  | Bottom Plate         | 1            | Plate compatible with uniCorne-3x5 PCB               |
  | M2x4 Screw           | 20           | Screws for assembling the case                       |
  | M2x6 Standoff        | 10           | Spacers for assembling the case                      |

- Wired or Wireless
  - Wired keyboard

    | **Component**        | **Quantity** | **Description**                                      |
    |---                   |---:          | ---                                                  |
    | MCU                  | 2            | Promicro-ish e.g. Promicro, Elite-Pi, etc.           |
    | TRRS Sockets         | 2            | For connecting the two halves of keyboard            |
    | TRRS Cable           | 1            | Cable to connect the two halves of keyboard          |

  - Wireless keyboard

    | **Component**        | **Quantity** | **Description**                                      |
    |---                   |---:          | ---                                                  |
    | MCU                  | 2            | Promicro-ish NRF52480 board e.g. [nice!nano](https://nicekeyboards.com/nice-nano)           |
    | MSK-12C02 SMD        | 2            | Power switch for wireless                            |
    | Pico-EZmate 78171 2P | 2            | 2P socket for battery                                |

- Optional parts<br>

  | **Component**        | **Quantity** | **Description**                                        |
  |---                   |---:          | ---                                                    |
  | OLED Screen          | 1            | For displaying information, 128x32                     |
  | Tenting Kit          | 1            | For ergonomic typing angle                             |

  - Wired keyboard

    | **Component**        | **Quantity** | **Description**                                      |
    |---                   |---:          | ---                                                  |
    | SK6812 mini-e        | 30           | For per-key LED                                      |
    | SK6812 mini 3535     | 6            | For backlight LED                                    |
    | 10k SMD2012(metric)  | 2            | For handedness for wired keyboard                    |
    | 4.7k SMD2012(metric) | 2            | For I2C communication for wired keyboard             |

## Step-by-Step Guide:
1. Before starting:<br>
   uniCorne is designed to be soldered only on the bottom side.
1. Align PCBs:<br>
   ![PCBs](imgs/build/3x5-PCBs.jpg)<br>
   Theres is a marking on top side indicating the correct side.<br>
   ![Markings indicating side](imgs/build/markings-indicating-side.jpg)
1. Hotswaps:<br>
   Place the hot-swappable sockets on the PCB, and make sure it align with the holes on the PCB. Then, solder it.<br>
   ![Hotswap soldered](imgs/build/3x5-right-bottom-hotswap-soldered.jpg)
1. Diodes:<br>
   Diodes have markings to indicate the direction.  Make sure they are aligned with slikscreen.<br>
   ![diode marking](imgs/build/diode.jpg)
1. MCU
   1. Solder jumpers for MCU on the bottom side.<br>
      ![MCU jumbers](imgs/build/MCU-jumpers.jpg)
   1. Solder pin sockets which allows you to replace MCUs later.<br>
      ![MCU pin sockets](imgs/build/3x5-MCU-pin-socket.jpg)
   1. Place the MUC on pin sockets and insert pin headers.<br>
      ![MCU pin header](imgs/build/3x5-MCU-pin.jpg)
   1. Cut the pin header for one side once everything is aligned.<br>
      ![MCU pin header](imgs/build/3x5-MCU-pin-cut-out.jpg)
   1. Solder one side and repeat for the other side. The result should look like this when done.<br>
      ![MCU soldered](imgs/build/3x5-MCU-solder.jpg)
1. TRRS Socket:<br>
   Solder TRRS socket.<br>
   ![diode marking](imgs/build/TRRS.jpg)
1. Test the PCB:<br>
   Before fully assembling, test the PCB to ensure all switches work correctly after installing the relavant [firmware](https://github.com/Thunderbird2086/tb2086-qmk/releases). You can use a keyboard tester software for this e.g. QMK Toolbox.
1. Optional parts:
   - LEDs:<br>
     Solder LEDs.  There are two types: one for per-key lighting and the other for backlighting.<br>
     ![LEDs](imgs/build/3x5-right-bottom-soldered.jpg)
   - OLED Screen:<br>
     If you have an OLED screen, solder jumpers for OLED as well as 5-pin socket on the bottom side.<br>
     ![OLED](imgs/build/OLED.jpg)
   - Hardware Handedness:<br>
     If you want to use hardware handedness, solder the handedness resitor on the bottom side.<br>
     ![Hardware Handedness](imgs/build/Handedness.jpg)
1. Assemble:<br>
   Place top plate, the PCB, and the bottom plate. Then, secure them with screws.
1. Add Keycaps:<br>
   Place your keycaps onto the switches. Ensure they are firmly seated.
1. Install Tenting Kit (optional):<br>
   If you have a tenting kit, attach it to the bottom of the case for an ergonomic typing angle.
1. Final Check:<br>
   Double-check all connections and ensure everything is securely in place.<br>
   Test the keyboard again to ensure all keys are functioning properly.
1. Enjoy Your New Keyboard:<br>
   Customize your keymap and enjoy typing on your new uniCorne-3x5 keyboard!
