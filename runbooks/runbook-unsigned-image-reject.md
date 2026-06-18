
# Runbook: Admission Webhook Reject - Unsigned Image

## Triệu chứng

- Pod không được tạo

- Error: admission webhook "policy.sigstore.dev" denied the request

## Nguyên nhân

Image chưa được ký bằng Cosign hoặc ký sai key.

## Xử lý

1. Kiểm tra image có signature chưa:

   cosign verify --key signing/cosign.pub <image>

2. Nếu chưa ký: chạy lại CI pipeline để build + sign

3. Kiểm tra ClusterImagePolicy đúng public key chưa:

   kubectl get clusterimagepolicy -o yaml

