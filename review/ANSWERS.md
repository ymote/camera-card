# Camera Card Demo 1.1.0 review

Reviewer: Codex (also author of this publication repair). Scope: static L0 sample on macOS; no camera functionality or phone acceptance.

1. **Claims:** The listing explicitly calls this a static rendering and publishing sample. `page.card` draws the camera storyboard, Chinese modes, zoom labels and artwork. It does not claim to capture photos.
2. **Platforms/category:** `photo-video` describes the subject. Only macOS is listed. Native hidden-window rendering passed at 406 by 776 and 900 by 800 logical points.
3. **Grants:** Empty capabilities and host lists, no storage grant and no agent. The bundle is local data and artwork.
4. **Deception:** This imitates a camera layout, not a permission, payment or sign-in sheet. The store name, subtitle and description disclose that it is a static demo. It does not request camera access.
5. **Assistant instructions:** No agent files or assistant-directed instructions. Source comments describe the static design.
6. **Abuse/private individuals:** None. The screen uses generic camera labels and neutral artwork.
7. **Route:** Pass for review as a static sample. GitHub proof and installation still need independent checks before catalog admission. This is not a fully functional camera app.

## Native findings

The first native capture exposed half-size child geometry. The exported page declared 406 by 776 points, but its screen and every child used half-scale geometry. The new source restores those data coordinates and dimensional style values to the declared artboard, without editing the L0 structure.

Obsolete `self:resources/service/NotoSansSC-*.ttf` paths were refused by the current gate. The kit now selects admitted built-in LXGW WenKai fonts; Chinese text was inspected in native captures with system font discovery disabled.

The corrected screen is readable at its 406 by 776 point artboard. A larger window leaves unused space: this is a fixed-artboard rendering sample, not a responsive camera interface. Controls remain static by design. No polished-interaction score is claimed.

Historical tags, signatures and images remain unchanged. The listing points to a new actual capture, not the old screenshot.
