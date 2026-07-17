# Git Rebase

## Definition
**Git Rebase** is a command that moves or reapplies your commits on top of another branch, creating a cleaner and more linear commit history.

> Think of it as: **"Take my changes and place them on top of the latest branch."**

---

## How It Works

Suppose your branches look like this:

```text
main:    A ── B ── C
               \
feature:        D ── E
```

Meanwhile, `main` gets a new commit:

```text
main:    A ── B ── C ── F
               \
feature:        D ── E
```

Run:

```bash
git checkout feature
git rebase main
```

Result:

```text
main:    A ── B ── C ── F
                         \
feature:                  D' ── E'
```

Git reapplies commits `D` and `E` on top of the latest `main`.

---

## Example 1

Update your feature branch with the latest changes from `main`:

```bash
git checkout feature
git rebase main
```

---

## Example 2

If a conflict occurs during rebase:

```bash
# Fix the conflict in your files
git add .

# Continue the rebase
git rebase --continue
```

If you want to cancel the rebase:

```bash
git rebase --abort
```