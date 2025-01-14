---
image: /generated/articles-docs-paths-get-bounding-box.png
title: getBoundingBox()
crumb: "@remotion/paths"
---

_Part of the [`@remotion/paths`](/docs/paths) package. Available from v3.3.40_

Returns the bounding box of the given path, suitable for calculating the `viewBox` value that you need to pass to an SVG.

The bounding box is the smallest rectangle which can contain the shape in full.

```tsx twoslash title="get-bounding-box.ts"
import { getBoundingBox } from "@remotion/paths";

const boundingBox = getBoundingBox(
  "M 35,50 a 25,25,0,1,1,50,0 a 25,25,0,1,1,-50,0"
);
// { x1: 35, x2: 85, y1: 24.999999999999993, y2: 75 };
```

This function will throw if the SVG path is invalid.

## `BoundingBox` type

In TypeScript, you can get the shape of the return value by importing the `BoundingBox` type:

```ts twoslash
import type { BoundingBox } from "@remotion/paths";
```

## See also

- [`@remotion/paths`](/docs/paths)
- [Source code for this function](https://github.com/remotion-dev/remotion/blob/main/packages/paths/src/get-bounding-box.ts)
