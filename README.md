# Inside Loxone Miniserver, Extensions and Devices

I talk about three different device types in this document:

  - Miniserver: the server hardware. At least one is required for a home.
  - Extensions: connected to the Miniserver via the Loxone Link bus.
  - Devices: connected to one of the two Tree Busses behind a Tree Extension or via IPv6 868MHz to an Air Base Extension.

I've split up the documentation into separate parts to make it easier to read, also because Legacy and NAT protocols are completely independent, you only need to care about the one that matters for you.

- Hardware
    - [Loxone Miniserver Hardware](LoxoneMiniserverHardware.md)
    - [Loxone Miniserver Go Hardware](LoxoneMiniserverGoHardware.md)
    - [Loxone Extensions and devices debug connectors](LoxoneDebugConnectors.md)
- Loxone Link Protocol
    - [Loxone Link Hardware](LoxoneLinkHardware.md)
    - [Loxone Link Protocol Introduction](LoxoneLinkProtocolIntro.md)
    - [Loxone Link Legacy Protocol](./Legacy/LoxoneLinkLegacyProtocol.md)
        - [Loxone Extension](./Legacy/LoxoneLinkLegacyExtension.md)
        - [Loxone Relay Extension](./Legacy/LoxoneLinkLegacyExtensionRelay.md)
        - [Loxone RS232 Extension](./Legacy/LoxoneLinkLegacyExtensionRS232.md)
        - [Loxone RS485 Extension](./Legacy/LoxoneLinkLegacyExtensionRS485.md)
        - [Loxone DMX Extension](./Legacy/LoxoneLinkLegacyExtensionDMX.md)
        - [Loxone 1-Wire Extension](./Legacy/LoxoneLinkLegacyExtension1Wire.md)
        - [Loxone Modbus Extension](./Legacy/LoxoneLinkLegacyExtensionModbus.md)
    - [Loxone Link NAT Protocol](./NAT/LoxoneLinkNATProtocol.md)
        - [Loxone DI Extension](./NAT/LoxoneLinkNATExtensionDI.md)
        - [Loxone AI Extension](./NAT/LoxoneLinkNATExtensionAI.md)
        - [Loxone AO Extension](./NAT/LoxoneLinkNATExtensionAO.md)
        - [Loxone Tree Extension](./NAT/LoxoneLinkNATTreeExtension.md)
        - [Loxone Link Tree Extensions and Devices](./NAT/LoxoneLinkNATTreeDevices.md)
