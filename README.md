# From workspace to production

An interactive walkthrough of one automation change moving from an
OpenShift Dev Spaces workspace to production through Ansible Automation Platform.

The main story follows one storage change through eight steps:

1. **Write** — open the workspace, write the playbook, lint before commit
2. **Approve** — pull request checks (yamllint, Ansible Lint, Molecule, execution
   environment parity), then CODEOWNERS review by the owning team
3. **Run** — `--check` first, then apply, and the same path for every team

Two optional appendices follow.

**Explore by domain** — the same path for five more domains, each
teaching something different:

- **Network** — check mode returns the exact CLI lines a resource module would send
- **Linux** — Ansible Lint rule `package-latest`, and rolling updates with `serial`
- **Windows** — Molecule's idempotence test catches a shell one-liner
- **Cloud** — push protection blocks a pasted key; AAP injects credentials at run time
- **Database** — where check mode can't help: pre-flight analysis, backup, approval node, restore path

**Go deeper** — one screen on what Molecule actually does: the scenario
config, a `molecule test` run through create / converge / idempotence /
verify / destroy, and the assertions that check the end state.

## Presenting

Open `index.html` in a browser. Arrow keys or Page Up/Down move between steps;
Home and End jump to the start and finish. Each step holds until you advance it.
After the last main step, Next becomes "Explore by domain", and after the
last domain it becomes "Go deeper".

## Hosting

Single self-contained file with no build step. Fonts load from Google Fonts,
so it needs a network connection.

Team names, repository paths, hostnames and versions are illustrative.
