# MyDrive-All in One
deploy alist to [fly.io](https://fly.io)

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