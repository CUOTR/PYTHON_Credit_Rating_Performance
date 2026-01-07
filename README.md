# PYTHON: CREDIT RATING PERFORMANCE

# OVERVIEW

This project analyzes a  consumer loan dataset from KAGGLE  to evaluate the performance of the internal credit rating system (`sub_grade`).

The main objective is to assess whether the rating grades (from A1 to G5) effectively discriminate credit risk by examining actual

(`default rates`)(Charged Off loans) across different grades.

Dataset: https://www.kaggle.com/datasets/nezukokamaado/auto-loan-dataset/data

## EDA

## Default loans / Default rate

**Insights:**
- Abnormally high credit risk in the portfolio; Losses are concentrated in defaults, not prepayments.
- Risks are typically concentrated in the low-income and moderate-DTI segments.
- Concentration Risk in Debt Consolidation, Untapped Potential in Home Improvement.

**Strategies:**
- Strengthen debt collection: Invest in early intervention, multi-channel recovery, and specialized teams to lower LGD below 50%.
- Tighten underwriting standards: Focus on excluding or limiting low-income and moderate-DTI applicants to reduce overall PD.
- Shift portfolio: Aggressively scale Home Improvement loans while capping exposure to Debt Consolidation to reduce concentration risk.

## Grade / Sub grade

**Insights:**
- Higher income borrowers tend to borrow more (positive correlation between income and loan amount).
- DTI is a stronger predictor of creditworthiness than income.
- Effective risk-based underwriting.
- Risk-based pricing works well in low-to-moderate risk (A-E3), pricing breaks down in high-risk tiers (E4-G).

**Strategies:**
- Maintaining strict verification for subprime
- Targeting higher-income borrowers selectively with low DTI.
- Ensure clear rate differentiation across all grades, especially adding term-based adjustments in high-risk tiers.

## Default Rate by Sub Grade

**Insights:**
- Linear interest rate increases perfectly offset rising risk, showing strong pricing discipline.
- Volatile default rates in F-G reveal loss of scoring stability and accuracy at the high-risk tail.
- High defaults paired with large loan sizes in lower grades create outsized loss potential.

**Strategies:**
- Restrict volume and loan sizes in F-G grades to control outsized loss potential.
- Add new criteria to improve the scale: Payment history, Transaction history, ... or switch to a point-based format to enhance quality.
