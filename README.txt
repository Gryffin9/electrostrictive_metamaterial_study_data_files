================================================================================
ELECTROSTRICTIVE METAMATERIAL DATA REPOSITORY
================================================================================
Paper: "Electrostrictive Metamaterial Study: Shaping Fields to Exceed
Intrinsic Material Limits"
Journal: Science Advances
================================================================================

ABSTRACT
--------
This repository contains simulation data supporting the findings of the paper
titled, "Electrostrictive Metamaterial Study: Shaping Fields to Exceed
Intrinsic Material Limits".

================================================================================

FOLDER STRUCTURE
----------------

02_Slab_Baseline/
    Reference slab geometry results (baseline for comparison)

03_Design1_Architected/
    Design D1 (4-arm ring structure with optimized parameters)

04_Design2_Architected/
    Design D2 (alternate architected geometry)

05_Optimization_Results/
    Nelder-Mead optimization convergence data
    - Parameter evolution: t0, theta4/theta5, r2
    - Objective function values per iteration

06_Validation_Data/
    P-E and S-E validation curves
    - Verifies COMSOL implementation against Hom & Shankar analytical model

07_Preliminary_Analysis/
    Early analysis before geometry optimization

================================================================================

FILE DESCRIPTIONS
-----------------

Each geometry folder (02_Slab_Baseline, 03_Design1_Architected, 04_Design2_
Architected) contains the following subfolders and files:

voltage_sweep_data/
    Surface-averaged quantities computed at each phase of the sinusoidal
    voltage drive V(t) = Vmax*sin(2*pi*t), where t is the drive phase
    parameter (0 to 0.5 in steps of 0.01).

    *_avg_displacement_vs_voltage.txt
        Surface-averaged displacement magnitude and components (ux, uy, uz)
        as a function of the drive phase parameter.
        Columns: t (s), |u| (um), ux (um), uy (um), uz (um)

    *_avg_strain_vs_voltage.txt
        Surface-averaged electrostrictive strain tensor components as a
        function of the drive phase parameter.
        Columns: t (s), Sxx, Syy, Sxy (dimensionless)

    *_avg_polarization_vs_voltage.txt
        Surface-averaged polarization components as a function of the
        drive phase parameter.
        Columns: t (s), Px (C/m^2), Py (C/m^2)

    *_avg_stress_vs_voltage.txt
        Surface-averaged stress tensor components as a function of the
        drive phase parameter.
        Columns: t (s), sigma_xx (N/m^2), sigma_yy (N/m^2), sigma_xy (N/m^2)

field_data_t025/
    Spatial field distributions at peak drive (t* = 0.25, corresponding to
    maximum applied voltage).

    *_displacement_field_t025.txt
        Nodal displacement field data containing x,y coordinates and
        displacement components for each mesh node at peak drive.
        Used for computing directionality metrics and generating arrow plots.

    *_polarization_arrows_t025.txt
        Polarization vector field data for arrow plot visualization.
        Contains position and polarization vector components.

    *_polarization_magnitude_t025.txt
        Surface polarization magnitude (norm) at each mesh node at peak drive.

stress_distribution/
    Stress field visualizations at peak drive (t* = 0.25).

    *_von_Mises_stress.png
        von Mises equivalent stress distribution across the geometry.
        Used for stress histogram generation and safe-bias analysis.

    *_stress_xx.png
        Normal stress component sigma_xx distribution.

    *_stress_yy.png
        Normal stress component sigma_yy distribution.

    *_stress_xy.png
        Shear stress component sigma_xy distribution.

stress_data/
    *_von_Mises_stress_data.txt
        Nodal von Mises stress values for all mesh nodes at peak drive.
        Used for generating area-weighted stress histograms.

--------------------------------------------------------------------------------

05_Optimization_Results/

    Fig8_D1_optimization_convergence.txt
        Nelder-Mead optimization iterations for Design 1.
        Columns: t0 (m), theta4 (rad), theta5 (rad), r2 (m), Objective

    Fig8_D2_optimization_convergence.txt
        Nelder-Mead optimization iterations for Design 2.
        Columns: r2 (m), t0 (m), theta1 (rad), theta2 (rad), theta4 (rad),
                 theta5 (rad), Objective

--------------------------------------------------------------------------------

06_Validation_Data/

    FigS1_polarization_vs_Efield_slab.txt
        Polarization vs electric field (P-E) curve for slab geometry.
        Validates the electrostriction implementation.
        Columns: Ey (MV/m), Py (C/m^2)

    FigS1_polarization_vs_Efield_disc.txt
        P-E curve for disc geometry (COMSOL benchmark comparison).

    FigS1_strain_vs_Efield_slab.txt
        Strain vs electric field (S-E) curve for slab geometry.
        Confirms quadratic electrostriction relationship S proportional to E^2.
        Columns: Ey (MV/m), Syy (dimensionless)

    FigS1_strain_vs_Efield_disc.txt
        S-E curve for disc geometry (COMSOL benchmark comparison).

    disc_simulation_parameters.txt
        Disc geometry simulation setup parameters used for validation.

--------------------------------------------------------------------------------

07_Preliminary_Analysis/

    preliminary_data/
        preliminary_stress_avg_2D.txt
            Average stress data from preliminary 2D design analysis.

        preliminary_stress_avg_slab.txt
            Average stress data from preliminary slab analysis.

    stress_time_evolution/
        stress_vonMises_vs_time.png
            von Mises stress evolution over the drive cycle.

        stress_xx_vs_time.png
            Normal stress sigma_xx evolution over the drive cycle.

        stress_xy_vs_time.png
            Shear stress sigma_xy evolution over the drive cycle.

        stress_yy_vs_time.png
            Normal stress sigma_yy evolution over the drive cycle.

        stress_components_consolidated.png
            Consolidated plot of all stress components.

================================================================================

UNITS
-----

Quantity              Unit            Notes
--------              ----            -----
Displacement          um              Micrometers
Stress                N/m^2 (Pa)      Pascals
Electric field        MV/m            Megavolts per meter
Polarization          C/m^2           Coulombs per square meter
Strain                dimensionless   Electrostrictive strain tensor component
Drive phase (t)       s               Parameter in V(t) = Vmax*sin(2*pi*t)
Length/Position       mm              Millimeters
Angles (optimization) rad             Radians

================================================================================

SOFTWARE
--------
COMSOL Multiphysics 6.2.0.339
  - Solid Mechanics module
  - Electrostatics module
  - Ferroelectroelasticity coupling

================================================================================

CONTACT
-------
For questions about this data repository, please contact the corresponding
author listed in the published manuscript.

================================================================================
Data organized: February 2026
================================================================================
