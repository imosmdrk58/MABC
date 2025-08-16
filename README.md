# Manga & Art Basics Club

一个基于 Next.js App Router + TypeScript + Supabase 的漫画艺术基础俱乐部官方网站。

## 功能特性

### 🏠 首页
- 俱乐部标题和地址信息
- 三个主要功能按钮：教程、比赛、作业提交
- 16:9 海报占位区域

### 📚 教程页面
- 四个分类：数字艺术、快速素描、素描、色彩
- 教师可上传视频教程
- 学生可提交作业
- 支持视频播放和文件上传

### 🏆 比赛页面
- 显示已发布的比赛列表
- 管理员和教师可创建/编辑比赛
- 支持奖项设置和发布状态管理

### 👥 关于页面
- 俱乐部介绍文案
- 显示所有教师和管理员信息
- 管理员可在线编辑教师姓名

### 🔐 认证系统
- 邮箱密码注册/登录
- 魔法链接登录
- 角色权限管理（admin/staff/student）

### 🛠️ 管理后台
- 用户角色管理
- 教程内容管理
- 比赛创建和编辑
- 作业评分和反馈
- 文件下载管理

## 技术栈

- **前端**: Next.js 15 + TypeScript + Tailwind CSS
- **后端**: Supabase (Auth + Database + Storage)
- **UI组件**: Radix UI + shadcn/ui
- **状态管理**: React Hooks
- **认证**: Supabase Auth
- **数据库**: PostgreSQL with RLS
- **文件存储**: Supabase Storage

## 快速开始

### 1. 克隆项目

```bash
git clone <repository-url>
cd manga-art-club
```

### 2. 安装依赖

```bash
npm install
```

### 3. 环境配置

复制 `env.example` 为 `.env.local` 并填写你的 Supabase 配置：

```bash
cp env.example .env.local
```

编辑 `.env.local` 文件：

```env
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key
NEXT_PUBLIC_SITE_URL=http://localhost:3000
```

### 4. 数据库设置

在 Supabase 中执行以下 SQL 脚本：

1. 运行 `supabase/schema.sql` 创建数据表和 RLS 策略
2. 运行 `supabase/storage-policies.sql` 创建存储策略

### 5. 启动开发服务器

```bash
npm run dev
```

访问 [http://localhost:3000](http://localhost:3000) 查看网站。

## 项目结构

```
manga-art-club/
├── app/                    # Next.js App Router 页面
│   ├── admin/             # 管理后台页面
│   ├── auth/              # 认证相关页面
│   ├── about/             # 关于页面
│   ├── competitions/      # 比赛页面
│   ├── tutorials/         # 教程页面
│   ├── profile/           # 个人资料页面
│   └── page.tsx           # 首页
├── components/             # React 组件
│   ├── ui/                # UI 基础组件
│   ├── auth-form.tsx      # 认证表单
│   └── navbar.tsx         # 导航栏
├── lib/                    # 工具库
│   ├── supabase/          # Supabase 配置
│   └── types.ts           # TypeScript 类型定义
├── supabase/               # 数据库脚本
│   ├── schema.sql         # 数据库表结构
│   └── storage-policies.sql # 存储策略
└── middleware.ts           # 路由中间件
```

## 数据库设计

### 主要数据表

- **profiles**: 用户资料和角色
- **tutorials**: 教程内容
- **competitions**: 比赛信息
- **submissions**: 作业提交
- **reviews**: 作业评分

### 权限控制

- **学生**: 查看内容、提交作业
- **教师**: 上传教程、评分作业
- **管理员**: 完全访问权限

## 部署

### Vercel 部署

1. 连接 GitHub 仓库到 Vercel
2. 设置环境变量
3. 部署

### 其他平台

项目支持部署到任何支持 Next.js 的平台。

## 开发指南

### 添加新功能

1. 在 `lib/types.ts` 中定义类型
2. 创建相应的页面组件
3. 更新导航和权限控制

### 样式修改

项目使用 Tailwind CSS，所有样式都在组件中通过原子类定义。

### 数据库修改

1. 修改 `supabase/schema.sql`
2. 在 Supabase 中执行 SQL
3. 更新相关的 TypeScript 类型

## 贡献

欢迎提交 Issue 和 Pull Request！

## 许可证

MIT License
# Force deployment
