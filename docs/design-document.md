# Design Document — Handheld Digital Companion

**Version:** 1.0  
**Date:** November 19, 2026  
**Status:** Concept Development / WIP

## 1. Project Overview

This project explores the design and development of a compact, circular handheld electronic device combining mechanical interaction, a small display, and interactive digital features.

The device is intended to be more than a conventional miniature screen. Its physical opening mechanism, customizable digital interface, and experimental holographic display aim to create a distinctive user experience.

The long-term vision is to build a small personal digital companion that combines functionality with playful interaction.

### Core Design Goals

- Compact and portable form factor
- Distinctive mechanical opening mechanism
- Interactive circular display
- Miniature Pepper's Ghost visual effect
- Expandable software features
- Modular hardware and enclosure design

## 2. Industrial and Mechanical Design

### 2.1 Enclosure

The current enclosure concept is circular and inspired by compact handheld objects.

| Parameter | Initial Target |
|---|---|
| Outer diameter | Approximately 65 mm |
| Thickness | Approximately 20–25 mm |
| Form factor | Circular |
| Construction | Modular enclosure |
| Final material | Undecided |

These dimensions are preliminary and may change during mechanical development.

### 2.2 Rotating Display Module

The display is mounted on a movable module capable of rotating approximately 180 degrees.

The intended behavior is:

- The display remains protected inside the enclosure when closed.
- Opening the device exposes the display.
- The mechanism should provide a controlled and satisfying physical movement.
- The display module should fit within the enclosure when closed.

A four-bar linkage mechanism is currently being explored as a possible solution.

The linkage geometry, pivot positions, clearances, and opening trajectory still require validation.

### 2.3 Folding Holographic Module

A miniature optical module is planned as part of the device's opening mechanism.

The transparent reflector should:

- Remain concealed inside the enclosure when closed.
- Rise into its operating position when the device is opened.
- Fold back into the enclosure when the device is closed.
- Be protected against scratches and mechanical damage.

A manually operated or mechanically linked hinge system may be considered during prototyping.

The initial design will prioritize a simple, single-panel reflector rather than a four-sided hologram pyramid.

## 3. Display and Optical System

### 3.1 Main Display

The current display target is a 1.28-inch circular LCD module with a resolution of 240 × 240 pixels.

The display will serve as the primary visual interface for the device.

### 3.2 Pepper's Ghost Effect

The project aims to implement a miniature Pepper's Ghost optical illusion.

This effect uses a transparent reflective surface positioned at an angle to reflect an image from the display, creating the appearance of a floating image.

Potential applications include:

- Floating digital characters
- Animated visual effects
- Music visualizations
- Mini-game elements
- Clock and status displays

This is an optical illusion rather than a true volumetric hologram.

The optical setup, reflector material, viewing angle, brightness, and enclosure geometry must be experimentally validated.

## 4. Electronics and Hardware

### 4.1 Main Controller

**Target controller:** ESP32-S3 development board.

The controller will handle:

- Display communication
- Input processing
- Digital animations
- Game logic
- Bluetooth Low Energy communication
- General device functionality

### 4.2 Planned Components

| Component | Purpose | Status |
|---|---|---|
| ESP32-S3 Mini | Main controller | Selected |
| 1.28-inch circular LCD | Visual interface | Selected |
| Rotary encoder | Navigation and interaction | Selected |
| Push buttons | Additional controls | Selected |
| Toggle switch | Power control | Selected |
| LEDs and resistors | Basic indicators | Selected |
| Rechargeable battery | Portable power | Planned |
| Buzzer | Optional sound effects | Undecided |
| Speaker | Audio playback | Not currently planned |

Exact pin assignments, power requirements, and electrical compatibility must be verified before assembly.

### 4.3 Power System

The device is intended to operate independently of a computer.

A rechargeable battery is planned for portable operation.

Battery capacity, charging circuitry, voltage regulation, and USB-C integration will be determined after measuring the hardware's power consumption.

## 5. Software and Planned Features

The software architecture should support multiple operating modes.

### 5.1 Digital Companion

A small animated character may act as the device's central identity.

Possible interactions include:

- Idle animations
- Reactions to user input
- Opening and closing animations
- Contextual animations based on the active mode

