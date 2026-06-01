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
- Visual polish: windows support `BackgroundImage`, image transparency, gradient overlays, and custom border/shadow stroke settings.
- Dashboard tab: `Window:AddDashboardTab()` creates a ready-made landing tab with overview panels, status cards, and quick actions.
- New element pack: `Library:ApplyNewElements()` exposes glass panels, liquid-glass toggles/buttons, highlight buttons, and shiny animated buttons on groupboxes.
- Nested tabboxes: `Groupbox:AddTabbox()` creates tabbed sections inside any groupbox, so compact category panels can hold their own sub-tabs.
- Layout modes: set `TabsMode = "Sidebar"` or `"Topbar"` and `TabStyle = "Card"` for card-like tab buttons.
- Sprite icon animation: use `Library:AnimateIconSprite(imageLabel, atlasInfo)` with atlas frames/size/columns and stop with `Library:StopIconSpriteAnimation(...)`.
- Advanced card dropdowns: set `CardDropdown = true` and provide `Cards` with thumbnails, bottom-bar transparency, icon, title, description, and per-card stroke options.
- The original `Library:Notify({...})` API still works and now accepts `Type`/`Variant`, `AccentColor`, `Progress`, `Actions`, `CloseButton`, and `Dismissible` fields.

See `Example.lua` for a complete notification and key-system showcase alongside the standard Obsidian element examples. The example loads this fork from `https://raw.githubusercontent.com/tanhoangviet/Obsidian-UI-Modded/refs/heads/main/`.
