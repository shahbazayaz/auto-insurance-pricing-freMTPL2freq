# Auto Insurance Pricing Model with GLM

A comprehensive actuarial pricing model for auto insurance using French motor claims data. This project implements a two-part Generalized Linear Model (GLM) approach to calculate pure premiums by modeling claim frequency and severity separately.

## 📋 Overview

This project predicts **pure premium pricing** for auto insurance using real French motor claims data from the `freMTPL2freq` and `freMTPL2sev` datasets. The core methodology follows industry-standard actuarial practice:

1. **Frequency Model** – How likely is a customer to make a claim? (Poisson GLM)
2. **Severity Model** – How large will claims be? (Gamma GLM with log link)
3. **Pure Premium** – Expected annual cost = Frequency × Severity

## 🎯 Key Features

- **Two-stage GLM modeling** following actuarial best practices
- **Comprehensive model validation** including lift charts and segment calibration
- **Diagnostic analysis** for overdispersion and distributional assumptions
- **Business-focused interpretations** with practical pricing recommendations
- **Comparative analysis** with Tweedie models
- **Segment-specific calibration** to identify cross-subsidies

## 📊 Dataset

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

**Source**: [HuggingFace - freMTPL2 Dataset](https://huggingface.co/datasets/mabilton/fremtpl2)

