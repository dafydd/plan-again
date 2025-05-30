# plan-again
Make Unix-style .plan files useful again.

A shell script to sync your `~/.plan` file to your GitHub profile repository as `README.md`.  
Useful for creating a public, self-maintaining status message on your GitHub profile page.

## Usage
Edit or create `~/.plan` with your message to the world.

``replan`` - Shows the diff between ~/.plan and README.md

``replan -c`` - Copies ~/.plan into README.md, commits and pushes it

## Features

- Pulls the latest `main` branch from your GitHub profile repo
- Compares `~/.plan` to `README.md`
- Warns if your working tree is dirty
- Only pushes changes when run with `-c`
- Enforces strict file permissions (`chmod 600`) for `~/.plan`
- Requires successful SSH authentication to GitHub
- Timestamps commits in ISO 8601 UTC

## Installation

1. ``git clone https://github.com/YOUR_USERNAME/plan-again.git``
2. Edit `replan` to replace the definition of `DEST_REPO` with the path to the locally checked-out version of the repository having your GitHub.com username. 
3. ``cp plan-again/replan ~/bin/replan``
4. ``chmod +x ~/bin/replan``

## Licence
This project is licensed under the [GNU General Public License](LICENSE).
Free forever, on the condition that it stays free.

© 2025 Dafydd Rees
