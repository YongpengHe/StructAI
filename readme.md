# StructAI: AI-Powered Structural Design System

## Overview

StructAI is a practical AI system that generates structural designs from natural language descriptions. By combining fine-tuned language models with CAD systems, it enables quick generation of 2D trusses and 3D grid structures for conceptual design. The system focuses on geometric configuration and pattern generation, providing a bridge between design intent and technical implementation.

## Training Dataset and Model

The system is built upon GPT-4 with fine-tuning on a focused dataset of structural design descriptions. The training data comprises:

- 100+ real-world structural designs from professional architects and engineers
- 900+ synthetic examples generated through prompt engineering with GPT-4
- Coverage of 2D truss and 3D grid structure typologies
- Basic validation for geometric feasibility

The synthetic data generation process ensures:
- Realistic parameter combinations
- Geometric feasibility
- Common design patterns
- Standard terminology

## Key Implementations

- **Natural Language Processing**: Fine-tuned GPT-4 model for parsing structural design requirements and generating geometric parameters
- **Geometric Generation**: Basic algorithms for translating descriptions into 3D models
- **Pattern Recognition**: Template-based pattern matching for common structural configurations
- **CAD Integration**: Direct API interface for geometric modeling

## Demonstrations

### Example 1: Three-Span Continuous Truss
```python
Input: "Generate a three-span continuous truss bridge with 120 meters total length."
```
Given the input, StructAI generates:
1. Basic span configuration: 35m - 50m - 35m
2. Standard height variation: 12m at midspan, 6m at supports
3. Regular nodal spacing
4. A typical truss pattern optimized for structrual continuity

![Three-Span Bridge Truss](demo/2D%20Truss.png)
*Generated three-span continuous truss with standard proportions*

### Example 2: Exhibition Space Gridshell
```python
Input: "Create a trumpet-shaped single-layer gridshell for a public exhibition space. It should span roughly 30m."
```
Given the architectural intent, StructAI creates:
1. Trumpet-shaped geometry, expanding from a 3-meter base to a 45-meter top diameter
2. An overall structural height of approximately 18 meters
3. Regularized grid pattern across the surface
4. A typical mesh density suitable for structural clarity and fabrication

![Exhibition Gridshell](demo/Single-layer%20Trumpet-shaped%20GridShell.png)
*Generated single-layer gridshell with standard pattern*

### Example 3: Flower-Shaped Space Frame
```python
Input: "Design a flower-shaped double-layer grid structure with 6 petals. It should have a dimension of 60m."
```
Given the design concept, StructAI delivers:
1. A Basic petal geometry spanning 60 meters in diameter
2. Uniform vertical layer spacing of 2 meters
3. A consistent radial arrangement
4. Standardized member density
5. Strategically support placements at petal tips and valley intersections

![Flower Space Frame](demo/Double-layer%20Flower-shaped%20GridShell.png)
*Generated double-layer space frame with standard pattern*

## Technical Architecture

### Core Components
- **Language Processing**: Fine-tuned GPT-4 model for:
  - Design intent interpretation
  - Parameter extraction and validation
  - Geometric constraint generation
  - Pattern selection guidance
- **Geometry Generation**: Basic algorithms for 2D and 3D model generation
- **Pattern Recognition**: Template-based pattern matching for structural configurations
- **Form Generation**: Standard geometric configuration

### Component Management System

#### 1. Geometric Generation
- **2D Truss System**:
  - Rule-based nodal point placement
  - Standard truss pattern templates
  - Automatic member connections
  - Span-to-depth ratio constraints

- **3D Grid System**:
  - Parametric surface algorithms
  - Grid projection methods
  - Layer spacing rules
  - Support point algorithms

#### 2. Pattern Management
- **Template System**:
  - Predefined truss patterns
  - Standard grid configurations
  - Connection details
  - Support arrangements

- **Pattern Application**:
  - Geometric similarity checks
  - Topology matching
  - Density evaluation
  - Support pattern verification

#### 3. CAD Integration
- **Model Generation**:
  - AutoCAD API automation
  - Layer management
  - Property assignment
  - Support conditions
  - Automatic dimensioning

#### 4. Design Validation
- **Geometric Checks**:
  - Feasibility verification
  - Length constraints
  - Support verification
  - Fabrication rules

- **Design Guidelines**:
  - Span-to-depth ratios
  - Member slenderness
  - Connection spacing
  - Support requirements

### System Structure
```
StructAI/
├── ai/                    # AI modules
│   ├── nlp/              # Language processing
│   ├── patterns/         # Pattern templates and matching
│   └── geometry/         # Form generation
├── core/                 # Core functionality
│   ├── geometry/        # Basic geometric computation
│   │   ├── truss/      # 2D truss generation
│   │   └── grid/       # 3D grid generation
│   ├── patterns/        # Standard pattern generation
│   │   ├── templates/  # Pattern templates
│   │   └── matching/   # Pattern matching
│   └── cad/            # CAD integration
│       ├── model/      # Model generation
│       └── docs/       # Documentation
├── api/                  # API interfaces
└── utils/               # Utility functions
```

## Implementation

### Processing Pipeline
1. Natural language processing of design intent
2. Basic parameter extraction
3. Geometric form generation
4. Pattern application
5. CAD model generation

### Design Considerations
- Geometric feasibility
- Pattern consistency
- Basic spatial quality
- Standard proportions

## Requirements

- Python 3.9+
- AutoCAD 2023+
- CUDA-compatible GPU (for AI processing)
- Required packages in requirements.txt

## Installation

```bash
git clone https://github.com/yourusername/StructAI.git
cd StructAI
pip install -r requirements.txt
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

