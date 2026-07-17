### Tag in Git
You can mark a particular commit as release using Tag.

---

### 2 Types of Tags
1. **Annotated Tags** (Recommended for official releases)
2. **Lightweight Tags** (Best for temporary or private use)

*Note: All changes should ideally go through pull requests before tagging.*

---

### Annotated Tag
1. Stores Metadata (tagger name, email, date, and message).
2. More informative and secure.
3. Can be GPG Signed.
   
   *Note: When a file, email, or piece of code is described as "can be GPG signed," it means it is compatible with GPG (GNU Privacy Guard) to verify authenticity.*

4. Highly recommended for production releases.

**Example:**
```bash
git tag -a v1.0.0 -m "Release Version 1.0.0"