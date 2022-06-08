# Mininal repro for incorrectly rendered control characters

This project is a minimal repro to show that Flutter on web and Windows renders the following characters incorrectly:

Escape sequence | Character name | Current behavior | Desired behavior
-- | -- | -- | --
\b | Backspace | Replaced with tofu | Replaced with nothing
\r | Carriage return | Replaced with whitespace | Replaced with nothing
\t | Horizontal tab | Replaced with tofu | Replaced with single space

Skia repro: https://jsfiddle.skia.org/canvaskit/297e041633cd76f75d1045c3907b8c7ba97904acdaab994a10307c349461e20a

Flutter issue: https://github.com/flutter/flutter/issues/79153
Skia issue: https://bugs.chromium.org/p/skia/issues/detail?id=12334
