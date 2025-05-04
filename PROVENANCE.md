# Provenance Statement / 结构来源声明

## Project Identity

**Repository:** `fireseed-core`  
**Structure Custodian:** Fyorigin  
**Protocol:** Fireseed-OEP-1.0  
**Anchoring Started:** 2025-05-01  
**Integrity System Activated:** 2025-05-04  
**Primary Mechanism:** GitHub Actions + SHA-256 hash + UTC timestamp

---

## Purpose / 项目目的

This repository is not a software repo in the traditional sense. It is a structural model:  
a signed and time-anchored system intended to define, prove, and preserve protocol-originated intellectual infrastructure.

本仓库非传统意义的软件代码库，而是一个结构型模型：  
用于签署、时间锚定，并证明协议起源下的知识性结构资产。

---

## File Anchoring System / 文件锚定机制

Every file in this repository is:
- Automatically hashed using **SHA-256**;
- Timestamped in **UTC**;
- Recorded inside [`hash_manifest.json`](./hash_manifest.json);
- Managed by a GitHub Actions automation routine (`.github/workflows/hash-manifest.yml`);

仓库内所有文件均：
- 自动以 SHA-256 哈希生成指纹；
- 使用 UTC 标准时间记录锚定时间；
- 登记于 [`hash_manifest.json`](./hash_manifest.json) 文件；
- 并由 GitHub Actions 自动执行，无人工干预。

---

## Signing Structure / 签署结构

Selected files include embedded headers:
```
Signed Declaration / 签署声明  
Structure Custodian: Fyorigin  
Signature Hash: SWITCH-XXXXXX  
UTC Anchor: YYYY-MM-DDTHH:MMZ  
Protocol: Fireseed-OEP-1.0
```

声明段手动嵌入文件顶部，表示该结构的原始起点与托管者，形成**主观签署**，与 `hash_manifest.json` 形成**主观+客观双锚定体系**。

---

## Workflow Trace / 自动化追踪链

All automated commits to `hash_manifest.json` are made by:  
`github-actions[bot]`, and can be inspected via the [GitHub commit history](https://github.com/Fyorigin/fireseed-core/commits/main/hash_manifest.json)

每一次 `hash_manifest.json` 的自动更新均由 GitHub 官方机器人执行，确保中立性与审计性。

---

## Future Extensions / 未来扩展

- OpenTimestamps anchoring  
- IPFS / Arweave permanent anchoring  
- Embedded file headers auto-generation  
- Version signature chain (`STRUCTURE-ID` + `HASH-ID` binding)

未来可扩展链上时间戳、不可篡改存储、结构 ID 签链等模块，构建全面结构证明体系。

---

## Endnote / 附言

This repository is a work of structure, not just software.

本项目不是代码，而是结构。所有可验证的锚定，都是它自己的呼吸。

<!-- STRUCTURE-ID: sha256:266cc15a9182405ab0f4baead6a16950674046e3db27a7de402ce4c5e8c90d7d uploaded_by: Fyorigin at 2025-05-04T15:16:27Z -->
