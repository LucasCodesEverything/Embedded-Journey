# Embedded Systems — Learning Log

A public build log documenting my self-taught path into embedded engineering, from bare-metal C on STM32 through to an RTOS-based capstone. Each phase ends with a concrete artifact (driver, write-up, or logic-analyser capture) rather than a tutorial checkbox.

**Background:** Software Engineering graduate (Cardiff Met), placement at Atlas Elektronik UK (defence electronics). This log exists to demonstrate hands-on competence, not just completed courses.

**Hardware:** STM32 Nucleo-64 (F446RE) · 8-channel logic analyser · breadboard prototyping.

**Guiding rule:** one concept → build the thing → write up what broke. No tutorial purgatory.

---

## Phase 0 — Prerequisites *(in parallel, not as a gate)*

- [ ] C pointer/bitwise fluency — *The C Programming Language* (K&R)
- [ ] Read "From Zero to main(): Bare metal C" (Interrupt blog)
- [ ] Multimeter basics — SparkFun tutorial
- [ ] Logic analyser basics — "Instrument Basics: Logic Analyzer"

*Skipping calculus/discrete-maths sections — not relevant to getting hired.*

---

## Phase 1 — Bare-metal STM32 (register level)

The differentiator. No HAL — write directly to registers to prove I understand memory-mapped I/O.

**Core resources**
- [ ] Modern Embedded Systems Programming (Miro Samek, YouTube) — the single best free resource
- [ ] "Bare Metal Embedded Programming Using STM32" (YouTube playlist)
- [ ] "#1 Intro to STM32F4 Register Based Programming — Clock Setup, LED Blink, NO HAL"
- [ ] GPIO → Timers → Interrupts (in that order)

**Artifacts**
- [ ] Register-level GPIO write-up
- [ ] Timer/interrupt blink + logic-analyser capture proving timing

---

## Phase 2 — Peripherals & protocols

The strongest section of the field. Datasheet-reading is the real skill being built here.

**Core resources**
- [ ] UART → I2C → SPI (in that order); "I2C in a Nutshell" (Interrupt blog)
- [ ] ADC/DAC, PWM, then DMA ("Polling/Interrupt/DMA differences explained easily")
- [ ] "How to Read a Microcontroller Datasheet" series (AllAboutCircuits)

**Artifact**
- [ ] Bare-metal driver for one I2C sensor (no HAL) + captured bus traces

---

## Phase 3 — RTOS & systems thinking

**Core resources**
- [ ] FreeRTOS on STM32 — *Beginning STM32* (Warren Gay)
- [ ] State Machines + Event-Driven Programming playlists (Miro Samek)
- [ ] Skim: Watchdog, Power Management, Bootloader/DFU
- [ ] "Device Firmware Update Cookbook" (Interrupt) — if attempting a bootloader

**Artifact**
- [ ] FreeRTOS project juggling multiple tasks with a shared resource (mutex/queue)

---

## Phase 4 — Capstone

**CAN-based multi-node project** — highest-signal choice, directly echoes the Atlas/defence background. Almost no self-taught portfolio has CAN.

**Core resources**
- [ ] Microchip University — CAN and CAN-FD Protocol & Physical Layer Basics
- [ ] "CAN Bus: A Beginners Guide" Parts 1 & 2

**Artifact**
- [ ] Multi-node CAN project with a real-time requirement and a constraint (deadline or low-power)

---

## Ongoing references
- **Interrupt blog (Memfault)** — professional-grade firmware writing
- **ControllersTech / DeepBlueMbedded** — practical STM32 how-tos when stuck

---

## Log index
*(Newest first — link each write-up as it's published.)*

| Date | Phase | Entry | Artifact |
|------|-------|-------|----------|
| — | — | *First entry pending* | — |
