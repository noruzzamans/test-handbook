# Get Set Up for Testing

Welcome — this page helps new contributors get started quickly. If you're new to testing, follow the short onboarding checklist below, then choose the environment that best fits the kind of testing you want to do.

## Quick onboarding checklist

- [ ] Join the Test Team Slack channel: `#core-test` on Make WordPress Slack.
- [ ] Read the Guidelines for writing great Test Reports (`test-reports/`) and review examples.
- [ ] Find tickets that need testing (see links on the handbook home page) and pick one to reproduce or patch-test.
- [ ] Open a Test Report with clear steps, environment details, and expected vs actual results.

If you aren’t sure where to start, ask in `#core-test` and someone will point you to good issues for beginners.

## Core / Trac testing (Quick start)

This section explains how to test Core tickets and Trac-linked work. Core testing often involves reproducing issues, testing patches, or using the WordPress Playground when a GitHub PR is available.

1. Check the Trac ticket for an associated GitHub PR or a patch. If there is a GitHub PR, you can often use automated environments (see "WordPress Playground" below).
2. If the Trac ticket only has a `.patch`, follow the patch testing guidance in `test-reports/patch-testing.md`.
3. When you open a Test Report, include: WordPress version, browser, steps to reproduce, expected vs actual results, and screenshots or logs where helpful.
4. Link to the Trac ticket or GitHub PR in your report and add any relevant labels or keywords.

Useful resources:

- Test Reports: `test-reports/`
- Patch testing guide: `test-reports/patch-testing.md`
- Test Core Tickets with Playground: `test-core-tickets-with-playground.md`

## Gutenberg (Editor) testing — environment options

The Gutenberg editor has its own recommended environments. If you want to test editor PRs or the latest editor features, choose one of the options below.

### Hosted / quick testing

- Use a hosted sandbox (e.g., InstaWP, TasteWP) for quick checks without local setup.
- Use the WordPress Playground (see `test-core-tickets-with-playground.md`) for disposable, PR-driven test instances.

### Local environment (recommended for deeper testing)

Use this option to test pull requests or the bleeding-edge codebase locally.

1. Make sure you have [git](https://git-scm.com), [node](https://nodejs.org), and [npm](https://www.npmjs.com/get-npm) installed.
2. Install [Docker](https://www.docker.com) (recommended for `wp-env`).
3. Clone the Gutenberg repository: `git clone https://github.com/WordPress/gutenberg.git`.
4. From the Gutenberg directory run `npm install`.
5. Start the WordPress dev environment with `npm run wp-env start`.
6. Visit `http://localhost:8888` (username: `admin`, password: `password`).

Need more detailed installation instructions? See the Gutenberg contributing docs (`https://github.com/WordPress/gutenberg/blob/master/CONTRIBUTING.md`).

## Additional environment notes

- Hosted sites are useful for quick checks across real hosting environments; local environments are better for debugging and iterative work.
- Always include environment details (PHP version, MySQL/MariaDB, browser and version) in test reports.
- If you need help setting up a specific environment, ask in `#core-test` on Slack — include what you want to test and your platform (Windows, macOS, Linux).

Thank you for testing — your reports and feedback help improve WordPress for everyone.
