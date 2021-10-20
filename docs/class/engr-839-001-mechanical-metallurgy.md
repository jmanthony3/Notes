---
title: Mechanical Metallurgy
subject: ENGR 839-001
date: 210823-2112XX
place: DH 3274
speaker: Dr. Mark Atwater
student: Joby M. Anthony III
email: jmanthony1@liberty.edu
---
<!-- output:
  pdf_document:
    latex_engine: xelatex
    includes:
      in_header: "C:/Users/jmanthony1/Documents/GitHub/JobyAnthonyIII/LaTeX/preamble.tex"
tags: 
bibliography: "biblio.bib"
link-citations: true -->
<script type="text/javascript"
        src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS_CHTML">
</script>
<script type="text/x-mathjax-config">
	MathJax.Ajax.config.path["Extra"] = "https://jmanthony3.github.io/Codes/MathJax/extensions/TeX",
	MathJax.Hub.Config({
		TeX: {
			equationNumbers: {
				autoNumber: "AMS"
			},
			extensions: [
				"[Extra]/MechanicalMetallurgy.js",
				"[Extra]/NumericalMethods.js"
			]
		},
		tex2jax: {
			inlineMath: [["$", "$"], ["\\(", "\\)"]],
			blockMath: [["$$", "$$"], ["\\[", "\\]"]],
		},
});
</script>
<!-- %%%%%%%% Document Metadata %%%%%%%% -->
# ENGR 839-001: Mechanical Metallurgy

