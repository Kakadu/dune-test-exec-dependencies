###### Question

How to add a dependency from tests to my executables? I want to make `dune test` call `dune build @install` automatically

```
✗ dune clean && dune test
Done: 5/7 (jobs: 1)File "test.t/run.t", line 1, characters 0-0:
         git (internal) (exit 1)
(cd _build/.sandbox/7cf28892c09af3683bfb99bc44ccf139/default && /usr/bin/git --no-pager diff --no-index --color=always -u ../../../default/test.t/run.t test.t/run.t.corrected)
diff --git a/../../../default/test.t/run.t b/test.t/run.t.corrected
index 7a8053d..3afe00f 100644
--- a/../../../default/test.t/run.t
+++ b/test.t/run.t.corrected
@@ -1,6 +1,12 @@
   $ dune build
   $ echo $PATH
+  /home/kakadu/asp/dune-exec-cram-demo/_build/install/default/bin:.................................................grafted
 $ ./asdf.exe
   $ which asdf
+  [1]
   $ asdf
+  asdf: not found
+  [127]
   $ qwe
+  qwe: not found
+  [127]
````
