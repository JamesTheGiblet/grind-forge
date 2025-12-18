⚙️ GrindForge: Particle Distribution Simulator

GrindForge models the physical breakdown of coffee beans into a bimodal distribution—a key characteristic of burr grinders where the output consists of a primary particle peak and a secondary peak of "fines."
🛠 Features

    Bimodal Distribution Engine: Unlike simple simulators, GrindForge uses a Box-Muller transform to generate realistic Gaussian curves for both main particles and microscopic fines.

    Thermal Friction Modeling: Calculates heat generation based on RPM and burr contact time. Excessive heat (>40°C) is modeled to degrade flavor clarity.

    Surface Area Analysis: Dynamically calculates total available surface area (in cm2), which is the primary driver for extraction speed in the next step, BrewForge.

    Procedural Particle Visualization: Animates particles falling through the burrs with visual density and color based on the selected grind size.

    Texture Mapping: Provides a visual "sand-to-pebble" texture preview to help users calibrate their mental model of grind sizes (Turkish to Cowboy).

🧪 The Science Behind the Simulation
1. Particle Geometry

The simulator treats coffee particles as irregular spheres. As the Target Size (μm) decreases, the Total Surface Area increases exponentially. This is calculated as:
Atotal​≈i=1∑n​di​K​

Where d is the diameter of particle i and K is a constant representing bean porosity derived from the RoastForge import.
2. Uniformity vs. Fines

The Uniformity % stat represents the standard deviation of the grind.

    High Uniformity: Results in "Flavor Clarity" (Clean cup).

    Low Uniformity: Increases "Flow Resistance" and body, but risks "muddiness" due to an over-abundance of fines clogging the filter.

🚀 How to Use

    Import Roast Data: Load your profile from RoastForge. Denser, lighter roasts are more brittle and produce different fine-to-boulder ratios.

    Select a Preset: Use the Quick Grind Presets to jump to industry-standard micron ranges (e.g., 250μm for Espresso).

    Tune the Burrs: Adjust RPM. High RPM grinds faster but generates more static and heat.

    Analyze the Histogram: Once the grind is complete, check the Distribution Analysis chart to see your bimodal peaks.

    Export: Generate the Brew Profile. The Surface Area Index and Flow Resistance values are specifically formatted to be ingested by BrewForge.
