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
- **Ziel**: `SeriousDlqin2yrs` (1 = Ausfall innerhalb von 2 Jahren)
- **Ausfallquote**: ~6,65 %

## 🔧 Tech-Stack
Python 3.10 | scikit-learn | XGBoost | LightGBM | SHAP | scorecardpy | MLflow

## 📁 Projektstruktur
(siehe Dokumentation oben)