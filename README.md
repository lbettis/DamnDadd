# damndadd.com

Homepage for Damn Dadd, the Bettis Family. It sends visitors to
[God First, Money Wise](https://app.damndadd.com/) first, then
[Black Movies Trivia](https://blacktrivia.damndadd.com/), and shows the
[Damn Dadd YouTube channel](https://www.youtube.com/channel/UCwl6vyhCfb38VtslrUGMfEg).

It's a single static page (`index.html`) with no build step.

## Deploying

Every push to `main` uploads the site to the HostIgnition server through
`.github/workflows/deploy.yml`. It can also be run by hand from the Actions tab.

Set these repository secrets once (Settings → Secrets and variables → Actions):

| Secret | Value |
| --- | --- |
| `FTP_SERVER` | FTP host from cPanel, e.g. `ftp.damndadd.com` |
| `FTP_USERNAME` | cPanel FTP account username |
| `FTP_PASSWORD` | That FTP account's password |
| `FTP_SERVER_DIR` | Folder damndadd.com is served from, ending in `/`, e.g. `public_html/` |

## Updating videos

The featured player always plays the channel's uploads. To add a new video to the
thumbnail grid, add its ID, title and length to the `VIDEOS` list in `index.html`.

## Preview locally

```bash
npx serve .
```
