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

---

---

---

---

---

---

---

---

---

---

---

---

---

## Support This Project

If you find this project useful, consider buying me a coffee! Your support helps me keep building and sharing open-source tools.

[![Donate via PayPal](https://img.shields.io/badge/Donate-PayPal-blue.svg?logo=paypal)](https://www.paypal.me/baal_hosting)

**PayPal:** [baal_hosting@live.com](https://paypal.me/baal_hosting)

Every donation, no matter how small, is greatly appreciated and motivates continued development. Thank you!
