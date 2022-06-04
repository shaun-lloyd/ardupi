# TODO: v0.1 Release
ArduPi-0.1 == OBAL

Initial porting of OBAL component modules to IC's on board is progressing.
Main schematic is almost complete.

## Current Work

### Schematic
- PASS kicad/erc "electrical rules checker"
	1. All the symbol's need to have the "pin table" correctly defined.
		- unfortunately all the symbols and footprints i have don't have valid pin table.
- Power Management
	1. Design/Confirm "archecture".
	2. Add components/schematic
- QA: Some external audit.

### Component selection
- Power input: XT60 ?
- Headers for all I/O. JST_GH ?

## NEXT
- schematic
- component selection
- pcb layout
- QA
- publish release
