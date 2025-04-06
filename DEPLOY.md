# Deploying MealFrame with Cloudflare Pages

MealFrame is designed to work seamlessly with [Cloudflare Pages](https://pages.cloudflare.com/) for fast, free, and secure hosting.

---

## 1. Fork the Repo

Start by forking this repository to your GitHub account.

---

## 2. Set Up Cloudflare Pages

1. Log in to your [Cloudflare dashboard](https://dash.cloudflare.com/).
2. Navigate to **Pages** and click **"Create a project"**.
3. Choose **"Connect to Git"** and select your forked MealFrame repo.
4. Configure the build settings:

   - **Framework Preset**: `None`
   - **Build command**: `hugo`
   - **Build output directory**: `public`

5. Set the **Environment variable** to use Hugo extended:

   | Variable name | Value        |
   |---------------|--------------|
   | `HUGO_VERSION` | `0.123.8` *(or latest)* |

---

## 3. Enable Submodules

After project creation:

1. Go to your Pages project settings.
2. Under **"Build settings" > "Git"**, enable **"Git submodules"**.

This ensures the Ananke theme (and any other future submodules) are pulled in during the build.

---

## 4. Trigger a Build

Once the setup is complete, any push to your repo will trigger a new build on Cloudflare Pages.

You’ll receive a preview URL and a production domain (which you can customize under custom domains).

---

## 5. Optional: Set Up a Custom Domain

In your Cloudflare dashboard, add a custom domain to your Pages project. Cloudflare will handle the DNS and SSL automatically.

---

## Troubleshooting

- **Theme not found?** Make sure you’ve initialized submodules:
  
  ```bash
  git submodule update --init --recursive
  ```

- **Hugo version errors?** Confirm `HUGO_VERSION` is correctly set in the build environment variables.

---

Enjoy fast and easy deployments with Cloudflare Pages!