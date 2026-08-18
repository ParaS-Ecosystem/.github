# ParaS Ecosystem Technical Charter

> **Open, Device-Agnostic HPC-AI Software Ecosystem**  
> **Vision:** “Code Once, Execute on All”

## Charter Information

| Item | Description |
|---|---|
| **Document Type** | Umbrella Technical Charter |
| **Applies To** | All projects, libraries, frameworks and tools formally hosted under the ParaS Ecosystem |
| **Governance** | ParaS Technical Steering Committee (TSC) with project-level maintainer autonomy |

## Table of Contents

1. [Purpose and Vision](#1-purpose-and-vision)
2. [Technical Scope](#2-technical-scope)
3. [Ecosystem Architecture](#3-ecosystem-architecture)
4. [Core Technical Principles](#4-core-technical-principles)
5. [Projects and Project Lifecycle](#5-projects-and-project-lifecycle)
6. [Technical Governance](#6-technical-governance)
7. [Maintainers, Contributors and Decision Making](#7-maintainers-contributors-and-decision-making)
8. [Cross-Project Engineering Requirements](#8-cross-project-engineering-requirements)
9. [Releases, Compatibility and Roadmap](#9-releases-compatibility-and-roadmap)
10. [Open Source, Licensing and Community](#10-open-source-licensing-and-community)
11. [Working Groups](#11-working-groups)
12. [Charter Maintenance](#12-charter-maintenance)

## 1. Purpose and Vision

ParaS is an open-source, device-agnostic software ecosystem for heterogeneous HPC-AI computing. It provides a sustainable software layer between applications and rapidly evolving processors/accelerators, reducing unnecessary dependence on vendor-specific programming environments while enabling portability and performance.

Its technical vision is **“Code Once, Execute on All”**: applications should be capable of being developed once and executed efficiently across supported heterogeneous platforms with minimal architecture-specific restructuring.

## 2. Technical Scope

ParaS is an umbrella ecosystem. Individual projects may address one or more of the following areas:

- **Programming environment** — programming models, compiler infrastructure, runtime systems, device discovery, hardware abstraction and architecture backends.

- **Scientific and mathematical libraries** — portable and optimized BLAS/LAPACK, FFT, sparse linear algebra, PDE solvers, numerical kernels and domain libraries.

- **Communication** — distributed and accelerator-aware communication, collective operations and interoperability with MPI and related technologies.

- **HPC-AI framework integration** — ParaS backends/adapters for established scientific-computing and AI frameworks.

- **Developer and performance tools** — debugging, profiling, performance analysis, portability analysis, benchmarking and optimization.

- **Architecture enablement** — x86, Arm, RISC-V, GPUs, NPUs, FPGAs, QPUs and future accelerator architectures. Support may differ by project and release.

- **Application** — enabling domain-based applications of HPC-AI.

## 3. Ecosystem Architecture

ParaS follows a layered, modular architecture with well-defined interfaces:

```text
Applications of HPC-AI
        ↓
AI Framework / Workflows
        ↓
ParaS Libraries / Developer Tools
        ↓
ParaS Compiler / Runtime / Hardware Abstraction / Backend Interfaces
        ↓
CPU | GPU | NPU | FPGA | QPU | Emerging Accelerators
```

Projects should expose stable interfaces wherever practical, minimize unnecessary cross-component dependencies, and allow new architectures or backends to be incorporated without redesigning the complete ecosystem.

## 4. Core Technical Principles

- **Architecture and Vendor Neutrality:** Interfaces shall avoid unnecessary assumptions about a specific processor, accelerator or vendor.

- **Standards Alignment:** ParaS shall adopt, implement and contribute to relevant open standards where appropriate.

- **Performance Portability:** Portability includes functional correctness and the pursuit of competitive performance across supported architectures.

- **Modularity and Extensibility:** Components shall use defined interfaces and permit independent evolution or replacement of backends.

- **Interoperability:** ParaS projects shall interoperate with one another and with established HPC-AI software ecosystems where technically appropriate.

- **Open Development:** Source development, issues, design discussions, reviews and contribution processes should be open and traceable.

## 5. Projects and Project Lifecycle

The ecosystem may contain projects which progress through:

**Experimental → Incubating → Active → Mature → Maintenance → Archived**

Each major project shall maintain a product-specific Technical Charter defining its mission, scope, architecture, interfaces, supported platforms, maintainers, contribution and decision process, testing, releases, roadmap and relationship to other ParaS components.

A new project should demonstrate alignment with the ParaS vision, clear technical scope, architectural compatibility, maintainable source, appropriate open-source licensing, identified maintainers, documented interfaces, contribution guidance and defined technical objectives. Admission and lifecycle changes are approved by the TSC.

## 6. Technical Governance

The ParaS Technical Steering Committee (TSC) governs ecosystem-level technical direction. It is responsible for overall architecture, roadmap coordination, project admission/lifecycle, cross-project interfaces, common technical policies, standards alignment, coordinated releases where required, working groups and resolution of cross-project technical conflicts.

Project maintainers retain autonomy for implementation decisions, normal pull-request review, issue resolution and project releases within the scope of their approved charter. The TSC should not become an approval layer for routine project development.

Changes that materially affect ecosystem-wide architecture, shared interfaces, compatibility or multiple ParaS projects shall be coordinated with the affected maintainers and, where required, reviewed by the TSC.

## 7. Maintainers, Contributors and Decision Making

Contributors are participants whose technical contributions are accepted into a ParaS project. Maintainers are contributors entrusted with technical stewardship, including code review, quality, testing, documentation, releases and contributor support.

Maintainer status should be based on sustained contribution, technical competence and demonstrated responsibility.

Technical decisions should seek consensus. Routine decisions are made by relevant maintainers. Significant architectural changes should be documented through an RFC, design proposal, issue or equivalent public mechanism. Where consensus cannot be reached, the responsible project governance or TSC may use a documented voting mechanism.

## 8. Cross-Project Engineering Requirements

- Shared or cross-project APIs shall be documented, versioned where necessary, tested and reviewed by affected projects; backward compatibility should be maintained where practical.

- Production projects shall maintain appropriate unit, functional and regression tests, multi-platform validation, interoperability tests and CI/CD. Performance-sensitive components should maintain representative benchmarks.

- Projects shall follow responsible security practices including dependency management, secure coding, code review, vulnerability handling, release integrity and responsible disclosure.

- Projects should avoid unnecessary duplication and reuse common ParaS infrastructure when this improves maintainability without compromising modularity.

## 9. Releases, Compatibility and Roadmap

Each project may maintain an independent release cycle and versioning policy. Release information should identify supported platforms, major features, known limitations, compatibility requirements and deprecated functionality. Coordinated ecosystem releases may be produced when cross-project interoperability requires joint validation.

The ecosystem roadmap shall be developed collaboratively and should consider emerging architectures, HPC/AI application requirements, open standards, performance, interoperability, scientific-computing needs and long-term sustainability. The roadmap guides priorities without preventing community-led innovation.

## 10. Open Source, Licensing and Community

Each project shall use an approved open-source license and clearly identify applicable licensing and contribution requirements. Contributors shall comply with copyright, contribution and intellectual-property requirements of the project and its governing foundation or organization.

ParaS shall encourage participation from research institutions, universities, supercomputing centers, hardware and software vendors, application developers, open-source communities and individual contributors. Technical participation and decision making shall remain architecture- and vendor-neutral and be based on contribution and project responsibilities.

## 11. Working Groups

The TSC may establish open Technical Working Groups for compiler/programming models, mathematical libraries, communication, AI frameworks, architecture enablement, benchmarking/performance, developer tools, testing/CI/CD, documentation and emerging technologies. Working Groups provide focused technical coordination and report outcomes through the ecosystem’s open governance mechanisms.

## 12. Charter Maintenance

This umbrella Charter defines the common technical and governance framework for the ParaS Ecosystem. Product charters may add project-specific requirements but shall remain consistent with it. Amendments affecting governance, project responsibilities or ecosystem architecture shall be proposed to the TSC and discussed openly before adoption.

---

## Guiding Principle

**Unified Programming. Performance Portability. Universal Reach.**
