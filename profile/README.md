https://github.com/sequent-lang/sequent/blob/main/Sequent_Logic_banner.png?raw=true

<div align="center">
    <a href="https://sequent-lang.org">
        <img src="[URL_TO_YOUR_BANNER_IMAGE]" alt="Sequent Logic: ACHIEVE OPERATIONAL AUTHORITY." width="100%">
    </a>
</div>

<p align="center">
    <img src="[URL_TO_INFERENCE_CORE_BADGE]" alt="Inference Core: Prolog/Datalog">
    <img src="[URL_TO_GRAPH_BACKEND_BADGE]" alt="Graph Backend: Neo4j Graph">
    <img src="[URL_TO_CORE_FEATURE_BADGE]" alt="Core Feature: Temporal Logic">
    <img src="[URL_TO_LICENSE_BADGE]" alt="License: Apache 2.0">
    <img src="[URL_TO_STATUS_BADGE]" alt="Status: Alpha">
    <img src="[URL_TO_ACTIVITY_BADGE]" alt="Activity: Active Development">
</p>

# Sequent Logic

**Logic programming for rendered sequences**

Sequent Logic (or Sequent for short) is a declarative programming language that combines Prolog-style inference with Neo4j graph queries for rendering pipelines, VFX workflows, and media processing systems.

## 🎯 What Makes Sequent Logic Different?

Instead of writing imperative scripts that specify *how* to execute each step:

```python
# Traditional approach - brittle and procedural
run_denoise(shot_010)
run_color_grade(shot_010)
run_composite(shot_010)

# Sequent Logic

**Logic programming for rendered sequences**

Sequent Logic (or Sequent for short) is a declarative programming language that combines Prolog-style inference with Neo4j graph queries for rendering pipelines, VFX workflows, and media processing systems.

## 🎯 What Makes Sequent Logic Different?

Instead of writing imperative scripts that specify *how* to execute each step:

```python
# Traditional approach - brittle and procedural
run_denoise(shot_010)
run_color_grade(shot_010)
run_composite(shot_010)
```

Write declarative logic that defines *what* relationships exist:

```sequent
% Sequent Logic - declarative and queryable
shot(shot_010).
requires(shot_010, denoise).
requires(shot_010, color_grade).
requires(shot_010, composite).

depends_on(composite, color_grade).
depends_on(color_grade, denoise).

% Query: What's the optimal render order?
?- render_order(shot_010, Order).
% Result: [denoise, color_grade, composite]
```

The inference engine automatically resolves dependencies, determines execution order, and adapts to changes.

## 🚀 Core Projects

- **[sequent](https://github.com/sequent-lang/sequent)** - Language implementation and interpreter
- **[sequent-docs](https://github.com/sequent-lang/sequent-docs)** - Documentation and tutorials *(coming soon)*
- **[sequent-examples](https://github.com/sequent-lang/sequent-examples)** - Example programs and patterns *(coming soon)*
- **[sequent-tools](https://github.com/sequent-lang/sequent-tools)** - IDE extensions and tooling *(coming soon)*

## ✨ Key Features

- **Declarative Logic**: Define relationships and constraints, not procedural steps
- **Graph-Native**: Built-in Neo4j integration with native Cypher query support
- **Temporal Reasoning**: Frame-based and timecode operations for media workflows
- **Automatic Optimization**: Inference engine determines optimal execution paths
- **Domain-Specific**: Purpose-built predicates for rendering and asset management
- **Extensible**: Python integration for custom predicates and tool bindings

## 🎬 Use Cases

Sequent Logic is designed for scenarios where complex dependencies, temporal relationships, and asset management intersect:

- **VFX Pipelines**: Track shot dependencies, asset versions, and render requirements
- **Sports Analytics**: Coordinate computer vision, tracking data, and 3D visualization
- **Architectural Viz**: Manage scene composition, lighting, and rendering workflows
- **Scientific Viz**: Define data processing pipelines with automatic optimization
- **Game Cinematics**: Coordinate animation, rendering, and post-processing

## ⚠️ Project Status

**Alpha Development** - Sequent Logic is under active development and is not yet ready for production use. We are currently building:

- [x] Project foundation and organization
- [ ] Parser and lexer implementation
- [ ] Inference engine (unification + backtracking)
- [ ] Neo4j integration with Cypher support
- [ ] Standard library for rendering predicates
- [ ] CLI tool and REPL
- [ ] VS Code extension

Expected first alpha release: **v0.1.0** (target: 2-3 months)

## 🤝 Get Involved

We welcome contributions from developers, researchers, VFX professionals, and anyone interested in declarative programming or rendering pipelines.

**Ways to Contribute:**
- **Code**: Implement language features, fix bugs, add predicates
- **Documentation**: Write tutorials, improve examples, translate docs
- **Testing**: Try the language and report bugs or usability issues
- **Design**: Participate in language design discussions
- **Examples**: Share real-world use cases and example programs

**Getting Started:**
- Read our [Contributing Guide](https://github.com/sequent-lang/.github/blob/main/CONTRIBUTING.md)
- Join [GitHub Discussions](https://github.com/sequent-lang/sequent/discussions)
- Follow [@sequentlang](https://twitter.com/sequentlang) for updates
- Check out [good first issues](https://github.com/sequent-lang/sequent/labels/good%20first%20issue)

## 📚 Resources

- **Website**: [sequent-lang.org](https://sequent-lang.org) *(coming soon)*
- **Tutorial**: [Getting Started Guide](https://sequent-lang.org/learn/tutorial) *(coming soon)*
- **Language Spec**: [Reference Documentation](https://sequent-lang.org/docs/reference) *(coming soon)*
- **Community**: [Discord Server](https://discord.gg/sequent) *(coming soon)*

## 🌟 Philosophy

Sequent Logic is an AI-assisted language project. We believe the future of programming language design involves collaboration between human creativity and AI capabilities. We embrace:

- **Open Development**: Building in the open from day one
- **AI Collaboration**: Leveraging AI for design, implementation, and documentation
- **Community-Driven**: Shaped by real-world needs of practitioners
- **Academic Rigor**: Grounded in formal logic and proof theory

## 📄 License

All Sequent Logic projects are licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) - a permissive open-source license.

---

**Built for the rendering age, designed with logic** ✨

*Questions? Open a [Discussion](https://github.com/sequent-lang/sequent/discussions) or reach out at hello@sequent-lang.org*
