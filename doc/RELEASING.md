## Release checklist

- Check the Travis log from the latest build(s) and make sure nothing strange is
  happening, such as errors or warning that did not result in a command exiting
  with nonzero status.
- Update the `CHANGES` file.
- `grep` for the previous version number. Replace all occurences with the new
  version number. This should include `META`, `opam`, `version.ml`, `README.md`,
  and the manual.
- Tag (`tag -a`) the release and push the tag.
- Submit the release to OPAM.
- After release is accepted in OPAM, make a GitHub release for it as well. List
  the changes there. The reason this is done after OPAM is that the OPAM release
  may have to be amended before it is accepted.