# LLMO Writer

LLMO Writer は **Large Language Model Optimization (LLMO)** を意識した記事生成・編集・評価ツールです。  
検索上位サイトの構造を参考にしつつ、ユーザーがアウトラインを編集し、AIと共同で最適化された記事を作成できます。  

---

## 🚀 特徴
- **検索上位サイトの構造収集**  
  Serper.dev API を利用して検索結果のサイト構造をJSON化。  
- **アウトライン編集の中間層**  
  LLMに任せきりではなく、人間が記事構造を選択・編集可能。  
- **AIによる記事生成（Gemini API）**  
  アウトラインに基づき、セクションごとに記事本文を生成。  
- **編集・再生成・評価機能**  
  - セクションごとに編集可能  
  - ワンクリックでAIにリライト依頼  
  - AIによる評価・改善提案を受けられる  
- **独自データ統合**  
  ユーザーの持つ一次データを記事に組み込み、権威性を向上。  
- **出力形式**  
  - HTML（マークアップ済みプレビュー）  
  - JSON-LD（FAQスキーマ対応）  
  - LLM TXT（ログ保存用）  

---

## 🛠️ 使用技術
- Python (Flask)  
- Google Gemini API  
- Serper.dev API  
- HTML + JavaScript (UI)  

---

## 📂 インストール方法
```bash
# クローン
git clone https://github.com/kuubo360/llmo-writer.git
cd llmo-writer

# 必要なライブラリをインストール
pip install -r requirements.txt

# 環境変数を設定（例：Windows PowerShell）
setx SERPER_API_KEY "your_serper_api_key"
setx GEMINI_API_KEY "your_gemini_api_key"

# サーバーを起動
python app.py
