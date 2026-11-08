# DNA Double Helix Visualization

### Interactive 3D Visualization of Experimental DNA Structure Using C++, CHAI3D and GLFW

An interactive 3D application for exploring the atomic structure of a DNA double helix using experimental structural data from the Protein Data Bank (PDB).

Developed in **C++** using **CHAI3D 3.3.0**, **GLFW**, and **Visual Studio 2022**, the project demonstrates scientific data parsing, 3D geometry generation, interactive visualization, collision detection and real-time graphical interaction.

## Project Overview

The application loads the experimental DNA structure **PDB ID: 1BNA** and converts atomic coordinates into an interactive three-dimensional molecular representation.

Each atom is represented by a sphere, with colors assigned according to its chemical element.

The application allows users to rotate the DNA structure, zoom in and out, and examine its spatial organization.

The project focuses on interactive scientific visualization rather than molecular dynamics or physically accurate atomic interactions.

## Features

- **Experimental DNA structure:** Loads atomic coordinates from a PDB file.
- **Custom PDB parser:** Extracts atom names, residue names, chain identifiers, chemical elements and 3D coordinates.
- **3D molecular rendering:** Represents atoms as spheres using CHAI3D geometry.
- **Element-based coloring:** Uses distinct colors to identify different chemical elements.
- **Interactive rotation:** Rotates the DNA model using mouse or keyboard-assisted interaction.
- **Zoom control:** Supports mouse-wheel or touchpad scrolling.
- **Centered rotation:** Positions the molecular structure around its geometric center for smooth rotation.
- **Collision detection:** Uses CHAI3D collision-detection functionality.
- **Element legend:** Displays a color legend for interpreting the molecular representation.

## Technologies Used

| Technology | Purpose |
|---|---|
| C++ | Application development and PDB parsing |
| CHAI3D 3.3.0 | 3D graphics, scene management and collision detection |
| GLFW | Window creation and mouse/keyboard input |
| OpenGL | Graphics rendering through the application framework |
| Visual Studio 2022 | Development and compilation |
| RCSB Protein Data Bank | Experimental DNA structural data |

## DNA Structure

The visualization uses **PDB ID: 1BNA**, a well-known experimental structure of B-form DNA.

Structural data source: [RCSB Protein Data Bank — 1BNA](https://www.rcsb.org/structure/1BNA)

The application reads atomic coordinate records from the PDB file and generates the molecular representation programmatically.

### Atom Color Scheme

| Element | Color |
|---|---|
| Carbon (C) | Red |
| Nitrogen (N) | Green |
| Oxygen (O) | Gray |
| Phosphorus (P) | Orange |
| Other elements | Blue |

## Controls

| Input | Action |
|---|---|
| Hold `R` + move mouse/touchpad | Rotate the DNA model |
| Right mouse button + drag | Rotate the DNA model |
| Mouse wheel / two-finger scroll | Zoom in or out |

## Project Structure

```text
DNA-Double-Helix-Visualization/
├── DNAbasepairs.cpp
├── 1BNA.pdb
├── README.md
└── screenshots/
    └── dna-double-helix.png
```

*The directory structure above is the recommended repository layout. The screenshot file should be added when available.*

## Building and Running

### Requirements

- Windows development environment
- Visual Studio 2022 with C++ desktop development tools
- CHAI3D 3.3.0
- GLFW and its required dependencies
- OpenGL-compatible graphics hardware

### Setup

1. Download or clone this repository.
2. Set up CHAI3D 3.3.0 and the GLFW example build environment.
3. Add `DNAbasepairs.cpp` to a compatible Visual Studio project.
4. Ensure that `1BNA.pdb` is available at the file path expected by the application.
5. Configure the required CHAI3D, GLFW and OpenGL dependencies.
6. Build and run the application in Visual Studio.

**Important:** The current source code uses a Windows-specific absolute path to load `1BNA.pdb`. Update this path to match your local environment before running the application.

The repository does not provide a standalone build configuration at this stage.

## Implementation Details

### PDB Data Processing

A custom parser reads PDB atomic records and extracts information including:

- Chemical element
- Atom name
- Residue name
- DNA chain identifier
- Cartesian atomic coordinates

### Molecular Geometry

Atomic positions are converted into sphere geometry and organized into CHAI3D meshes according to chemical element.

The coordinates are centered around their arithmetic mean before visualization, allowing the DNA model to rotate around its own center.

### User Interaction

GLFW input callbacks provide interactive rotation and zoom functionality.

CHAI3D handles scene organization, geometry rendering and collision-detection setup.

## Engineering Skills Demonstrated

- C++ programming
- Scientific data parsing
- Object-oriented graphics frameworks
- 3D coordinate transformations
- Interactive computer graphics
- Mouse and keyboard event handling
- Collision-detection integration
- Scientific visualization
- Visual Studio development and debugging

## Limitations

This application is a molecular visualization tool and does not currently implement:

- Molecular dynamics simulation
- Atom-level manipulation
- Physically accurate intermolecular forces
- Physical haptic-device feedback
- Automated atom identification
- Structural energy minimization

## Possible Future Extensions

Potential extensions include atom selection and identification, molecular distance measurements, support for additional PDB structures and integration with interactive force-feedback systems.

These are proposed improvements and are not part of the current implementation.

## Data Attribution

The DNA structural coordinates are obtained from the **RCSB Protein Data Bank**, structure **1BNA**.

RCSB PDB: https://www.rcsb.org/structure/1BNA

The experimental structure should be cited using the primary literature referenced by its RCSB PDB entry.

## Dependencies and Licensing

This project was developed using CHAI3D and GLFW.

These third-party libraries remain subject to their respective licenses. The repository should retain applicable third-party copyright and attribution notices.

No license is currently specified for the original project code.

## Project Status

**Completed prototype — Interactive DNA double helix visualization**

The current version supports experimental structure loading, 3D rendering, rotation and zoom.

---

Developed as an independent C++ scientific visualization project, building on previous work in robotics, interactive simulation and haptic technologies.
