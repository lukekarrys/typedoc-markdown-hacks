```sh
# install deps
npm install
# run example which will build two folders and diff them
npm run example
```

````patch
========================================
asserts-template-literal.md
========================================
- Original
+ Modified

@@ -32,3 +32,3 @@

- \`sha512-$\{string\}\`
+ `` `sha512-${string}` ``

@@ -50,3 +50,3 @@

- asserts i is \`sha512-$\{string\}\`
+ `` asserts i is `sha512-${string}` ``

@@ -104,3 +104,3 @@

- i is \`sha512-$\{string\}\`
+ `` i is `sha512-${string}` ``

========================================
constructor-override.md
========================================
- Original
+ Modified

@@ -22,3 +22,4 @@

- `LRUCache<
+ ```ts
+ LRUCache<
    CacheFetchContext,
@@ -26,3 +27,4 @@
    CacheFetchContext
- >.constructor`
+ >.constructor
+ ```

========================================
index-signature.md
========================================
- Original
+ Modified

@@ -10,68 +10,70 @@

-  \[`key`:
-   \| \`·$\{string\}·$\{string\}·$\{string\} $\{string\}\`
-   \| \`git·$\{string\}·$\{string\}·$\{string\} $\{string\}\`
-   \| \`·$\{string\}·$\{string\} $\{string\}\`
-   \| \`git·$\{string\}·$\{string\} $\{string\}\`
-   \| \`file·$\{string\}·$\{string\} $\{string\}\`
-   \| \`remote·$\{string\}·$\{string\} $\{string\}\`
-   \| \`workspace·$\{string\}·$\{string\} $\{string\}\`
-   \| \`file·$\{string\} $\{string\}\`
-   \| \`remote·$\{string\} $\{string\}\`
-   \| \`workspace·$\{string\} $\{string\}\`\]:
-   \| \`optional ·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`optional git·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`optional ·$\{string\}·$\{string\}\`
-   \| \`optional git·$\{string\}·$\{string\}\`
-   \| \`optional file·$\{string\}·$\{string\}\`
-   \| \`optional remote·$\{string\}·$\{string\}\`
-   \| \`optional workspace·$\{string\}·$\{string\}\`
-   \| \`optional file·$\{string\}\`
-   \| \`optional remote·$\{string\}\`
-   \| \`optional workspace·$\{string\}\`
-   \| `"optional MISSING"`
-   \| \`dev ·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`dev git·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`dev ·$\{string\}·$\{string\}\`
-   \| \`dev git·$\{string\}·$\{string\}\`
-   \| \`dev file·$\{string\}·$\{string\}\`
-   \| \`dev remote·$\{string\}·$\{string\}\`
-   \| \`dev workspace·$\{string\}·$\{string\}\`
-   \| \`dev file·$\{string\}\`
-   \| \`dev remote·$\{string\}\`
-   \| \`dev workspace·$\{string\}\`
-   \| `"dev MISSING"`
-   \| \`peer ·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`peer git·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`peer ·$\{string\}·$\{string\}\`
-   \| \`peer git·$\{string\}·$\{string\}\`
-   \| \`peer file·$\{string\}·$\{string\}\`
-   \| \`peer remote·$\{string\}·$\{string\}\`
-   \| \`peer workspace·$\{string\}·$\{string\}\`
-   \| \`peer file·$\{string\}\`
-   \| \`peer remote·$\{string\}\`
-   \| \`peer workspace·$\{string\}\`
-   \| `"peer MISSING"`
-   \| \`peerOptional ·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`peerOptional git·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`peerOptional ·$\{string\}·$\{string\}\`
-   \| \`peerOptional git·$\{string\}·$\{string\}\`
-   \| \`peerOptional file·$\{string\}·$\{string\}\`
-   \| \`peerOptional remote·$\{string\}·$\{string\}\`
-   \| \`peerOptional workspace·$\{string\}·$\{string\}\`
-   \| \`peerOptional file·$\{string\}\`
-   \| \`peerOptional remote·$\{string\}\`
-   \| \`peerOptional workspace·$\{string\}\`
-   \| `"peerOptional MISSING"`
-   \| \`prod ·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`prod git·$\{string\}·$\{string\}·$\{string\}\`
-   \| \`prod ·$\{string\}·$\{string\}\`
-   \| \`prod git·$\{string\}·$\{string\}\`
-   \| \`prod file·$\{string\}·$\{string\}\`
-   \| \`prod remote·$\{string\}·$\{string\}\`
-   \| \`prod workspace·$\{string\}·$\{string\}\`
-   \| \`prod file·$\{string\}\`
-   \| \`prod remote·$\{string\}\`
-   \| \`prod workspace·$\{string\}\`
-   \| `"prod MISSING"`
+ ```ts
+  [key:
+   | `·${string}·${string}·${string} ${string}`
+   | `git·${string}·${string}·${string} ${string}`
+   | `·${string}·${string} ${string}`
+   | `git·${string}·${string} ${string}`
+   | `file·${string}·${string} ${string}`
+   | `remote·${string}·${string} ${string}`
+   | `workspace·${string}·${string} ${string}`
+   | `file·${string} ${string}`
+   | `remote·${string} ${string}`
+   | `workspace·${string} ${string}`]:
+   | `optional ·${string}·${string}·${string}`
+   | `optional git·${string}·${string}·${string}`
+   | `optional ·${string}·${string}`
+   | `optional git·${string}·${string}`
+   | `optional file·${string}·${string}`
+   | `optional remote·${string}·${string}`
+   | `optional workspace·${string}·${string}`
+   | `optional file·${string}`
+   | `optional remote·${string}`
+   | `optional workspace·${string}`
+   | "optional MISSING"
+   | `dev ·${string}·${string}·${string}`
+   | `dev git·${string}·${string}·${string}`
+   | `dev ·${string}·${string}`
+   | `dev git·${string}·${string}`
+   | `dev file·${string}·${string}`
+   | `dev remote·${string}·${string}`
+   | `dev workspace·${string}·${string}`
+   | `dev file·${string}`
+   | `dev remote·${string}`
+   | `dev workspace·${string}`
+   | "dev MISSING"
+   | `peer ·${string}·${string}·${string}`
+   | `peer git·${string}·${string}·${string}`
+   | `peer ·${string}·${string}`
+   | `peer git·${string}·${string}`
+   | `peer file·${string}·${string}`
+   | `peer remote·${string}·${string}`
+   | `peer workspace·${string}·${string}`
+   | `peer file·${string}`
+   | `peer remote·${string}`
+   | `peer workspace·${string}`
+   | "peer MISSING"
+   | `peerOptional ·${string}·${string}·${string}`
+   | `peerOptional git·${string}·${string}·${string}`
+   | `peerOptional ·${string}·${string}`
+   | `peerOptional git·${string}·${string}`
+   | `peerOptional file·${string}·${string}`
+   | `peerOptional remote·${string}·${string}`
+   | `peerOptional workspace·${string}·${string}`
+   | `peerOptional file·${string}`
+   | `peerOptional remote·${string}`
+   | `peerOptional workspace·${string}`
+   | "peerOptional MISSING"
+   | `prod ·${string}·${string}·${string}`
+   | `prod git·${string}·${string}·${string}`
+   | `prod ·${string}·${string}`
+   | `prod git·${string}·${string}`
+   | `prod file·${string}·${string}`
+   | `prod remote·${string}·${string}`
+   | `prod workspace·${string}·${string}`
+   | `prod file·${string}`
+   | `prod remote·${string}`
+   | `prod workspace·${string}`
+   | "prod MISSING"
+ ```
````
