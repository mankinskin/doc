Back to [workflow-tools](..).

# doc

Documentation workspace model: ingest `cargo metadata` for a Rust workspace and surface crate docs, READMEs, and doc-comment structure over HTTP.

## Primary Use Case

Discover and browse the documentation surface of a Rust workspace (crates, their READMEs, and their `cargo doc` output) without hand-maintaining a separate index.

## Usage

Build the desired transport from the `workflow-tools` workspace root:

```bash
cargo run -p doc-http --bin doc-http
cargo run -p doc-viewer --bin doc-viewer
```

`doc-http` serves the REST API; `doc-viewer` serves the HTTP UI and an MCP server on top of it.

## Related Crates

- [crates/doc-api](crates/doc-api): core library (workspace model, `cargo_metadata` ingestion).
- [crates/doc-http](crates/doc-http): HTTP REST API (binary `doc-http`).
- [crates/doc-viewer](crates/doc-viewer): HTTP + MCP viewer application (binary `doc-viewer`).
