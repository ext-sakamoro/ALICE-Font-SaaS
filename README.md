# ALICE-Font SaaS

Parametric metafont SDF glyph renderer API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Font |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/render` | グリフレンダリング |
| `POST /api/v1/generate` | パラメトリックフォント生成 |
| `GET  /api/v1/families` | フォントファミリー一覧 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
