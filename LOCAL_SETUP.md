# Binary Adder Lab: local setup (Windows / PowerShell)

`source/index.html` is the complete source (HTML, CSS, and JavaScript).
`output/index.html` is the standalone published web page. These are identical because the site has no build step.

## Put the page into your existing Vite project

1. Download this ZIP and extract it. In VS Code, open your `logic-adder` folder.
2. Back up the project's current `index.html` if you want to keep the React starter page.
3. Copy `source/index.html` into the root of `logic-adder`, replacing `logic-adder/index.html`.
4. Open a PowerShell terminal in `logic-adder` and run:

```powershell
npm install
npm run dev
```

Open the local URL displayed by Vite (usually http://localhost:5173/). To create the local web output:

```powershell
npm run build
```

Vite places the generated page in `dist/index.html`. You can also open `output/index.html` directly in a browser without Vite.

## Commit the source and output

From the `logic-adder` folder:

```powershell
git status
# Only if the folder is not a Git repository:
git init
git add index.html
git add -f dist/index.html
git commit -m "Add interactive binary adder page"
git remote -v
```

If `origin` is already configured, push your current branch with `git push -u origin HEAD`. If there is no remote, create a repository on GitHub and add its URL as `origin` before pushing. `dist` is commonly ignored by Vite's `.gitignore`, so `git add -f` includes the generated page deliberately.
