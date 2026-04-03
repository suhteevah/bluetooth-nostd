# bluetooth-nostd

`no_std` Bluetooth HCI/L2CAP/GATT/HID driver in Rust for bare-metal systems.

## Features

- **HCI**: Command/event packet building and parsing, BLE and Classic opcodes
- **L2CAP**: Connection-oriented channels, signaling, LE credit-based flow control
- **GATT**: Client with service/characteristic discovery, read/write, notifications
- **GAP**: Device discovery (inquiry + LE scan), connection management
- **HID**: Boot protocol keyboard/mouse report parsing, key event tracking
- **USB Transport**: Trait-based HCI-over-USB abstraction

## Architecture

```text
BluetoothController (driver.rs)    -- top-level API
    |
GAP (gap.rs)  |  GATT (gatt.rs)   -- discovery, services
    |
HID Profile (hid.rs)              -- keyboard/mouse
    |
L2CAP (l2cap.rs)                  -- channels, flow control
    |
HCI (hci.rs)                      -- commands, events, data
    |
USB Transport (usb_transport.rs)  -- bulk/interrupt endpoints
```

## License

Licensed under either of Apache License 2.0 or MIT License at your option.
