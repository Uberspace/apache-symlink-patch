# Apache Symlink Race Condition Vulnerability Patch

There is a race condition vulnerability in Apache httpd, starting from version 2.2.
The race condition still exists with httpd 2.4. It is unlikely to be fixed in future
versions, because the vulnerability is documented. It allows a malicious user to
serve arbitrary files from nearly anywhere on a server that isn't protected by strict
OS level permissions, even when instructing httpd to only follow symlinks if the owner
matches (SymLinksIfOwnerMatch). This patch fixes that vulnerability. It also contains proof
of concept code to check if the vulnerability has been fixed in the build.

# Credits

We want to thank [Bluehost](https://github.com/bluehost/apache-symlink-patch) for
their work on this patch for httpd 2.2. We just slightly updated the patch to also
work with upstream httpd 2.4.

# License

Apache v2.0
