# Signal verification status

`signalsets/v3/default.json` mixes two kinds of signals.

## Verified on a real Enyaq

Measured on a 2021 Škoda Enyaq Sportline 80 on 2026-11-02 (DC charging). Each has a test case under `tests/test_cases/2021/commands/`.

- `ENYAQ_CAR_MODE` (7448), bit meaning still open (DC read as `06`)
- `ENYAQ_HVBAT_CHARGE_CURRENT_LIMIT` (1E1B)
- `ENYAQ_HVBAT_VOLTAGE` (1E3B)
- `ENYAQ_HVBAT_TEMP_MIN`, `ENYAQ_HVBAT_TEMP_MIN_ID` (1E0F)
- `ENYAQ_SOC_BMS` (028C), dashboard match not yet checked

## Imported, not yet verified on an Enyaq

Every other command (246 commands) was imported from the OBDb Volkswagen ID.4 signal set (CC-BY-SA-4.0, https://github.com/OBDb/Volkswagen-ID.4), with the `ID4_` id prefix renamed to `ENYAQ_`. The Enyaq shares the MEB platform, but these commands have not been run on an Enyaq. Some may return nothing or decode differently.

When a signal is captured on the car, add a test case under `tests/test_cases/<year>/commands/` and move it to the list above.
