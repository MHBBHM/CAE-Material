# Temperature-Dependent Steel Plastic Material Properties Generator (Post-Fire)

## Introduction

This Python script generates temperature-dependent steel plastic material properties for finite element analysis, particularly for Abaqus software packages. The material properties generated are essential for accurately simulating steel behavior under various thermal conditions.

## Input Data

- **T (Temperature):** A list of temperatures in degrees Celsius.
- **f (Residual Yield Factor):** A list of factors representing the residual yield strength at each temperature.
- **E (Young's Modulus):** Young's modulus of the steel material in GPa.
- **Fy (Yield Strength):** Yield strength of the steel material in MPa.
- **Fu (Ultimate Strength):** Ultimate strength of the steel material in MPa.
- **ey (Yield Strain):** Calculated yield strain based on the yield strength and Young's modulus.
- **eu (Ultimate Strain):** Ultimate strain of the steel material.
- **ef (Final Strain):** Final strain for calculation purposes.

## Code Description

The code performs the following steps:

1. **Define Combined Equation:** A function to calculate plastic stress based on given engineering strain and residual yield factor.
2. **Initialize Lists:** Empty lists to store plastic stress and strain data.
3. **Engineering Strain:** Generate engineering strain data.
4. **Calculate Plastic Stress and Strain:** For each temperature and strain rate pair, calculate plastic stress and strain.
5. **Flatten the Lists:** Combine plastic stress and strain data into single arrays.
6. **Create DataFrame:** Store plastic stress, plastic strain, and temperature data in a Pandas DataFrame.
7. **Export to Excel:** Save the DataFrame to an Excel file.

## Requirements

- Python 3.x
- Required Python packages: numpy, pandas

## Usage

1. Ensure Python 3.x is installed on your system.
2. Install required Python packages using pip:

