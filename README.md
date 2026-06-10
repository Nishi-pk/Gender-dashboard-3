# UAE Gender Balance Dashboard

## How to update the data (no coding needed)

### Your repository should contain these files:
```
data.csv          ← your data file (update this to refresh the dashboard)
build.py          ← the script that converts CSV → dashboard (don't touch)
index.html        ← the live dashboard (auto-generated, don't edit manually)
.github/
  workflows/
    build.yml     ← the automation rule (don't touch)
```

---

## To update the dashboard with new data:

### Step 1 — Go to your GitHub repository
Open your repository on github.com

### Step 2 — Upload the new data.csv
1. Click on `data.csv` in the file list
2. Click the **pencil icon** (Edit) — or click the three-dot menu → **"Upload file"**
3. If uploading: drag your new `data.csv` onto the page
4. Scroll down and click **"Commit changes"**

### Step 3 — Wait ~2 minutes
GitHub automatically:
- Detects that `data.csv` changed
- Runs `build.py` to regenerate `index.html`
- Pushes the new `index.html` back to your repo
- GitHub Pages picks up the change

### Step 4 — Check your live site
Refresh your GitHub Pages URL. The dashboard will show the updated data.

---

## To trigger a rebuild manually (without changing data.csv):
1. Go to your repository on GitHub
2. Click **Actions** tab
3. Click **"Rebuild Dashboard"** in the left sidebar
4. Click **"Run workflow"** → **"Run workflow"**

---

## CSV format requirements
Your `data.csv` must keep the same column names:
- `Report`
- `Country Name`
- `Year of Report`
- `Latest` (value must be `"Latest"` for the most recent row per indicator)
- `Indicator (English)`
- `Indicator Description`
- `Rank` / `Previous Rank`
- `Score`
- `First Globally` / `First Arab` / `First GCC` / `First G20`
- `Main Entity (English)`
