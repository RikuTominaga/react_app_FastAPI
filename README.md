# similar item searcher  

## 開発環境・ライブラリー情報
- Windows 11
- Python 3.9.7
- react 18.3.1
- axios 1.7.7
- sentence-transformers 3.2.0
- langchain-community 0.3.2
- faiss-cpu 1.9.0
- fastapi 0.115.4

## 構築手順
1. プロジェクト作成  
`npx create-react-app react-info-app`
2. backendフォルダーをreact-info-appに新規作成
3. レポジトリーにあるapp.pyもしくはmain.pyとinfo.dbをbackendに配置
4. App.jsとApp.cssをレポジトリーにあるApp.jsとApp.cssに書換
5. レポジトリーにあるDockerフォルダーをreact-info-appに配置
6. 仮想環境の作成  
`python -m venv venv`  
7. 仮想環境のアクティベート  
`.\venv\Scripts\activate`
8. ライブサーバーの実行
`uvicorn main:app --host 0.0.0.0 --port 8000 --reload`
9. ライブラリーのインストール

## ディレクトリ構成
```
.  
└── react-info-app/ 
    ├── .venv/  
    │   └── ...  
    ├── node_modules/  
    │   └── ...  
    ├── bakend/ #新規作成  
    │   ├── venv
    │   │   └──...   
    │   ├──　main.py #レポジトリーにあるmain.py配置  
    │   └── info.db #レポジトリーにあるinfo.dbを配置
    ├── docker
    │   ├── backend
    │   │   ├──Dockerfile
    │   │   └──requirements.txt
    │   └── frontend
    │       └──  Dockerfile
    ├── public/    
    │   └── ...  
    ├── src/
    │   ├── App.css #書換  
    │   ├── App.js #書換  
    │   ├── App.test.js  
    │   ├── index.css  
    │   ├── index.js  
    │   └── ...  
    ├── .gitignore  
    ├── package-lock.json  
    ├── package.json  
    └── READNE.md
```