The character may also appear through the Pepper's Ghost optical system.

### 5.2 Mini Games

The device may include small games designed around its limited display and physical controls.

Potential interaction methods:

- Rotary encoder navigation
- Button-based actions
- Short, replayable gameplay sessions
- Holographic visual elements

### 5.3 Music Mode

The device is intended to function as a companion controller for music played on a connected smartphone.

Potential features:

- Display current track and artist
- Play and pause
- Previous and next track
- Volume control
- Music-reactive holographic animations

The ESP32-S3 will communicate with a companion smartphone application over BLE.

The phone application will be responsible for accessing supported media information and controlling playback through the relevant platform APIs.

Android and iOS capabilities and restrictions must be investigated separately.

Direct Bluetooth audio streaming is not part of the current design.

### 5.4 Additional Modes

Other possible modes include:

- Clock Mode
- Focus Mode
- Custom animations
- Notifications
- Additional interactive experiences

These features are exploratory and are not required for the first working prototype.

## 6. Enclosure and Manufacturing

### 6.1 Prototyping

The initial enclosure and mechanical components will be produced using external 3D printing services.

To reduce repeated printing costs, the design should be modular.

Components that may require separate production include:

- Main enclosure
- Display carrier
- Linkage components
- Reflector holder
- Hinges and mechanical connectors

Only modified components should need to be reprinted during design iterations.

### 6.2 Final Enclosure

Potential final manufacturing materials:

- ABS or PC plastic
- CNC-machined aluminum
- Other suitable engineering plastics

The final material will be selected based on durability, weight, cost, surface finish, and manufacturing complexity.

If a metal enclosure is selected, antenna placement and wireless signal performance must be considered.

## 7. Development Roadmap

### Phase 1 — Concept and Mechanical Design
- Refine the industrial design.
- Explore the 180-degree rotating mechanism.
- Investigate four-bar linkage geometry.
- Design the folding reflector mechanism.
- Establish preliminary component dimensions.

### Phase 2 — Optical Prototype
- Build a simple Pepper's Ghost experiment.
- Test reflector materials and angles.
- Evaluate image brightness and visibility.
- Validate the effect using the actual circular display.

### Phase 3 — Electronics Prototype
- Test the ESP32-S3 and LCD.
- Implement basic display output.
- Connect the rotary encoder and buttons.
- Test individual electronic components.
- Establish a stable power configuration.

### Phase 4 — Firmware and Interaction
- Develop the main interface.
- Implement character animations.
- Experiment with mini-game mechanics.
- Investigate BLE communication.
- Explore smartphone companion application requirements.

### Phase 5 — Mechanical Integration
- Integrate the display and optical modules.
- Test the complete opening and closing mechanism.
- Validate cable routing and internal component placement.
- Produce a functional enclosure prototype.

### Phase 6 — Final Design
- Refine the enclosure.
- Select final materials.
- Improve mechanical durability.
- Integrate hardware and software.
- Prepare the final device.

## 8. Open Questions and Technical Risks

The following topics require further investigation:

- Can the rotating display and folding reflector fit within the target enclosure dimensions?
- What linkage geometry provides reliable 180-degree rotation?
- Can the reflector deploy automatically during the opening movement?
- Which optical material provides sufficient brightness and image clarity?
- How should the display's flexible cable be routed through the moving mechanism?
- What battery capacity is appropriate?
- What are the practical BLE media-control limitations on Android and iOS?
- How can wireless performance be preserved if a metal enclosure is used?
- Which manufacturing method is most suitable for the final enclosure?

## 9. Current Project Scope

The first functional prototype will prioritize:

1. A working ESP32-S3 and circular display.
2. Physical input through the rotary encoder and buttons.
3. A functional rotating display mechanism.
4. An experimental folding Pepper's Ghost module.
5. Basic interactive animations.

Music control, smartphone integration, mini-games, and additional modes can be developed incrementally.

The final enclosure material and advanced features will remain flexible until the core hardware and mechanical design have been validated.

---

**Project Status:** Early concept and prototyping preparation.

**Design Philosophy:** Build a distinctive physical experience first, then expand its digital capabilities through modular hardware and software.
