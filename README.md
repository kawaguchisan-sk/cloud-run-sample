# cloud-run-sample

## Overview

[Cloud Run](https://cloud.google.com/run) を [ko](https://www.cncf.io/projects/ko/), [skaffold](https://skaffold.dev/docs/), [Artifact Registry](https://cloud.google.com/artifact-registry/docs/overview), [Cloud Deploy](https://cloud.google.com/deploy/docs/overview) を用いてビルドからデプロイまで行うサンプルです。  

[こちらの記事 ※ TODO]() にて、解説を行っています。

## Directories

```
.
├── app: Go 製アプリケーションファイル
│   ├── v1
│   │   ├── go.mod
│   │   └── main.go
│   └── v2
│       ├── go.mod
│       └── main.go
│
├── deploy: Cloud Deploy 用の設定ファイル
│   ├── Makefile
│   └── deploy.yaml
│
└── manifest: Cloud Run 用の設定ファイル
    ├── Makefile
    ├── build_v1.json
    ├── build_v2.json
    ├── service.yaml
    ├── skaffold_v1.yaml
    └── skaffold_v2.yaml
```
