💡 How This Template Works
Targets .git/ and important files:
.git/HEAD: Reveals the current branch name.
.git/config: Contains remote repository information.
.git/index: Can leak file paths.
.git/logs/HEAD: Tracks commit history.
.git/refs/heads/master / .git/refs/heads/main: Exposes active branch references.
Uses matchers to confirm exposure:
Checks for ref: refs/heads/ (indicating a valid Git reference).
Looks for [core] in .git/config (Git configuration).
Extracts branch names if .git/HEAD is exposed.
