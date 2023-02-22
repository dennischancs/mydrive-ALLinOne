# MyDrive-All in One
deploy alist to [fly.io](https://fly.io)

1. Fork [mydrive-allinone](https://github.com/dennischancs/mydrive-allinone) to your own GitHub repository.
2. Get a Fly API token with `flyctl auth token`.
3. Go to your newly created repository on GitHub and select Settings.
4. Go to Secrets and create a secret called FLY_API_TOKEN with the value of the token from step 2.
5. Clone the repository to your local machine to edit `fly.toml` and change `app = "mydrive-allinone"` to your `APP_NAME`.
6. Run `flyctl launch` to create an APP which called `APP_NAME`. Say `N` to create `.dockerignore` file.
7. Run `flyctl volumes create data --size 1 --app APP_NAME` to create a 1GB persistent storage space.
8. Commit your changes and push them up to GitHub.

[Demo](https://mydrive-allinone.fly.dev)

## Reference
* [在 Fly.io 上部署 alist 网盘程序 - 春风吹 - 浅秋枫影的博客](https://cuojue.org/read/deploy-alist-in-flyio.html#%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C)
* [Continuous Deployment with Fly.io and GitHub Actions · Fly Docs](https://fly.io/docs/app-guides/continuous-deployment-with-github-actions/)


## From alist-render

### Deploy Alist to Render
[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

### database
You may need to use another remote MySQL database as instance restarts will lose data.
Recommended Free MySQL Databases:
- https://db4free.net/
- https://remotemysql.com/
- https://www.freesqldatabase.com/

### password
The initial password is randomly generated, and you can get it by checking the `logs`.