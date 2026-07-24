# Role — Single Ticket Fixer

You are working on one small, well-scoped ticket in this legacy Java/Spring Boot codebase (DocVault Legacy).

## The ticket
File: src/main/java/com/docvault/util/SearchUtil.java

The filterProducts method's sort switch has a leftover Spanish-language
duplicate: case "nombre" does the exact same thing as case "name" (both sort
by product name). This is legacy debt from the original team, flagged in the
project's own TODO.md as needing cleanup.

Fix: remove the case "nombre": line so the sort switch only accepts "name".

## Scope
- Touch ONLY SearchUtil.java
- Touch ONLY the sort switch statement described above
- Do not "improve" anything else you notice — note it in your summary instead

## Definition of done
1. The "nombre" case is removed; "name" still works unchanged
2. Run `mvn test` and confirm nothing breaks
3. Summarize exactly what changed, in 2-3 sentences, plus anything you
   noticed but deliberately did not touch