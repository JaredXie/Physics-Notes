# Derivation of the Wave Equation

This note systematically outlines the derivation of the wave equation. The wave equation describes how waves propagate through a medium or a field. It can be derived from different physical models. Two classic derivation pathways are the **vibrating string model** and **electromagnetic field theory**.

## Core Result: The Standard Form of the Wave Equation

Whether we are discussing mechanical waves or electromagnetic waves, the standard wave equation is a second-order partial differential equation in both time and space:

<mark>∂²u/∂t² = v² ∇²u</mark>

In this equation, `u` represents the wave function, `v` is the wave speed, and `∇²` is the Laplacian operator.

---

## 1. Derivation from the Vibrating String Model

This is one of the most intuitive physical models. It describes transverse waves travelling along elastic objects such as strings or ropes.

### 1.1 Physical Model and Assumptions

Consider a uniform and flexible string. The string is fixed at both ends and stretched under a constant tension `T`. Its linear mass density is `μ`.

When the string undergoes small transverse vibrations, we describe its shape using the displacement function `y(x,t)`, which depends on both position `x` and time `t`.

### 1.2 Key Idea: Newton’s Second Law

We analyse a small element of the string with length `dx`.

Because the string is slightly curved, the two ends of this small element experience tensions with the same magnitude but slightly different directions. The difference between their **vertical components** provides the restoring force for the vibration.

- **Net force:**  
  Under the small vibration approximation, the net vertical force is proportional to the spatial curvature of the string. This curvature is represented by the second derivative of `y` with respect to `x`:

  `∂²y/∂x²`

- **Equation of motion:**  
  According to Newton’s second law, `F = ma`.  
  The mass of the small string element is `μdx`, and its transverse acceleration is `∂²y/∂t²`.

  Therefore:

  `T * (∂²y/∂x²) * dx = (μdx) * (∂²y/∂t²)`

- **Wave equation:**  
  Cancelling `dx` on both sides and rearranging gives the one-dimensional wave equation:

  **∂²y/∂t² = (T/μ) * ∂²y/∂x²**

### 1.3 Wave Speed

In this model, the wave speed `v` is determined by the physical properties of the string:

`v = √(T/μ)`

This means that a tighter string, with a larger tension `T`, gives a faster wave speed. A heavier string, with a larger linear density `μ`, gives a slower wave speed.

---

## 2. Derivation from Maxwell’s Equations

This is one of the most important achievements in the history of Physics. It reveals that light is an electromagnetic wave.

### 2.1 Theoretical Foundation: Maxwell’s Equations

In a vacuum and source-free region, the behaviour of electromagnetic waves is described by Maxwell’s equations:

- **Faraday’s law:**  
  A changing magnetic field produces an electric field.

  `∇ × E = - ∂B/∂t`

- **Ampère-Maxwell law:**  
  A changing electric field produces a magnetic field.

  `∇ × B = μ₀ε₀ * ∂E/∂t`

- **Gauss’s law for electricity:**  

  `∇ · E = 0`

- **Gauss’s law for magnetism:**  

  `∇ · B = 0`

Here, `μ₀` is the vacuum permeability, and `ε₀` is the vacuum permittivity.

### 2.2 Key Idea: Taking the Curl to Eliminate Variables

To obtain an equation that contains only `E` or only `B`, we apply vector calculus operations to Maxwell’s equations.

- **Take the curl of Faraday’s law:**

  `∇ × (∇ × E) = - ∂(∇ × B)/∂t`

- **Substitute the Ampère-Maxwell law:**

  Since:

  `∇ × B = μ₀ε₀ * ∂E/∂t`

  we substitute this into the right-hand side:

  `∇ × (∇ × E) = - μ₀ε₀ * ∂²E/∂t²`

- **Apply the vector identity:**

  Use the identity:

  `∇ × (∇ × E) = ∇(∇ · E) - ∇²E`

  In a vacuum, `∇ · E = 0`. Therefore, the equation becomes:

  `- ∇²E = - μ₀ε₀ * ∂²E/∂t²`

- **Obtain the electromagnetic wave equation:**

  Rearranging gives the wave equation for the electric field:

  **∂²E/∂t² = (1/μ₀ε₀) * ∇²E**

### 2.3 Wave Speed and the Nature of Light

- **Wave speed:**  
  The coefficient `1/μ₀ε₀` corresponds to the square of the wave speed.

  Therefore:

  `v = 1/√(μ₀ε₀) ≈ 3.0 × 10⁸ m/s`

  This value matches the experimentally measured speed of light.

- **Historical significance:**  
  This derivation showed that light is an electromagnetic wave. It unified optics and electromagnetism, making it a major milestone in the history of Physics.

  Similarly, by applying the same method to the magnetic field `B`, we can obtain a wave equation with the same form for the magnetic field.

---

## Summary

| Derivation Pathway | Core Physical Principle | Key Assumptions | What Determines the Wave Speed `v` | Application |
| :--- | :--- | :--- | :--- | :--- |
| **Vibrating String Model** | Newton’s second law, `F = ma` | Small vibration, uniform string, constant tension | Tension `T` and linear density `μ`, where `v = √(T/μ)` | Mechanical waves, sound waves, seismic waves |
| **Maxwell’s Equations** | Changing electric and magnetic fields generate each other | Vacuum, no free charges, no free currents | Vacuum permittivity `ε₀` and vacuum permeability `μ₀`, where `v = c` | Electromagnetic waves, light, radio waves |

These two examples show that waves can have different physical origins. However, their mathematical structure is unified through the wave equation.

In both cases, the wave equation describes a core idea: a disturbance propagates through space at a finite speed.
