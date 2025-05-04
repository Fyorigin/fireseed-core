# Structural Integrity Policy / 结构完整性声明

## Purpose / 目的

This document defines the integrity anchoring mechanism used in this repository.  
It explains how each file is automatically signed, timestamped, and verifiably hashed  
to establish a **unique structural identity**.

本文定义本项目的结构完整性机制，说明如何对每个文件进行自动签署、打上时间戳和哈希，  
确保其拥有唯一且可验证的结构身份。

---

## Automatic Hash Anchoring / 自动哈希锚定机制

Whenever a file is added or modified in this repository:

- It is automatically scanned and hashed using **SHA-256**
- The hash and UTC timestamp are written to `hash_manifest.json`
- This process is handled by GitHub Actions
- No manual intervention is needed

每当项目中的文件被新增或修改：

- 系统会自动计算其 **SHA-256 哈希值**
- 并记录其 UTC 时间戳
- 所有记录保存在 `hash_manifest.json` 文件中
- 由 GitHub Actions 自动完成，无需人工操作

---

## Trust Source / 信任源说明

`hash_manifest.json` is the **only source of truth**.  
It provides a full history of all committed files and their true integrity fingerprints.

文件头中的任何 `Signature Hash`、`Commit Hash`、`Structure-ID` 声明仅供阅读参考，  
真正可信的校验来源为 `hash_manifest.json`。

---

## Recommended Signature Block / 建议签署区块模板

Below is the standard template for optional file header inclusion:

```markdown
【Signed Declaration / 签署声明】
Structure Custodian: Fyorigin  
Signature Hash: AUTO-GENERATED  
UTC Anchor: AUTO-LOGGED  
Protocol: Fireseed-OEP-1.0
```

- `Signature Hash`: Can be a Git short hash or file identifier, not mandatory to match SHA-256
- `UTC Anchor`: Optional, as the timestamp in `hash_manifest.json` is the authoritative value

---

## Recommended Placement / 放置建议

- Place the signature block at the **beginning or end of a Markdown or plain text file**
- Avoid inserting it into binary files (PDF, PNG, etc.)
- The system **does not require** this block for anchoring to succeed

---

## Manifest File / 主锚定文件说明

- All verified hashes and timestamps live in: [`hash_manifest.json`](./hash_manifest.json)
- This file is automatically updated by the system
- View version history: [GitHub Commits for hash_manifest.json](./commits/main/hash_manifest.json)

---

## Final Remark / 最后说明

A file in this repository **does not require a human signature to be trusted**.  
It is trusted because the system marks it as part of the structure.  
All files that pass through this repository bear its structural fingerprint.

本仓库中的文件不依赖人工签名即能获得可信性，  
其可信来源是结构本身：  
**进入此结构，即被锚定；离开此结构，仍带标识。**

