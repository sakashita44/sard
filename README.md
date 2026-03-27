# sard

A structured-analysis framework designed for reproducible research data management.

**S**tructured **A**nalysis for **R**esearch **D**ata — 実験データ解析における暗黙的な依存関係を宣言的に記述し、再現性と追跡性の確保を志向するフレームワーク。

## コンセプト

- **属性ベースのデータアクセス**: データ属性の定義と統一的なインターフェースの提供により、パスに依存しない直感的なデータアクセスを可能にする
- **データ依存関係の明示化**: 処理単位間のデータ依存を宣言的に記述し、変更の影響範囲を追跡可能にする
- **スキーマに基づくデータ構造の維持**: データ属性とテーブルスキーマの宣言的定義により、規約に沿ったデータ構造を促す
- **再現性を志向するパイプライン管理**: データバージョン管理との連携と実行記録の保持により、解析状態の再現を支援する

## セットアップ

```bash
# 依存インストール
uv sync

# pre-commitフックの有効化
uv run pre-commit install

# テスト実行
uv run pytest
```

## 技術スタック

| カテゴリ                 | ツール                     |
| ------------------------ | -------------------------- |
| クエリエンジン           | DuckDB                     |
| DataFrame                | Polars                     |
| 型定義・バリデーション   | Pydantic, Pandera, pyright |
| DAG構造                  | networkx                   |
| パイプライン・データ管理 | DVC                        |
| 設定ファイル             | ruamel.yaml                |
| CLI                      | Typer                      |

## ライセンス

MIT
