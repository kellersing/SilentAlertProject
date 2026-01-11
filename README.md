# 🔔 ESP32 Deaf-Friendly Doorbell Strobe System

A **wireless visual doorbell system** built with **ESP32-C3 + ESP-NOW**, designed to help **Deaf / Hard-of-Hearing families** know when someone is at the door using **bright RGB strobe lights** instead of sound.

This project focuses on:

* ⚡ **Instant response**
* 🔌 **Offline operation (no Wi-Fi, no internet)**
* 💡 **Highly visible LED alerts**
* 🧠 **Simple, reliable design**

---

## ❤️ Why This Project Exists

I am **Deaf / Hard of Hearing**, and so is my family.

Many doorbells rely only on sound. That means:

* Missed visitors
* Missed deliveries
* Missed important moments

I noticed how often Deaf people struggle with this problem in everyday life.
This project is my solution:
A **wireless doorbell button** that triggers a **bright RGB strobe alarm** inside the house.

No apps.
No cloud.
No Wi-Fi.
Just works.

---

## 🧩 System Overview

### 🟦 Sender (Doorbell Button)

* ESP32-C3
* Push button
* ESP-NOW wireless transmission
* Sends a single command (`'1'`) when pressed

### 🟩 Receiver (Strobe Alarm)

* ESP32-C3
* WS2812 / WS2818 RGB LED strip
* Push button for **color selection**
* ESP-NOW receiver
* Bright flashing strobe patterns

---

## ✨ Features

### Receiver

* 🔴🟢🔵 **7 selectable colors**

  * Red
  * Blue
  * Yellow
  * Green
  * White
  * Purple
  * Violet
* 🎛 **Button on GPIO0** to cycle colors
* ⚡ **Multiple strobe modes**

  * Normal strobe (`'1'`) – 10 seconds
  * Turbo strobe (`'2'`) – fast flash
  * Police strobe (`'3'`) – red / blue alternating
  * Off (`'0'`)
* 💾 Designed to support future color memory
* 🔌 USB-powered (no external power required)

### Sender

* 🧷 One-button operation
* 📡 ESP-NOW (very fast, low power)
* 💡 Optional LED blink confirmation
* 🔋 Can be expanded for battery + deep sleep

---

## 🛠 Hardware Used

### Required

* ESP32-C3 (Sender)
* ESP32-C3 (Receiver)
* WS2812 / WS2818 RGB LED strip (5–30 LEDs)
* Push buttons (2-pin)
* USB-C cables

### Optional / Recommended

* 330Ω resistor (data line)
* 1000µF capacitor (LED power stability)
* 3D printed enclosure (future)

---

## 📡 Why ESP-NOW?

ESP-NOW was chosen because it is:

* 🚀 Extremely fast (near instant)
* 🔒 Local only (no internet)
* 🔋 Low power
* 📶 Works even if Wi-Fi is down

Perfect for accessibility devices.

---

## 📂 Code Structure

```
/sender
  └── Sender-V1.1.ino

/receiver
  └── Receiver-V1.4.ino
```

Each file is independent and easy to upload using **Arduino IDE**.

---

## 🚀 How It Works

1. Someone presses the doorbell button
2. Sender sends `'1'` using ESP-NOW
3. Receiver gets the command
4. RGB LEDs flash brightly for 10 seconds
5. Deaf family members see the alert immediately

---

## 🧪 Current Status

✅ Sender working  
✅ Receiver working  
✅ ESP-NOW communication stable  
✅ Button color selection working  
✅ Strobe patterns working

---

## 🔮 Planned Features

* ⏱ Long-press pairing mode (add new senders)
* 💾 Save selected color in flash memory
* 👆 Long-press / double-press button actions
* 🔋 Battery-powered sender (deep sleep)
* 📦 Enclosure design
* 🧩 Multi-receiver support

---

## 🤝 Contributions

This project is open for:

* Accessibility improvements
* Power optimizations
* Hardware design ideas
* Code cleanup
* Documentation improvements

If you care about **accessibility technology**, your help is welcome.

---

## 📜 License

This project is released under the **MIT License**.  
Use it, modify it, improve it — especially if it helps others.

---

## 🙏 Final Note

This is more than a hobby project.

It’s about **independence**, **accessibility**, and **not missing important moments**.

If this helps even one Deaf family — it’s worth it.
