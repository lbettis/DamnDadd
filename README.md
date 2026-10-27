# damndadd.com

Homepage for Damn Dadd, the Bettis Family. It sends visitors to
[God First, Money Wise](https://app.damndadd.com/) first, then
[Black Movies Trivia](https://blacktrivia.damndadd.com/), and shows the
[Damn Dadd YouTube channel](https://www.youtube.com/channel/UCwl6vyhCfb38VtslrUGMfEg).

It's a single static page (`index.html`) with no build step.

## Deploying

The site is hosted on HostIgnition and deployed with cPanel's Git Version Control,
which keeps a clone of this repo. `.cpanel.yml` copies the site files into
`public_html`. The first deploy saves the page that was there before as
`index-before-damndadd-site.html`.

After pushing to `main`:

1. In cPanel, open **Git Version Control** and click **Manage** on **Damn Dadd**.
2. On the **Pull or Deploy** tab, click **Update from Remote**.
3. Click **Deploy HEAD Commit**.

## Updating videos

The featured player always plays the channel's uploads. To add a new video to the
thumbnail grid, add its ID, title and length to the `VIDEOS` list in `index.html`.

## Preview locally

```bash
npx serve .
```
