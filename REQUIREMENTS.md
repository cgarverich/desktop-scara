# SCARA Robotic Arm — Project Requirements

**Project Owner:** Caleb Garverich
**Institution:** UMass Amherst — Mechanical & Industrial Engineering
**Project Period:** May 2026 – August 2026 (15 weeks)
**Last Updated:** May 18, 2026

---

## 1. Project Summary

Design, build, and demonstrate a desk-scale 4-DOF SCARA (Selective Compliance Articulated Robot Arm) capable of autonomous pick-and-place tasks. The arm will serve as both a portfolio project for robotics-industry job applications and a functional desk assistant for use during senior year.

## 2. Functional Requirements

| ID | Requirement | Notes |
|----|-------------|-------|
| FR-1 | The arm shall execute pick-and-place between any two points in its workspace | Core demo capability |
| FR-2 | The arm shall accept (x, y, z) Cartesian commands and convert them to joint angles via inverse kinematics | |
| FR-3 | The arm shall home to a known reference position on startup using limit switches | |
| FR-4 | The arm shall detect and pick up colored objects using a webcam and OpenCV | Stretch goal, Phase 5 |
| FR-5 | The arm shall be controllable from a Python script running on a laptop | Serial over USB |

## 3. Performance Specifications

| Parameter | Target Value | Justification |
|-----------|--------------|---------------|
| Payload (max) | 250 g | Shot glass, phone, small mug |
| Design payload (with 2× safety factor) | 500 g | Standard engineering practice |
| Horizontal reach | 254 mm (10 in) | Covers usable desk area |
| Link lengths | L₁ = L₂ = 125 mm | Maximum workspace dexterity |
| Vertical (Z) travel | ~80 mm | Sufficient for pick clearance |
| Repeatability target | ±1.0 mm | Demonstrable with simple tests |
| Workspace footprint | ~100 × 100 mm base | Fits on desk corner |
| Max joint speed | ~90°/s | Comfortable, non-aggressive motion |

## 4. Constraints

- **Budget:** $300–450 (tight-to-moderate)
- **Timeline:** Must be functional and demo-ready by August 31, 2026
- **Manufacturing:** 3D-printed structural parts (PETG preferred for stiffness)
- **Power:** Single 24V DC supply, ≤120 W
- **Workspace:** Must operate safely on a typical desk surface

## 5. Component Selection (Locked Specs)

- **Motors:** 4× stepper motors (NEMA 17 for joints 1–3, NEMA 14 or 17 pancake for joint 4)
- **Drivers:** 4× TMC2209 stepper drivers (silent microstepping)
- **Controller:** Teensy 4.0 microcontroller
- **Mechanical reduction:** 4:1 GT2 belt at joint 1, 3:1 GT2 belt at joint 2
- **Z-axis:** Tr8×8 lead screw + linear rail
- **End effector:** Servo-driven parallel-jaw gripper
- **Vision (Phase 5):** USB webcam + OpenCV (Python on laptop)

## 6. Skills Demonstrated (Resume Outcomes)

- Forward and inverse kinematics derivation (closed-form, 2-link planar)
- MATLAB modeling and simulation (Robotics System Toolbox)
- Motor sizing via rotational inertia analysis
- CAD design (SolidWorks) and design-for-manufacture
- Embedded motion control (C++ on Teensy)
- Trajectory planning (trapezoidal velocity profiles)
- Computer vision integration (Python + OpenCV)
- End-to-end mechatronic system integration

## 7. Success Criteria

- [ ] Arm physically built and powered
- [ ] Successful homing routine on startup
- [ ] Arm reaches commanded (x, y, z) positions within ±2 mm
- [ ] At least 15 of 20 consecutive pick-and-place trials successful (75% reliability)
- [ ] Vision-guided pick demonstrated on at least one object
- [ ] GitHub repo published with documentation, math, CAD, code
- [ ] 60–90 second demo video produced

## 8. Out of Scope

The following are explicitly excluded from this project to manage scope:

- 6-DOF or articulated (cobot-style) configurations
- Real-time obstacle avoidance
- Force/torque feedback at end effector
- Multi-arm coordination
- ROS2 integration (clean Python + Arduino architecture is sufficient)
- Industrial-grade repeatability (±0.1 mm or better)

## 9. Risks and Mitigations

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| 3D printing access falls through | Medium | High | Confirm in Week 1; backup = home printer or service |
| Motor undersized for load | Low | High | Inertia analysis done; 2× safety factor applied |
| Vision integration runs late | Medium | Low | Phase 5 is cuttable; arm with hardcoded coordinates still demos well |
| Schedule slips | Medium | Medium | Buffer week built into Week 14 |

---



Caleb Garverich — May 18, 2026
