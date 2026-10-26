# Reef

**Find the moment. Build the cut. Keep shaping it.**

Reef is a native Mac media editor backed by a Python engine and an MCP interface. I'm building it around my underwater footage: a useful moment is often a few seconds inside a much longer clip, and finding it is only the beginning of making a film.

## The workflow

Reef's implemented systems cover searching for moments, inspecting their source intervals, assembling persistent multitrack cuts, and revising captions, titles, music, narration, and playback. Rendering and editable timeline export carry those decisions toward a finished video. The native editor and assistant tools operate on saved project state, so the edit can continue beyond a conversation.

## Engineering decisions

- **Keep source ranges explicit.** Selected moments retain their source identity and timing through edits, so the user can inspect the actual footage behind a choice.
- **Protect newer edits.** Revision-aware operations reject stale writes when the project has changed since a tool read it.
- **Separate source time from timeline time.** Trimming and playback changes affect where retained words and media belong; captions and audio need that mapping.
- **Connect output to an edit.** Delivery records associate rendered artifacts with the cut state they represent.

My work spans the native interactions and the engine beneath them. The product goal is consistent: a proposed edit should become something a person can inspect, change, save, and reopen.

**Built with:** Swift / SwiftUI, Python, SQLite, GRDB, FFmpeg, and MCP.

**Status:** active development; source is private. This page describes implemented capabilities. The public concept walkthrough uses the native interface with a staged conversation and proposed interactions; it is not a live end-to-end execution recording. Resolve timeline export and Grade Lab are separate workflows.

[Watch the 90-second concept walkthrough](https://henryhcooperr.github.io/henryhcooperr/#reef) · [Back to profile](../README.md)
