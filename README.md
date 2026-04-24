# MVC 電影管理系統（MVC Movie Web App）

本專案為一個以 ASP.NET Core MVC 建構的電影資料管理系統，實作完整的 MVC 架構與資料庫整合流程，提供基本的資料新增、查詢、修改與刪除功能（CRUD）。

## 專案簡介

本系統提供使用者透過網頁介面管理電影資料，涵蓋資料操作與基本查詢功能。
主要目的在於展示後端開發能力，包括 MVC 架構設計、ORM 使用，以及請求處理流程。

## 技術棧

* ASP.NET Core MVC
* C#
* Entity Framework Core
* SQL Server / LocalDB
* Razor Pages
* HTML / CSS / JavaScript

## 功能

* 電影資料 CRUD（新增 / 查詢 / 修改 / 刪除）
* 表單資料驗證（Model Validation）
* 使用 Entity Framework Core 進行資料庫操作
* MVC 架構分層（Model / View / Controller）
* 基本搜尋或篩選（若有實作）

## 系統架構

* Model
  定義電影資料結構與資料庫 schema，並透過 EF Core 進行 ORM 映射。

* View
  使用 Razor 模板負責前端畫面呈現與使用者輸入。

* Controller
  負責處理 HTTP 請求、執行商業邏輯，並協調 Model 與 View 的資料流。

## 資料層設計

* 使用 Entity Framework Core 作為 ORM
* 採用 Migration 管理資料庫版本
* 基本流程：
  Request → Controller → DbContext → Database → 回傳 View

## 專案啟動方式

### 1. 下載專案

```bash id="cl1"
git clone https://github.com/pengleo5422/MVC--Movie.git
cd MVC--Movie
```

### 2. 套用資料庫 Migration

```bash id="cl2"
dotnet ef database update
```

### 3. 執行專案

```bash id="cl3"
dotnet run
```

瀏覽器開啟：

```
https://localhost:<port>
```


## 核心實作重點

* 使用 EF Core DbContext 管理資料庫存取
* 實作 MVC Model Binding 與表單驗證流程
* Controller 採用標準 CRUD action pattern
* 使用 POST / Redirect / GET 流程避免重複提交


## 作者

https://github.com/pengleo5422
