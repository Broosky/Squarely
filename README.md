# 💡 Squarely

A super low-frequency square wave counter originally built back in high school, designed for basic signal counting and hands-on hardware experimentation. It uses classic 74-series logic to drive a multi-digit display and can be expanded or tuned for various applications.

Reflecting on the original design, here are a few areas worth improving:

- Replace discrete resistors with a resistor bank for cleaner layout and easier substitutions.
- Adjust the 555 timer's RC values to support higher input frequencies (up to low MHz).
- Add a third digit to extend the count range.
- Use logic chips from the same family (e.g., 74HCXX) for consistent behavior and performance.
- Pull unused inputs high or low to prevent erratic logic states.
- Support an external clock input via pin 14 (CP0) of the first 74XX90 counter for easier integration or testing.

> If you found this project useful, interesting, or worth keeping an eye on, consider giving it a ⭐️.
> It helps others discover the project and motivates me to keep building and sharing more.

## 🔹 Construction

![Squarely 1](<Construction/Squarely 1.jpg>)

## 🔹 Rev 1 Schematic

![Rev 1](<Schematics/Rev 1.png>)

## 🔹 Rev 1

- Initial release.

## 🔹 General Notes

- VDC: 7 - 12 V.
- Input Signal Options:
  - Internal 555 timer (adjustable via RC timing).
  - External square wave source (connect to pin 14 / CP0 of the first 74XX90).

- Display:
  - 2-digit 7-segment display (expandable).
  - Driven by chained 74XX90 decade counters and 74XX47 BCD-to-7-segment drivers.
  - A D flip-flop latches the output from the counters to the display drivers.

- Modularity:
  - RC timing is easily adjustable for frequency testing.
  - Logic chips can be swapped to experiment with propagation delays, power consumption, or chip families.

  ##

> Educational Use Notice: This project is provided for educational and learning purposes only. You are welcome to read, study, and experiment
> with this software and/or hardware. It is not intended for commercial use. This software and/or hardware is provided "as is", without warranty
> of any kind. The author assumes no responsibility for any damages or issues resulting from its use.