- [ENGR 839-001: Mechanical Metallurgy](#engr-839-001-mechanical-metallurgy)
	- [Materials: Structure, Properties, and Performance](#materials-structure-properties-and-performance)
		- [Introduction](#introduction)
		- [Review](#review)
		- [Metallic Crystal Structure](#metallic-crystal-structure)
			- [Energy and Packing](#energy-and-packing)
			- [Crystalline (Periodic) Structure](#crystalline-periodic-structure)
		- [Density Comparison of Materials](#density-comparison-of-materials)
			- [Polycrystalline Materials](#polycrystalline-materials)
			- [Anistropy](#anistropy)
			- [Istropy](#istropy)
			- [Miller Indices](#miller-indices)
				- [1) Point coordinates Algorithm](#1-point-coordinates-algorithm)
				- [2) Crystallographic Directions Algorithm](#2-crystallographic-directions-algorithm)
				- [3) Crystallographic Planes Algorithm](#3-crystallographic-planes-algorithm)
			- [Crystal Structure and Deformation](#crystal-structure-and-deformation)
			- [Slip System (fcc)](#slip-system-fcc)
			- [Polycrystalline Slip](#polycrystalline-slip)
		- [Summary](#summary)
	- [Elasticity](#elasticity)
		- [Introduction](#introduction-1)
		- [Elastic](#elastic)
			- [Stress](#stress)
			- [Strain](#strain)
			- [Engineering vs True Stress](#engineering-vs-true-stress)
			- [Notation!](#notation)
			- [Strain Energy](#strain-energy)
			- [Shear/Torsion](#sheartorsion)
			- [Poisson's Ratio](#poissons-ratio)
			- [Summary](#summary-1)
		- [Elasticity: Polycrystalline Materials and Bulk Metals](#elasticity-polycrystalline-materials-and-bulk-metals)
			- [Introduction](#introduction-2)
			- [Stress Tensor Revisited](#stress-tensor-revisited)
			- [Hooke's Law Revisited](#hookes-law-revisited)
			- [Simplifications](#simplifications)
			- [#Mohrs-Circle Revisited](#mohrs-circle-revisited)
		- [#pure-shear](#pure-shear)
		- [Elasticity: Atomic Bonds](#elasticity-atomic-bonds)
			- [Introduction](#introduction-3)
			- [Atomic Bonding](#atomic-bonding)
			- [Bond Interaction and Force](#bond-interaction-and-force)
			- [Stress and Strain in Bonds](#stress-and-strain-in-bonds)
			- [Summary](#summary-2)
	- [Exam Review](#exam-review)
	- [Plasticity](#plasticity)
		- [Introduction](#introduction-4)
			- [Engineering and true stress and strain](#engineering-and-true-stress-and-strain)
			- [Work-Hardening Basics](#work-hardening-basics)
			- [Summary](#summary-3)
		- [Tensile Curve Parameters, Necking, and #strain-rate](#tensile-curve-parameters-necking-and-strain-rate)
			- [Introduction](#introduction-5)
			- [Necking](#necking)
			- [Stress-strain and Necking](#stress-strain-and-necking)
				- [Bridgman Correction](#bridgman-correction)
				- [State of Stress in Deformation](#state-of-stress-in-deformation)
			- [#strain-rate](#strain-rate)
			- [Summary](#summary-4)
		- [Compression and Hardness](#compression-and-hardness)
			- [Introduction](#introduction-6)
			- [Practical Considerations](#practical-considerations)
			- [Compression Curve](#compression-curve)
			- [Compression Failure](#compression-failure)
			- [#Bauschinger-Effect](#bauschinger-effect)
			- [Hardness Testing](#hardness-testing)
			- [Hardness-Yield Relationship](#hardness-yield-relationship)
			- [Micro-Indentation Testing](#micro-indentation-testing)
			- [Nano-Indentation Testing](#nano-indentation-testing)
		- [Summary](#summary-5)
	- [Defects](#defects)
		- [Introduction](#introduction-7)
		- [Theoretical Shear Strength](#theoretical-shear-strength)
		- [Point Defects](#point-defects)
			- [Interstitial Defects](#interstitial-defects)
				- [#fcc sites](#fcc-sites)
				- [#bcc sites](#bcc-sites)
				- [#hcp sites](#hcp-sites)
			- [Equilibrium Concentration](#equilibrium-concentration)
			- [Vacancy or Self-Interstitial?](#vacancy-or-self-interstitial)
			- [Equilibrium Concentration](#equilibrium-concentration-1)
			- [Vacancy Formation](#vacancy-formation)
			- [Effect on Mechanical Properties](#effect-on-mechanical-properties)
			- [Summary](#summary-6)
		- [Line Defects](#line-defects)
		- [Types of Dislocations](#types-of-dislocations)
			- [Edge and Screw Character](#edge-and-screw-character)
			- [dislocation-motion](#dislocation-motion)
			- [Bubble Rafts](#bubble-rafts)
			- [Dislocation Confirmation](#dislocation-confirmation)
			- [Dislocation Looping](#dislocation-looping)
			- [Prismatic Loops](#prismatic-loops)
			- [Loop Expansion](#loop-expansion)
			- [Stress Around Dislocations](#stress-around-dislocations)
			- [Stress Equations for #screw-dislocation](#stress-equations-for-screw-dislocation)
			- [Stress Equations for #edge-dislocation](#stress-equations-for-edge-dislocation)
		- [Summary](#summary-7)
		- [Imperfections: Dislocation Energy and Bowing](#imperfections-dislocation-energy-and-bowing)
			- [Energy Around A Dislocation](#energy-around-a-dislocation)
			- [Deformation Energy](#deformation-energy)
			- [Screw Versus #edge-dislocation Energy](#screw-versus-edge-dislocation-energy)
			- [Dislocation Density](#dislocation-density)
			- [Dislocation Bowing](#dislocation-bowing)
			- [Peach-Koehler Equation](#peach-koehler-equation)
		- [Partial Dislocations](#partial-dislocations)
			- [Introduction](#introduction-8)
			- [Real Dislocations](#real-dislocations)
			- [Partial Dislocations in Close-Packed Planes](#partial-dislocations-in-close-packed-planes)
			- [Visualizing fcc Partial Dislocations](#visualizing-fcc-partial-dislocations)
			- [Determining the Partial Direction and Magnitude](#determining-the-partial-direction-and-magnitude)
			- [Decomposition of $\vec{b}_{1}$](#decomposition-of-vecb_1)
			- [Partial Dislocation Energy](#partial-dislocation-energy)
			- [Stacking Faults](#stacking-faults)
			- [Sessile Dislocations](#sessile-dislocations)
			- [Lomer-Cotrell Locks](#lomer-cotrell-locks)
			- [HCP Dislocations](#hcp-dislocations)
			- [BCC Dislocations](#bcc-dislocations)
			- [Summary](#summary-8)
				- [Dislocation density, homogeneous nucleation](#dislocation-density-homogeneous-nucleation)
			- [Dislocation Sources](#dislocation-sources)
			- [Frank-Read Source](#frank-read-source)
			- [Cross-Slip and Dislocation Multiplication](#cross-slip-and-dislocation-multiplication)
			- [Dislocation Pileup](#dislocation-pileup)
			- [Summary](#summary-9)
		- [Imperfections: Dislocation Interactions](#imperfections-dislocation-interactions)
			- [Introduction](#introduction-9)
			- [Intersection of Dislocations and Forest Dislocations](#intersection-of-dislocations-and-forest-dislocations)
			- [Jogs and Kinks](#jogs-and-kinks)
			- [Effects on #dislocation-motion](#effects-on-dislocation-motion)
			- [Dislocation Looping](#dislocation-looping-1)
			- [Orowan Equation](#orowan-equation)
			- [Peirels-Nabarro Stress (Lattice Friction)](#peirels-nabarro-stress-lattice-friction)
			- [Kink Pair Nucleation](#kink-pair-nucleation)
			- [Temperature and Strain Rate](#temperature-and-strain-rate)
		- [Interfacial Defects](#interfacial-defects)
			- [Grain Boundary](#grain-boundary)
			- [Tilt Boundary](#tilt-boundary)
			- [Twist Boundary](#twist-boundary)
			- [Grain Boundary Energy](#grain-boundary-energy)
				- [Parameter A](#parameter-a)
			- [Grain Boundary Misorientation-Energy Relation](#grain-boundary-misorientation-energy-relation)
			- [Coincident Site Lattice Boundary](#coincident-site-lattice-boundary)
			- [Triple Junctions](#triple-junctions)
			- [Grain Boundary Dislocations and Ledges](#grain-boundary-dislocations-and-ledges)
			- [Summary](#summary-10)
		- [Twinning](#twinning)
			- [Crystallography](#crystallography)
			- [Difference from Slip](#difference-from-slip)
			- [Twinning and Slip](#twinning-and-slip)
			- [Effect of the c/a Ratio](#effect-of-the-ca-ratio)
			- [Mechanical Effects](#mechanical-effects)
			- [Effects of Stacking Fault Free Energy](#effects-of-stacking-fault-free-energy)
			- [Twinning and Slip Stress](#twinning-and-slip-stress)
			- [Summary](#summary-11)
		- [Grain-Size Boundaries](#grain-size-boundaries)
			- [Hall-Petch Equation](#hall-petch-equation)
			- [Theories Behind the Mechanisms](#theories-behind-the-mechanisms)
			- [Cottrell Theory](#cottrell-theory)
			- [Li Theory](#li-theory)
			- [Meyers-Ashworth](#meyers-ashworth)
			- [Summary](#summary-12)
		- [Obstacles to Deformation](#obstacles-to-deformation)
			- [Substructural Effects](#substructural-effects)
			- [Iron-Carbon System Considerations](#iron-carbon-system-considerations)
			- [Nanocrystalline Materials](#nanocrystalline-materials)
				- [Strengthening Mechanisms](#strengthening-mechanisms)
			- [Volumetric Defects](#volumetric-defects)
<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->





<!-- START WRITING BELOW -->





<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->
*Lecture: August 23, 2021*
## Materials: Structure, Properties, and Performance
### Introduction
**Objectives** The course content will enable students to set and meet expectations.
All of this material, in its content and instruction, are new: so, leave room for error.
Be inspired to tackle whatever comes our way.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/creationeering_diagram_210906_200723_EST.png) |
|:--:|
| Creationeering diagram. $\label{fig:creationeering_diagram}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/creationeering_t_diagram_210906_200841_EST.png) |
|:--:|
| Cross-shaped Liberty University Creationeer. $\label{fig:creationeering_t_diagram}$ |

**Definitions**
This class will make more familiar the "chemistry-process-structure" portion of the *chemistry-process-structure-property-performance*" (#CPSPP) relationship.
LU seeks to apply these engineering disciplines into entrepreneurship.
**Mechanical**: force response of materials, which includes the underlying principles/effects of microstructure.
**Metallurgy**: microstructural transformations dictated by composition/processing that is the foundation.
**Mechanical Metallurgy**, as a course, studies not *how* materials behave, by *why* they behave a certain way.

**Syllabus:** Homeworks due only before the relevant exams, and graded for the good ol' college try.
If you can do the homeworks, then you can do the tests.
**Final Exam is cummulative.**
Critical Review: "Reverse engineer" an article and explain it with additional comments or inferences.
The accompanying presentation should explain the takeaway from the application articles/comments.

### Review
**#CPSPP:** Relationship for how some chemical composition (e.g: FeC) is processed to produce some structure, which has some property that allows some performance.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/iron_carbon_phase_diagram_210906_201712_EST.png) |
|:--:|
| Iron-Carbon phase diagram. $\label{fig:iron_carbon_phase_diagram}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/fec_with_microstructure_210906_201830_EST.png) |
|:--:|
| Microstructures in FeC phase diagram. #phase-diagrams pack a lot of information for CPS of CPSPP sequence. Lines denote what structure is found after some process with some chemical composition. *Lever Rule*: ratio of phases proportional to weight percent distance to other phases. $\label{fig:fec_with_microstructure}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/crystallographic_types_210906_201926_EST.png) |
|:--:|
| Crystallographic examples. $\label{fig:crystallographic_types}$ |

>**Crystallographic Types:** simple cubic, face-center cubic (#fcc), body-center cubic (#bcc), hexagonal close-packed (#hcp).
The atomic packing factor, #apf, the ratio lattice that is filled, increases down this list.
 #fcc and #hcp are similar, but #hcp is more brittle.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/precipitation_hardening_210906_202124_EST.png) |
|:--:|
| Copper phase diagram. $\label{fig:precipitation_hardening}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/burgers_vector_210906_202432_EST.png) |
|:--:|
| The angle at which one stuffs at burger into his face. $\label{fig:burgers_vector}$ |

>**#burgers-vector, $\vec{b}$:** lattice displacement by a dislocation;  vector of dislocation; location, magnitude, and direction of influence on lattice.
Can weaken metals when many dislocations exist.


---


*Lecture: August 25, 2021*

| ![](../../attachments/engr-839-001-mechanical-metallurgy/thomas_tetrahedron_210906_202746_EST.png) |
|:--:|
| Pictographic way to visual CPSPP relationship according to processing techniques. $\label{fig:thomas_tetrahedron}$ |

>**#CPSPP Example:** includes low-carbon steel; high-carbon steel; and, cast iron.
All same chemistry with different composition ratios and examples of different processing techniques applied/able.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/cpspp_example_210906_202828_EST.png) |
|:--:|
| Common steels in automotive applications. $\label{fig:cpspp_example}$ |

**Monolithic** Previously explained homogeneous or isotropic, but depends on length scale.
Here, means the same crystal structure throughout: e.g. pearlite.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/pearlite_in_iron_210906_203009_EST.png) |
|:--:|
| Phase diagram for FeC with microstructure. $\label{fig:pearlite_in_iron}$ |

**Materials Design** Exposed to variety of conditions, but can be designed to suit.
More complex designs may have better performance.
Composites have "rules-of-mixtures" to balance performance.
Hierarchical materials vary structure/composition to enhance functional/structural properties at different length scales.

**Our Focus:** not on manufacturing techniques: e.g. ENGR 835.
Will consider how manufacturing variables affect structure.
We will move up length up from atomistics.

### Metallic Crystal Structure
#### Energy and Packing
| ![](../../attachments/engr-839-001-mechanical-metallurgy/nondense_interatomic_potential_curve_210906_203334_EST.png) | ![](../../attachments/engr-839-001-mechanical-metallurgy/dense_interatomic_potential_curve_210906_203436_EST.png) |
|:--:|:--:|
| Non-dense, random packing. $\label{fig:nondense_interatomic_potential_curve}$ | Dense, ordered packing. $\label{fig:dense_interatomic_potential_curve}$ |

Ordered structures tend to be nearer the minimum bonding energy and are more stable.

**Atomic Packing** Dense crystal structures for metals.
Reasons for dense packing: *1)* bonds between metal atoms are non-directional; *2)* nearest neighbor distances tend to be small in order to lower bond energy; *3)* high degree of shielding (of ion cores) provided by free electron cloud; and, *4)* crystal structures for metals simpler than structures for ceramics and polymers.

#### Crystalline (Periodic) Structure
| ![](../../attachments/engr-839-001-mechanical-metallurgy/crystalline_structure_example_210906_203659_EST.png) |
|:--:|
| Crystalline (Periodic) Structure. $\label{fig:crystalline_structure_example}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/simple_cubic_structure_210906_204211_EST.png) | 
|:--:|
| Simple Cubic (#sc) Crystal Structure: centers of atoms at corners and close packed along edges. $\label{fig:simple_cubic_structure}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgybody_centered_cubic_210906_204258_EST.png) |
|:--:|
| Body-Centered Cubic (#bcc) Structure: atoms located at 8 cube corners with a single atom at cube center. $\label{fig:body_centered_cubic}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/face_centered_cubic_210906_204511_EST.png) |
|:--:|
| Face-Centered Cubic (#fcc) Structure: atoms located at 8 cube corners with half atoms at center of 6 cube faces. $\label{fig:face_centered_cubic}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/fcc_hcp_packing_sequence_210906_204623_EST.png) |
|:--:|
| Hexagonal Close-Packed (#hcp) Structure: only B or C positions can be filled in a single layer. $\label{fig:fcc_hcp_packing_sequence}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/hexagonal_close_packed_structure_210906_204915_EST.png) |
|:--:|
| Interces in each layer can be filled only according to some pattern: "A" or "B". $\label{fig:hexagonal_close_packed_structure}$ |

**Structure**}$ | **Coor. #**}$ | **$\frac{atoms}{cell}$**}$ | **#apf**}$ | **#slip-plane**}$ | **#slip-system**
|:-:|:-:|:-:|:-:|:-:|:-:|
#sc}$ | 6}$ | 1
#bcc}$ | 8}$ | 2}$ | 0.68}$ | 3}$ | 48
#fcc}$ | 12}$ | 4}$ | 0.74}$ | 1}$ | 12
#hcp}$ | 12}$ | 6}$ | 0.74}$ | 3}$ | 12


---


*Lecture: August 27, 2021*

### Density Comparison of Materials
| ![In general, $\rho_{metals} > \rho_{ceramics} > \rho_{polymers}$](../../attachments/engr-839-001-mechanical-metallurgy/density_comparison_of_materials_210906_205030_EST.png) |
|:--:|
| $\label{fig:density_comparison_of_materials}$ |

#### Polycrystalline Materials
| ![](../../attachments/engr-839-001-mechanical-metallurgy/polycrystalline_example_210906_205257_EST.png) |
|:--:|
| Higher cooling rates at edges make for smaller grains; whereas, slower cooling rate at center make for larger, directionally aligned grains. $\label{fig:polycrystalline_example}$ |

*Most* engineering materials are composed of many, small single crystals.
Each "grain" is a single crystal.
Grain sizes typically range from 1 nm to 2 cm.
Smaller grains usually mean higher strength and lower ductility.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/unit_cell_orientation_in_polycrystal_210906_205554_EST.png) |
|:--:|
| Same crystal type that repeat in different orientations. $\label{fig:unit_cell_orientation_in_polycrystal}$ |

#### Anistropy
| ![](../../attachments/engr-839-001-mechanical-metallurgy/anistropy_example_210906_205851_EST.png) |
|:--:|
| Unit cell of #bcc ($\alpha$) iron. $\label{fig:anistropy_example}$ |

#anistropy: A property value that depends on crystallographic direction of measurement.
Properties depend on direction loading, because of linear density along that direction.
Best observed in single crystals.
The higher linear density means higher stiffness, usually.

#### Istropy

| ![](../../attachments/engr-839-001-mechanical-metallurgy/isotropy_comparisons_210907_132012_EST.png) |
|:--:|
| Randomly oriented versus textured grains. $\label{fig:isotropy_comparisons}$ |

**Polycrystals:** properties may (not) vary with direction.
If grains randomly oriented, properties are #isotropic: independent of loading direction.
If grains, "textured"--crystallographic orientation--properties are #anistropic: dependent on loading direction.

#### Miller Indices
A method of assigning coordinate values to crystallographic lattice sites.
Used to identify specific points, directions, and planes or families of these.
Used to identify crystallographic information.
Three ways to identify:

##### 1) Point coordinates Algorithm

>**NOTE** A lattice position with a unit cell and determined as fractional multiples of unit cell edge lengths.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/point_coordinates_example_210907_132404_EST.png) | ![](../../attachments/engr-839-001-mechanical-metallurgy/point_coordinate_example_with_annotations_210907_132446_EST.png) |
|:--:|:--:|
| Determined as fractional multiples of unit cell edge lengths. $\label{fig:point_coordinates_example}$ | $\label{fig:point_coordinate_example_with_annotations}$ |

1. Lattice position is a, b, c.
2. Divide by unit cell edge lengths and remove commas: $\frac{a}{a}\frac{b}{b}\frac{c}{c} = 111$

##### 2) Crystallographic Directions Algorithm

| ![](../../attachments/engr-839-001-mechanical-metallurgy/crystallographic_example_210907_132620_EST.png) |
|:--:|
| $\label{fig:crystallographic_example}$ |

>**NOTE** Remember from calculus the $tip - tail$ method to find vector direction and length.

1. Determine coordinates of vector head and tail: $(x_{2}, y_{2}, z_{2})$ and $(x_{1}, y_{1}, z_{1})$, respectively.
2. Subtract tail coordinates from head coordinates.
3. Normalize this subtraction by lattice parameters of unit cell edge length: $\frac{x_{2} - x_{1}}{a}\frac{y_{2} - y_{1}}{b}\frac{z_{2} - z_{1}}{c}$.
4. Multiply to smallest integer values.
5. Enclose in square brackets with no commas: `[uvw]`.

>**NOTE** Negative indices represented with overbars: $-4, 1, 2 \implies [\bar{4}12]$
A *#family-of-directions* are crystallographically equivalent (same atomic spacing) and indicated by angle brackets, `<>`.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/common_cystallographic_directions_210907_133812_EST.png) |
|:--:|
| Common crystallographic directions. $\label{fig:common_cystallographic_directions}$ |

##### 3) Crystallographic Planes Algorithm
1. If plane passes through origin, establish a new origin in another unit cell.
2. Read off values of intercepts of plane (designated $A, B, C$) with $x, y, z$ axes in terms of $a, b, c$.
3. Take reciprocals of intercepts.
4. Normalize reciprocals by multiplying lattice parameters $a, b, c$.
5. Reduce to smallest integer values.
6. Enclose resulting indices in parentheses without commas: i.e. `(hkl)`.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/crystallographic_planes_example_1_210907_134442_EST.png) |
|:--:|
| Resulting Miller Indices: (110). $\label{fig:crystallographic_planes_example_1}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/crystallographic_planes_example_2_210907_134534_EST.png) |
|:--:|
| Resulting Miller Indices: (200). $\label{fig:crystallographic_planes_example_2}$ |

>**NOTE** A #family-of-planes cannot be reduced any simpler than LCM. Family may be parallel to other families and planar densities may be equivalent, but linear density will vary.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/plane_families_210907_135038_EST.png) |
|:--:|
| Pay attention to origin! $\label{fig:plane_families}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/crystallographic_plane_example_3_210907_135200_EST.png) |
|:--:|
| Resulting Miller Indices: (634). $\label{fig:crystallographic_plane_example_3}$ |

>**NOTE** A *#family-of-planes* are crystallographically equivalent (same #apf) and are indicated by indices in braces, `{}`.

---


*Lecture: August 30, 2021*

>**EXAMPLE** For #hcp, determine intercepts with $a_{1}, a_{2}$ and $z$ axes, then determine the Miller-Bravais indices $h, k, i, l$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/crystallographic_planes_example_4_210907_140554_EST.png) |
|:--:|
| Resulting Miller Indices: $(10\bar{1}1)$. $\label{fig:crystallographic_planes_example_4}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/dk_question_of_hcp_projection_210907_142839_EST.png) |
|:--:|
| Projections are parallel to edge. $\label{fig:dk_question_of_hcp_projection}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/planar_density_example_210830_184426_EST.png) |
|:--:|
| *Planar Density (#PD) of Atoms*, $PD = \frac{\#~of~atoms~centered~on~plane}{area~of~plane}$. $\label{fig:planar_density_example}$ |

#### Crystal Structure and Deformation
Planar density determine #slip-plane: the more dense, the easier to move.
Unit cell represents single crystal, but the behavior of that structure is not equivalent in all directions.
Permanently deforming materials requires that atoms must shift over one another: *#slip-plane*.
Closely packed (high #apf) do not have to move as much to get by one another.
Not all #slip-directions...
 #fcc materials are generally ductile, because of few #slip-system and one  #slip-plane.
Not many preferred directions to slip and few preferred: e.g. 48 spoons to cut a steak does not equal cutting with a knife.
More of a bad thing does not outweigh few good things.
Coordination number is the number of nearest neighboring atoms.

#### Slip System (fcc)

| ![](../../attachments/engr-839-001-mechanical-metallurgy/fcc_slip_system_210830_184833_EST.png) |
|:--:|
| $\label{fig:fcc_slip_system}$ |

**Slip system is ${111}<110>$**
 #dislocation-motion on ${111}$ planes.
 #dislocation-motion in $<110>$ directions.
12 independent #slip-system for #fcc.


| ![](../../attachments/engr-839-001-mechanical-metallurgy/visual_example_of_slip_210830_184900_EST.png) |
|:--:|
| More force over more distance = more work to move #bcc than #fcc, which requires less distance because closely packed (dense). $\label{fig:visual_example_of_slip}$ |

#### Polycrystalline Slip
Many grains, often with random crystallographic directions.
Orientation of #slip-plane and #slip-directions, $(\phi, \lambda)$ vary from grain to grain.
On application of stress, slip in each grain on most favorable slip system.
With largest $T_{R}$.
When $T_{R} > T_{crss}$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/example_of_polycrystal_slip_210830_185242_EST.png) |
|:--:|
| $\label{fig:example_of_polycrystal_slip}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/impact_deformed_monel_210907_142431_EST.png) |
|:--:|
| Edge of indent shows texture from #slip-plane from moving atoms out of the way of impact. Accumulates with amount of deformation applied. $\label{fig:impact_deformed_monel}$ |

### Summary
Important to have common understanding of vocabulary to describe crystal structure. We focus on *#bcc*, *#fcc*, and *#hcp* structures.
Miller indices give exact orientation or active atoms/planes to determine the associated properties.
The #apf is import to density and #slip-system, but it is not the only critical property.


---


*Lecture: September 01, 2021*

## Elasticity
### Introduction
Stresses occur at varying scales within a material.
Macro-stresses include component design and assemblage.
Micro-stresses are found within the material and include those from defects: dislocations, alloying elements. etcetera.
Stresses at smallest scale act cumulatively to produce the response to the largest scale.
This all relates to the **#CPSPP** relationship.

### Elastic
- Reverse deformation, that instantaneously recovers to its original dimensions after force is removed.
- Analogous to a spring, the relationship was conveniently described by Robert Hooke: $F = k\delta x$

#### Stress
- Stress is the result of applied force and response of material to balance external force.
	- Area resisting force is perpendicular to applied force line of action.
	- Material response is determined by atomic bonds and orientation relative to crystal lattice.
	- >**NOTE** Polycrystalline materials assumed #anisotropic.
	- Component response dictated by design and material properties.
	- Tensile stress often positive in sign and compression is negative, by convention.

#### Strain
- Physical result of stress.
- Linear proportional to stress in Hookean material up to its elastic limit/yield stress.
- >**NOTE** #proportional-limit is that when the stress-strain deviates from linear and yield stress is at the 0.02% strain offset.
- Metals often Hookean in nature and assumed until otherwise stated.
- True strain: $\begin{equation}\epsilon = \frac{dl}{l}, \epsilon = \int_{l_{0}}^{l_{1}}\frac{dl}{l} = ln(\frac{l_{1}}{l_{0}})\label{
true_strain}\end{equation}$
- Engineering strain: $\begin{equation}\epsilon = \frac{\delta l}{l}\label{eq:engineering_strain}\end{equation}$

#### Engineering vs True Stress
- Comes from initial conditions and easily measured.
- >**NOTE** Area does not change, so the initial area determines the stress throughout the entire deformation.
- True stress and strain are more accurate and use an instantaneous cross-section.
- In the elastic region for metals, deformation is typically small and engineering and true stress-strain values are comparable.
- $\sigma_{T} = \sigma(1 + \epsilon)$
- $\epsilon_{T} = ln(1 + \epsilon)$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_strain_curve_210907_144454_EST.png) |
|:--:|
| $\label{fig:stress_strain_curve}$ |

#### Notation!
Notation is not always the same.

$$\begin{equation}
\begin{bmatrix}
\sigma_{xx}, \tau_{xy}, \tau_{xz} \\\\
\tau_{yx}, \sigma_{yy}, \tau_{yz} \\\\
\tau_{zx}, \tau_{zy}, \sigma_{zz}
\end{bmatrix}\begin{bmatrix}
(x) \\\\
(y) \\\\
(z)
\end{bmatrix}\equiv\begin{bmatrix}
\sigma_{11}, \tau_{12}, \tau_{13} \\\\
\tau_{21}, \sigma_{22}, \tau_{23} \\\\
\tau_{31}, \tau_{32}, \sigma_{33}
\end{bmatrix}\begin{bmatrix}
(1) \\\\
(2) \\\\
(3)
\end{bmatrix}
\label{eq:tensor_notation}
\end{equation}$$


| ![](../../attachments/engr-839-001-mechanical-metallurgy/tensor_notation_210907_145720_EST.png) |
|:--:|
| $\label{fig:tensor_notation}$ |

#### Strain Energy
- Work done during deformation is converted to heat and internal energy.
- $W = Fd$, but $F$ is not constant!
- Elastic deformation does not typically produce much heat, so most is stored internally.
- $dU = dQ - dQ$
- $U = W$ (without heat)
- $W = \frac{1}{2}\sigma_{ij}\epsilon_{ij} = \frac{1}{2}E\epsilon_{ij}^{2} = \frac{1}{2E}\sigma_{ij}^{2}$

#### Shear/Torsion
- Shear and torsional stress are handled similarly, but vary by configuration.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/shear_stress_example_210907_150449_EST.png) |
|:--:|
| For a cylindrical punch, the average diameter of the punch and hole can be taken, and the area will be the circumference times the thickness of the material. $\label{fig:shear_stress_example}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/torsional_stress_example_210907_150530_EST.png) |
|:--:|
| For torsion of a rod, the stress and strain vary radially and axially. $\label{fig:torsional_stress_example}$ |

- $\tau = \frac{F}{A}$
- $\gamma = \frac{dl}{l} = tan\theta \cong \theta$
- $G = \frac{\tau}{\gamma}$

**Q&A** Why does $\gamma \cong \theta$?
Small angle assumptions in radians mean that $sin\theta = \theta$.

#### Poisson's Ratio
$$\begin{equation}
\nu = -\frac{\epsilon_{11}}{\epsilon_{33}} = -\frac{\epsilon_{22}}{\epsilon_{33}}
\label{eq:poisson_ratio}
\end{equation}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/poisson_ratio_210907_151239_EST.png) |
|:--:|
| $\label{fig:poisson_ratio}$ |

- Describes the consequent strains orthogonal to an applied stress.
- Most metals are 0.3.
- For constant volume without lateral contraction, the ratio is 0.5 (plastic only).

#### Summary
- Elasticity affects everything, because it is initial response to stress.
- Material behavior in elastic region dictates behavior in application.
- Components rarely useful in plastic region, so they will spend their lifetime in the elastic range.
- Although elastic properties are commonly discussed at a continuum scale, we will find it important to atomic scale phenomena.



---


*Lecture: September 03, 2021*

### Elasticity: Polycrystalline Materials and Bulk Metals
#### Introduction
- Stress may be applied in any arrangement, and we can determine the overall conditions of strain.
- This is often reduced to two dimensions, but it does not have to be (it is just simpler).
- We can determine the state of stress as a point in any orientation (not just aligned with the applied stress) by using transformation techniques.
- Certain orientations will result in only normal or shear stresses, which can be important for determining the resulting performance.

#### Stress Tensor Revisited

| ![](../../attachments/engr-839-001-mechanical-metallurgy/cauchy_stress_tensor_210907_152153_EST.png) |
|:--:|
| $\label{fig:cauchy_stress_tensor}$ |

- Cuachy stress tensor describes the complete state of stress in three dimensions.
- Valid for small deformations (Eq. \eqref{eq:tensor_notation}).

#### Hooke's Law Revisited
- Linear elastic response in homogeneous metals and alloys which allows us to relate stress and strain in three dimensions through the #poisson-ratio, $\nu$ \eqref{eq:poisson_ratio}.

$$\begin{split}
\epsilon_{11} &= \frac{1}{E}[\sigma_{11} - \nu(\sigma_{22} + \sigma_{33})] \\\\
\epsilon_{22} &= \frac{1}{E}[\sigma_{22} - \nu(\sigma_{11} + \sigma_{33})] \\\\
\epsilon_{33} &= \frac{1}{E}[\sigma_{33} - \nu(\sigma_{11} + \sigma_{22})] \\\\
\gamma_{12} &= \frac{\sigma_{12}}{G} \\\\
\gamma_{13} &= \frac{\sigma_{13}}{G} \\\\
\gamma_{23} &= \frac{\sigma_{23}}{G}
\end{split}$$

>**Example 1:** For the following stress tensor, what are the resulting normal strains if $E = 10e3 kip$ and $\nu = 0.3$?
$\sigma = \begin{bmatrix}5, 3, 2 \\\\ 3, -1, 0 \\\\ 2, 0, 4\end{bmatrix}kip$
$$\epsilon_{normal} = \begin{bmatrix}\frac{1}{10e3 ksi}[5 ksi - 0.3(-1 + 4)]ksi \\\\ \frac{1}{10e3 ksi}[1 ksi - 0.3(5 + 4)]ksi \\\\ \frac{1}{10e3 ksi}[4 ksi - 0.3(5 + (-1))]ksi\end{bmatrix}ksi = \begin{bmatrix}4.1e-4 \\\\ -3.7e-6 \\\\ 2.8e-6\end{bmatrix}$$

#### Simplifications
- To avoid complex tridimensional description of stress and strain, especially during plastic deformation, simplifications are possible.

#plane-stress
: strain and strain go to zero at free surface (normal and shear).

#plane-strain
: one dimension is considered infinite.

- Conditions of #pure-shear can also be considered, such that no normal forces are present.

$$\begin{bmatrix}
\sigma_{xx}, \tau_{xy} \\\\
\tau_{yx}, \sigma_{yy}
\end{bmatrix}\begin{bmatrix}
(x) \\\\
(y)
\end{bmatrix}$$

$$\begin{bmatrix}
\epsilon_{xx}, \gamma_{xy} \\\\
\gamma_{yx}, \epsilon_{yy}
\end{bmatrix}\begin{bmatrix}
(x) \\\\
(y)
\end{bmatrix}$$

#### #Mohrs-Circle Revisited
- A graphical way to represent stress transformation to alternative orientations.
- These are set of equations that describe stress transformation, but a graphical solution is often useful.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_illustration_210907_153956_EST.png) |
|:--:|
| $\label{fig:mohrs_circle_illustration}$ |

- Principal stress: maximum/minimum normal stresses (no shear)

| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_transformation_equation_illustration_210907_154859_EST.png) |
|:--:|
| $\label{fig:mohrs_circle_transformation_equation_illustration}$ |

- $R = \sqrt{(\frac{\sigma_{11} + \sigma_{22}}{2})^{2} + \tau_{12}^{2}}$
- $\sigma_{11}' = \frac{\sigma_{11} + \sigma_{22}}{2} + \frac{\sigma_{11} - \sigma_{22}}{2}cos(2\theta) + \sigma_{12}sin(2\theta)$
- $\sigma_{12}' = -\frac{\sigma_{11} - \sigma_{22}}{2}sin(2\theta) + \sigma_{12}cos(2\theta)$

>**Example 1:** What is the stress state if rotated $30\text{\textdegree}$ CCW?
| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_problem_1_210907_155042_EST.png) |
|:--:|
| $\label{fig:mohrs_circle_example_problem_1}$ |
*Given: $\sigma_{11} = -8 ksi, \sigma_{22} = 12 ksi, \sigma_{12} = -6 ksi$*
Center point, $C = \sigma_{avg} = \frac{\sigma_{11} + \sigma_{22}}{2} = \frac{-8 + 12}{2} = 2 ksi$
| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_problem_step_t_find_r_210907_155511_EST.png) |
|:--:|
| $\label{fig:mohrs_circle_example_1_problem_step_t_find_r}$ |
$R = \sqrt{10^{2} + 6^{2}} = 11.66$
| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_cricle_example_1_problem_step_to_find_angle_210907_155632_EST.png) |
|:--:|
| $\label{fig:mohrs_cricle_example_1_problem_step_to_find_angle}$ |
Use trig to find $\phi$ and $\psi$: $\phi = tan^{-1}(\frac{6}{10}) = 30.96\text{\textdegree}, \psi = 60 - \phi = 29.04\text{\textdegree}$
$\sigma_{11}' = 2 - 11.66cos(29.04) = -8.2 ksi$
$\sigma_{12}' = -11.66sin(29.04) = 5.66 ksi$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_complete_210907_160049_EST.png) |
|:--:|
| Slight drop increase of normal stress and slight decrease of shear stress. $\label{fig:mohrs_circle_example_1_complete}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_complete_clean_210908_192355_EST.png) |
|:--:|
| Basic steps to find all stresses and strains at orientations relative to what you start with. $\label{fig:mohrs_circle_example_1_clean}$ |


---


*Lecture: September 06, 2021*

### #pure-shear
There exists a condition which has only shear stresses and no normal stress. This condition is called *#pure-shear*, which means that $\sigma_{11} = -\sigma_{22}$. This implies that #Mohrs-Circle is centered at the origin, because $\sigma_{avg} = 0$. Graphically, the maximum shear stress possible in this condition is the radius of #Mohrs-Circle and at $90\text{\textdegree}$ from the horizontal. However, recall that angles in #Mohrs-Circle are twice real angles: e.g. if $\theta_{Mohr} = 2*\theta_{real}$ and $\theta_{Mohr} = \text{\textdegree}90$, then $\theta_{real} = 45\text{\textdegree}$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/pure_shear_depicted_210908_193214_EST.png) |
|:--:|
| If a component experiences compression in one axis and tension in a perpendicular axis, then elements within the component experience #pure-shear. $\label{fig:pure_shear_depicted}$ |

Using knowledge of this condition, we can find stress and strain information with the following relations:

$$\begin{split}
\epsilon_{11} &= \frac{1}{E}(\sigma_{1} - \nu\sigma_{2}) = \frac{\sigma_{1}}{E}(1 + \nu) \\\\
\tau &= -\sigma_{1} (on~circle,~with~sign~convention) \\\\
\tau &= G\gamma \\\\
\epsilon_{11} &= -\frac{G\gamma}{E}(1 + \nu) \\\\
2\epsilon_{11} &= -\gamma \\\\
G &= \frac{E}{2}(1 + \nu)
\end{split}$$

"(on circle, with sign convention)" holds true because the radius, $R$ of #Mohrs-Circle is $\sigma_{1} = - \sigma_{1}$. Some of these relationships are not limited to #pure-shear, because $E, G \text{and} \nu$ are material properties.

Expressing three-dimensional stress is important, but can be achieved with tensor notation.
Analysis of stress states can be reduced from three to two dimensions if assuming #plane-stress (zero stress in third axis) or #plane-strain (zero strain in third axis).
This simplified analysis can be transformed to desired stress states by equations or #Mohrs-Circle.
Recall that #Mohrs-Circle is a graphical representation of all possible stress states, but it must be drawn accurately that trigonometric functions might be used effectively.

### Elasticity: Atomic Bonds
#### Introduction
What preceded was continuum elasticity.
What follows is observing the previously explored behaviors at the atomistic level.
These behaviors determine the way force, stress, and strain occur.
Characterizing these behaviors informs the results of bond strength in materials: we focus on metals.
There exist competing behaviors of attraction and repulsion.

Continuum looks and homogeneous units wherein stress states are described without knowing the exact material makeup.
Here, we can continue to ignore anisotropic conditions, but must observe the source of elasticity: atomic bonds.
Strength of bonds determined by electronic characteristics, but can be influenced by external conditions: heat, magnetic fields, etcetera.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/electronic_bonds_simplified_210908_195046_EST.png) |
|:--:|
| We assume only planar, uniaxial attractions. $\label{fig:electronic_bonds_simplified}$ |

#### Atomic Bonding
Electronic bonds govern behavior of all material properties. All mechanical behavior first exhibits elastic behavior.
These effects can be observed with a simple spring model between two atoms.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/simple_spring_model_210908_195302_EST.png) |
|:--:|
| Simplified spring model to visually show attractive and repulsive forces of electronic bonds between atoms. $\label{fig:simple_spring_model}$ |

#### Bond Interaction and Force
Two atoms will have an equilibrium separation, $r_{0}$. We assume this until some external influence is applied.
The minimum bonding energy also occurs here. Repulsion is caused by the *#Pauli-Exclusion-Principle* and attraction is *#Coulombic-forces* in nature.

$$\begin{equation}
	U_{i} = -\frac{A}{r^{m}} + \frac{B}{R^{n}}
	\label{eq:bonding_energy}
\begin{equation}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/interaction_energy_and_force_210908_195751_EST.png) |
|:--:|
| Electronic bonding occurs according to these two curves between any two atoms. $\label{fig:interaction_energy_and_force}$ |

>**Example**
Potential energy of $Na^{+}Cl^{-}$, an ionic pair, at distance $r$ where $q_{0} = 1.6e-19~[C]$, $\epsilon_{0} = 8.85e-12~[\frac{C}{N-m^{2}}]$, and $U_{i} = 1.12~[eV]$. If $r_{0} = 0.276~[nm]$, then find: **a)** the value of B; and **b)** the total, attractive, and repulsive forces at $r = 0.25 [nm]$.
$$\begin{split}
U_{i} &= -\frac{A}{r^{m}} + \frac{B}{r^{n}} \\\\
U &= U_{i} - \frac{q^{2}}{4\pi\epsilon_{0}r} + \frac{B}{r^{9}}
\end{split}$$
Because $\frac{dU}{dr} = 0$ at $r_{0}$,
$$\begin{split}
\frac{dU}{dr} &= 0 = \frac{q^{2}}{4\pi\epsilon_{0}r^{2}} - \frac{9B}{r_{0}^{10}} \\\\
\frac{q^{2}}{4\pi\epsilon_{0}r^{2}} &= \frac{9B}{r_{0}^{10}} \\\\
\implies B &= \frac{r_{0}^{8}q^{2}}{36\pi\epsilon_{0}}
\end{split} \\\\
\begin{split}
B &= 8.61e-106 [N-m^{10}]
\end{split}$$
$B$, then, is simply plugged into the following equations to find electronic bond forces at not the equilibrium distance, $r = 0.25 [nm]$.
$$\begin{split}
F &= \frac{dU}{dr} = F_{A} - F_{R} \\\\
F &= \frac{q^{2}}{4\pi\epsilon_{0}r^{2}} - \frac{9B}{r_{0}^{10}}
\end{split} \\\\
\begin{split}
F_{A} &= \frac{q^{2}}{4\pi\epsilon_{0}r^{2}} = 3.68e-4 [N] \\\\
F_{B} &= \frac{9B}{r_{0}^{10}} = -8.13e-9 [N] \\\\
\implies F &= 4.44e-9 [N]
\end{split}$$

#### Stress and Strain in Bonds
Force is proportional to atomic displacement and change in energy.
Stress requires number of atoms involved in some area by estimating atomic spacing at equilibrium, $r_{0}^{2}$.
Strain, then, is the change in spacing divided by the equilibrium spacing.
#Youngs-modulus is a material property of stress over strain. These can be summarized by the following relations:

$$\begin{split}
F &= \frac{dU_{i}}{dr} \\\\
d\sigma &= NdF \\\\
d\sigma &= \frac{dF}{r_{0}^{2}} \\\\
d\epsilon &= \frac{dr}{r_{0}} \\\\
E &= \frac{Am(n-m)}{r_{0}^{m + 3}} \\\\
A &= \frac{q^{2}}{4\pi\epsilon_{0}} \\\\
E &= \frac{kq^{2}}{r_{0}^{4}}
\end{split}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/outcomes_of_bonding_210908_203140_EST.png) |
|:--:|
| Stronger bonding can effect melting point, stiffness, etcetera. Understanding these effects informs how higher length scales behave under some condition. $\label{fig:outcomes_of_bonding}$ |

#### Summary
Bulk properties come from atomic bonds.
Treatment of elasticity at atomic scale determines balances of attractive and repulsive forces; therefore, external forces cause a shift from the equilibrium state.
Bond properties can be adjusted to preference with some processing technique: e.g. alloying.


---


*Lecture: September 09, 2021*

## Exam Review
**Miller Indices**
When drawing Miller indices--coordinates, vectors, and planes--keep to Fig. @fig-milled_index_axis convention.
This makes grading quicker, because a different orientation is not necessarily wrong but are harder to grade.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/axes_for_milled_indices_210908_182057_EST.png) |
|:--:|
| Keep cubes with z-vertical and #hcp with c-vertical. $\label{fig:milled_index_axis}$ |

#apf will be used in the exam (per the provided table from earlier lectures). **The content of the homework is the template for the exam: no new content on exams.** WRT to calculating unit cell mass, follow this algorithm example for iron (Fe):

$$\begin{split}
\rho &= \frac{nA}{V_{c}N_{A}}
\end{split} \\\\
\begin{split}
\rho_{Fe} &= (55 amu) (\frac{g}{mol}/1 amu) / (N_{A}) \\\\
\rho_{Fe} &= 3.053e-22 g/atom \\\\
\rho_{Fe, {\#bcc}} &= \rho_{Fe}*2/a_{0}^{3}
\end{split}$$

**Tensorial vs. Engineering Strain**

| ![](../../attachments/engr-839-001-mechanical-metallurgy/engineering_vs_tensor_strains_210908_183912_EST.png) |
|:--:|
| Engineering strain keeps deformation in one axis. Actual strain is half that, but in two axes. $\label{fig:engineer_vs_tensor_strain}$ |

Because we know the relation, $\epsilon_{ij} = \frac{\gamma_{ij}}{2}$, we know $G = \frac{\tau}{\gamma} = \frac{E}{2(1 + \nu)}$.
We can then know the deformation on some axis: e.g. $\gamma_{12} = \frac{\sigma_{12}}{G} = -37.1e-6$.
But tensor notation for shear strain, $\gamma_{shear} = \frac{\gamma_{calc}}{2}$.

**Calculating Strains from Poisson's Ratio**
Because the compression test is performed in a single axis to squish some specimen, the other lateral strains can be calculated by assuming #plane-stress: zero stress in the direction normal to the thinnest dimension.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/plane_stress_example_210908_185050_EST.png) |
|:--:|
| $\label{fig:plane_stress_example}$ |

#pure-shear occurs when $\sigma_{22} = -\sigma_{11}$. The shear stress, $\tau$ is the radius of #Mohrs-Circle.
The principal stress are the maximum and minimum of #Mohrs-Circle.
A stress tensor is the sum of the #hydrostatic-stress and #deviatoric-stress tensors: $[\sigma] = [\sigma_{hydro}] + [\sigma_{dev}]$
 #hydrostatic-stress, $\sigma_{hydro} = \frac{\sigma_{11} + \sigma_{22} + \sigma_{33}}{3}$ goes on the diagonal of the tensor and will cause a change volume, but not the object's shape.
 #deviatoric-stress: (elements not on the diagonal) will change an object's shape, but not its volume.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/pure_shear_state_example_210908_185227_EST.png) |
|:--:|
| Remember that maximum shear on #Mohrs-Circle, at $90\text{\textdegree}$, is twice the angle in real space: i.e. #pure-shear occurs $45\text{\textdegree}$ of the actual part. $\label{fig:pure_shear}$ |


---


*Lecture: September 13, 2021*

## Plasticity
### Introduction
Plasticity is sometimes involved with engineering design.
It may also prove integral to performance.
This chapter explores the importance the stress-strain behavior and the effects thereof.

Materials always follow elastic to plastic deformation before ultimate failure.
Most applications will operate within the elastic region (ceramics with narrow elastic regimes), but accommodations for work-hardening may be considered.
Not all materials work-harden the same way.
Two yield points in materials: *first yield* is the elastic limit, and *ultimate strength* is ultimate plasticity.
**Plasticity** is imperative for processing and performance of materials.
>*Think of Dr. Atwater's lawn mower!*

**Mechanical Testing** Determines mechanical properties for materials: such as various tension or compression.
Tension is the most popular, but all give same information: *stress-strain* curve.

#### Engineering and true stress and strain
Recall that #engineering-stress is from $A_{0}$ and #true-stress uses $A_{i}$.
*Plastic deformation is volume conservative*, which allows calculating #true-stress and #true-strain from the engineering values.
Stress-strain curves relates initial conditions to overall performance.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_strain_curve_comparisons_true_to_engineering_210913_183110_EST.png) |
|:--:|
| True stress-strain gives more accurate understanding of stress states, but can be more difficult to interpret. $\label{fig:stress_strain_curve_comparisons_true_to_engineering}$ |

**Q&A**
**DK: Is conversion from engineering to true stress-strain meaningful with necking?** *It depends. We will discuss this later.*

#### Work-Hardening Basics
*#Ludwik-Hollomann* equations: $\sigma = \sigma_{0} + K\epsilon^{n} \label{eq:ludwik_hollomann}$.
$\sigma_{0}$ is the yield stress, $K$ is experimentally found ($\frac{G}{100}-\frac{G}{1000}$); $\epsilon$ is true strain; and, $n$ is some work hardening coefficient (0.2-0.5).

>**Example** Use the *#Ludwik-Hollomann* equation (Eq. \eqref{eq:ludwik_hollomann}) to determine work hardening exponent, $n$ in an alloy of true strain at 0.1 and true stress = 415 MPa. Assume $K = 1035 MPa$ and $\sigma_{0} = 0$.
$$\begin{split}
\sigma &= \sigma_{0} + K\epsilon^{n} \\\\
log[\sigma &= \sigma_{0} + K\epsilon^{n}] \\\\
log(\sigma) &= log(K) + n*log(\epsilon) \\\\
\frac{log(\sigma) - log(K)}{log(\epsilon)} &= n
\end{split} \\\\
\begin{split}
\implies n &= \frac{log(415) - log(1035)}{log(0.1)} \\\\
n &\approx 0.397
\end{split}$$
*The greater, $n$, the more work-hardening can occur.*

**Refined Methods**
*L=H* has limits; therefore, *Voce* equations adds asymmetry.
*#Johnson-Cook* expands with strain-rate and temperature dependence: $\sigma = (\sigma_{0} + K\epsilon^{n})\bigl(1 + C*ln(\frac{\dot{\epsilon}}{\dot{\epsilon_{0}}})\bigr)\bigg[1 - \bigl(\frac{T - T_{r}}{T_{m} - T_{r}}\bigr)^{m}\bigg] \label{eq:johnson_cook}$.
Each term in the *#Johnson-Cook* equation represents a different failure mechanism.

**Volume Conservation**
Volume is assumed to be constant through deformation; however, volume is not always assumed constant in the elastic region.
*#poisson-ratio*, $\nu$ is constant in the elastic region, but varies in the plastic region.
True and engineering stress-strains considered equivalent up to elastic limit.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_strain_jog_210913_185442_EST.png) |
|:--:|
| Steels have upper and lower yield limits to break dislocations apart. $\label{fig:stress_strain_jog}$ |

#### Summary
Plasticity introduces new requirements to calculate stress and strain.
Elastic portion considered inconsequential and plastic deformation is volume constant.


---


*Lecture: September 15, 2021*

### Tensile Curve Parameters, Necking, and #strain-rate
Features of the stress-strain curve indicate when necking occurs, and give insight when correction factors apply: only when cylindrical samples neck.
New equations for material behavior after necking.
Strain-rate affects material response as well.

#### Introduction
Tensile testing is the most basic form to determine material properties.
Parameters of test affect outcome: temperature, etcetera.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/tensile_curve_features_210915_192748_EST.png) |
|:--:|
| *A:* $0.2\%$ strain offset yield stress. *B:* #upper-yield. *C:* #lower-yield. *D:* #proportional-limit. *D`:* #ultimate-tensile-strength (UTS). *E:* #rupture-stress. *F:* non-uniform plastic strain limit. *G:* #rupture-strain (strain to failure). *H:* lower yield region. The area under the elastic region is the *#modulus-of-resilience* and *#toughness* is area under entire curve. $\label{fig:tensile_curve_features}$ |

The more dislocations/impurities, the more local stresses exist, and more global force is required to overcome the sum of the internal stress: this is true for plain carbon steels.

**Items of Note**
Yielding is preceded by *micro-yielding*, where  #dislocation-motion can occur below traditional yield stress.
Upper-lower yield behavior is largely seen in plain, low-carbon steels.
Vacancy and dislocation pinning resist initial yielding.
#strain-rate will modify the tensile curve and can obscure the upper-lower yield phenomenon when present.

#### Necking
Occurs when localized deformation begins to dominate the strain: *void nucleation, coalescence, and growth*.
This is also known as *#plastic-instability* and is defined by **#Considere-Criterion**: increase in stress relative to strain (work-hardening) reaching a maximum in the engineering stress-strain curve.
*The higher the strain exponent, the more strain you get out of the material.*
Using this criterion, substituting true stress-strain into the derivative and apply Eq. \eqref{eq:ludwik_hollomann}, you get the relationship $\epsilon_{u} = n$, where $\epsilon_{n}$ is maximum, uniform plastic strain.

Work-hardening exponent from *engineering* stress-strain curve.
Work-hardening decreases during increase of plastic strain until that point at which necking occurs.
A metal unable to work-harden immediately reaches the point of necking after yielding, which is consistent with equations.

*Work-softening*
: the more it deforms, the easier it can be deformed (not necessarily from reduced area)--is possible under extreme conditions.
>**Think of void nucleation, coalescence, and growth!**

#### Stress-strain and Necking
After necking, instantaneous cross-sectional area must be continuously determined.
Neck acts as a "second", miniature tensile specimen, so it's strain-rate is higher from shorter length.
Irregular geometry of neck also introduces triaxial flow stress.
Magnitude of transverse stresses depends on sample and neck geometry and strain-rate.

##### Bridgman Correction
This only applies to *cylindrical* samples, because sample area and neck radius must be known.

$$\begin{equation}
\sigma = \frac{\sigma_{avg}}{(1 + 2\frac{R}{r_{n}})ln(1 + \frac{r_{n}}{2R})}
\label{eq:bridgmann_correction}
\end{equation}$$

$R$ is radius of curvature of the neck, and $r_{n}$ is the cross-sectional radius at thinnest part of neck.
The further away from necking (higher strains), this correction factor increases.

##### State of Stress in Deformation
Necking is onset of failure in a non-uniform fashion.
Applies only to tensile testing, because compression samples *barrel*.
Necking can be suppressed to achieve higher strains in more complex stress states.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/wire_drawing_example_210915_193440_EST.png) |
|:--:|
| Wire drawing shows ability to achieve 7.4 true strain of copper. $\label{fig:wire_drawing_example}$ |

#### #strain-rate
Increasing strain-rate work-hardens faster: **void nucleation controls**!!
This parameter is part of stress-#strain-rate relationship: $\sigma = K\dot{\epsilon}^{m}$.
$m$ can be found from a jump test between two strain-rates using the #Ludwik-Hollomann equation: $m = \frac{ln(\frac{\sigma_{2}}{\sigma_{1}})}{ln(\frac{\dot{\epsilon_{2}}}{\dot{\epsilon_{1}}})}$.

**Strain-rate In Practice**
Strain-rate can vary from $10^{-6}s^{-1}$ to $10^{6}s^{-1}$.
Tensile tests usually within $10^{-4}s^{-1}$ to $10^{-1}s^{-1}$.
High strain-rate (Hoppy bar) and creep or stress relaxation tests invaluable to determine material behavior under extreme conditions.
Creep and stress relaxation tests incorporate higher temperatures, which is important to material performance.

Strain-rate affects material behavior.
Increasing strain-rate often increases yield stress and the work-hardening rate.
Typically, $0.02<m<0.2$ for $0-0.9T_{H}$.

**Super-plastic Behavior**
Effective strain-rate in necking area increases.
Positive strain-rate sensitivity implies an increased stress and the yield point will shift to the weaker section.
Same concept that assists in distributing strain across tensile specimen length in work-hardening.

#### Summary
Stress-strain curve contains much information, but not all can be known from only the engineering curve.
Necking changes specimen geometry, which affects test results.
Stress states may control onset and progression of necking, which may allow for much higher strains before failure.
Strain-rate affects material response and is dependent on processing and performance applications.


---


*Lecture: September 17, 2021*

### Compression and Hardness
#### Introduction
Many applications use compressive stresses; therefore, testing for compression is more relevant.
Some materials perform well under compression and not tension.
Simpler and more cost-effective to perform compression tests; therefore, metal alloy research heavily utilizes this method.

#### Practical Considerations
Compression is simple but requires care to ensure good data.
Plate alignment and sample parallelism and flatness are imperative.
Lubricant between plates and sample reduce barreling.
*Plates should be much harder than the sample.*
Machine compliance must be removed from measured stress-strain curve, especially at lower strains.
Can also measure strain from video recordings and point markers on sample.

#### Compression Curve
Stress-strain opposite from tensile curve.
Barreling is source of non-uniform plastic strain.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/compression_stress_strain_curve_with_barreling_210917_184501_EST.png) |
|:--:|
| True stress-strain moves the curve down and to the right from the engineering stress-strain curve, which is opposite that seen for tension testing. $\label{fig:compression_stress_strain_curve_with_barreling}$ |

Effects of barreling most pronounced at strains exceeding 0.4; therefore, compression testing usually limited to less than that.
Friction is very important when initial $\frac{height}{diameter}$ is reduced: if too tall and thin, the specimen will buckle first.

#### Compression Failure
If perfectly striked, stress state greatly varies through specimen.
Although extreme, ductility allows for stress-strain behavior off the central axis.
Non-uniform stress occurs, then, across top and bottom surfaces (friction hill).

$$\begin{equation}
p = \sigma_{0}\exp(\frac{2\mu(a - r)}{h})
\label{eq:friction_hill_pressure}
\end{equation}$$

$\mu$ is coefficient of friction, $r$ is distance from center, $a$ is radius of sample, and $h$ is height of sample.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/compression_failure_friction_hill_210917_185143_EST.png) |
|:--:|
| Friction hill seen at top and bottom surfaces of sample when barreling. $\label{fig:compression_failure_friction_hill}$ |

>**Example** If $\frac{height}{diameter} = 2$, then what is $p_{max}$?
$$\begin{split}
\frac{l}{d} 	&= 2 \\
p 	&= \sigma_{0}\exp(\frac{2\mu(a - r)}{h})
\end{split} \\
\begin{split}
p &= \sigma_{0}\exp(2(0.15)(\frac{a}{h})), \frac{d}{h} = \frac{1}{2}(\frac{\frac{a}{2}}{h}) = \frac{1}{2} \longrightarrow \frac{a}{h} = \frac{1}{4} \\
\implies p 	&= \sigma_{0}\exp(2(0.15)(\frac{1}{4})) \\
&= \sigma_{0}\exp(\frac{0.3}{4})
\end{split}$$

#### #Bauschinger-Effect
If you pull something in tension, then switch to compression, the yield point will lower from tension to compression.
The strain in the material from tension weakens the material and causes a lower yield point: the *#Bauschinger-Effect*.

#### Hardness Testing
**Hardness is a material's resistance to plastic flow by indentation.**
Scale of indentation varies with load, which is standardized with the indenter while its displacement is measured.

**Brinell**
Uses a hard sphere of known dimension and known force to measure the size of indent.
Amount of applied force changes size of indention.

$$\begin{equation}
HB = \frac{P}{\pi Dh} = \frac{2P}{\pi D(D - \sqrt{D^{2} - d^{2}})}
\label{eq:brinell_hardness_number}
\end{equation}$$

$$\begin{equation}
HB_{Meyer} = \frac{4P}{\pi d^{2}}
\label{eq:meyer_hardness_number}
\end{equation}$$

**Rockwell**
Testing is simple, provides direct, arbitrary hardness reading, but relatable to known values.
Useful on a wide range of materials.
*Testing Process:*
- Apply pre-load.
- Apply indentation load.
- Remove "major" load from specific indenter and load.
- Measure depth read on scale: 0-100.

Indenter geometry will determine scale: A, B, or C.
*Rockwell-C* is best for harder steels and metals of similar properties.
Superficial scales for thin samples with lower loads to avoid anvil effects.

**Vickers**
Also known as *Diamond Pyramid*, because indenter is pyramid with $136\text{\textdegree}$, which is based on $d_{Brinell} = 0.375D$ relationship.
Can be used on any material.
Indentation size measured by average length across diagonals.
Hardness computed by...

$$\begin{equation}
HV = \frac{2Psin(\frac{\alpha}{2})}{d^{2}}
\label{eq:vickers_hardness}
\end{equation}$$

#### Hardness-Yield Relationship
For Vickers hardness, measured value...

#### Micro-Indentation Testing
Creates indent that 10's of microns in size.

> Vickers is macro- and micro-indent test method: wherein, anything below $200g$ force is considered micro-testing.

Allows testing of small features: particles or areas of grain.
Ability to probe microscale features limited if larger scale features dominate material.

$$\begin{equation}
KHN = \frac{14.228}{L}
\label{eq:knoop_hardness}
\end{equation}$$

#### Nano-Indentation Testing
Highly sensitive force-displacement device, which allows for general microstructural investigation at lowest length scales.
Examine small volume of material with *Berkovich* indenter.

$$\begin{equation}
H = \frac{P_{max}}{A}
\label{eq:berkovich_hardness}
\end{equation}$$

### Summary
Compression testing is opposite tension.
Equations of true stress-strain are same, but have different effects.
Hardness provides simple means...

## Defects
### Introduction
Crystal structure assumes perfect patterns.

### Theoretical Shear Strength
If we consider material failure when a crystal fails, then we must shift the nearest neighbors of all atoms on a  #slip-plane simultaneously.
Each bond must be stretched and broken together, each of which has an associated unit of energy.
According to #Frenkel, for two rows of atoms, shear stress follows a sinusoidal shear stress behavior that atoms in equilibrium, $a_{min}$ and metastable equilibrium, $a_{max}$.

**#fcc Strength**
Crystal structure...

### Point Defects
Affects a single lattice site.
Can be a:
- #vacancy: missing atom.
- #interstitial/self-interstitial: an extra atom between lattice sites.
- #substitutional: different atom in regular lattice.

 #vacancies introduce stress fields but are critical to diffusion processes.
In compounds, #vacancies introduce other non-equilibrium conditions: e.g. charge imbalance.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/point_defect_examples_210920_185341_EST.png) |
|:--:|
| $\label{fig:point_defect_examples}$ |

#### Interstitial Defects
Position of #interstitial defects vary by crystal structure.
##### #fcc sites
##### #bcc sites
##### #hcp sites
#### Equilibrium Concentration
 #vacancies and self- #interstitial are thermodynamically favorable.
No work is done creating a point defect, so some heat is required.
Configurational entropy is increased by defect formation but goes to 0 at $0 K$.
Concentration determined by: $$\frac{n}{N} = \exp(-\frac{G_{f}}{kT}), k = 8.62e-5\frac{eV}{K} tag{eq:equilibrium_concentration} \label{eq:equilibrium_concentration}$$

>**Example** Find equilibrium concentration of vacancies at $1000\text{\textdegree} C$ for Cu, where $G_{f} = 0.9 \frac{eV}{atom}$, $A_{Cu} = 63.5 \frac{g}{mol}$, and $\rho_{Cu} = 8.4 \frac{g}{cm^{3}}$.

$$\begin{split}
\frac{n}{N} &= e^{-\frac{G_{f}}{kT}}, N = \frac{N_{A}\rho}{A_{Cu}} = 7.97e28 \\
\implies n &= Ne^{-\frac{G_{f}}{kT}} \\
&= 7.97e28e^{-\frac{0.9}{8.62e-5(1273)}} \\
&= 2.2e25[\frac{1}{m^{3}}]
\end{split}$$

#### Vacancy or Self-Interstitial?
Either a #vacancy or self- #interstitial can be formed thermodynamically, but not equal in likelihood or concentration.
Formation energies related by $\frac{G_{i}}{G_{v}}$, but concentrations require calculation: $$\frac{X_{v}}{X_{i}} \approx \exp(\frac{G_{i} - G_{v}}{kT})$$

#### Equilibrium Concentration
 #vacancies

#### Vacancy Formation
High #vacancy concentration occurs at elevated temperatures and rapidly quenched.
Retaining #vacancies requires no significant sources of sinks to absorb them: grain boundaries, surface area, dislocation, etcetera...
Cold working increases defect concentration, as opposite sign dislocation combine to form rows of #vacancies or #interstitials.
*#Climb* is  #dislocation-motion not on a #glide-plane but at elevated temperatures.

#### Effect on Mechanical Properties
Point defects not created in isolation by deformation, but high concentration can be made by irradiation.
High-energy bombardments displace atoms to cause self- #interstitials, which produces #vacancies.
Single crystal strength increases orders of magnitude when #vacancies are quenched.
Plastic deformation

#### Summary
Point defects exist in all crystals, but concentration is affected by processing and temperature.
Self-#interstitials can be increased with plastic strain, which produces other types of defects.
High concentrations of defects...

### Line Defects
| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_caterpillar_210922_184101_EST.png) |
|:--:|
|  #dislocation-motion through material sometimes thought as pushing a kink through a rug, or a caterpillar crawling. $\label{fig:dislocation_caterpillar}$ |

### Types of Dislocations
Basic understanding of dislocation results in two options:
1. #edge-dislocations
2. #screw-dislocations

| ![](../../attachments/engr-839-001-mechanical-metallurgy/edge_dislocation_example_210922_184402_EST.png) | ![](../../attachments/engr-839-001-mechanical-metallurgy/screw_dislocation_example_210922_184423_EST.png) |
|:--:|:--:|
| Often thought as extra "half-plane" of atoms: the ** #burgers-vector**. $\label{fig:edge_dislocation_example}$ | Helical interruptions of the crystal lattice. $\label{fig:screw_dislocation_example}$ |

Continuous variations can exist in a material between these two types of dislocations.

#### Edge and Screw Character
If #burgers-vector, $\vec{b}$ is perpendicular to dislocation line, $l$, then it is an #edge-dislocation.
If #burgers-vector, $\vec{b}$ is parallel to dislocation line, $l$, then it is a #screw-dislocation.
i.e. dislocation character = $\begin{cases}
\vec{b} \perp l,~edge \\
\vec{b} \parallel l,~screw
\end{cases}$
Mixed dislocations are combinations of these.

#### dislocation-motion
Edge and #screw-dislocations achieve the same thing in various ways.
#dislocation-motion along #slip-plane is called #glide.
#dislocation-motion perpendicular to #slip-plane is called #climb.
Transfer of dislocation from one #slip-plane to another is called #cross-slip.
Immobile dislocations are called #sessile, while mobile ones are called #glissile.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_motion_types_210924_182051_EST.png) |
|:--:|
| Visualizing how dislocations move is not as important as knowing the equations. $\label{fig:dislocation_motion_types}$ |

#### Bubble Rafts
Dislocations were considered many years before experimentally validated.
| ![](../../attachments/engr-839-001-mechanical-metallurgy/bubble_raft_example_210922_190135_EST.png) |
|:--:|
| One means $\label{fig:bubble_raft_example}$ |

| [![](https://img.youtube.com/vi/UEB39-jlmdw/0.jpg)](https://www.youtube.com/watch?v=UEB39-jlmdw "Link Title")}$ |
|:--:|
| *Video* Experiments with the bubble model of metal structure 1952 - sir lawrence bragg}$ |


---


*Lecture: September 24, 2021*
#### Dislocation Confirmation
#TEM microscope sends electrons to interact with the medium of material that the interaction might be viewed. Variety of characterization techniques reveal their presence, which causes #crystal-lattice distortions. For seeing #dislocation-motion #glide watch EXbiEopDJ_g

#### Dislocation Looping
Dislocations forms loops with both edge and #screw-dislocation pairs of opposite signs. Positive edge: $\perp$; negative edge: $\top$; positive screw: $S$; negative screw; &#423;.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_looping_examples_210924_182512_EST.png) |
|:--:|
| Loops are not square in reality, because it is more energetically favorable to be elliptical. $\label{fig:dislocation_looping_examples}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_loop_example_210924_182723_EST.png) |
|:--:|
| Under shear, loop expands to all edges, which then produces the shear $\label{fig:dislocation_loop_example}$ |

#### Prismatic Loops
#Prismatic-Loops occur when extra disc of atoms are inserted to the #crystal-structures (or removed), and not #glissile like a "common" loop.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/prismatic_loop_example_210924_182844_EST.png) |
|:--:|
| bar $\label{fig:prismatic_loop_example}$ |

#### Loop Expansion
| ![](../../attachments/engr-839-001-mechanical-metallurgy/loop_expansion_example_210924_182957_EST.png) |
|:--:|
| Common dislocation loops have no incompatibility between dislocation moving in loop plane. Dislocation character allows expansion in each direction until loop eventually creates a unit step in the #crystal-structures. $\label{fig:loop_expansion_example}$ |

#### Stress Around Dislocations
Defects introduce stress/strains due to imperfect lattice spacing. If continuum understanding for infinite, straight line is assumed, then calculation is greatly simplified, and a cylinder is sufficient to portray the concept.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_around_dislocations_210924_183159_EST.png) |
|:--:|
| A hollow center is assumed to avoid infinite stress, and it is appropriate since real are not continuous but periodic. $\label{fig:stress_around_dislocations}$ |

#### Stress Equations for #screw-dislocation
Relating stress and strain through #Hookes-Law. $\sigma_{11} = \sigma_{22} = \sigma_{33} = \tau_{12} = \tau_{21} = 0$. $$\begin{split}\tau_{13} = \tau_{31} &= -\frac{Gbx_{2}}{2\pi(x_{1}^{2} + x_{2}^{2})} \\\\ \tau_{23} = \tau_{32} &= \frac{Gbx_{1}}{2\pi(x_{1}^{2} + x_{2}^{2})}\end{split} \label{eq:screw_dislocation_stress}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/screw_dislocation_stress_example_210924_183609_EST.png) |
|:--:|
| Dislocation motion increments by 1 #burgers-vector. $\label{fig:screw_dislocation_stress_example}$ |

#### Stress Equations for #edge-dislocation
| ![](../../attachments/engr-839-001-mechanical-metallurgy/edge_dislocation_stress_equation_example_210924_183746_EST.png) |
|:--:|
| $$\begin{split}\end{split}$$ $\label{fig:edge_dislocation_stress_equation_example}$ |

### Summary
Dislocations are critical to understanding macroscale deformation and strengthening mechanisms. Dislocations can interact to form loops, which result in same shear on crystal as a dislocation passes through, as long as loop is not prismatic. All of this discussion is for plastic deformation.
*Critical Review Topic is due October 15. Be thinking of a topic related to this material, which also correlates to your own research.*

### Imperfections: Dislocation Energy and Bowing
Quantify energy around dislocations and determines relationships...Take the energy at each dislocation and determine how difficult to move that dislocation. This correlates to #dislocation-energy and #dislocation-density, etcetera. Dislocations act like a line, fixed in space and is allowed to bow out: like blowing a bubble.
Dislocations are never alone. Their relation determines their #dislocation-energy. For some number of dislocation, #volumetric-density can be found. Idealized #dislocation-energy applies to a straight dislocation.

#### Energy Around A Dislocation
Each dislocation exhibits elastic deformation energy around it in three dimensions. Those energy distributions vary with orientation and type (normal vs. shear stress).

#### Deformation Energy
Elastic deformation related to magnitude of area displacement under a straight line (ideally). Stress-strain relationship according to #Hookes-Law. Displacement dictated by #burgers-vector. Displacement in-plane relates to distance from dislocation core: $\approx 5b$.

$$\begin{split}
U &= \frac{1}{2}\sigma_{ij}\epsilon_{ij} \\
	&= \frac{1}{2G}\bigl[\bigr] \\
\end{split}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/foo_210924_184805_EST.png) |
|:--:|
| bar $\label{fig:foo}$ |

#### Screw Versus #edge-dislocation Energy
Equations for stress around dislocation vary between screw and edge. Energy of #screw-dislocation is $\approx\frac{2}{3}$ the #edge-dislocation energy. $U\longrightarrow \infty~as~R\longrightarrow\infty$, but $R$ is average distance between dislocations.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/foo_210924_184816_EST.png) |
|:--:|
| bar $\label{fig:foo}$ |

#### Dislocation Density
Unit area and volume considered to determine #dislocation-density and interaction. The area/volume considered bounded by straight dislocations. From these densities, $R \approx \frac{1}{\sqrt{\rho_dsl}}$. Orientation matters! $$\alpha = \begin{cases}\frac{\pi}{2}, edge \\ 0, screw\end{cases}$$. Energy of core$\dots$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_radius_of_influence_example_1_210924_185225_EST.png) | ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_radius_of_influence_example_cube_210924_185432_EST.png) |
|:--:|:--:|
| Think of these as the "Internet *influencers*" of metals. Dislocations are counted in 4 squares; therefore, only 1 total dislocation: $\rho = \frac{1}{4R^{2}}$. $\label{fig:dislocation_radius_of_influence_example_1}$ | Each side of the cube is a dislocation line: $\rho = \frac{3}{4R^{3}} \implies R \approx \rho^{-\frac{1}{2}}$. $\label{fig:dislocation_radius_of_influence_example_cube}$ |

If these above examples are not helpful, just think of the equations.

#### Dislocation Bowing
| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_bowing_picture_210924_185854_EST.png) |
|:--:|
| $F_{1}$ is the force to retain shape, and $F_{2}$ is the applied load to cause bowing. $\label{fig:dislocation_bowing_picture}$ |

Dislocations are not straight in practice, but understanding deformation is crucial to other factors: e.g. propogation. Dislocations can be thought to resist bowing by line tension, which is a function of unit length. Remember #small-angle-assumption: $sin(\theta) = \theta,~sin(\frac{d\theta}{2}) = \frac{d\theta}{2}$

#### Peach-Koehler Equation
The #Peach-Koehler-Equation converts force to stress. Considering a unit cube with a dislocation on $x_{1}$ moving some distance in $x_{2}$ in cube height of $x_{3}$. To get the work done, $F$, the force (per unit length) must be multiplied by length $x_{1}$ and distance $x_{2}$. Strain energy equal to work $\dots$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/foo_210924_190114_EST.png) |
|:--:|
| bar $\label{fig:foo}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/peach_koehler_equation_example_210924_190358_EST.png) |
|:--:|
| The book has a typo and actually refers to Eq. 4.22b! $\label{fig:peach_koehler_equation_example}$ |


---


*Lecture: September 27, 2021*
### Partial Dislocations
#### Introduction
Dislocations are not as simple as traditional imagery. There exist import energy considerations.

#### Real Dislocations
Traditional representation of #dislocation-motion is simple, 2D cubic structure where movement of dislocation restores perfect crystal: $\mathbf{b} = a$ in $[100]$. Real crystals, especially #fcc, a dislocation may change the structure and is considered a partial/imperfect dislocation. To move from one dislocation to the next, atoms do not necessarily travel over each other, but between each other, to minimize work-energy of motion.

#### Partial Dislocations in Close-Packed Planes
| ![](../../attachments/engr-839-001-mechanical-metallurgy/real_dislocation_in_close_packed_plane_example_210927_182553_EST.png) |
|:--:|
| Easier for atoms to move along $(111)$ in grooves between atomic positions, not over top. This requires two movements to restore original stacking pattern. $\label{fig:real_dislocation_in_close_packed_plane_example}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/real_dislocation_in_close_packed_plane_example_move1_210927_182640_EST.png) |
|:--:|
| bar $\label{fig:real_dislocation_in_close_packed_plane_example_move1}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/real_dislocation_in_close_packed_plane_example_move2_210927_182710_EST.png) |
|:--:|
| bar $\label{fig:real_dislocation_in_close_packed_plane_example_move2}$ |

Overall motion of one #burgers-vector, $\vec{b}$.

#### Visualizing fcc Partial Dislocations
| ![](../../attachments/engr-839-001-mechanical-metallurgy/visualizing_fcc_partial_dislocations_210927_182927_EST.png) |
|:--:|
| Translation of $\vec{b}_{1} = 2R$. The direction, $\vec{b}_{1} = [\bar{1}10]$, which, in vector notation, is $\vec{b}_{1} = a(i + i + 0k)$. $\|\vec{b}_{1}\| = 2R = \frac{a}{\sqrt{2}} = \frac{a}{2}[\bar{1}10] = \frac{1}{2}[\bar{1}10]$ $\label{fig:visualizing_fcc_partial_dislocations}$ |

$\vec{b}_{2}$ and $\vec{b}_{3}$ will be in same plane for energetically favorable motion.

>**Q&A**
Do partial dislocations stop forming in some metals?
One partial can shift an row of atoms over; therefore, this changes the stacking pattern, which may be corrected later.

#### Determining the Partial Direction and Magnitude
| ![](../../attachments/engr-839-001-mechanical-metallurgy/partial_dislocation_direction_magnitude_example_210927_184728_EST.png) |
|:--:|
| Moving from one interstitial site to the next. $\label{fig:partial_dislocation_direction_magnitude_example}$ |

#### Decomposition of $\vec{b}_{1}$
| ![](../../attachments/engr-839-001-mechanical-metallurgy/decomposition_of_burgers_vector_210927_184821_EST.png) |
|:--:|
| #burgers-vector, $\vec{b}_{1}$ is mathematically equivalent to addition of two partial dislocations, $\vec{b}_{2}$ and $\vec{b}_{3}$. The scalar product should be zero in a single plane where $[111] \perp (111)$. $\label{fig:decomposition_of_burgers_vector}$ |


#### Partial Dislocation Energy
| ![](../../attachments/engr-839-001-mechanical-metallurgy/partial_dislocation_energy_example_210927_185247_EST.png) |
|:--:|
| Because $\vec{b}$ is lower $\dots$ $\tag{fig:partial_dislocation_energy_example} \label{fig:partial_dislocation_energy_example}$ |

#### Stacking Faults
Two partial dislocations repel one another, but the change in stacking sequence causes an increase in energy. Spacing of the partials, $d$ is determined by this energy balance. The #stacking-fault-free-energy (#SFE) is strongly affected by composition, with alloys having a lower SFE than pure metals. Low #SFE metals will be dominated by #stacking-faults with fewer dislocation cells or tangles. $\dots$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stacking_fault_examples_210927_185540_EST.png) |
|:--:|
| Upper-right is a tangle of dislocation faults. Lower-right (plaid) is different stacking patterns in the stacking faults. $\tag{fig:stacking_fault_examples} \label{fig:stacking_fault_examples}$ |

#### Sessile Dislocations
Energetically favorable to have dislocations. Addition or subtraction of plane of material causes an immobile #stacking-fault, which is not energetically favorable. Removal of layer in *intrinsic*

#### Lomer-Cotrell Locks
| ![](../../attachments/engr-839-001-mechanical-metallurgy/lomer_cotrell_lock_example_210927_185940_EST.png) |
|:--:|
| Two #glissile dislocations may interact and produce a #sessile dislocation if they start on intersecting planes. *Think of a headlock.* $\tag{fig:lomer_cotrell_lock_example} \label{fig:lomer_cotrell_lock_example}$ |

#### HCP Dislocations
Close-packed plane is #basal-plane, which form *intrinsic* #stacking-faults. #basal-plane is preferred plane$\dots$

#### BCC Dislocations
Not usually energetically favorable, so rarely seen.
| ![](../../attachments/engr-839-001-mechanical-metallurgy/bcc_dislocation_example_210927_190203_EST.png) |
|:--:|
| All share same #slip-plane. $\tag{fig:bcc_dislocation_example} \label{fig:bcc_dislocation_example}$ |

#### Summary
Lowest energy portion is preferable mechanism for #dislocation-motion$\dots$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/problem_4_28_solution_210927_190345_EST.png) |
|:--:|
| To determine which is energetically favorable, simply plug-n-chug. $\|\vec{b}\| = \sqrt{b^{2}}$ $\tag{fig:problem_4_28_solution} \label{fig:problem_4_28_solution}$ |


---


*Lecture: September 29, 2021*
##### Dislocation density, homogeneous nucleation
An annealed, polycrystalline metal may have a dislocation density of about $10^{7}cm^{-2}$, but after only 10% strain, the density increases three orders of magnitude. Intuitively, dislocations should be annihilated upon gliding on a free surface. Simplest way dislocations could be produced is through direst shear resulting in two dislocations of opposite signs forming, but the stress to do so is comparable to the theoretical strength (all bonds at once) and is therefore unlikely to contribute in a meaningful way. Dislocations sometimes get stuck and bogged down.

#### Dislocation Sources
Stress concentrations and higher energy are potential sources for dislocations to be formed. Grain boundaries, the irregular steps a ledges of the atoms along them act as dislocation sources: considered important to early dislocation emission at the early stages of deformation. Stress concentrations exist here. Free surfaces, with similarities to internal surface work similarly, but are not dominate in polycrystalline materials. Discontinuities in structures which nucleate dislocations. Precipitates or other phase discontinuities can also assist in dislocation emission.

#### Frank-Read Source
Dislocations can become immobilized by other dislocations or cross-slipped segments. With increasing stress, the pinned segment will bow out: recall that dislocations are defined as having a unit length energy or line tension. After sufficient stress, the dislocation bows out so far that the opposing segment ends meet and reconnect because of the their opposite signs. *Think of the lollipop in the balloon.*

| ![](../../attachments/engr-839-001-mechanical-metallurgy/frank_read_source_example_210929_183507_EST.png) |
|:--:|
| The semi-circle is the highest energy state, but if you can overcome that, then a #Frank-Read-Source is activated and dislocations are nucleated. $\tag{fig:frank_read_source_example} \label{fig:frank_read_source_example}$ |

The radius of curvature reaches minimum when equal to one-half the length of the straight line segment (unbowed or spacing between pinned points), which is semi-circular. The #Peach-Koehler-Equation applies here, with the value of $R$ being spacing of pinned points. **Formed dislocations create a back stress.** #Frank-Read-Source are not common in real experiment.

#### Cross-Slip and Dislocation Multiplication
Standard #Frank-Read-Source is unlikely route for dislocation multiplication. Many complicated interactions between dislocations in 3D, which create nodes and similar behavior. A #screw-dislocation may #cross-slip to a parallel plane, thereby pinning the segment in #Frank-Read-Source fashion. Dislocation may also be generated at interfaces with differing lattice parameters.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_multiplication_210929_184221_EST.png) |
|:--:|
| Epitaxy includes other phase boundaries. $\tag{fig:dislocation_multiplication} \label{fig:dislocation_multiplication}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/cross_slip_summary_210929_184436_EST.png) |
|:--:|
| #burgers-vector in same direction as #edge-dislocation and perpendicular as #screw-dislocation. The #edge-dislocation tries to move the #glide-plane out-of-plane to another #glide-plane. The #screw-dislocation allows the #glide-plane to move in-plane and #cross-slip. $\tag{fig:cross_slip_summary} \label{fig:cross_slip_summary}$ |

#### Dislocation Pileup
#dislocation-pileup
: Any boundary/barrier to #dislocation-motion during #glide.

Force on any dislocation in pileup can be determined from its position in the pileup (think of Black Friday shoppers squeezing to get in line for a sale). Stress increases on the lead dislocation. Collective response of pileup may be thought of as a "#super-dislocation", which can #cross-slip or cross grain boundaries.

$$\begin{equation}
\tau b = \sum_{j = 0, i \neq j}^{n}\frac{Gb^{2}}{2\pi(1 - \nu)(x_{i} - x_{j})
\label{eq:dislocation_pileup}
\end{equation}$$

where, $\tau_{lead~dsl}^{\star} = n\tau$ and $L_{length~of~pileup} = \frac{nGb}{\pi\tau}$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_pileup_example_210929_190339_EST.png) |
|:--:|
| bar $\tag{fig:dislocation_pileup_example} \label{fig:dislocation_pileup_example}$ |

#### Summary
Extensive dislocation occurs when dislocation are continuously produced within crystal.


---


*Lecture: October 1, 2021*
This will be the last lecture for this topic. Today will be more conceptual with only a few equations.

### Imperfections: Dislocation Interactions
We purpose to look at the various length scales to understand how dislocations are formed, how they interact, and what that means. We move to dislocations from plasticity, which is #dislocation-motion. We will also look at the #ductile-brittle-transition-temperature.

#### Introduction
Deformation introduces increasing #dislocation-density. If dislocations immediately pass through crystal, #dislocation-density would never increase and plasticity would not occur. There is a limit to their interactions: pinning, bowing, etcetera. Then fracture occurs at this limit, because the atoms can no longer move around. Failure can also occur if the dislocations cannot move faster than the strain-rate allows.

#### Intersection of Dislocations and Forest Dislocations
#dislocation-motion by 1 #burgers-vector, but that motion introduces a #kink or #jog in the lattice structure. This creates a section of dislocations with varying behavior.

#### Jogs and Kinks

#jog
: Shifted segment of "tree" transfers to another #slip-plane.

#kink
: Shifted segment of "tree" stays in same plane.

Created the same way, but the only difference is to which #slip-plane a dislocation moves to.

>**Example** A #kink dislocation forest at a #screw-dislocation moves all the trees the same, plane direction: #burgers-vector. #jog when moving to another plane. Every piece of the tree has the same #burgers-vector.
| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_forest_in_edge_dislocation_211001_183900_EST.png) | ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_forest_in_screw_dislocation_211001_183548_EST.png) |
|:--:|:--:|
| #edge-dislocation moves parallel to #burgers-vector. $\tag{fig:dislocation_forest_in_edge_dislocation} \label{fig:dislocation_forest_in_edge_dislocation}$ | [burgers-vector for #screw-dislocation in line of dislocation (#right-hand-rule) $\tag{fig:dislocation_forest_in_screw_dislocation} \label{fig:dislocation_forest_in_screw_dislocation}$ |

#### Effects on #dislocation-motion
When two dislocations intersect, the mobility of dislocations afterward is important for #work-hardening. Segments on #edge-dislocation do not hinder continued mobility. Segments on #screw-dislocation are not conservative; therefore, hinder dislocation mobility.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/effects_on_dislocation_motion_211001_184200_EST.png) |
|:--:|
| Moving an out-of-plane #jog in #screw-dislocation requires #climb and thermal activation. $\tag{fig:effects_on_dislocation_motion} \label{fig:effects_on_dislocation_motion}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/edge_versus_screw_dislocation_example_211001_184411_EST.png) |
|:--:|
| Edge dislocations want to shove things forward; whereas, screw dislocations want to push things out of the way. $\tag{fig:edge_versus_screw_dislocation_example} \label{fig:edge_versus_screw_dislocation_example}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/edge_versus_screw_dislocation_example_another_look_211001_184739_EST.png) |
|:--:|
| Direction, line vector of dislocation, and #burgers-vector. $\tag{fig:edge_versus_screw_dislocation_example_another_look} \label{fig:edge_versus_screw_dislocation_example_another_look}$ |

>A #screw-dislocation with a #jog must emit #vacancies to allow climb, which may also produce dislocation bowing. <cite> Dr. Atwater

#### Dislocation Looping
If the jog does not move, advancing segments eventually form a loop. This occurs by the pinching of of the segments such that a dipole is formed. This is only for #screw-dislocation.

#forest-hardening
: A hardening mechanism that increases immobility of dislocations.

#### Orowan Equation
Cumulative effect of dislocations can be modeled as a #unit-cube with parallel dislocations moving in one direction with all contributing a step size of #burgers-vector. The #dislocation-density, #burgers-vector, and average distance travelled will all affect the total strain, $\tau$. A constant, $k$ accounts for misalignment of the dislocations with the deformation. #strain-rate is related to #dislocation-velocity assuming a constant #dislocation-density.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/dislocation_unit_cube_211001_185140_EST.png) |
|:--:|
| Not all dislocations are mobile, so the overall #dislocation-density is much higher than that contributing to deformation. $\tag{fig:dislocation_unit_cube} \label{fig:dislocation_unit_cube}$ |

>**Q: Is the dislocation velocity dependent on temperature, because temperature adds or removes electron energy to allow or restrict glide?** <cite> JMA3
*A: Yes.*

#### Peirels-Nabarro Stress (Lattice Friction)
The movement of dislocations follows a non-linear energy due to the atomic nature of the motion (non-continuum). The #energy-barrier is related to the exchange of bonds and shifting of the atoms on the plane. The stress to move the dislocation is a sinusoidal: 

$$\begin{equation}
\tau_{PN} = \alpha\frac{Gb}{2c}e^{-\frac{\pi a}{c}sin(\frac{2\pi x}{c})}
\label{eq:peirels_nabarro_stress}
\end{equation}$$

$\alpha$ is dependent on barrier characteristics, $a$ is the #lattice-parameter, and $c$ is spacing of atoms in direction, $x$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/peirels_nabarro_stress_lattice_friction_211001_185824_EST.png) |
|:--:|
| Think of a Lay's Sun Chip. $\tag{fig:peirels_nabarro_stress_lattice_friction} \label{fig:peirels_nabarro_stress_lattice_friction}$ |

#### Kink Pair Nucleation
It is difficult for #screw-dislocation to move in #bcc metals due to the Peirels #energy-barrier. It is easier...

#### Temperature and Strain Rate
Temperature and #strain-rate have similar effects, with low temperature and high #strain-rate reducing #dislocation-motion during deformation. Shear stress required for deformation dependent on mechanical and thermal conditions. #bcc metals are primarily restricted by the #Peirels-stress, and #fcc metals are restricted by #forest-hardening Thermal and #strain-rate components of deformation, which dominate mechanical response. Above $0.5T_{m}$, creep becomes more important and #dislocation-climb is activated.

$$\begin{equation}
v = A\tau^{m}e^{\frac{-Q}{RT}}
\label{eq:dislocation_velocity}
\end{equation}$$

#dislocation-velocity restricted to real velocities, and is mostly related to the elastic shear wave.


---


*Lecture: October 04, 2021*
>**EXAM REVIEW**
One-page formula sheet is permissible.
Not looking for describing characterizing #dislocation-motion, but more so on the equations.
Will also not focus on drawing #edge-dislocation nor #screw-dislocation.
If there is dislocation interaction of forces, then what is the #burgers-vector? Refer to #jog and #kink concepts.
If presented with labelled stress-strain curve, what are the different parts? Refer to Fig. @fig-stress_
What is with the hardening equations for the subscripts? #Ludwik-Hollomann equation has no $\sigma_{0}$. Just focus on this one equation: true uniform strain is #work-hardening exponent, n, which occurs at the engineering #ultimate-tensile-strength (when the curve comes back down, which is aka #Considere-Criterion).
Know #Frank-Read-Source and its equations, which will likely come from the homeworks.
Nothing foreign from the homework.
#bcc more sensitive to temperature, because di#dislocation-motionaided by temperature.: double-kink nucleation easier to move slip systems with higher energies.
How do vacancies affect electronegativity? Defects reduce electrical conductivity, but effects are negligible. Participants are electron sharing reduce with more inhibiting imperfections.
Gold-Schmidt radius related to coordination number and atomic radius; therefore, #burgers-vector is twice that to move from atomic position to the next (p. 287).
![](../../attachments/engr-839-001-mechanical-metallurgy/problem_4_15_a_211004_185728_EST.png)
#fig-problem_4_15_a
*Bowing of dislocations will also be in exam.*
Favorable to nucleate more dislocations in crystal, because energy required of dislocation to move material infinitely increases with radius of material.
Energetically favorable if magnitude of vector addition of dislocations greater then or equal to that ask.
![](../../attachments/engr-839-001-mechanical-metallurgy/homework_question_on_energetically_favorable_211004_190420_EST.png)
#fig-homework_question_on_energetically_favorable
![](../../attachments/engr-839-001-mechanical-metallurgy/homework_question_on_energetically_favorable_solution_211004_190528_EST.png)
Energy comparison is $\vec{b}^{2}$ (p. 292). $\ref{fig:homework_question_on_energetically_favorable_solution}$
#bcc does not generate partial dislocations, because of high #stacking-fault-free-energy.



---


*Lecture: October 08, 2021*
### Interfacial Defects
#### Grain Boundary
Grain boundaries are areas where crystal grains of varying orientations meet.


<dl>
<dt><strong>Interfacial</strong></dt>
<dd>Two-dimensional discontinuity in structure and often not a flat plane.</dd>
</dl>

Each grain is a single crystal, so the boundaries are simply orientation differences between grain is in three- dimensions. The degree of misalignment determines characteristic of the boundary.Low-angle grain boundaries can be described.

Grains are not circular, but are often
 simplified to having a diameter. #ASTM grain number indicates grains/$in^{2}$ at 100X magnification. $\bar{l} = \frac{L}{N_{l}M} = \frac{2}{S_{v}}$. $$S_{v} = \frac{2\pi r^{2}}{\frac{4}{3}\pi r^{3}} =\frac{3}{2r} = \frac{3}{D},~D = \frac{3}{2}\bar{l}$$ Relative grain size can also be determined by linear intercept method, where grain intersections, $N$ along a line of length, $L$ at magnification, $M$ are used to determine the grin sizeArea is then related to volume and grain size can be determined. [Image-J is a basic, free analysis software for grain size.](https://imagej.net)

#### Tilt Boundary
Sometimes called "edge boundary, because deformation occurs like if one lifted a table from its edge. Orientation of adjacent grains will determine this terminology. More dislocations may be necessary to accomodate the boundaries. A #tilt-boundary occurs when two lattices intersect at an angle. Tilt boundaries are formed by #edge-dislocation: $D = \frac{\frac{\vec{b}{2}}{sin(\theta/2)} \approx \frac{\vec{b}}{\theta},~D = \frac{1.3a}{\thet \approx 7.8a$.



#### Twist Boundary
Is an array of #screw-dislocation: where two lattices have parallel faces, but are rotated relative to another such that they have different orientations (like turning a Rubik's cube). #grain-boundary is often a network of edge and screw dislocations to accommodate the misorientation type and amount.

#### Grain Boundary Energy
Dislocation network concept of a low-angle #grain-boundary means that the energy of that boundary can be determined by the cumulative effect of the dislocations. With #dislocation-pileup, the spacing is important, and at high angles the dislocations may only be a few atomic spaces from each other. Dislocation core energy should be considered as dislocation spacing decreases.

$$\begin{split}
\frac{\vec{b}}{D} &\approx \theta \leq 10\degree \approx \frac{1}{6} rad~\text{or}~D \approx 6\vec{b} \\
E &= E_{\perp}(\frac{1}{D}) = E_{\perp}(\frac{\theta}{\vec{b}}) = \frac{\theta}{\vec{b}}\bigg[\frac{G\vec{b}^{2}}{4\pi(1 - \nu)}ln(\frac{D}{r_{0}}) + E_{core}\bigg]
\end{split}$$

##### Parameter A
Assuming a core radius of $5\vec{b}$, the #dislocation-energy is equal to the #core-energy when separated by $10\vec{b}$.

$$\begin{split}
E &= \theta\frac{G\vec{b}}{4\pi(1 - \nu)}(-ln(\theta) + A) \\
U &= \frac{G\vec{b}^{2}}{10},~\text{for}~D = 10\vec{b} = \frac{\vec{b}}{\theta} \\
E &= \frac{G\vec{b}^{2}}{10D} = \frac{G\vec{b}^{2}}{100\vec{b}} = \frac{G\vec{b}}{100},~(\theta = 0.1) \\
\frac{G\vec{b}}{100} &= \frac{G\vec{b}*0.1}{4\pi(1 - \nu)}(A - ln(0.1)) \\
A &= \frac{4\pi(1 - \nu)}{10} + ln(0.1) = 0.866 - 2.30 \\
&= -1.436
\end{split}$$

#### Grain Boundary Misorientation-Energy Relation
At low angles, #grain-boundary will have a linear increase in energy with angle (for isolated dislocations). As the angle increases, dislocation interaction cause the energy to maximize around $30\degree$. High angle #grain-boundary have a combination of fit and misfit regions, and their energy is better understood as #surface-tension. 

| ![](../../attachments/engr-839-001-mechanical-metallurgy/special_grain_boundary_energy_relations_211008_185804_EST.png) |
|:--:|
| Twins are actually high angle grains with low energies. $\tag{fig:special_grain_boundary_energy_relations} \label{fig:special_grain_boundary_energy_relations}$ |

#### Coincident Site Lattice Boundary
#coincident-site is disordered in general, but has a period of alignment between lattice sites such that the sites are shared between grains. Energy of #grain-boundary decreases with increasing frequency of coincident sites. 

| ![](../../attachments/engr-839-001-mechanical-metallurgy/coincident_site_boundary_example_211008_190048_EST.png) |
|:--:|
| Density of sites range from $\frac{1}{3}$ to $\frac{1}{9}$. Where the sites are $3-9$ atoms apart. $\tag{fig:coincident_site_boundary_example} \label{fig:coincident_site_boundary_example}$ |

Degree of #coincident-site will affect overall #grain-boundary-energy:
- Lower #grain-boundary energy in pure metals.
- Lower diffusivity.
- Lower electrical resistivity.
- Greater resistance to #grain-boundary sliding, fracture, etcetera.
- Greater resistance to corrosion.
- Higher mobility per energy.

>For the *Critical Review* concept, perform the review over something practical with **5** of any of the listed topics. Be as specific as possible.


---


*Lecture: October 11, 2021*
**Exam Answer Key**
1. True stress-strain moves tension up-left and compression moves down-right.
2. Necking is not uniform, but local, plastic strain.
3. Only engineering decreases for increasing strain.
4. #Ludwik-Hollomann uses true stress-strain; therefore, the engineering stress-strain must be converted to true and that is the exponent. Then find the stress at the highest point of the engineering stress-strain curve in the true stress-strain regime and convert back to engineering.
5. The "friction hill" is highest at the center of the specimen, which tapers off towards the edges. Can mitigate this with lubricant or ring.
6. Load and indenter type are only parameters of Rockwell testing.
7. Order of magnitude too large.
8. $\gamma = \frac{G\vec{b}^{2}}{2\pi d}$. Solve for d.
9. Use radius, not pinning distance.
10. Simply use the information from (9) and plug into (10).
11. ![](../../attachments/engr-839-001-mechanical-metallurgy/test2_11_solution_211011_183219_EST.png)
12. Normal stresses and $\tau_{12}$ are 0; therefore, no volume changing.

#### Triple Junctions
Formed when three grain boundaries meet: have lower mobility and higher diffusivity than other grain boundaries. Comprise a larger fraction of the total boundary volume at smaller grain sizes. Grain growth is difficult at these junctions.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/triple_junction_example_211011_185321_EST.png) |
|:--:|
| Approximated by 14-sided polygons, which can perfectly fit together in 3D without gaps. $\tag{fig:triple_junction_example} \label{fig:triple_junction_example}$ |

#### Grain Boundary Dislocations and Ledges
A #grain-boundary dislocation is path of the #grain-boundary and not the parent lattice and mayform steps on the #grain-boundary interface. Dislocation passing through a #grain-boundary can result in shearing and step formation. Ledges are accummulated steps, and they are common in high-angle #grain-boundary.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/step_example_211011_185812_EST.png) |
|:--:|
| Dislocation arrays want to remain align to minimize their cummulative stress field. $\tag{fig:step_example} \label{fig:step_example}$ |

#### Summary
Fundamental to structure of #polycrystalline metal is #grain-boundary. Characteristics of these boundaries inform the mechanical properties of the material.

>**Q: Concerning the *Critical Review* assignment, do you want the article we want to review?** <cite> Julian
*A: Share the article and outline what you will discuss. *Mechanical Testing* can include nano-indentation, hardness, etcetera. Explain enough of the material that you show comprehension of the subject matter.*


---


*Lecture: October 13, 2021*
### Twinning
Very strange boundary, and may occur without or without #slip. 

<dl>
<dt><strong>Twinning</strong></dt>
<dd>Boundary that acts as a line of symmetry between mirroring grain structures. Is a deformation mechanism.</dd>
</dl>

#twinning only exists in $\Sigma 3$ boundaries and is favored when #slip is not: i.e. #hcp metals are very susceptible to #twinning. Function of microstructure, temperature, and strain-rate.

#### Crystallography
Twinning can allow for more slip. Slip is more common, but twinning is an alternate route, especially when slip is restricted.
- #hcp: occurs at ambient temperatures from lack of #slip-planes.
- #bcc: sub-ambient temperature and slip is more difficult.
- #fcc: not common because slip is easy.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/twinning_example_depicted_211013_182458_EST.png) |
|:--:|
| Twins can only occur within a single grain. E.g. silver has a low #stacking-fault-free-energy and twins easily when annealed. $\tag{fig:twinning_example_depicted} \label{fig:twinning_example_depicted}$ |

#### Difference from Slip
#twinning mechanisms and results vary significantly from slip.
- Twinning
  - Mirror image of lattice.
- Slip
  - foo
  - bar

#### Twinning and Slip
Stress required to initiate #twinning is high, but low to propogate. More likely to occur after extensive #work-hardening, low-temperature, high strain-rates: e.g. tin cry when bending a piece of tin.

#### Effect of the c/a Ratio
- #twinning occurs when stress state$= \begin{cases}\frac{c}{a} > \sqrt{3} &, \text{compression} \\\\ \frac{c}{a} < \sqrt{3} &, \text{tension}$
- An ideal $\frac{c}{a} = 1.633 \text{ and } \sqrt{3} = 1.732$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_state_with_twinning_example_211013_183241_EST.png) |
|:--:|
| If slip is not preferred, crystal may twin to accommodate deformation. $\tag{fig:stress_state_with_twinning_example} \label{fig:stress_state_with_twinning_example}$ |

#### Mechanical Effects
>If temperature drops, then #twinning is more likely. If #strain-rate decreases, then #twinning is more likely. <cite> Atwater

| ![](../../attachments/engr-839-001-mechanical-metallurgy/temperature_dependence_of_twinning_211013_183543_EST.png) |
|:--:|
| Competition between twinning and slip resolves to whichever is easier. Remember that twinning is mainly driven by the stress-state of the material. $\tag{fig:temperature_dependence_of_twinning} \label{fig:temperature_dependence_of_twinning}$ |

#### Effects of Stacking Fault Free Energy
| ![](../../attachments/engr-839-001-mechanical-metallurgy/effects_of_stacking_fault_energy_211013_183648_EST.png) |
|:--:|
| As #stacking-fault-free-energy decreases, the propensity toward #twinning increases. #work-hardening rate drops in copper, but allows brass to stabilize its stress state. $\tag{fig:effects_of_stacking_fault_energy} \label{fig:effects_of_stacking_fault_energy}$ |

$$\begin{equation}
\sigma_{T} = K\sqrt{\big(\frac{\gamma_{SFE}}{G\burgers}\big)}
\label{eq:twinning_stress}
\end{equation}$$

Twins will act as slip barrier, which increases the #work-hardening rate of the material.

#### Twinning and Slip Stress
Domains in which #twinning or #slip can be determined by setting their initiation stresses equal to one another: $\sigma_{T} = \sigma_{S}$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/grain_size_temperature_strain_rate_and_twinning_211013_184103_EST.png) |
|:--:|
| More strain raises the curve: i.e. more area under the curve means more [twinning. $\tag{fig:grain_size_temperature_strain_rate_and_twinning} \label{fig:grain_size_temperature_strain_rate_and_twinning}$ |

#### Summary
Primarily an #hcp thing and can occur in #fcc: not likely in #bcc. Deformation mechanism that allows for more strain, but this mechanism competes with #slip.

### Grain-Size Boundaries
Effect of #grain-boundary on strength and bulk properties commonly characterized by the #Hall-Petch-Equation. #grain-boundary must maintain contact under deformation; therefore, #slip must occur, which implies that #work-hardening is proportional to #grain-boundary-area. *This assumes that the material is not coming apart.*

<dl>
<dt><strong>Texture</strong></dt>
<dd>Alignment of grains along a particular direction.</dd>
</dl>

We will focus on random orientation.

#### Hall-Petch Equation
| ![](../../attachments/engr-839-001-mechanical-metallurgy/hall_petch_equation_211013_185308_EST.png) |
|:--:|
| Still used today to determine #grain-size; however, is not as accurate for #nanograins ($\lt 10 nm$). $\tag{fig:hall_petch_equation} \label{fig:hall_petch_equation}$ |

$$\begin{equation}
\sigma_{y} = \sigma_{0} + kD^{-\frac{1}{2}}
\label{eq:hall_petch_equation}
\end{equation}$$

Much work today is starting to look at grain size strengthening through #heterostructure. $\sigma_{0}$ is the #lattice-friction: the stress to move a dislocation.

#### Theories Behind the Mechanisms
Based on #dislocation-pileup crossing #grain-boundary due to high stress on lead dislocation. What is the strength for a dislocation to move from one grain to another?

$$\begin{equation}
\begin{split}
L &= \frac{\alpha nG\burgers}{\pi\tau_{a}} \\\\
n\tau_{a} &\geq \tau_{c} \\\\
\frac{\alpha\pi D\tau_{a}^{2}}{2G\burgers} &\geq \tau_{c}
\end{split}
\label{eq:hall_petch_mechanisms}
\end{equation}$$

#### Cottrell Theory
Instead of assuming that dislocations pass through #grain-boundary, the #stress-concentration does 

$$\begin{equation}
\begin{split}
\tau_{c} &= (\tau_{a} - \tau{0})\sqrt{\frac{D}{4r}} \\\\
\tau_{a} &= \tau_{0} + 2\tau_{c}\sqrt{r}D^{-\frac{1}{2}}
\end{split}
\label{eq:cottrell_theory_mechanisms}
\end{equation}$$

#### Li Theory
Rather than considering the approaching of #grain-boundary as source for dislocations, where ledges act as #stress-concentration to initial #dislocation-initiation. These act as a forest near the #grain-boundary and stress is related to that required to move dislocation through this forest. Therefore, flow stress, $\tau$ is often related to #dislocation-density, $\rho = \dots$


---


*Lecture: October 18, 2021*

#### Meyers-Ashworth
Incompatible stresses between grains generate #anistropy. This causes and interfacial shear stress 3 times higher than normal, applied stress, which may be homogeneous. Dislocations form at interfaces, rather than grain interior; therefore, dislocations do not propagate through the grain because nothing pushes them through from localized stresses at boundary and resolved stress elsewhere. Highly entangled dislocations form in higher density at #grain-boundary. #microyielding can occur in the #grain-boundary region, which causes a composite behavior of harder #grain-boundary network due to plastic incompatibility. When applied stress reaches the #grain-boundary flow stress, then #macroyielding occurs.

$$\begin{equation}
\begin{split}
\tau_{I} &= 1.37\sigma_{0} \\
\tau_{H} &= \dots
\end{split}
\label{eq:meyers-ashworth-equations}
\end{equation}$$

#### Summary
Grain size plays a crucial role in mechanical performance of materials. Mechanisms of strengthening$\dots$

### Obstacles to Deformation
Mechanisms of strengthening have focused on dislocation interactions thus far. Grains may be too small to even contain dislocations; alternatively, grains may have substructures within the grain.

| ![](../../../attachments/engr-839-001-mechanical-metallurgy/obstacle_equations.png) |
|:--:|
| May not even cover these in the homeworks. \\(\tag{fig:obstacle_equations} \label{fig:obstacle_equations}\\) |

#### Substructural Effects
<dl>
<dt><strong>Dislocation Cells</strong></dt>
<dd>Formed during deformation and hinder continued deformation: e.g. twinning. Affect on flow stress by $\sigma_{f} = \sigma_{0} + K\Delta^{-m}, \text{ where } 0.5 \leq m \leq 1$.</dd>
</dl>

To include #grain-size, the #Hall-Petch-Equation (Eq. \eqref{eq:hall_petch_equation}) contribution is added.

$$\begin{equation}
\sigma_{f} = \sigma_{0} + K_{1}\sqrt{D} + K_{2}\Delta^{-m}
\label{eq:substructural_effects}
\end{equation}$$

**Very temperature-dependent.** *$\Delta$ is likely the strain.* Plotting the stress difference against the #grain-size in a log-log plot gives an approximately linear behavior, which also depends on temperature.

| ![](../../../../attachments/engr-839-001-mechanical-metallurgy/substructural_effect_loglog_plot_stress_grain_size_211018_184457_EST.png) |
|:--:|
| Slope of this depends on temperature, and can show recrystallization, which is a pre-cursor to recover. \\(\tag{fig:substructural_effect_loglog_plot_stress_grain_size} \label{fig:substructural_effect_loglog_plot_stress_grain_size}\\) |

#### Iron-Carbon System Considerations
Fe-C systems allow for various microstructures within single composition. Ratio of spacing of ferrite, $f_{\alpha}$ and cementite layers in pearlite, then composition grain size, D, lamellar spacing, S, and pearlite colony size, P will affect strength and ductility.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/iron_carbon_system_considerations_211018_184927_EST.png) |
|:--:|
| Iron-carbon system considerations from multiple angles. \\(\tag{fig:iron_carbon_system_considerations} \label{fig:iron_carbon_system_considerations}\\) |

#### Nanocrystalline Materials
At lower limits of grain size, the strength of materials can be maximized. This comes with other challenges, such as brittleness in metals and thermal instability. Small amount of grain actually make up grain boundary volume (disordered regions). The #Hall-Petch-Equation does not apply here or may invert.

##### Strengthening Mechanisms
Several possibilites exist in nature of nanocrystalline strengthening: #dislocation-pileup no longer explains strengthing (too small); #dislocation-network model required (similar to Meyers-Ashworth); and #grain-boundary sliding (especially below 10 nm.) Higly disorded nature of nanocrystalline materials when taken to maximum.
A maxmimum in the strength of nanocrystalline copper Science 301.5638

#### Volumetric Defects
Voids and inclusions are stress concentrators that will weaken the material. Inclusion is often described as an unwanted impurity to the material: often from processing technique. Some second-phase additions may be desired, if properly controlled. Voids are empty spaces, often from entrapped gases: tpyical in casting or powder sintering, where diffusion of vacancies is required to produce full density.