# Auto Insurance Pricing Model using GLMs

This project develops a two-part actuarial pricing model using French motor claims data. The objective is to estimate the pure premium (expected annual claim cost) by separately modeling claim frequency and claim severity using Generalized Linear Models (GLMs).

The modeling framework follows standard actuarial pricing methodology.

## Overview

This project predicts **pure premium pricing** for auto insurance using real French motor claims data from the `freMTPL2freq` and `freMTPL2sev` datasets. The core methodology follows industry-standard actuarial practice:

1. **Frequency Model** – How likely is a customer to make a claim? (Poisson GLM)
2. **Severity Model** – How large will claims be? (Gamma GLM with log link)
3. **Pure Premium** – Expected annual cost = Frequency × Severity

## Key Features

- **Two-stage GLM modeling** following actuarial best practices
- **Comprehensive model validation** including lift charts and segment calibration
- **Diagnostic analysis** for overdispersion and distributional assumptions
- **Business-focused interpretations** with practical pricing recommendations
- **Segment-specific calibration** to identify cross-subsidies

## Dataset

The data originates from French motor claims and includes:

| Feature | Description |
|---------|-------------|
| `ClaimNb` | Number of claims per policy |
| `Exposure` | Fraction of year policy was active |
| `DrivAge` | Age of the driver |
| `VehAge` | Age of the vehicle |
| `VehPower` | Engine power |
| `BonusMalus` | Claims history score (50 = clean record) |
| `Area` | Urban density (A=rural, F=very urban) |
| `VehBrand` | Vehicle brand category |
| `VehGas` | Fuel type (Regular/Diesel) |
| `Region` | French administrative region |

## Limitations & Future Improvements

- Assumes independence between frequency and severity
- Loading Factors applied according to Customer Behaviour within each risk segment
- No interaction terms included
- Could extend using machine learning comparison

## Actuarial Concepts Utilized
- Exposure-based rate modeling
- Poisson process assumption for claim frequency
- Gamma modeling for positively skewed severity
- Risk-based pricing framework
- Interpretation of GLM coefficients in insurance context

**Source**: [HuggingFace - freMTPL2 Dataset](https://huggingface.co/datasets/mabilton/fremtpl2)

