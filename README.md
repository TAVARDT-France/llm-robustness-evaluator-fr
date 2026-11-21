
# Évaluateur de Robustesse LLM & Testeur de Garde-fous

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-00ff88?style=flat-square&logo=github)](https://tavardt-france.github.io/llm-robustness-evaluator-fr/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![OWASP LLM](https://img.shields.io/badge/OWASP-LLM01%2FLLM02-red?style=flat-square)](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
[![NIST AI RMF](https://img.shields.io/badge/NIST-AI%20RMF-blue?style=flat-square)](https://www.nist.gov/artificial-intelligence)

**Audit Défensif des Garde-fous, Injection de Prompt et Résilience des Modèles IA**

Outil interactif et CLI défensif pour les développeurs évaluant la robustesse des garde-fous LLM contre les vecteurs d'injection, les fuites de prompt et les attaques structurelles. Score de Résilience 0-100 + blueprint défensif.

---

## Aperçu

> **OWASP LLM01 & LLM02** | **NIST AI RMF** | **100% Defensive — Zero Offensive Payloads**

## 5 Vecteurs de Test Défensifs

| # | Vector | Coverage |
|---|--------|----------|
| 1 | **Échappement de Délimiteur** — Détecte les tokens de contrôle injectés (`</system>`, `[/INST]`) | ✅ |
| 2 | **Fuite du System Prompt** — Identifie les patterns d'extraction d'instructions | ✅ |
| 3 | **Substitution de Rôle/Persona** — Vérifie la résistance aux substitutions (DAN, mode dev) | ✅ |
| 4 | **Obfuscation Structurelle** — Évalue la couverture contre Base64, leetspeak, homoglyphes | ✅ |
| 5 | **Injection Indirecte de Contexte** — Simule un document RAG avec payload intégré | ✅ |

---

## Outil En Ligne

Accédez à l'outil interactif directement :

🌐 **[https://tavardt-france.github.io/llm-robustness-evaluator-fr/](https://tavardt-france.github.io/llm-robustness-evaluator-fr/)**

🛠 **[https://tools.tavardt.com/fr/](https://tools.tavardt.com/fr/)**

---

## Utilisation via CLI

### Installation

```bash
git clone https://github.com/TAVARDT-France/llm-robustness-evaluator-fr.git
cd llm-robustness-evaluator-fr
pip install -r requirements.txt
```

### Exécution

```bash
python llm_robustness_evaluator.py --prompt "You are a helpful assistant."
```

```
Resilience Score: 85/100
✅ V1 Delimiter Escape — PASS
✅ V2 System Prompt Leakage — PASS
✅ V3 Role/Persona Override — PASS
✅ V4 Structural Obfuscation — PASS
⚠️  V5 Indirect Context Injection — WARNING
```

---

## Architecture Défensive

Le blueprint défensif inclut :

- 🐍 Filtre Python pour la détection de patterns d'injection
- 📦 Middleware TypeScript pour les APIs Next.js
- 🔒 Template de System Prompt renforcé avec délimiteurs immuables

---

## Portails Officiels

Accédez au réseau officiel de portails TAVARDT :

| Portal | URL |
|--------|-----|
| Portail Officiel TAVARDT | [https://ag.tavardt.com/fr/](https://ag.tavardt.com/fr/) |
| Centre d'Outils | [https://tools.tavardt.com/fr/](https://tools.tavardt.com/fr/) |
| Contact | [https://ag.tavardt.com/fr/contact/](https://ag.tavardt.com/fr/contact/) |
| GitHub | [https://github.com/TAVARDT-France](https://github.com/TAVARDT-France) |

---

## Licence

Licence MIT — utilisation libre à des fins défensives et éducatives.

---

<p align="center">
  <strong>TAVARDT — France</strong><br>
  <a href="https://ag.tavardt.com/fr/">https://ag.tavardt.com/fr/</a> &bull;
  <a href="https://tools.tavardt.com/fr/">https://tools.tavardt.com/fr/</a><br>
  &copy; 2026 TAVARDT. Tous droits réservés.
</p>
