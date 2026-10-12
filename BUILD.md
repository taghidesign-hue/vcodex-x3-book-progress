# Build notes

The patch was checked locally against the supplied `cpr-vcodex-master` source archive using `patch --dry-run -p1`. It has **not** been compiled or tested on an Xteink X3.

## Apply the patch

1. Obtain the matching CPR-vCodex source tree. Upstream repository: https://github.com/franssjz/cpr-vcodex
2. From the source root, apply this repository's patch:

   ```sh
   git apply /path/to/vcodex-x3-book-progress/patches/vcodex-x3-book-page-counter.patch
   ```

   Or, if using the `patch` utility:

   ```sh
   patch -p1 < /path/to/vcodex-x3-book-progress/patches/vcodex-x3-book-page-counter.patch
   ```

3. Build with the PlatformIO environment matching the device and source revision. The supplied source archive has `default_envs = default`; verify the board/environment settings before building.
4. Test the resulting firmware on the exact Xteink X3 hardware revision before relying on it.

## Important limitation

The current patch estimates whole-book page count from the first laid-out chapter and the EPUB's byte sizes. It keeps the displayed count from resetting at chapter boundaries, but the total is an estimate—not an exact pagination of every chapter. Font size, margins, orientation, and other layout settings can change the real page count. A precise total requires laying out/counting all EPUB spine sections (or maintaining per-section page-count data).

No `.bin` firmware is included yet.
