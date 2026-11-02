# Škoda Enyaq

This repository contains signal set configurations for the Škoda Enyaq, organized by model year and version. The files are structured to allow for easy differentiation between model generations and other vehicle parameters, ensuring accurate signal mapping for each version of the Škoda Enyaq.

## Contributing

Contributions are welcome! If you would like to add support for additional model years or other configurations, please open an issue or submit a pull request.

1. Fork the repository
2. Create a new branch for your changes
3. Commit your changes and open a pull request with a detailed description

## Issues

If you encounter any issues or would like to discuss improvements, please feel free to open an issue. We encourage collaboration and appreciate feedback to make the repository as accurate and useful as possible.

## Provenance

The initial signal set (battery pack voltage, charge current limit, minimum pack temperature, BMS state of charge and car mode) was measured on a single 2021 Škoda Enyaq Sportline 80 during a DC charging session on 2026-11-02. Other MEB cars and model years are untested. Formulas were cross-checked against the OBDb Volkswagen ID.4 and Audi Q4 e-tron signal sets (CC-BY-SA-4.0).

Known open points: the bit meaning of `ENYAQ_CAR_MODE` (DC charging read as `06`) and whether `ENYAQ_SOC_BMS` equals the dashboard state of charge.
