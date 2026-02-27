## Will there be a standard template for projects in the RIL?

Yes. Please see the [Rust Innovation Lab Project Template Repository](https://github.com/rustfoundation/rust-innovation-lab-new-project-template) for how a project will be generally structured.

### What kinds of projects clearly fit?

**rustls.** A TLS library written in Rust. This is a clear fit because it both *showcases Rust's strengths* (demonstrating that Rust can deliver a secure, high-performance TLS implementation) and *fills a gap* (providing Rust developers with a memory-safe TLS option).

**Rust-specific plugins for popular projects.** — Plugins that make other projects support Rust clearly fill a gap for Rust developers, even though they are typically written in whatever language that project uses (e.g., for GDB, Python; for Emacs, elisp). The benefit to Rust developers who use the project is direct and obvious. (On the other hand, if this is a plugin to a niche project, the benefit may still be too small.)

### What kinds of projects clearly don't fit?

**Java Spring** — A popular Java framework. This has no connection to Rust. It neither showcases Rust nor fills any gap for Rust developers.

### What about projects where the fit is less clear?

**LSP (Language Server Protocol)** — LSP clearly benefits Rust developers (rust-analyzer implements it), but LSP itself is a language-agnostic protocol. The argument *in favor* of hosting LSP would be that Rust needs better IDE support, and LSP provides a high-leverage way to bootstrap that support quickly. Bootstrapping the spec helps ensure Rust's needs are represented, even if the project ultimately moves to another home. The argument *against* is that LSP is a general specification that by design doesn't have much to do with Rust specifically and that it won't benefit from being housed in the *Rust* Foundation (vs some other software Foundation with a broader focus).

Other similar examples might be:

* **Projects that focus on interop between multiple languages.** A specification for cross-language FFI that covers vectors, maps, and other higher-level types would benefit Rust developers who do FFI work, even though the spec would also benefit other languages. The argument structure is similar to LSP: participating in such a standard could ensure Rust's needs are well-represented, but the standard itself is inherently language-agnostic.
* **General-purpose infrastructure.** Projects like ELF or DWARF specifications are important, and Rust uses them, but the connection may be too indirect. These standards benefit all compiled languages equally, with no particular Rust focus. That said, if Rust had specific needs that weren't being met by such a standard, there could be a case for involvement.