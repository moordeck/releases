# Moordeck Releases

Official signed desktop installer mirrors, SHA-256 verification sums, release notes, and public issue tracker for **Moordeck** — a local-first anti-detect fingerprint browser and standard Local API engine.

**Moordeck** 官方安装包分发镜像、SHA-256 校验清单、版本更新日志与公开问题反馈仓库。

---

## Download Channels / 下载渠道

| Channel / 渠道 | Entry / 地址 | Notes / 说明 |
| :--- | :--- | :--- |
| **Primary Download Page** | [moordeck.com/download](https://moordeck.com/download) | macOS Apple Silicon DMG, Linux x86_64 headless runner, and on-demand signed anti-detect Chromium kernels |
| **GitHub Releases Mirror** | [github.com/moordeck/releases/releases](https://github.com/moordeck/releases/releases) | Signed & notarized client archives with `SHA256SUMS.txt` |
| **Homebrew Cask (macOS)** | `brew install --cask moordeck/tap/moordeck` | Maintained in [moordeck/homebrew-tap](https://github.com/moordeck/homebrew-tap) |
| **Public Documentation** | [moordeck/docs](https://github.com/moordeck/docs) | Local API, `mdk` CLI, diagnostic methodology, and Agent Skill |

---

## Integrity & Signature Verification / 签名与完整性校验

### 1. macOS Developer ID & Apple Notarization
Verify Gatekeeper signature and notarization ticket after installing `Moordeck.app`:

```bash
spctl -a -vvv -t exec /Applications/Moordeck.app
```

### 2. Artifact SHA-256 Checksums
Each release includes `SHA256SUMS.txt`. Verify downloaded installers locally:

```bash
shasum -a 256 -c SHA256SUMS.txt
```

### 3. Release & Signed Kernel Manifests
Live release metadata and cryptographic verification manifests:
- Client latest manifest: `https://moordeck.com/api/v1/releases/client/latest.json`
- Signed anti-detect Chromium kernel manifest: `https://moordeck.com/api/v1/releases/kernels/manifest.json`

---

## Diagnostics & Resources / 在线检测与文档

- **70-Vector Fingerprint Check**: <https://moordeck.com/check>
- **Proxy IP Purity Inspector**: <https://moordeck.com/ip>
- **AI & Claude Environment Check**: <https://moordeck.com/ai-check>
- **Agent Discovery**: <https://moordeck.com/llms.txt> · <https://moordeck.com/mcp>

---

## Feedback & Bug Reports / 问题反馈

Please open an issue in [moordeck/releases/issues](https://github.com/moordeck/releases/issues) with your client version, OS version, kernel version, and reproduction steps.
