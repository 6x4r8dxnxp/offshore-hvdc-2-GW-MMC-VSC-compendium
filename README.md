# Systems Engineering & Operations Compendium for 2-GW MMC-VSC Platforms

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Version](https://img.shields.io/badge/version-2.0-blue)]()
[![Status](https://img.shields.io/badge/status-active-success)]()

> **A comprehensive framework for governing offshore-to-mainland HVDC transmission corridors under European scale-up**

---

## 📋 About This Repository

This repository contains technical documentation for engineering, operating, and governing 2-gigawatt modular multilevel converter (MMC) based voltage source converter (VSC) platforms in Europe's offshore transmission infrastructure.

### **Key Documents:**

| Document | Pages | Audience | Purpose |
|----------|-------|----------|---------|
| **[Research Brief](docs/research-brief/2026-03_Research_Brief_Offshore_Corridors.pdf)** | 2 | Multi-stakeholder | Strategic framing & core principles |
| **[Full Compendium](docs/compendium/compendium-v2.0.pdf)** | 65 | HVDC engineers, TSOs | Technical deep-dive with mathematical annex |

---

## 🎯 Core Contribution

This work addresses a critical gap in offshore HVDC engineering: **how to govern converter-dominated transmission corridors as coherent cyber-physical systems rather than isolated asset chains.**

### **The Offshore Corridor Problem:**

Europe's offshore build-out faces a fundamental challenge:
- Offshore wind volumes are growing (333 GW by 2050)
- Distances to shore are increasing (>100 km becoming common)
- Landing corridors are tightening
- Engineering complexity rises faster than linearly

The decisive engineering object is not the offshore station, the cable, or the onshore station in isolation—it is the **bounded offshore-to-mainland transmission and conversion corridor**: from offshore wind-farm-side AC collection through offshore conversion, HVDC transmission, landfall transition, to onshore reconversion.

---

## 🔑 Five Governing Principles

### **1. Define role & behaviour before vendor instantiation**
Functional requirements must stabilize before supplier-specific optimization closes the design space. This preserves future compatibility without forcing identical hardware across all projects.

### **2. Keep control, protection, and restoration in one logic**
In converter-dominated corridors, continuous control, sequential control, fault containment, and recovery form one coupled operating architecture. A corridor becomes fragile when these layers evolve independently.

### **3. Preserve bounded degraded states**
Degraded operation is not a failure mode—it is a designed operating regime. Offshore value depends heavily on the ability to maintain bounded service under reduced capability while preserving recovery options.

### **4. Treat evidence as an operating asset**
The Engineering Evidence Bill of Materials (Evidence BOM) preserves traceability from claim to model, test, acceptance, and operating envelope. This continuity is essential for re-evidence after changes, expansion assessment, and post-event analysis.

### **5. Align technical + governance architecture**
Multi-party offshore systems require explicit allocation of ownership, operational authority, settings authority, model access, and decision rights. Governance is part of operability, not a contractual afterthought.

---

## 📂 Repository Structure

├── docs/ # All technical documents │ ├── research-brief/ # 2-page strategic overview │ │ └── research-brief-v1.0.pdf │ ├── compendium/ # Full 62-page technical work │ │ ├── compendium-v2.0.pdf │ │ └── errata.md │ └── supplementary/ # Figures, references, glossary │ ├── figures/ │ ├── references.bib │ └── glossary.md │ ├── templates/ # Practical tools from Annex II │ ├── evidence-bom-template.xlsx │ ├── kpi-template.xlsx │ └── re-evidence-decision-matrix.md │ ├── examples/ # Future: case studies │ └── case-study-placeholder.md │ └── community/ # Contributing guidelines ├── CONTRIBUTING.md ├── CODE_OF_CONDUCT.md └── discussions.md


---

## 🚀 Quick Start

### **For Decision-Makers & Policy:**
→ Start with the **[Research Brief](docs/research-brief/research-brief-v1.0.pdf)** (2 pages)  
→ Focus: Strategic framing, governing principles, system-level implications

### **For HVDC Engineers & TSO Technical Staff:**
→ Read the **[Full Compendium](docs/compendium/compendium-v2.0.pdf)** (62 pages)  
→ Key sections:
   - **Part I** – Strategic & System Context
   - **Part II** – Platform Framing
   - **Part III** – Technical & Operational Core (control, protection, disturbance response)
   - **Part IV** – Evidence, Validation & Digital Dependencies
   - **Part V** – Delivery, Operations & Evolution
   - **Annex I** – Mathematical Definitions & Key Inequalities
   - **Annex II** – Evidence BOM Templates, Validation Artefact Classes, KPI Sets

### **For Operations & Maintenance Teams:**
→ See **Part V** (Delivery, Operations, Evolution)  
→ Download practical templates from `/templates/`:
   - Evidence BOM Template
   - Acceptance & Operational KPI Sets
   - Re-evidence Decision Matrix

---

## 📊 Use Cases

This framework is designed for:

- **Transmission System Operators (TSOs)** designing, procuring, or operating offshore HVDC corridors
- **Original Equipment Manufacturers (OEMs)** developing functional specifications for converter platforms
- **Regulators & Policy Makers** assessing offshore interoperability and standardization requirements
- **Research Institutions** advancing systems-engineering methods for critical infrastructure
- **CIGRE/IEEE Working Groups** on HVDC standardization, offshore wind integration, and interoperability

---

## 🛠️ Practical Tools Included

### **From Annex II (Evidence, Validation & Governance):**
- ✅ **Evidence BOM Template** – Structured lifecycle evidence architecture
- ✅ **Acceptance KPI Catalogue** – Functional, protection, recovery, power-quality, timing KPIs
- ✅ **Operational KPI Sets** – Availability, maintainability, resilience, data quality, governance
- ✅ **Re-evidence Trigger Classification** – When old proof becomes insufficient
- ✅ **Lifecycle-Phase KPI Matrix** – Pre-FEED through extension & major change

### **From Annex I (Mathematical Foundations):**
- ✅ Operating-state partitions & state-dependent constraints
- ✅ Constraint classes: voltage, current, thermal, dielectric, harmonic, stability, timing
- ✅ Protection timing inequalities & selectivity conditions
- ✅ Recovery-time formulations & fault-ride-through profiles
- ✅ Reliability, availability, maintainability (RAM) definitions
- ✅ Uncertainty, confidence & safe-operation bounds

---

## 🌍 Context & Motivation

### **Why Platform Logic Matters:**

European offshore planning already assumes large standardized transmission units:
- The **Offshore Network Development Plan (ONDP)** for the Northern Seas projects 119 GW by 2030 and 333 GW by 2050
- Most near-term projects remain radial; hybrid and multi-terminal structures gain relevance post-2030
- The **2-GW scale** emerges as a repeatable building block fitting far-shore distances and planning assumptions

### **Why Standardization Is Economic Necessity:**

Bespoke repetition under rising offshore complexity becomes too expensive, too slow, and too difficult to govern:
- Larger turbines + larger clusters + longer routes = non-linear complexity growth
- Material intensity, offshore footprint, marine logistics, and interface density all increase
- **Repeatability, common functional logic, and disciplined operational learning** are among the few credible ways to keep decarbonization infrastructure investable

### **Why Evidence Continuity Matters:**

Offshore HVDC corridors are long-lived (30+ years), high-consequence assets:
- Settings evolve, firmware changes, neighboring systems change, people leave projects
- Without an explicit **evidence architecture**, the corridor gradually becomes harder to understand even if hardware remains unchanged
- The Evidence BOM preserves the reasoning that justifies accepted behavior—enabling re-evidence, extension assessment, and post-event analysis

---

## 📚 How to Cite

If you use this work in research, practice, or policy development, please cite:

```bibtex
@techreport{boettcher2026offshore,
  author    = {Böttcher, Enno},
  title     = {Systems Engineering \& Operations Compendium for a 2-GW MMC-VSC Converter Platform},
  year      = {2026},
  month     = {March},
  type      = {Technical Report},
  note      = {Version 2.0},
  url       = {https://github.com/[your-username]/offshore-hvdc-compendium}
}
