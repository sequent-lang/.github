Sequent Logic: Decoding Topological Patterns<!-- 1. The Custom Logo Banner --><!-- 2. The Dynamic Shields.io Badges --><p align="center"><a href="https://www.google.com/search?q=https://github.com/sequentlogic/sequent/stargazers" target="_blank"><img alt="GitHub Stars" src="https://www.google.com/search?q=https://img.shields.io/github/stars/sequentlogic/sequent%3Fstyle%3Dfor-the-badge%26logo%3Dgithub%26color%3D33CC99"></a><a href="https://www.google.com/search?q=https://github.com/sequentlogic/sequent/blob/main/LICENSE" target="_blank"><img alt="License" src="https://www.google.com/search?q=https://img.shields.io/github/license/sequentlogic/sequent%3Fstyle%3Dfor-the-badge%26color%3D800080"></a><img alt="Status" src="https://www.google.com/search?q=https://img.shields.io/badge/Status-Alpha%2520Development-orange%3Fstyle%3Dfor-the-badge%26logo%3Ddata:image/svg%2Bxml%3Bbase64,PHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJMYXllcl8xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB4PSIwcHgiIHk9IjBweCIKCSB2aWV3Qm94PSIwIDAgMjQgMjQiIGVzaGFwZT0iaGVsZGVyIiBlbmFibGUtYmFja2dyb3VuZD0ibmV3IDAgMCAyNCAyNCIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI%2BCjxwYXRoIGZpbGw9IiNGRkZGRkYiIGQ9Ik0xMiwyYzUuNiwwLDEwLDQuNCwxMCwxMHMtNC40LDEwLTEwLDEwUzIsMTcuNiwxMiwxMlMyNiwxMiwyNiwxMiIvPgo8L3N2Z3M%3D%26logoColor%3Dwhite"><a href="https://www.google.com/search?q=https://discord.gg/your-discord-invite" target="_blank"><img alt="Discord" src="https://www.google.com/search?q=https://img.shields.io/badge/Join%2520the%2520Community-Discord-5865F2%3Fstyle%3Dfor-the-badge%26logo%3Ddiscord%26logoColor%3Dwhite"></a><a href="https://www.google.com/search?q=https://github.com/sequentlogic/sequent-docs" target="_blank"><img alt="Docs" src="https://www.google.com/search?q=https://img.shields.io/badge/Language%2520Spec-online-blue%3Fstyle%3Dfor-the-badge%26logo%3Dreadthedocs%26logoColor%3Dwhite"></a><a href="https://www.google.com/search?q=https://github.com/sequentlogic/sequent/graphs/contributors" target="_blank"><img alt="Contributors" src="https://www.google.com/search?q=https://img.shields.io/github/contributors/sequentlogic/sequent%3Fstyle%3Dfor-the-badge%26color%3Dblueviolet"></a><img alt="Python" src="https://www.google.com/search?q=https://img.shields.io/badge/Python-3.10%252B-blue%3Fstyle%3Dfor-the-badge%26logo%3Dpython%26logoColor%3Dwhite"><img alt="Neo4j" src="https://www.google.com/search?q=https://img.shields.io/badge/Graph%2520Native-Neo4j-008C8C%3Fstyle%3Dfor-the-badge%26logo%3Dneo4j%26logoColor%3Dwhite"><img alt="Prolog-Style" src="https://www.google.com/search?q=https://img.shields.io/badge/Inference-Prolog--Style-darkgreen%3Fstyle%3Dfor-the-badge%26logo%3Ddata:image/svg%2Bxml%3Bbase64,PHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJMYXllcl8xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB4PSIwcHgiIHk9IjBweCIKCSB2aWV3Qm94PSIwIDAgMjQgMjQiIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiB4bWw6c3BhY2U9InByZXNlcnZlIj4KPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTE2LDEwSDguNWMwLDAsMC4yLTAuMiwwLjMtMC40YzAuMi0wLjIsMC40LTAuNSwwLjUtMC44QzkuNyw4LjQsOS45LDcuOSwxMC4xLDcuMyBDMTAuNCw2LjYsMTAuNyw2LDExLDUuNUgxNkwxNiwxMFoiLz4KPHBhdGggZmlsbD0iI0ZGRkZGRiIgZD0iTTE2LDEzSDh2MUgxNlYxM3oiLz4KPC9zdmc%2BCg%3D%3D"&logoColor=white"></p>The Declarative AdvantageTurn systemic chaos into operational order... [The rest of your README text follows here]

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
