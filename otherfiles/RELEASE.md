# MyTimer Release Instructions

#### Last Update: 2023-06-30

1. Create the `release` branch under `dev`
2. Update all version tags
	1. `setup.py`
	2. `README.md`
	3. `otherfiles/version_check.py`
	4. `mytimer/params.py`
3. Update `CHANGELOG.md`
	1. Add a new header under `Unreleased` section (Example: `## [0.1] - 2022-08-17`)
	2. Add a new compare link to the end of the file (Example: `[0.2]: https://github.com/sepandhaghighi/mytimer/compare/v0.1...v0.2`)
	3. Update `dev` compare link (Example: `[Unreleased]: https://github.com/sepandhaghighi/mytimer/compare/v0.2...dev`)
4. Create a PR from `release` to `dev`
	1. Title: `Version x.x` (Example: `Version 0.1`)
	2. Tag all related issues
	3. Labels: `release`
	4. Set milestone
	5. Wait for all CI pass
	6. Need review
	7. Squash and merge
	8. Delete `release` branch
5. Merge `dev` branch into `main`
	1. Checkout to `main`
	2. `git merge dev`
	3. `git push origin main`
	4. Wait for all CI pass
6. Create a new release
	1. Target branch: `main`
	2. Tag: `vx.x` (Example: `v0.1`)
	3. Title: `Version x.x` (Example: `Version 0.1`)
	4. Copy changelogs
	5. Tag all related issues
7. Bump!!
8. Close this version issues
9. Close milestone