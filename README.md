---
title: FEM vs Least-Squares FEM | Introduction
description: Galerkin limitations → LSFEM advantages → Systematic PDE comparison (ADR → Stokes → NS → FSI → PINNs)
---

# Introduction

The finite element method (FEM) is a cornerstone numerical technique for the approximate solution of partial differential equations (PDEs) that arise in modeling a broad range of physical phenomena, including **fluid flow, heat transfer, porous media transport, and fluid-structure interaction**.[web:42]

## 🎯 Classical Galerkin FEM

The classical **Galerkin finite element method** discretizes the **weak (variational) form** of PDEs by projecting onto finite-dimensional approximation spaces, typically constructed from piecewise polynomial basis functions:


