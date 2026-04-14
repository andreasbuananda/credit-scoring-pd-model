# Kreditbewertung & Ausfallwahrscheinlichkeitsmodell (PD)

## Projektübersicht
End-to-End-Pipeline zur Kreditbewertung zur Vorhersage der Ausfallwahrscheinlichkeit (PD)
für Antragsteller von Privatkrediten. Entwickelt im Rahmen eines persönlichen Risikomanagement-Portfolio-Projekts

## Geschäftlicher Kontext
Bezieht sich auf reale Anwendungsfälle im Bankwesen:
- **Kreditprüfung**: PD-basierte Kreditgenehmigungsentscheidungen
- **Basel II/III-Compliance**: Internes Ratingsystem (PD, LGD, EAD)
- **Erwarteter Verlust**: EL = PD × LGD × EAD

## 📊 Datensatz

- **Quelle**: [Give Me Some Credit — Kaggle](https://www.kaggle.com/c/GiveMeSomeCredit)
- **Umfang**: 150.000 Trainingsbeispiele, 11 Merkmale
- **Zielvariable**: `SeriousDlqin2yrs` (1 = Zahlungsausfall innerhalb von 2 Jahren)
- **Ausfallquote (Bad Rate)**: ~6,65 %

### 📋 Merkmalsbeschreibung

| Nr. | Ursprünglicher Spaltenname | Umbenennung | Datentyp | Beschreibung | Bankkontext |
|-----|---------------------------|-------------|----------|--------------|-------------|
| 1 | `SeriousDlqin2yrs` | `target` | Binär (0/1) | **Zielvariable**: Gibt an, ob ein Kreditnehmer innerhalb von 2 Jahren in Zahlungsverzug geraten ist | Ausfallkennzeichnung (PD-Label) |
| 2 | `RevolvingUtilizationOfUnsecuredLines` | `utilization` | Float (0–1+) | Verhältnis des genutzten Kreditrahmens zu ungesicherten Kreditlinien (z. B. Kreditkarten) | Kreditauslastungsquote |
| 3 | `age` | `age` | Integer | Alter des Kreditnehmers in Jahren | Demografisches Risikoprofil |
| 4 | `NumberOfTime30-59DaysPastDueNotWorse` | `past_due_30_59` | Integer | Anzahl der Zahlungsverzögerungen von 30–59 Tagen (nicht schlimmer) in den letzten 2 Jahren | Zahlungshistorie – leichte Verstöße |
| 5 | `DebtRatio` | `debt_ratio` | Float | Verhältnis von monatlichen Schulden zu monatlichem Bruttoeinkommen (Schuldenquote) | Schulden-Einkommens-Verhältnis (DTI) |
| 6 | `MonthlyIncome` | `monthly_income` | Float | Monatliches Bruttoeinkommen des Kreditnehmers in USD | Einkommensnachweis (~29 % fehlende Werte) |
| 7 | `NumberOfOpenCreditLinesAndLoans` | `open_credit_lines` | Integer | Anzahl der offenen Kreditlinien und Darlehen (einschl. Ratenkredite wie Autokredite) | Kreditportfolio-Komplexität |
| 8 | `NumberOfTimes90DaysLate` | `past_due_90` | Integer | Anzahl der Zahlungsverzögerungen von 90 oder mehr Tagen | Zahlungshistorie – schwere Verstöße |
| 9 | `NumberRealEstateLoansOrLines` | `real_estate_loans` | Integer | Anzahl der Hypotheken- und Immobilienkredite einschließlich Kreditlinien | Besicherte Kreditbelastung |
| 10 | `NumberOfTime60-89DaysPastDueNotWorse` | `past_due_60_89` | Integer | Anzahl der Zahlungsverzögerungen von 60–89 Tagen (nicht schlimmer) in den letzten 2 Jahren | Zahlungshistorie – mittlere Verstöße |
| 11 | `NumberOfDependents` | `num_dependents` | Integer | Anzahl der unterhaltsberechtigten Personen im Haushalt (ohne den Antragsteller selbst) | Haushaltrisikofaktor (~2,6 % fehlende Werte) |

