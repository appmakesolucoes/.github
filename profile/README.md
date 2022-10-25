# Appmake Soluções

## Git Commit Message Conventions

Rules to most readable commits

### Commit Message Format
Each commit message consists of a **header**, a **body** and a **footer**.  The header has a special
format that includes a **type**, a **scope** and a **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The **header** is mandatory and the **scope** of the header is optional.

Any line of the commit message cannot be longer 100 characters! This allows the message to be easier
to read on GitHub as well as in various git tools.

### Type
Must be one of the following:

* **fit**: General changes not found in other types (prefer to use the specific types below)
* **build**: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
* **ci**: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
* **docs**: Documentation only changes
* **feat**: A new feature
* **fix**: A bug fix
* **perf**: A code change that improves performance
* **refactor**: A code change that neither fixes a bug nor adds a feature
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
* **test**: Adding missing tests or correcting existing tests

### Subject
The subject contains a succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize the first letter
* no dot (.) at the end

### Body
Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Footer
The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then used for this.

### Examples
<hr>

**Commit message with description and breaking change footer**
```
feat: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending other config files
```

**Commit message with ! to draw attention to breaking change**
```
feat!: send an email to the customer when a product is shipped
```

**Commit message with scope and ! to draw attention to breaking change**
```
feat(api)!: send an email to the customer when a product is shipped
```

**Commit message with both ! and BREAKING CHANGE footer**
```
fit!: drop support for Node 6

BREAKING CHANGE: use JavaScript features not available in Node 6.
```

**Commit message with no body**
```
docs: correct spelling of CHANGELOG
```

**Commit message with scope**
```
feat(lang): add Polish language
```

**Commit message with multi-paragraph body and multiple footers**
```
fix: prevent racing of requests

Introduce a request id and a reference to latest request. Dismiss
incoming responses other than from latest request.

Remove timeouts which were used to mitigate the racing issue but are
obsolete now.

Reviewed-by: Z
Refs: #123
```

### References
* https://www.conventionalcommits.org/
* https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md
