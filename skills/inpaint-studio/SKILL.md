---
name: inpaint-studio
description: Open a reusable Korean inpainting mask editor in the Codex right-side conversation panel and prepare marked images or mask PNG files for precise AI image editing. Use whenever the user says 인페인트 스킬, 인페인트, 인페인트 스튜디오, 수정할 부분을 표시해줘, 마스크를 만들어줘, or asks to crop, select, mark, and edit only part of an image.
---

# Inpaint Studio

Open the bundled editor immediately when the user wants to mark or mask part of an image.

## Open the editor

1. Copy `assets/inpaint-studio.html` unchanged to a new `inpaint-studio.html` file in the current thread-scoped visualization directory.
2. Return the inline visualization directive for the copied file so the editor appears in the right-side panel.
3. Tell the user to load or paste a photo, mark the target, press **코덱스로 보내기**, and paste it into the Codex input with `⌘V` or `Ctrl+V`.

## Preserve the workflow

- Preserve file selection, drag-and-drop, clipboard paste, crop, rectangle, ellipse, polygon, brush, eraser, undo, clear, mask PNG, marked preview, and clipboard copy.
- Close an in-progress polygon on double-click.
- Cancel only the in-progress selection when the user presses `Esc`.
- Preserve the mask convention: the marked or white area is editable and the black area is preserved.
- Treat **코덱스로 보내기** as copying the marked image to the clipboard. Do not download automatically.
- Keep all interface text in Korean unless the user asks otherwise.

## Continue with image editing

When the user pastes the marked image and describes a replacement, edit only the marked area. Preserve the camera, composition, structure, objects, materials, and pixels outside the marked area as aggressively as possible.

If the browser blocks clipboard access, direct the user to allow clipboard permission or use **표시 이미지** as a manual fallback.
