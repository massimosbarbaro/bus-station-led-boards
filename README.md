# Corriere: LED departure boards for the bays of a coach station

*Tabelloni a LED delle partenze per le banchine di un'autostazione*

**APEL Easy Board Text (DOS)** · 2002 · version 2002  
Author: **Massimo Sbarbaro** ([ORCID 0009-0006-8965-9013](https://orcid.org/0009-0006-8965-9013))

## Overview

This project drove the LED matrix boards above the bays (*banchine*) of a coach station in north-eastern Italy, serving regional and international lines. Each bay had its own board, addressed on a serial line. The work consisted of writing the messages for every departure (destination, bay and time, for regional and international lines), the summer timetable variants, and the message plans that switch each board automatically to the next departure by date and time window. Everything was handled through text-based message files and batch scripts.

I designed and programmed this application in 2002. It is published here in 2026 as part of the documented record of my software work, with a permanent DOI on Zenodo.

## Main functions

- Message files (`.ezt`) for every departure, named `<bay><destination code><hhmm>`, e.g. `2Ud1800` = bay 2, Udine, 18:00.
- Destination folders with stored variants (airport, Udine, Grado, Gradisca, Koper, Sežana, Rijeka, Split and others) and a summer timetable for each bay (`Estivo/`).
- Message plans (`BANCH01A.EZP`, `BANCH02B.EZP`, `BANCH03C.EZP`) that list, for each bay, which message to show in each time window.
- Batch scripts (`SCBanc1-3.bat`, `ScaricoBanchine/Banc1-3.bat`) that launch the board software on COM2 at 2400 baud for each board address and 16×4 matrix.

## Data

Binary message files and message plans in the format of the APEL “Easy Board Text” system.

## Technology

APEL Series/700 Easy Board Text System v3 (third-party DOS software, not included), RS-232 serial line.

## Repository contents

| Path | Content |
|---|---|
| `boards/` | Message files (`.ezt`), message plans (`.EZP`) and launch scripts (`.bat`), in the original folder structure: one folder per destination, `Estivo/` for the summer timetable, `ScaricoBanchine/` for the download scripts. |

## What is not included

Only the files written for the bus station in 2002 are published: messages, message plans and launch scripts. The APEL Easy Board Text software (executables, menus and installation scripts, © APEL SpA) and older message files written by others are **not** included.

## How to cite

Use the citation metadata in [`CITATION.cff`](CITATION.cff) (GitHub: *Cite this repository*). Each release is archived on Zenodo with its own DOI.

> Sbarbaro, Massimo. *Corriere: LED departure boards for the bays of a coach station (APEL Easy Board Text (DOS), 2002)*. Software, version 2002. GitHub: https://github.com/massimosbarbaro/bus-station-led-boards

## License

Released under the [MIT License](LICENSE). © 2002 Massimo Sbarbaro.
