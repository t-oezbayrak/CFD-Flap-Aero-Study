# CFD Study – Multi-Element Rear Wing (2D Steady RANS, k-ω SST)

## Objective

This study evaluates the aerodynamic behavior of a 3-element high-downforce rear wing configuration (Main Plane + 2 Flaps) under 2D steady RANS conditions.

The goal is to analyze pressure distribution, boundary layer behavior, slot-gap effectiveness, and separation mechanisms through iterative geometric refinement.

---

## Numerical Setup

Solver: Steady RANS  
Turbulence Model: k-ω SST (selected for separation sensitivity)  
Dimensionality: 2D  

### Boundary Conditions
- Inlet: Uniform velocity profile
- Outlet: Pressure outlet (0 Pa gauge)
- Airfoil surfaces: No-slip wall condition
- Far-field domain extended to reduce blockage effects

Note: This study focuses on qualitative aerodynamic behavior and flow physics. 
Reynolds number and aerodynamic coefficients (Cl, Cd) will be incorporated in future iterations for quantitative validation.

---

# Iteration v1 – Baseline Configuration

## Pressure Distribution

The static pressure contour demonstrates a clear distinction between:

- Pressure side (concave surface) → high static pressure  
- Suction side (convex surface) → strong negative pressure peak  

Stagnation points are visible at the leading edges of all three elements, confirming effective load transfer.

The suction peaks indicate strong circulation and high downforce generation.

However, steep adverse pressure gradients are observed toward the trailing edge of the final flap.

---

## Turbulence & Flow Separation (Kinematic Viscosity / TKE)

The turbulence field reveals localized separation near the most aggressively loaded flap.

Key Observations:

- Wake expansion behind the final element
- Increased turbulent kinetic energy in shear layer region
- Partial loss of flow attachment

Despite this, the main plane remains largely attached.

### Aerodynamic Interpretation

The configuration operates near its aerodynamic loading limit.

The slot-gap mechanism is still partially effective in re-energizing the boundary layer, allowing downstream elements to contribute to lift.

This iteration produces high downforce but with increasing induced drag.

---

# Iteration v2 – Gap & Incidence Adjustment

Modifications:
- Adjusted slot-gap geometry
- Modified element incidence angle

---

## Flow Field Analysis (TKE)

In the second iteration, separation initiates at the suction side of the main plane.

This is a critical aerodynamic failure mode in multi-element airfoils.

Once upstream separation occurs:

- Slot acceleration becomes ineffective
- Downstream flaps operate in low-momentum wake flow
- Lift contribution from secondary elements collapses
- Pressure drag increases significantly

The turbulent kinetic energy contour confirms a large separated shear layer enveloping the entire rear assembly.

---

# Root Cause Diagnosis

The main element camber/incidence combination generates an adverse pressure gradient exceeding the boundary layer momentum capacity under the given setup.

Multi-element wings rely on attached flow on the primary element.

If the main plane detaches:

- The slot no longer injects high-energy flow
- Downstream aerodynamic synergy is lost
- Overall efficiency drops sharply

---

# Engineering Strategy for Next Iteration (v3)

1. Reduce main plane incidence to ensure upstream flow attachment.
2. Re-optimize slot-gap spacing to enhance local acceleration.
3. Perform mesh refinement in shear layer regions.
4. Introduce aerodynamic coefficient extraction (Cl, Cd, L/D).
5. Validate solution sensitivity to Reynolds number.

---

# Skills Demonstrated

- 2D Steady RANS CFD setup
- k-ω SST turbulence modeling
- Multi-element airfoil interaction analysis
- Boundary layer separation diagnosis
- Iterative aerodynamic reasoning
- Physics-driven design refinement

<img width="1260" height="425" alt="Screenshot 2026-02-02 151451" src="https://github.com/user-attachments/assets/e51b3474-21c3-4fcc-96c8-69ee800ab045" />
<img width="1270" height="437" alt="Screenshot 2026-02-02 151530" src="https://github.com/user-attachments/assets/acdc9149-62c9-49bd-af67-d8d8a0fd33bc" />
<img width="1289" height="755" alt="Screenshot 2026-02-02 212143" src="https://github.com/user-attachments/assets/ea0a0eee-7577-449c-9df8-650f0f64546e" />
