# 适配中国网络环境的Supabase部署

### 原理:
每日定时爬取`supabase`仓库并且将最新的`docker image`上传到**阿里云**仓库,将原`docker-compose.yml`的**image**部分都换成**国内**仓库

```bash
git clone https://github.com/sanbei101/supabase-china-host.git -b mirror
```
```bash
cp .env.example .env
```
```
sudo docker compose -f ./docker-compose-mirror.yml up -d
```