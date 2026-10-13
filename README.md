# Picker & Placer 3D Gantry Dashboard

A Vite + JavaScript + Three.js visualization for a four-pallet tyre placement concept.

## Cell plan
- 4 pallets, each with 4 rows × 5 tyre columns (20 positions each; 80 total)
- 28.0 second target cycle per tyre
- Theoretical rate at target: 128.6 tyres/hour; 80-position plan time: 37 minutes 20 seconds
- X/Y/Z gantry concept with a bridge, cross rail, vertical carriage, and gripper
- Demo cycle controls, pallet occupancy, camera presets, and cycle-log export

## Drawing dimensions shown in the dashboard
The supplied Festo GA PDF labels its drawing conceptual and for reference only. The dashboard surfaces the readable 2506 mm and 1541 mm callouts, the 791 mm and 750 mm vertical segments, and EGC-TB 2000 / EGC-BS 1000 axis module designations from its BOM. These are source drawing values, not a certified machine envelope.

The PDF does not dimension the four-pallet layout, pallet pitch, or full cell footprint. Those parts of the 3D scene are schematic planning assumptions and must be replaced with approved layout dimensions before mechanical design or fabrication.

This dashboard is a browser simulation. It is not connected to a PLC, safety circuit, servo drives, or a real machine. Its cycle timer illustrates the requested target and is not a validated production cycle-time study.

## Run locally
1. Open this folder in VS Code.
2. Run `npm install`.
3. Run `npm run dev`.
4. Open the local URL printed by Vite.

## Structure
- `src/main.js` — app bootstrap
- `src/modules/dashboard.js` — dashboard UI markup
- `src/modules/gantryScene.js` — Three.js 3D cell
- `src/modules/cycleController.js` — 28-second demo sequence and UI state
- `src/styles/main.css` — responsive industrial UI
- `public/reference/` — reference images
