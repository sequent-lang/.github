Sequent Logic
Logic programming for rendered sequences
Show Image
Show Image
Show Image
Show Image

Overview
Sequent Logic (or Sequent for short) is a declarative logic programming language designed for complex rendering pipelines, VFX workflows, and media processing systems. By combining Prolog-style inference with native Neo4j graph database integration, Sequent Logic enables you to define what should happen in your pipeline rather than prescribing how to execute each step.
The Problem
Traditional rendering pipelines rely on imperative scripts where dependencies are manually managed, execution order is rigidly specified, and changes cascade into brittle, error-prone code. As pipelines grow in complexity—spanning computer vision, 3D rendering, video editing, and asset management—maintaining these systems becomes increasingly difficult.
The Solution
Sequent Logic treats pipelines as logical relationships. You declare facts about your assets, define rules about dependencies, and query the system for answers. The inference engine automatically resolves dependencies, determines optimal execution order, and adapts to changes in your pipeline structure.
⚠️ Project Status
Sequent Logic is in active early development and is not yet ready for production use. We are currently building the core language infrastructure. Contributions, feedback, and early adopters are welcome, but expect breaking changes as the language evolves.
Quick Example
sequent% Define a shot and its requirements
shot(shot_010).
requires(shot_010, denoise).
requires(shot_010, color_grade).
requires(shot_010, composite).

% Define dependencies between stages
depends_on(composite, color_grade).
depends_on(color_grade, denoise).

% Query: What's the correct render order?
?- render_order(shot_010, Order).
% Result: Order = [denoise, color_grade, composite]

% Query with graph integration (Neo4j/Cypher)
?- uses_asset(Shot, 'character_model_v3'),
   modified_since_last_render(Shot).
% Returns all shots using this asset that need re-rendering
Key Features

Declarative Logic: Define relationships and constraints, not procedural steps
Graph-Native: Built-in Neo4j integration with native Cypher query support
Temporal Reasoning: Frame-based and timecode operations for media workflows
Automatic Optimization: Inference engine determines optimal execution paths
Domain-Specific: Purpose-built predicates for rendering, compositing, and asset management
Extensible: Python integration for custom predicates and tool bindings

Installation
Sequent Logic is not yet published to PyPI. For development installation:
bashgit clone https://github.com/sequent-lang/sequent.git
cd sequent
pip install -e ".[dev]"
Requirements:

Python 3.8 or higher
Neo4j 5.0+ (optional, for graph features)

Usage
bash# Run a Sequent program
sequent run pipeline.seq

# Interactive REPL
sequent repl

# Validate syntax
sequent check *.seq

# Show help
sequent --help
Python Integration
pythonfrom sequent import Engine

# Initialize engine
engine = Engine()

# Load Sequent rules
engine.consult('pipeline.seq')

# Execute queries
results = engine.query('render_order(shot_010, Order)')
print(results)  # [{'Order': ['denoise', 'color_grade', 'composite']}]

# With Neo4j integration
engine.connect_neo4j('bolt://localhost:7687')
impacts = engine.query('impact_analysis("character_model_v3", Affected)')
Documentation

Language Tutorial - Step-by-step introduction (coming soon)
Language Reference - Complete specification (coming soon)
Examples - Real-world examples (coming soon)
API Documentation - Python integration guide (coming soon)

Use Cases
Sequent Logic is designed for scenarios where complex dependencies, temporal relationships, and asset management intersect:

VFX Pipeline Management: Track shot dependencies, asset versions, and render requirements
Sports Video Analysis: Coordinate computer vision, tracking data, and 3D visualization
Architectural Visualization: Manage scene composition, lighting, and rendering workflows
Scientific Visualization: Define data processing pipelines with automatic optimization
Game Cinematics: Coordinate animation, rendering, and post-processing stages

Roadmap
v0.1.0 - Foundation (Target: Month 2)

 Project structure and organization
 Lexer and parser implementation
 Basic unification algorithm
 Simple SLD resolution engine
 Core predicate library

v0.2.0 - Graph Integration (Target: Month 3)

 Neo4j driver integration
 Cypher query execution
 Graph pattern matching
 Hybrid query optimization

v0.3.0 - Standard Library (Target: Month 4)

 Rendering predicates
 Temporal logic operators
 Asset management utilities
 Pipeline optimization predicates

v0.4.0 - Tooling (Target: Month 5)

 CLI tool with REPL
 VS Code extension
 Syntax highlighting for popular editors
 Debugging utilities

v1.0.0 - Stable Release (Target: Month 12)

 Complete language specification
 Production-ready interpreter
 Comprehensive documentation
 Integration examples for major VFX tools

Contributing
We welcome contributions from developers, researchers, VFX professionals, and anyone interested in declarative programming or rendering pipelines. Sequent Logic is an AI-assisted project, and we embrace contributions from both human developers and AI-augmented workflows.
Ways to Contribute:

Report bugs and request features via GitHub Issues
Improve documentation and write tutorials
Implement language features or standard library predicates
Share example programs and use cases
Test the language and provide feedback

See our Contributing Guide for details.
Community

GitHub Discussions: Ask questions and share ideas
Discord: Join our community server (coming soon)
Twitter: Follow @sequentlang for updates
Mailing List: Subscribe for announcements (coming soon)

Inspiration
Sequent Logic draws from several established paradigms and systems:

Prolog - Logic programming foundation and inference mechanisms
Datalog - Declarative database queries and guaranteed termination
Cypher - Graph pattern matching and declarative graph queries
Mercury - Strong typing and mode systems for logic languages
Sequent Calculus - Formal proof theory (Gentzen, 1934)

The name "Sequent Logic" reflects both the mathematical concept of sequents (Γ ⊢ Δ) from proof theory and the sequential nature of frame-based media processing.
License
Sequent Logic is licensed under the Apache License 2.0. This is a permissive open-source license that allows commercial use, modification, and distribution.
Acknowledgments
Sequent Logic is an AI-assisted language project, created through collaboration between human vision and AI capabilities. We believe the future of programming language design involves leveraging both human creativity and AI assistance.
Project Creator: [Your Name]
AI Collaboration: Claude (Anthropic)
Special Thanks: The Prolog, Datalog, and Neo4j communities for foundational work

Built for the rendering age, designed with logic ✨
For questions, feedback, or collaboration opportunities, open a Discussion or reach out via email.
