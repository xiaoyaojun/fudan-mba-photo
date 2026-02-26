# 复旦MBA摄影协会网站部署包

## 快速部署指南（国内可用）

### 方案一：Cloudflare Pages（推荐，免费，国内可访问）

1. 打开 https://dash.cloudflare.com （注册/登录）
2. 点击 Pages → Create a project → Upload assets
3. 上传本 zip 文件
4. 部署完成后获得 `xxx.pages.dev` 链接
5. 可绑定自己的域名

### 方案二：阿里云 OSS（稳定，低费用）

1. 登录阿里云控制台 → OSS
2. 创建 Bucket，选择「静态网站托管」
3. 上传 index.html
4. 绑定域名（可选）

### 方案三：腾讯云 COS（类似阿里云）

1. 登录腾讯云控制台 → 对象存储 COS
2. 创建存储桶，开启静态网站
3. 上传文件

### 方案四：自有服务器（Nginx）

```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /var/www/fudan-mba-photo;
    index index.html;
}
```

---

网站文件：index.html
技术栈：HTML + Tailwind CSS + GSAP 动画
