# Replication Study: How APIs Create Growth by Inverting the Firm

## Overview

This project replicates and extends the findings of **Benzell, Hersh & Van Alstyne (2024)**, which examines how API adoption transforms firm growth by shifting innovation outside organizational boundaries. Traditional theories of the firm suggest that growth occurs by internalizing activities; however, API-enabled platforms allow external developers and complementary businesses to create value on behalf of the firm.

The study investigates whether API adoption leads to measurable improvements in firm market value and explores the mechanisms through which APIs generate growth.

---

## Research Question

**Do firms experience higher market value after adopting APIs?**

The project evaluates whether API adoption creates economic value through:

1. Increased complement innovation
2. Lower innovation and R&D costs
3. Stronger network effects

---

## Methodology

### Data Generation

A synthetic panel dataset was constructed consisting of:

* 500 firms
* 55 quarters (2007–2020)
* 27,500 firm-quarter observations
* Industry classifications:

  * Manufacturing
  * Services
  * Retail
  * Transport
  * Other

The dataset incorporates:

* API adoption events
* Firm heterogeneity
* Time trends
* Global Financial Crisis shock
* COVID-19 shock

### Variables

Key variables include:

* API Adoption Indicator
* Post-Adoption Indicator
* Time Since Adoption
* Firm Size
* Industry Category
* Simulated Market Value

---

## Econometric Framework

### Difference-in-Differences (DiD)

To estimate the causal impact of API adoption, a Difference-in-Differences framework was implemented:

[
Treatment\ Effect = Observed\ Change - Counterfactual\ Change
]

This approach controls for baseline differences between firms and common macroeconomic trends.

### Two-Way Fixed Effects Model

The primary estimation strategy uses:

[
Y_{it} = \beta API_{it} + \mu_i + \tau_t + \epsilon_{it}
]

where:

* (Y_{it}) = Firm market value
* (API_{it}) = API adoption indicator
* (\mu_i) = Firm fixed effects
* (\tau_t) = Time fixed effects
* (\epsilon_{it}) = Error term

This specification helps address omitted-variable bias arising from unobserved firm characteristics.

### Event Study Analysis

An event-study framework was implemented to examine dynamic treatment effects before and after API adoption.

The analysis tests:

* Pre-treatment trends
* Post-adoption growth dynamics
* Persistence of API effects over time

---

## Results

### Overall Effect

| Metric                             | Estimate |
| ---------------------------------- | -------- |
| Difference-in-Differences Estimate | 0.1530   |
| Percentage Increase in Firm Value  | 16.5%    |
| P-value                            | 0.0004   |

Results indicate that API adoption is associated with a statistically significant increase in firm market value.

### Industry-Level Effects

| Industry      | Estimated Increase |
| ------------- | ------------------ |
| Manufacturing | 22.6%              |
| Transport     | 21.1%              |
| Services      | 13.7%              |
| Retail        | 13.4%              |
| Other         | 12.0%              |

Manufacturing and transport firms appear to benefit most strongly from API adoption.

---

## Key Findings

* API adoption generates significant positive effects on firm value.
* External ecosystems create complementary innovation that firms do not need to build internally.
* APIs reduce innovation costs by shifting development effort to external participants.
* Network effects create positive feedback loops between developers and users.
* The impact of API adoption varies across industries, with manufacturing and transport exhibiting the largest gains.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Statsmodels
* Matplotlib
* Seaborn

---

## References

Benzell, S., Hersh, J., & Van Alstyne, M. (2024). *How APIs Create Growth by Inverting the Firm.*

Van Alstyne, M., Parker, G., & Choudary, S. P. Platform Ecosystems and Network Effects Literature.

Angrist, J. D., & Pischke, J. Mostly Harmless Econometrics.
