# BarrerCode

**A lightweight, fast, .NET-based code editor**

> "Like VS Code, but it doesn't eat your RAM"

## The Problem

VS Code (Electron-based):
- 300-500MB RAM usage for a text editor
- Slow startup (loading Chromium + Node.js)
- Extensions crash the entire editor
- Memory leaks everywhere
- Built on JavaScript/TypeScript (the 10-day hack)

## The Solution

BarrerCode (.NET 10 + Avalonia):
- **50-100MB RAM** (5x less than VS Code)
- **Fast startup** - compiled binary, not interpreted
- **Stable** - compile-time safety, no runtime crashes
- **Cross-platform** - Windows, Linux, macOS (native, not Electron)
- **C# extensions** - type-safe, isolated, can't crash editor

## Architecture

```
BarrerCode
├── Core (C#)
│   ├── Text editing engine
│   ├── LSP client (Language Server Protocol)
│   ├── Extension host
│   └── Project management
├── UI (Avalonia)
│   ├── Cross-platform native UI
│   ├── No Electron bloat
│   └── Hardware-accelerated rendering
└── Extensions (C#)
    ├── Compile-time checked
    ├── Sandboxed execution
    └── Git integration (LibGit2Sharp)
```

## Features (Planned)

### Phase 1: MVP
- [x] Create Avalonia project structure
- [ ] Basic text editing component
- [ ] File explorer
- [ ] Syntax highlighting
- [ ] Open/Save files

### Phase 2: LSP Integration  
- [ ] Language Server Protocol client
- [ ] C# language support (.NET SDK integration)
- [ ] IntelliSense/autocomplete
- [ ] Go to definition
- [ ] Find references

### Phase 3: Extensions
- [ ] C# plugin architecture
- [ ] Extension marketplace
- [ ] Git integration (LibGit2Sharp)
- [ ] Terminal integration

### Phase 4: Advanced Features
- [ ] Debugger support
- [ ] Multi-cursor editing
- [ ] Search/replace
- [ ] Theme system
- [ ] Settings sync

## Why .NET 10?

- **Memory efficient** - No V8 engine overhead
- **Fast** - Compiled, not interpreted
- **Type-safe** - Catch errors at compile time
- **Cross-platform** - Runs everywhere without Electron
- **Modern** - Actually modern (2025), not 1995 JavaScript

## Comparison

| Feature | VS Code | BarrerCode |
|---------|---------|------------|
| Memory (idle) | 300-500MB | 50-100MB |
| Startup time | 2-5 seconds | <1 second |
| Runtime | Electron (Chromium + Node.js) | .NET 10 native |
| Language | TypeScript/JavaScript | C# |
| Extensions | JavaScript (can crash editor) | C# (isolated, safe) |
| Updates | Often break things | Compile-time safety |

## Philosophy

**Use the right tool for the job.**

- Text editors should be lightweight, not Chromium browsers
- Applications should be compiled, not interpreted
- Extensions should be type-safe, not runtime disasters
- "Good enough" is not good enough

Built by BarrerSoftware with the same philosophy as BarrerOS:
- Question everything
- Build what SHOULD exist  
- Own your stack
- 🏴‍☠️ Fuck it, we ball

## Development

```bash
# Clone
git clone https://github.com/BarrerSoftware/BarrerCode

# Build
cd BarrerCode
dotnet restore
dotnet build

# Run
dotnet run
```

## License

MIT License - Fork it, modify it, use it.

## Status

**Early Development** - Born December 5, 2025

This is a proof of concept that .NET can build better desktop applications than Electron. 

If you're tired of VS Code eating your RAM, star this repo and let's build something better together.

---

*"The best way to predict the future is to build it."*  
— BarrerSoftware, 2025
