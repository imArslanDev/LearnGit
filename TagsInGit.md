### Tag in Git

You can mark a particular commit as a release using a **Tag**.

---

## 2 Types of Tags

1. **Annotated Tags** *(Recommended for official releases)*
2. **Lightweight Tags** *(Best for temporary or private use)*

> **Note:** All changes should ideally go through pull requests before tagging.

---

## Annotated Tag

1. Stores metadata (tagger name, email, date, and message).
2. More informative and secure.
3. Can be GPG signed.
   - **Note:** When a file, email, or piece of code is described as **"can be GPG signed,"** it means it is compatible with **GPG (GNU Privacy Guard)** to verify authenticity.
4. Highly recommended for production releases.

**Example:**

```bash
git tag -a v1.0.0 -m "Release Version 1.0.0"
```

---

## Lightweight Tag

1. Acts as a pointer to a specific commit.
2. Does not store any extra metadata.
3. Best used for temporary, local, or private markers.

**Example:**

```bash
git tag v1.1
```