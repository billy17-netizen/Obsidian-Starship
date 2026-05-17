# Obsidian UI Library Modded

**Documentation:** https://docs.mspaint.cc/obsidian

**Source code to documentation site:** https://github.com/mspaint-cc/docs.mspaint.cc/tree/main/content/obsidian

This fork keeps the familiar Obsidian/Linoria-style API while adding quality-of-life features for polished script hub UIs.

## Modded highlights

- Notification variants: `Library:NotifyInfo`, `Library:NotifySuccess`, `Library:NotifyWarning`, and `Library:NotifyError` add sensible icons and accent colors automatically.
- Actionable notifications: pass an `Actions` array with button text and callbacks to let users confirm, cancel, or open follow-up UI directly from a toast.
- Progress notifications: pass `Progress = 0` and update it later with `Notification:SetProgress(0.5)` for long-running jobs.
- The original `Library:Notify({...})` API still works and now accepts `Type`/`Variant`, `AccentColor`, `Progress`, and `Actions` fields.

See `Example.lua` for a complete notification showcase alongside the standard Obsidian element examples.
