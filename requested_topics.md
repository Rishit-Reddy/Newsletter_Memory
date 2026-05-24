# Requested Topics Queue

Add topics you specifically want the newsletter to cover. The routine reads this file at the start of every run.

## How it works
- If this file contains one or more **pending** topics (lines starting with `- [ ]`), the routine picks the **topmost pending topic**, writes that day's digest about it, and marks the line as `- [x]` with the date it was covered.
- If every line is already checked off (or the Pending section is empty), the routine falls back to its normal logic: continue an existing multi-day arc, or auto-select the next logical topic.
- You can add arc hints in parentheses, e.g. `- [ ] Diffusion models (3-day arc)` to request a deeper, multi-day treatment.
- You can add focus hints, e.g. `- [ ] U-Net (focus: skip connections and medical segmentation)`.

## Pending

<!-- Add topics below. Examples (uncomment / replace):
- [ ] Neural Radiance Fields (NeRF) foundations
- [ ] DINOv2 self-supervised vision representations (2-day arc)
- [ ] The Chinchilla scaling laws paper — distilled review
-->

## Completed

<!-- The routine moves checked-off topics here automatically with the date covered. -->
