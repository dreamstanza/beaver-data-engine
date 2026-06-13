# 小狸 Last-100m Passage Data Engine

**末端100米机器人通行数据引擎**

> 不是存视频，而是把真实末端通行经验沉淀成机器人可学习、可评测、可授权的数据资产。

A real-world passage data engine for last-100-meter robot delivery, covering routes, terrains, obstacles, failures, human interactions, privacy processing, licensing, and data product packaging.

面向末端100米机器人配送场景，系统化管理真实路线、地形障碍、动态障碍、人工接管、异常失败、隐私处理、授权许可和数据产品包，服务机器人通行大脑、世界模型训练、benchmark评测和客户场景报告。

---

## Live Demo

**[Open V0.2 Prototype](https://dreamstanza.github.io/beaver-data-engine/)**

## V0.2 Features

### Core Modules (10 pages)

| Module | Description |
|--------|-------------|
| **Dashboard 驾驶舱** | 10 business KPI cards + charts + roadmap |
| **Assets 资产列表** | 20 mock assets with 13 filter dimensions |
| **Missions 采集任务** | Collection mission management |
| **Collectors 采集员** | Courier/rider/engineer management |
| **Routes 路线库** | Route passability scoring & ranking |
| **Privacy 合规授权** | Privacy processing & consent tracking |
| **Reports 报告中心** | Auto-generated insight reports |
| **Create 创建资产** | 8-step asset creation wizard |
| **Packages 产品包** | Commercial data product packages |
| **Files 文件管理** | Video file upload & asset linking |

### Key Capabilities

- **localStorage Persistence**: All data persists across page refreshes
- **Multi-CDN Fallback**: jsDelivr → unpkg → cdnjs for reliability
- **Scene & Failure Taxonomy**: 13 scene tags, 17 blocker tags, 8 failure phases
- **Business Notes**: Every asset includes commercial judgment fields
- **Quality Rules**: 9-dimensional quality scoring with weighted average
- **Hash Routing**: Direct URL access to any module via `#dashboard`, `#missions`, etc.

### Data Coverage (Mock)

- 20 data assets (10 robot test + 10 courier POV)
- 5 collection missions (planned/collecting/completed)
- 6 collectors (couriers, engineers, operators)
- 5 routes with passability scores
- 3 product packages
- 2 pre-built reports
- 10 video files

## How to Run Locally

```bash
# Simply open the file in a browser
open beaver-deploy/index.html

# Or use a local server
cd beaver-deploy
python -m http.server 8899
# Open http://localhost:8899
```

## How to Deploy to GitHub Pages

```bash
# Push to GitHub
git add beaver-deploy/index.html
git commit -m "update: V0.2 prototype"
git push origin master

# Deploy (if using GitHub CLI)
gh api repos/{owner}/{repo}/pages -X POST  # or configure in repo settings
```

## Architecture

Single-file React 18 application with Babel Standalone for in-browser JSX compilation. All dependencies loaded via CDN with multi-source fallbacks.

```
index.html
├── CDN Scripts (React 18 + ReactDOM + Babel Standalone)
├── CSS (inline styles, loading/error screens)
├── Icons (SVG icon system, 40+ icons)
├── Charts (CSS-based bar/pie charts)
├── Constants (asset types, terrain tags, scene tags, blocker tags, etc.)
├── Mock Data (assets, missions, collectors, routes, products, files, reports)
├── localStorage Persistence Layer
├── UI Primitives (Badge, Card, Button, Input, Select, etc.)
├── Page Components (12 pages)
└── Main App (hash routing + state management)
```

## Roadmap

| Feature | Status |
|---------|--------|
| 采集任务 Collection Missions | V0.2 ✓ |
| 路线库 Route Library | V0.2 ✓ |
| 采集员管理 Collectors | V0.2 ✓ |
| 隐私合规 Privacy & Consent | V0.2 ✓ |
| 报告生成 Report Generator | V0.2 ✓ |
| 商业化产品包 Products | V0.2 ✓ |
| localStorage 持久化 | V0.2 ✓ |
| PDF导出 Export | V0.3 |
| OSS云存储上传 | V0.3 |
| 权属存证 On-chain | V0.3 |
| API后端 Backend | V0.3 |
| 多用户权限 RBAC | V0.3 |

## Changelog: V0.1 → V0.2

- **Product Positioning**: Renamed from "小狸数据资产引擎" to "小狸 Last-100m Passage Data Engine"
- **Dashboard**: Upgraded from simple stats to 10-card Business Cockpit with strategic tagline
- **New Modules**: Added Missions, Collectors, Routes, Privacy, Reports (5 new pages)
- **Taxonomy**: Added 13 scene tags, 17 blocker tags, 8 failure phases
- **Mock Data**: Expanded from 10 to 20 assets (added 10 courier POV scenarios)
- **Persistence**: Added localStorage for all data entities
- **Search/Filter**: Enhanced with 13 filter dimensions including blocker tags and scene tags
- **Create Asset**: Renamed "Token 代币化" to "Rights & Proof 权属与存证"
- **Quality Rules**: Added 9-dimensional quality scoring with sub-scores
- **Business Notes**: Added commercial judgment fields to asset detail
- **CDN Stability**: Added multi-CDN fallback (jsDelivr → unpkg → cdnjs)
- **UI**: Chinese-first bilingual, empty states, V0.2 roadmap card, Reset Demo Data button

## Tech Stack

- **Frontend**: React 18 (single-file, Babel Standalone)
- **Charts**: Pure CSS (no chart library)
- **Icons**: Custom SVG icon system
- **Storage**: localStorage (V0.2 prototype)
- **Hosting**: GitHub Pages

## License

Internal prototype — 小狸科技 (XiaoLi Tech)
