---
"@astrojs/astro2tsx": patch
---

Fixes `<?xml ... ?>` and other processing instructions in templates. They used to fail with "expected `?>` but instead found `>`" and drop the rest of the template. They are now read as bogus comments ending at the first `>`, the way the HTML tokenizer and the Astro compiler read them.
