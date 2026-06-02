# Obsidian UI Library Modded

**Documentation:** https://docs.mspaint.cc/obsidian

**Source code to documentation site:** https://github.com/mspaint-cc/docs.mspaint.cc/tree/main/content/obsidian

This fork keeps the familiar Obsidian/Linoria-style API while adding quality-of-life features for polished script hub UIs.

## Modded highlights

- Notification variants: `Library:NotifyInfo`, `Library:NotifySuccess`, `Library:NotifyWarning`, and `Library:NotifyError` add sensible icons, titles, and accent colors automatically.
- Actionable notifications: pass an `Actions` array with button text and callbacks to let users confirm, cancel, or open follow-up UI directly from a toast.
- Progress notifications: pass `Progress = 0` and update it later with `Notification:SetProgress(0.5)` for long-running jobs.
- Dismissible toasts: notifications include a close button by default; use `CloseButton = false` or `Dismissible = false` to hide it.
- Improved key tabs: `AddKeyBox` now supports expected-key validation, Enter-to-submit, status text, auto-clear behavior, and dynamic `SetExpectedKey` updates.
- Visual polish: windows support `BackgroundImage`, image transparency, content/panel image overlay transparency, gradient overlays, and custom border/shadow stroke settings.
- Remote background images: `BackgroundImage`, `Window:SetBackgroundImage(url)`, and `Window:SetFullscreenBackgroundImage(url)` accept direct internet image URLs and cache them through `Library.ImageManager`.
- Dashboard tab: `Window:AddDashboardTab()` creates a ready-made landing tab with overview panels, status cards, and quick actions.
- New element pack: `Library:ApplyNewElements()` exposes glass panels, liquid-glass toggles/buttons, highlight buttons, and shiny animated buttons on groupboxes.
- Shiny image masks: shiny buttons use bounded PNG alpha masks with `ClipsDescendants`; loading bar media is clipped inside the progress fill instead of overflowing rounded UI.
- Nested tabboxes: `Groupbox:AddTabbox()` creates tabbed sections inside any groupbox, so compact category panels can hold their own sub-tabs.
- Full-width tab content: `Tab:AddFullGroupbox()` and `Tab:AddFullTabbox()` span the tab above the normal left/right columns for large previews or viewport-style layouts.
- Premium loading screen: `Library:CreateLoading()` now supports entrance/exit motion, optional backdrop fade, ambient gradients, floating particles, icon pulse rings, textured progress, and animated text updates.
- Loading media polish: loading screens include a tiled progress-bar texture plus a 32fps black-hole ring spritesheet around the loading UI; the dark backdrop overlay is off by default and still configurable through `LoadingInfo`.
- Advanced custom fonts: `Library.Font:Download(url)` / `Library:DownloadFont(url)` loads a bitmap-font JSON manifest from any internet URL, downloads atlas pages, and renders text with `ImageLabel` glyphs through `Library:CreateCustomText()` or `Groupbox:AddCustomFontLabel()` (TTF/OTF files need to be converted to a bitmap atlas manifest first).
- Keybind menu controls: `Library:AddKeybindMenuButton()` and `Library:AddKeybindMenuToggle()` add actions directly to the keybind menu, and synced keybind toggles now use a liquid-glass pill style.
- Compact keybind menu: set `KeybindMenuWidth` in `CreateWindow` to resize the draggable keybind menu without it expanding across the screen.
- Layout modes: set `TabsMode = "Sidebar"` or `"Topbar"` and `TabStyle = "Card"` for card-like tab buttons.
- Sprite/video URL media: `Library:DownloadSprite(url)` and `Library:DownloadVideo(url)` download direct URLs through `getcustomasset`; `Groupbox:AddSprite()` and `Library:AddFloatingSprite()` animate sprite sheets with atlas frames/size/columns.
- Advanced card dropdowns: set `CardDropdown = true` and provide `Cards` with thumbnails or code-native preview colors/gradients, bottom-bar transparency, icon, title, description, and per-card stroke options.
- Gradient themes: ThemeManager includes 17 new gradient presets and the built-in theme picker renders as searchable preview cards in UI Settings.
- The original `Library:Notify({...})` API still works and now accepts `Type`/`Variant`, `AccentColor`, `Progress`, `Actions`, `CloseButton`, and `Dismissible` fields.

See `Example.lua` for a complete notification and key-system showcase alongside the standard Obsidian element examples. The example loads this fork from `https://raw.githubusercontent.com/tanhoangviet/Obsidian-UI-Modded/main/`.
