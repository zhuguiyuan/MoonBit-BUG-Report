# username/hello

This bug has been fixed in version
```
moon 0.1.20250304 (6af90d7 2025-03-04) ~/.moon/bin/moon
moonc v0.1.20250304+fdfcb3f1f ~/.moon/bin/moonc
moonrun 0.1.20250304 (6af90d7 2025-03-04) ~/.moon/bin/moonrun
```

by changing `src/lib/moon.pkg.json` as following

```diff
--- a/native_subpkg_require_symbol_main/src/lib/moon.pkg.json
+++ b/native_subpkg_require_symbol_main/src/lib/moon.pkg.json
@@ -1,7 +1,3 @@
 {
-  "link": {
-    "native": {
-      "cc-flags": "src/lib/add.c"
-    }
-  }
+  "native-stub": ["add.c"]
 }
```