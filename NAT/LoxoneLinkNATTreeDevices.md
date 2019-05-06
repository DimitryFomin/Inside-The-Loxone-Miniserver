# Tree Devices

## Motion Sensor Tree

| Type    | Index   | Name       | Dir | Description |
| ------  | ------- | ---------- | --- | ----------- |
| Digital | 0x00    | Motion     | S←E | Motion detected (==1, resets to 0 after about 3 seconds) |
| Analog  | 0x00    | Brightness | S←E | Brightness in Lx, sent when the value changes, which can happen about every ~1.5s |

Configuration Version 2:

| Offset   | Value | Description |
| -------- | ----- | ----------- |
|          |       |             |

02ff00840300000f000000010000000000



## LED Ceiling Light Tree

| Type    | Index   | Name        | Dir | Description |
| ------  | ------- | ----------- | --- | ----------- |
| Composite RGBW | 0x00 | Smart Actuator | S←E | Light settings |

Brightness & Motion input and configuration!

Configuration Version 2:

| Offset   | Value | Description |
| -------- | ----- | ----------- |
|          |       |             |

01656565650000000000000000

## Leaf Tree

| Type    | Index   | Name        | Dir | Description |
| ------  | ------- | ----------- | --- | ----------- |
| Digital | 0x00    | ?           | S→E | ? |
| Analog  | 0x00    | ?           | S→E | ? |
| Analog  | 0x01    | ?           | S→E | ? |

Configuration Version 1:

| Offset   | Value | Description |
| -------- | ----- | ----------- |
|   8…11   |  2200 | Filter change interval in hours |


## Alarm Siren Tree

| Type    | Index   | Name        | Dir | Description |
| ------  | ------- | ----------- | --- | ----------- |
| Digital | 0x00    | Tamper Contact | S←E |  |
| Digital | 0x00    | Alarm       | S←E | Bit 0:Strobe Light, Bit 1:Alarm Sound |

Configuration Version 1:

| Offset   | Value | Description |
| -------- | ----- | ----------- |
|   8      |    0  | Unknown |
|   9…10   |  120  | Maximum audible alarm duration in seconds (0=no limit, 1-1800s) |

Tamper Contact has a special case, because after reboot it triggers. This means the Alarm Siren needs to have some communication.


## Weather Station Tree

| Type    | Index   | Name        | Dir | Description |
| ------  | ------- | ----------- | --- | ----------- |
| Digital | ?       | ?           | S←E | |
| Digital | ?       | ?           | S←E | |
| Digital | ?       | ?           | S←E | |
| Analog  | ?       | ?           | S←E | |
| Analog  | ?       | ?           | S←E | |
| Analog  | ?       | ?           | S←E | |

Analog values: Brightness, Wind Speed, Temperature
Digital values: Rain, Storm Warning, Sunshine

Configuration Version 2:

| Offset   | Value | Description |
| -------- | ----- | ----------- |
|     8    |    5  | Unknown |
|     9    |    0  | Unknown |
|    10    |   28  | Unknown |
|    11    |    0  | Unknown |
|    12    |   20  | Unknown |
|    13    |   80  | Sunshine Threshold |
|    14    |   35  | Storm Warning Threshold (0…150km/h) |

## NFC Code Touch Tree

Uses an encrypted communication, this device should be on a dedicated Tree branch, otherwise the encryption would be kind of useless, because a hacker could inject the door open messages directly.

## Touch Surface Tree

Like a Touch Pure Tree, but with an additional input and options (Activiation required, use activation LEDs, a timeout [1-20s, 5s] and a calibration, controlled via WebRequests, like 'GetCalibration/60')

## Universal Tree

An unreleased Loxone Extension for the Tree bus with 4 analog inputs, 4 analog outputs, 8 digital inputs and 8 relays.

These are somehow not stored in the config, which is version 2 with 00000000000000000000000000000000

## Integrated Window Contact Tree

An unreleased door handle, which is currently only available as an Air device.
