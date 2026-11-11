<h1 align="center">Hi, I'm José Pablo Beristain 👋</h1>

<p align="center">
  <b>Embedded Software Engineer</b> · C/C++ · FreeRTOS · ESP-IDF · Rust (learning)
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/josé-pablo-beristain-silva-7a7b02145">
    <img src="https://img.shields.io/badge/LinkedIn-José%20Pablo%20Beristain-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:jberistainsil@hotmail.com">
    <img src="https://img.shields.io/badge/Email-jberistainsil@hotmail.com-D14836?style=flat&logo=gmail&logoColor=white" alt="Email"/>
  </a>
  <img src="https://img.shields.io/badge/Location-Mexico%20City-555?style=flat&logo=googlemaps&logoColor=white" alt="Location"/>
</p>

---

## About me

Mechatronics Engineer focused on **embedded software**: writing firmware from the register up, integrating sensors over I²C/SPI/UART, and building fault-tolerant RTOS applications.

I enjoy the part of embedded work that sits between the datasheet and the oscilloscope: reading a register map, implementing a vendor compensation algorithm by hand, and then debugging why the sensor returns the same 8 bytes every time. I care about **layered designs**, **clear documentation**, and **code that can be reused** in the next project.

- 🔭 Currently building an **ESP32 environmental monitoring platform** (ESP-IDF + FreeRTOS + from-scratch BME280 driver).
- 🌱 Learning **Rust for embedded systems** — no production code yet, just exercises and reading.
- 🧭 Interested in automotive, energy, and telecommunications.
- 📫 Reach me at **jberistainsil@hotmail.com** or on [LinkedIn](https://www.linkedin.com/in/josé-pablo-beristain-silva-7a7b02145).

---

## Featured project

### [ESP32 Environmental Monitoring Platform](https://github.com/JosePabloBS)
Bare-metal firmware for the ESP32 that reads a **BME280** over I²C and publishes temperature, pressure, and humidity over UART. No third-party sensor libraries — the driver is written from scratch against the Bosch datasheet.

**Highlights**
- **Register-level BME280 driver** (I²C, `i2c_master_transmit_receive`).
- **Bosch compensation algorithms** in 64-bit integer arithmetic, including sign-extension for 12-bit humidity coefficients.
- **FreeRTOS producer/consumer** design with a queue: non-blocking sensor task, blocking display task, `vTaskDelayUntil` for a stable 1 s sampling period.
- **Fault detection and recovery**: consecutive I²C failure tracking, "stuck sensor" detection via `memcmp` on raw bytes, and automatic soft-reset / re-initialization.

`C` · `ESP-IDF` · `FreeRTOS` · `I²C` · `UART` · `BME280`

> Roadmap: MPU6050 driver, microSD logging (SPI + FatFS), SSD1306 OLED display, sea-level pressure, unit tests for the compensation functions.

---

## Tech I work with

<p>
  <img src="https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white" alt="C"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white" alt="C++"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Rust-000000?style=flat&logo=rust&logoColor=white" alt="Rust (learning)"/>
  <img src="https://img.shields.io/badge/ESP--IDF-E7352C?style=flat&logo=espressif&logoColor=white" alt="ESP-IDF"/>
  <img src="https://img.shields.io/badge/FreeRTOS-4B8BBE?style=flat&logo=freertos&logoColor=white" alt="FreeRTOS"/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black" alt="Linux"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white" alt="Git"/>
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white" alt="GitHub Actions"/>
  <img src="https://img.shields.io/badge/KiCad-314CB0?style=flat&logo=kicad&logoColor=white" alt="KiCad"/>
</p>

**Embedded:** ESP32, Raspberry Pi, GPIO, UART, SPI, I²C, CAN (basic), PWM, ADC, interrupts, register-level drivers, sensor compensation, fault detection.
**Practices:** datasheet-driven development, root cause analysis, technical documentation, code review.

---

## Beyond firmware

Before focusing fully on embedded software, I worked as an **Automation Engineering Trainee at Honeywell** (HMI for industrial DCS, commissioning and validation) and as a **Process Engineer at Kimberly-Clark** (root cause investigations, cross-functional coordination, SOPs). That background shapes how I approach embedded work: **documented, testable, and built to be maintained by someone else.**

---

<p align="center">
  <i>Open to embedded software opportunities — feel free to reach out.</i>
</p>
