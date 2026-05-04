# Prometheus AI Analyzer

Grafana iframe AI 監控分析系統設計規格。

## 文件

- `2026-05-04-prometheus-ai-analyzer-design.md` — 完整設計規格（Phase 1 + Phase 2）

## 摘要

AI 即時解讀 Grafana Dashboard 監控數據，自動生成異常偵測、趨勢預測、優化建議卡片。

| 元件 | 技術 |
|------|------|
| 後端 | Python FastAPI |
| AI | Ollama（本地）/ GPT-4o-mini（雲端備援）|
| 圖表 | Plotly |
| 知識庫（Phase 2）| PostgreSQL + pgvector |
| 部署 | Docker Compose |