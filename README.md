# MVC 電影管理系統

本專案為一個使用 ASP.NET Core MVC 開發的電影資料管理系統，實作電影資料的新增、查詢、修改與刪除功能，並支援電影標題搜尋與類型篩選。

---

## 專案簡介

本系統提供基本的電影資料管理功能，使用者可以透過網頁介面管理電影資料，包括新增電影、查看電影詳細資料、編輯電影資訊、刪除電影資料，以及依照標題或電影類型進行查詢。

本專案主要用於練習 ASP.NET Core MVC 架構、Entity Framework Core 資料庫操作、Razor View 畫面呈現，以及基本 CRUD 流程設計。

---

## 技術棧

- ASP.NET Core MVC
- C#
- .NET 5
- Entity Framework Core
- SQL Server / LocalDB
- Razor View
- HTML / CSS / JavaScript

---

## 核心功能

- 電影資料新增
- 電影資料列表查詢
- 電影詳細資料查看
- 電影資料編輯
- 電影資料刪除
- 依電影標題搜尋
- 依電影類型篩選
- 使用 SeedData 建立初始電影資料

---

## 系統架構

本專案採用 MVC 架構：

- Model：定義電影資料結構與驗證標註
- View：使用 Razor View 呈現前端畫面
- Controller：處理使用者請求、CRUD 流程與資料查詢邏輯
- Data：透過 DbContext 管理資料庫連線與資料表操作

---

## 資料模型

主要資料表：

- Movie（電影）

Movie 欄位包含：

- Id
- Title（標題）
- ReleaseDate（釋出日期）
- Genre（種類）
- Price（價格）
- Rating（分級）

---

## 專案結構

```text
MVC--Movie
├── Controllers
│   ├── HelloWorldController.cs
│   ├── HomeController.cs
│   └── MoviesController.cs
├── Data
│   └── MvcMovieContext.cs
├── Migrations
├── Models
│   ├── ErrorViewModel.cs
│   ├── Movie.cs
│   ├── MovieGenreViewModel.cs
│   └── SeedData.cs
├── Views
├── wwwroot
├── Program.cs
├── Startup.cs
├── appsettings.json
├── appsettings.Development.json
└── MvcMovie.csproj
```

---

## 專案啟動方式

### 1. Clone 專案

```bash
git clone https://github.com/pengleo5422/MVC--Movie.git
cd MVC--Movie
```

### 2. 還原套件

```bash
dotnet restore
```

### 3. 建立或更新資料庫

```bash
dotnet ef database update
```

### 4. 執行專案

```bash
dotnet run
```

開啟瀏覽器：

```text
https://localhost:<port>
```

---

## 核心實作重點

- 使用 Entity Framework Core 進行資料庫操作
- 透過 MvcMovieContext 管理 Movie 資料表
- 使用 LINQ 實作電影標題搜尋
- 使用 SelectList 實作電影類型篩選
- 使用 MovieGenreViewModel 整合電影列表、搜尋條件與類型選單
- 使用 Data Annotation 設定欄位顯示名稱與資料格式
- 使用 SeedData 初始化電影測試資料
- 使用非同步方法處理資料庫查詢與儲存
- 使用 POST / Redirect 流程處理新增、修改與刪除

---

## 作者

https://github.com/pengleo5422
