1) Go to the ``bin/`` directory at the top-level
   of an up-to-date worktree of the ``brltty-website`` repository.
2) Check that there's nothing that might get
   accidentally committed to the repository.
   The easiest way to do this is to use this command::

     git status -s -uno

   Ideally, there should be no output. 
   Resolve any issues that you find.

3) Update the source worktree so that the latest documentation will be built::

     ./updsrc

4) Build the documentation::

     ./upddocs

5) Stage the updated documents in the git cache::

     ./chkdocs -u

   There shouldn't be any output.
   If you see any ``git status`` output lines
   then those are for files that weren't handled.
   You'll need to resolve them.

6) Commit the changes to the repository::

     git commit

7) Publish the updated documentation::

     git push origin

The update won't be immediate.
There's a daily cron job on the server which will eventually pick it up.

