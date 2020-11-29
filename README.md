# mvn-reproducer

Sample project that shows maven-compiler-plugin does not handle removed source directories correctly.

## Steps to reproduce

1. Run `mvn test` and see the build fail due to test failures
1. Delete `src`
1. Run `mvn test` again

The second build will show the same test failures as the first one despite all test classes having been removed.
