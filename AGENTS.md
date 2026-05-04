# Prometheus AI Analyzer — Design Repository

## Context

This repository contains the product design specification, not implementation code.

## Primary Document

- `2026-05-04-prometheus-ai-analyzer-design.md` — Full design spec (Phase 1 + Phase 2)

## Key Design Decisions (from spec)

| Component                | Technology                                                    |
| ------------------------ | ------------------------------------------------------------- |
| Backend                  | Python FastAPI                                                |
| AI                       | Ollama (local, primary) / OpenAI GPT-4o-mini (cloud fallback) |
| Charts                   | Plotly                                                        |
| Knowledge base (Phase 2) | PostgreSQL + pgvector                                         |
| Deployment               | Docker Compose                                                |

## Architecture Summary

- Grafana iframe calls FastAPI backend on dashboard page load
- Backend queries Prometheus for metrics
- AI module generates insight cards (anomaly detection via z-score/IQR, trend prediction via linear regression)
- Phase 2 adds RAG with internal运维 documents

## Language

Design documentation is in Traditional Chinese ( Mandarin).