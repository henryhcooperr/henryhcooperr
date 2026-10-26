# COOPR / Content Brain

**A creator workspace for making better decisions about what to make—and how to make it.**

COOPR brings together video analysis, writing tools, and interactive creative workflows. I explored how a person could move between chat, media, and documents while keeping their own choices central to the work.

## Implemented workflows

- **Compare candidate clips.** Upload several clips, track their analysis, and request a ranked comparison with reasons and tradeoffs.
- **Turn critique into a working document.** Review a clip's suggestions, accept the useful ones, and create a document containing those selected edits.
- **Develop a creative direction.** Generate hook alternatives, select one, and use it to guide scripts, shot planning, and filming notes.
- **Refine the writing.** Score draft text against a creator-style profile and use rewriting or platform-adaptation tools to explore alternatives.

These are individual implemented workflows; they are not all one continuous production pipeline.

## Engineering and interface choices

The frontend uses structured results and explicit loading, selection, and error states. API routes reuse tools also available through MCP. Creator-scoped data informs analysis and writing, while accepted suggestions remain explicit user decisions during the document handoff.

The separate public interface prototype explores a shared workspace for chat, documents, a media library, and creative feedback, with navigable detail views and persistent interface state.

**Built with:** React / TypeScript, Python, PostgreSQL, and MCP. The standalone prototype uses React with in-browser Babel.

**Status:** experimental and unfinished. The private backend contains implemented capabilities; the public prototype demonstrates interaction design and does not establish a production backend connection.

[Explore the interface prototype](https://github.com/henryhcooperr/coopr-prototype) · [Back to profile](../README.md)
