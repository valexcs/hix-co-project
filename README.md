# HIX-CO Project

Data and analysis repository for:

## The H IX galaxy survey IV: What does the molecular gas reveal in HI eXtreme galaxies?
> V. A. Capa, H. Dénes, K. A. Lutz, and T. H. Brown.

---

## Overview

Galaxies with extreme neutral hydrogen reservoirs ($\mathrm{H~\scriptstyle I}$-eXtreme / $\mathrm{H~\scriptstyle IX}$) paradoxically exhibit normal or low star formation rates. This project investigates the molecular gas content and kinematic properties of five $\mathrm{H~\scriptstyle IX}$ survey galaxies using ALMA $\mathrm{CO}(1-0)$ rotational transition observations combined with ATCA $\mathrm{H~\scriptstyle I}$ data:
- **ESO055-G013**
- **ESO208-G026**
- **ESO378-G003**
- **ESO381-G005**
- **ESO417-G018**

---

## Repository Structure

```text
.
├── LICENSE
├── README.md
└── data/
    └── 3dbarolo/
        ├── co/                  # 3DBarolo modeling for ALMA CO(1-0) data
        │   ├── eso055_g013/
        │   ├── eso208_g026/
        │   ├── eso378_g003/
        │   ├── eso381_g005/
        │   └── eso417_g018/
        └── hi/                  # 3DBarolo modeling for ATCA HI data
            ├── eso055_g013/
            ├── eso208_g026/
            ├── eso378_g003/
            ├── eso381_g005/
            └── eso417_g018/
```

### 3DBarolo Output Products
Each galaxy subdirectory under `data/3dbarolo/` contains:
- `rings_initial.txt`: Configuration file detailing the initial parameters used in [3DBarolo](https://editeodoro.github.io/Bbarolo/).
- `rings_final2.txt`: Tilted-ring model parameter tables containing galactocentric radii ($r$, RAD), rotation velocities ($v_{\text{rot}}$, VROT) and velocity dispersions ($\sigma$, DISP) with respective uncertainties, and inclinations ($\mathrm{INC}$, INC), position angles ($\mathrm{PA}$, P.A.) and systemic velocities ($v_\mathrm{sys}$, VSYS).
- `densprof.txt`: Surface density and Mass surface density with respective uncertainties.
- Maps, parameters and position-velocity plots.

---

## Data Sources

- **ALMA $\mathrm{CO}(1-0)$ data:** Raw and pipeline-calibrated data cubes are available in the [ALMA Science Archive](https://almascience.nrao.edu/aq) under Project Code: `2019.2.00169.S`.
- **ATCA $\mathrm{H~\scriptstyle I}$ data:** Primary $\mathrm{H~\scriptstyle I}$ data cubes and catalogues from the $\mathrm{H~\scriptstyle IX}$ survey (Lutz et al. 2017, 2018) are accessible via the online [CDS VizieR database](https://vizier.cds.unistra.fr/viz-bin/VizieR).


---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.
