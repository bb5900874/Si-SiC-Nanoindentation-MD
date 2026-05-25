# Si-SiC-Nanoindentation LAMMPS Simulations

## Overview
This repository contains the LAMMPS input scripts and data files used in the research article:
**"Heterogeneous deformation and phase transformation mechanisms in dual-phase RB-SiC: nanoindentation and molecular dynamics analysis"**
submitted to *Computational Materials Science*.

## System Requirements
- LAMMPS (version 2020 or later recommended)
- Built with the following packages:
  - MANYBODY (for Tersoff potential)
  - MOLECULE (for molecular dynamics simulations)
  - KSPACE (for long-range interactions if needed)
  - EXTRA-FIX (for additional fix commands)

## Simulation Details
- **Material**: Dual-phase RB-SiC (Si and SiC phases)
- **Simulation method**: Molecular dynamics (MD) nanoindentation
- **Potential**: Tersoff potential for Si-C system
- **Indentation**: Vickers indenter
- **Temperature**: 300 K (room temperature)
- **Time step**: 1 fs
- **Indentation Velocity**: 50 m/s

## File Descriptions

### Input Scripts
- `Si-SiC-MD.in`: Main LAMMPS input script for nanoindentation simulation
- `SiC.tersoff`: Tersoff potential parameters for Si-C system

### Compressed Data Files
- `si-sic-data.zip`: Initial atomic configuration of dual-phase Si-SiC system
- Unzip command: `unzip si-sic-data.zip`
- Contains: `si-sic-data` (30 MB uncompressed)

## How to Run
1. Install LAMMPS with the required packages
2. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Si-SiC-nanoindentation-LAMMPS.git
   cd Si-SiC-nanoindentation-LAMMPS
3. Run the simulation:
   mpiexec -np 4 lmp -in Si-SiC-MD.in
