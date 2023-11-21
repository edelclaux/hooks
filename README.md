# Hooks

## Geonature post-checkout

### What is it ?

This post-checkout commit trigger a silent `geonature db status` after each checkout. In case of failure, it goes back to where you were, aka the previous git version.
This is a way to detect that your alembic state is dirty.

### How to setup

Post checkout hook is loaded from the file `.git/hooks/post-checkout`

To setup, you can duplicate the geonature-post-checkout to this directory, or use a symbolic link:

```bash
# ln example
ln GIT-HOOK-REPO/git-hook/geonature-post-checkout GEONATURE-REPO/.git/hooks/post-checkout
```

tadam.
