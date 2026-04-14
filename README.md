# Kreditbewertung & Ausfallwahrscheinlichkeitsmodell (PD)

## 📌 Projektübersicht
End-to-End-Pipeline zur Kreditbewertung zur Vorhersage der Ausfallwahrscheinlichkeit (PD)
für Antragsteller von Privatkrediten. Entwickelt im Rahmen eines persönlichen Risikomanagement-Portfolio-Projekts

## 🎯 Geschäftlicher Kontext
Bezieht sich auf reale Anwendungsfälle im Bankwesen:
- **Kreditprüfung**: PD-basierte Kreditgenehmigungsentscheidungen
- **Basel II/III-Compliance**: Internes Ratingsystem (PD, LGD, EAD)
- **Erwarteter Verlust**: EL = PD × LGD × EAD

## 📊 Datensatz
- **Quelle**: [Give Me Some Credit — Kaggle](https://www.kaggle.com/c/GiveMeSomeCredit)
- **Umfang**: 150.000 Trainingsbeispiele, 11 Merkmale
- **Merkmale**:
| Merkmale | Beschreibung | Kontext |
| --- | --- | --- |
| default | **Target**: Ausfall | Ausfallbezeichnung (1 = Ausfall) |
| utilization | Kreditkartennutzung | Kreditauslastung |
| past_due_30/60/90 | Anzahl der Zahlungsverzögerungen | Verstöße in der Vergangenheit |
| debt_ratio | Schulden-Einkommens-Verhältnis | DTI-Verhältnis |
| monthly_income | Monatliche Einkommen | Einkommensnachweis |
| num_dependents | Anzahl der Angehörigen | Haushaltrisikofaktor |

