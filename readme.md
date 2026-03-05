### Working with webhook

```bash
# use base64 to encode your secret before go to add the webhook secret
echo -n "your-secret" | base64

# add the secret
kubectl edit secret argocd-secret -n argocd
# apiVersion: v1
# kind: Secret
# metadata:
#   name: argocd-secret
#   namespace: argocd
# type: Opaque
# data:
#   admin.password: <BASE64_PASSWORD>
#   admin.passwordMtime: <BASE64_TIME>
#   server.secretkey: <BASE64_KEY>

#   # Webhook secrets
#   webhook.github.secret: bXlXZWJob29rU2VjcmV0MTIz
#   webhook.gitlab.secret: bXlXZWJob29rU2VjcmV0MTIz


```