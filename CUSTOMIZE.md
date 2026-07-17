# Customize your alien GitHub profile

This package is already structured as a GitHub profile repository. You only need to replace the placeholders and push it.

## 1. Replace these values

Search all files for `YOUR_` and replace:

| Placeholder | Replace with |
|---|---|
| `YOUR_GITHUB_USERNAME` | Your exact GitHub username |
| `YOUR_LINKEDIN` | The final part of your LinkedIn profile URL |
| `YOUR_X_HANDLE` | Your X/Twitter handle, without `@` |
| `YOUR_HUGGINGFACE` | Your Hugging Face username |
| `YOUR_PORTFOLIO` | Your portfolio domain prefix, or replace the full URL |
| `YOUR_EMAIL@example.com` | Your public contact email |

Also update the four repository slugs in the **Active Missions** table if your repo names differ.

On macOS/Linux, you can replace the GitHub username everywhere with:

```bash
find . -type f \( -name '*.md' -o -name '*.yml' \) -exec sed -i.bak 's/YOUR_GITHUB_USERNAME/your-real-username/g' {} +
find . -name '*.bak' -delete
```

## 2. Create the special profile repository

On GitHub, create a **public** repository whose name exactly matches your GitHub username. For example, user `abdul` must create the repository `abdul/abdul`.

Then run from this folder:

```bash
git init
git add .
git commit -m "launch alien profile"
git branch -M main
git remote add origin git@github.com:YOUR_GITHUB_USERNAME/YOUR_GITHUB_USERNAME.git
git push -u origin main
```

## 3. Activate the animated contribution serpent

The included workflow runs automatically after the first push and then once per day. If it cannot publish the `output` branch:

1. Open the profile repository on GitHub.
2. Go to **Settings → Actions → General**.
3. Under **Workflow permissions**, choose **Read and write permissions**.
4. Open **Actions → Generate Alien Contribution Serpent → Run workflow**.

The contribution graph, streak, and summary cards need only the username replacement; no tokens or secrets are required for their public versions.

## 4. Make the profile honest and sharp

- Keep only tools you can discuss in an interview.
- Link every active mission to a real repository.
- Pin the same four projects on your GitHub profile.
- Add benchmark tables and profiler screenshots inside the performance repos.
- Delete social buttons for accounts you do not use.

The four custom insignia are intentionally playful engineering identities—not claims of external awards. GitHub's real Achievements automatically appear in the Achievements area of your profile.

