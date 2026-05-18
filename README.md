# SCARA Robotic Arm

A desk-scale 4-DOF SCARA (Selective Compliance Articulated Robot Arm) for autonomous pick-and-place. Personal portfolio project, Summer 2026.

![Status](https://img.shields.io/badge/status-in_progress-yellow)
![Phase](https://img.shields.io/badge/phase-0_requirements-blue)

## Project Goal

Design, build, and demonstrate a 4-DOF SCARA arm capable of autonomous vision-guided pick-and-place, with 250 mm reach and 250 g payload, fitting on a standard desk.

## Specifications

| Parameter | Value |
|-----------|-------|
| Degrees of freedom | 4 (θ₁, θ₂, Z, θ₄) |
| Horizontal reach | 250 mm |
| Link lengths | L₁ = L₂ = 125 mm |
| Payload | 250 g (500 g design with 2× safety factor) |
| Repeatability target | ±1 mm |
| Budget | $300–450 |
| Timeline | 15 weeks (May–August 2026) |

## Skills & Tools

**Engineering domains:** kinematics, trajectory planning, motor sizing, mechatronics, control systems, computer vision

**Tools:** MATLAB (Robotics System Toolbox), SolidWorks, Python, OpenCV, Arduino/Teensy C++, GT2 belt drives, NEMA 17 steppers, TMC2209 drivers

## Repository Structure
```
desktop-scara/
├── README.md                  ← you are here
├── REQUIREMENTS.md            ← formal requirements document
├── PROJECT_NOTEBOOK.md        ← running log of decisions and progress
├── docs/                      ← writeups, math derivations, lessons learned
│   ├── kinematics.md
│   ├── motor_sizing.md
│   └── lessons_learned.md
├── matlab/                    ← Phase 1: kinematic modeling & simulation
│   ├── forward_kinematics.m
│   ├── inverse_kinematics.m
│   ├── workspace_plot.m
│   └── trajectory_sim.m
├── cad/                       ← Phase 2: SolidWorks files, STLs, BOM
│   ├── assembly.sldasm
│   ├── stl/
│   └── BOM.md
├── firmware/                  ← Phase 4: Teensy/Arduino code
│   ├── scara_control/
│   └── README.md
├── host/                      ← Phase 5: Python host + vision
│   ├── pick_and_place.py
│   ├── vision.py
│   └── requirements.txt
├── media/                     ← photos, renders, demo video
└── LICENSE
```
## Project Phases

- [x] **Phase 0** — Requirements & setup (Week 1)
- [ ] **Phase 1** — MATLAB modeling & simulation (Weeks 2–3)
- [ ] **Phase 2** — CAD & component selection (Weeks 4–5)
- [ ] **Phase 3** — Fabrication & assembly (Weeks 6–7)
- [ ] **Phase 4** — Electronics & motion control (Weeks 8–9)
- [ ] **Phase 5** — Application layer & vision (Weeks 10–11)
- [ ] **Phase 6** — Polish, documentation, demo (Weeks 12–13)

See [REQUIREMENTS.md](REQUIREMENTS.md) for the full project scope and success criteria. See [PROJECT_NOTEBOOK.md](PROJECT_NOTEBOOK.md) for the running build log.

## Progress Log

### Week 1 (May 18–24, 2026)
- Established project requirements and specs
- Motor sizing: 0.068 kg·m² shoulder inertia, 1.47 N·m design torque, 14% margin on NEMA 17 + 4:1 reduction
- Selected SCARA architecture after evaluating 3-DOF articulated alternative
- Set up GitHub repo with full documentation
- [ ] Confirm 3D printer access 
- [x] Install MATLAB with Robotics System Toolbox
- [ ] Sketch workspace on physical desk

*(Future weeks will be logged here as the project progresses.)*

## Inspiration & References

- Dejan Nedelkovski (HowToMechatronics) — SCARA build series on YouTube
- MATLAB Robotics System Toolbox documentation

## License

MIT License — see [LICENSE](LICENSE) for details.

## Contact

Caleb Garverich — UMass Amherst, Mechanical & Industrial Engineering
