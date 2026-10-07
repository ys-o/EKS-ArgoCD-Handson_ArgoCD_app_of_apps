# EKS-ArgoCD-Handson_ArgoCD_app_of_apps

## 概要

Argo CDの子Applicationを定義するリポジトリです。
親Applicationから、Web/APアプリ、External Secrets Operator（ESO）、AWS Load Balancer Controllerの3個の子Applicationを管理します。

## 4リポジトリの役割

| リポジトリ | 役割 |
|---|---|
| [Terraform](https://github.com/ys-o/EKS-ArgoCD-Handson_Terraform) | AWSリソースの構築とArgo CDの初期導入 |
| [Argo CDアプリケーション定義（本リポジトリ）](https://github.com/ys-o/EKS-ArgoCD-Handson_ArgoCD_app_of_apps) | Web/AP、ESO、AWS Load Balancer Controllerの子Application定義 |
| [Web/APマニフェスト](https://github.com/ys-o/EKS-ArgoCD-Handson_Application_manifests) | Deployment、Service、Ingress、SecretStore、ExternalSecret |
| [Web/APアプリ資材](https://github.com/ys-o/EKS-ArgoCD-Handson_Application) | PHP、Dockerfile、Nginx設定、GitHub Actionsワークフロー |

## ファイル構成

```text
ko_application_install/
├── web_ap.yaml            # Web/APアプリのマニフェストを管理
├── external_secrets.yaml  # ESOをHelm Chartから導入・管理
└── ingress_alb.yaml       # AWS Load Balancer ControllerをHelm Chartから導入・管理
```
