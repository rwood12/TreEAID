# TreEAID  
**Treefall Evaluation, Analysis, and Identification through Deep Learning**

TreEAID is an open-source framework designed to automate the detection, characterization, and geospatial analysis of tornado-induced treefall and root-ball disturbance using high-resolution aerial imagery. The system integrates deep-learning segmentation, shape-aware post-processing, geometric feature extraction, and spatial aggregation to support large-scale post-storm assessments and near-surface wind-field interpretation.

---

# Features

- **Automated Treefall and Root-Ball Detection:** Uses YOLO-based instance segmentation models trained on thousands of manually annotated treefall and root-ball instances.

- **Shape-Aware Mask Refinement:** Applies SA-NMS and geometric reconstruction methods to correct fragmented or overlapping predictions.

- **Geometric Characterization:** Computes orientation, length, thickness, taper rate, root-ball axes, and other quantitative metrics.

- **Wind-Field Mapping:** Aggregates orientation vectors within grid cells to generate spatial wind-direction fields for tornado analysis.

- **Tile Boundary Correction:** Consolidates duplicated or partial vectors across image tiles using ROI-based vector aggregation.

- **GIS-Ready Output:** Exports refined vectors and feature tables to standard formats for QGIS, ArcGIS, or other geospatial workflows.

- **Graphical User Interface:** Provides structured model execution, visualization, and export options without requiring extensive coding.

---

# Input Requirements

- Orthomosaic or tiled aerial imagery (≈1.5–5 cm GSD preferred).  
- Corrected geographic metadata in EPSG-consistent coordinate systems.  
- Sufficient tree density for treefall-based wind-field reconstruction.

---

# Core Workflow

- Image Preprocessing Tiling, metadata confirmation, and optional brightness normalization.

- Deep-Learning Inference
Segmentation of fallen trees and root balls.

- Shape-Aware Refinement
Application of SA-NMS and α-shape reconstruction.

- Feature Extraction
Orientation estimation via taper analysis, trunk geometry, and root-ball dimension calculations.

- Vector Aggregation and Boundary Correction
Merging and filtering vectors to ensure spatial continuity across large areas.

- Export and Visualization
GIS-ready shapefiles, GeoPackages, summary tables, and wind-direction maps.

---

# Applications

- Post-storm reconnaissance  
- Tornado-terrain interaction studies  
- Validation of numerical or analytical wind-field models  
- Forestry and ecological disturbance analysis  
- Emergency-management and hazard-mapping workflows
