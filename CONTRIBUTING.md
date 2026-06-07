# one-time
git remote add upstream https://github.com/juanfont/headscale.git
git fetch upstream --tags

# each sync cycle — track RELEASE TAGS, not upstream/main
git fetch upstream --tags
git checkout -b sync/v0.30.0 main
git merge v0.30.0          # resolve conflicts ONCE, here
# build + test, then PR into your main
