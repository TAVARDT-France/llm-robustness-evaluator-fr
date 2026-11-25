# Évaluateur de Robustesse LLM & Testeur de Garde-fous

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-5b3cf5.svg)](https://tavardt-france.github.io/llm-robustness-evaluator-fr/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Audit Défensif des Garde-fous, Injection de Prompt et Résilience des Modèles IA**

Outil interactif et CLI défensif pour les développeurs évaluant la robustesse des garde-fous LLM contre les vecteurs d'injection, les fuites de prompt et les attaques structurelles. Score de Résilience 0-100 + blueprint défensif.

***

## Aperçu

> **OWASP LLM01 & LLM02** | **NIST AI RMF** | **100% Defensive  -  Zero Offensive Payloads**

## 5 Vecteurs de Test Défensifs

| # | Vector | Coverage |
|-|-|-|
| 1 | **Échappement de Délimiteur**  -  Détecte les tokens de contrôle injectés (`</system>`, `[/INST]`) | ✅ |
| 2 | **Fuite du System Prompt**  -  Identifie les patterns d'extraction d'instructions | ✅ |
| 3 | **Substitution de Rôle/Persona**  -  Vérifie la résistance aux substitutions (DAN, mode dev) | ✅ |
| 4 | **Obfuscation Structurelle**  -  Évalue la couverture contre Base64, leetspeak, homoglyphes | ✅ |
| 5 | **Injection Indirecte de Contexte**  -  Simule un document RAG avec payload intégré | ✅ |

***

## Outil En Ligne

Accédez à l'outil interactif directement :

🌐 **[https://tavardt-france.github.io/llm-robustness-evaluator-fr/](https://tavardt-france.github.io/llm-robustness-evaluator-fr/)**

***

## Utilisation via CLI

### Installation

```bash
git clone https://github.com/TAVARDT-France/llm-robustness-evaluator-fr.git
cd llm-robustness-evaluator-fr
pip install -r requirements.txt
```

### Exécution

```bash
python llm_robustness_evaluator.py -prompt "You are a helpful assistant."
```

```
Resilience Score: 85/100
✅ V1 Delimiter Escape  -  PASS
✅ V2 System Prompt Leakage  -  PASS
✅ V3 Role/Persona Override  -  PASS
✅ V4 Structural Obfuscation  -  PASS
⚠️  V5 Indirect Context Injection  -  WARNING
```

***

## Architecture Défensive

Le blueprint défensif inclut :

- 🐍 Filtre Python pour la détection de patterns d'injection
- 📦 Middleware TypeScript pour les APIs Next.js
- 🔒 Template de System Prompt renforcé avec délimiteurs immuables

***

## Liens Utiles

* **Portail Entreprise:** https://ag.tavardt.com/fr/
* **Suite de Diagnostic:** https://tools.tavardt.com/fr/
* **Contact Technique:** https://ag.tavardt.com/fr/contact/

***

### Licence
Distribué sous licence MIT. Consultez le fichier [LICENSE](LICENSE) pour plus de détails.

***

© 2026 TAVARDT. Tous droits réservés.
