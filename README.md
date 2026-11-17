# Glide libraries

The shared Rust crates of the [Glide desktop](https://github.com/Glide-Desktop):

| Crate | What it holds |
|---|---|
| `glide-geom` | points, sizes, rectangles |
| `glide-theme` | the Meridian design tokens (colours, type, motion, shape) |
| `glide-paint` | CPU drawing: text, shapes, SVG, wallpaper |
| `glide-ui` | animation primitives (`Reveal`, `Tween`, the frame clock) |
| `glide-config` | XDG paths, file helpers and the `glide-configd` client |
| `glide-ipc` | the compositor IPC and keychain protocol types |
| `glide-app` | session bus integration shared by every app (look, activation, menus) |
| `glide-appmenu` | global menu (dbusmenu / `org.gtk.Menus`) reader and server |
| `glide-netbird` | NetBird daemon client |
| `glide-desktop` | desktop entries, icon themes, battery, images |
| `glide-iced` | iced adapters for the design system |
| `glide-sdk` | the toolkit Glide apps are built with |
| `glide-catalog` | an interactive catalogue of every SDK component |

`design/MERIDIAN_DESIGN_SPEC.md` is the design system these crates implement.

Other Glide repositories depend on a tag of this one:

```toml
glide-sdk = { git = "https://github.com/Glide-Desktop/glide-libs", tag = "v0.1.0" }
```

## Build

```sh
cargo build --workspace
cargo test --workspace
```

Split from the Glide monorepo with its history in November 2026.
