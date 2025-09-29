# Agents Guide for Zellij Plugin Development

## Project Structure
- Rust Zellij plugin for session management
- Target: `wasm32-wasip1` (WebAssembly)

## Build/Test Commands
- Build: `cargo build`
- Check: `cargo check`
- Reload plugin: `zellij action launch-or-focus-plugin -m -s -f -- "file:target/wasm32-wasip1/debug/zj-session.wasm"`

## Code Style
- **Imports**: Group external crates first, then std library, then local modules
- **Error handling**: Use `Option<T>` and pattern matching extensively
- **Naming**: snake_case for variables/functions, PascalCase for types/enums
- **Macros**: Use declarative macros (like `render_assets!`) for repetitive UI code
- **Modules**: Organize UI components in `ui/` module with clear separation
- **Memory**: Prefer stack allocation, use `Vec` for dynamic collections
