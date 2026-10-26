# Reef Grade Lab

**Underwater color tools built around the shot—and the person grading it.**

Grade Lab is a specialized toolchain for analyzing underwater footage and developing editable grades in DaVinci Resolve. It grew from the practical problems in my own footage: changing exposure, shifting water color, haze, and subjects that need different treatment from the background.

The profile compares original GP-Log2 footage from my Catalina dive with my selected saved grade: a Garibaldi approaching through sunlit kelp. The six-second comparison uses matched source frames and follows the saved result’s slow-motion timing. The camera side has no creative grade or camera-conversion LUT. The eight-second interface demo includes this comparison and a final still hold. The browser layout is restaged; this demonstration does not run a new grading operation or reconstruct the historical recipe.

## The workflow

The MCP toolset includes inspecting a timeline, proposing a grading recipe, applying supported editable native processing, capturing the result, and revising retained versions. Comparison and review tools help judge a moving shot rather than relying on a single attractive frame.

Additional analysis and planning tools use camera telemetry, image measurements, temporal changes, and relative depth to inform exposure, white balance, and underwater restoration. These are distinct capabilities; their native integration varies by processing route.

## Engineering decisions

- **Bind a treatment to its source.** Plans and feedback identify the selected segment and version, so a decision about one cut cannot silently become a decision about another.
- **Leave useful controls behind.** Supported native grading routes retain editable processing for further adjustment in Resolve.
- **Evaluate changes through time.** Exposure and color treatment need to account for transitions, noise, and visible pumping.
- **Check generated color math.** NumPy reference implementations provide comparisons for generated DCTL and Fusion processing.
- **Retain specific feedback.** Recorded preferences and similar-shot retrieval preserve the context behind a creative choice.

**Built with:** Python, NumPy, DaVinci Resolve scripting, Fusion, DCTL, and MCP.

**Status:** ongoing development, with documented native grading sessions on selected footage. Newer restoration and planning components have separate validation boundaries. Source is private. The public comparison demonstrates the retained result and review interface; it does not demonstrate the full MCP grading process.

[Watch the Grade Lab review](https://henryhcooperr.github.io/henryhcooperr/#grade-lab) · [Back to profile](../README.md)
