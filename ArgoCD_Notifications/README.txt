
# Installation of triggers from the catalog

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/notifications_catalog/install.yaml

# Do changes for email and smtp password and create secret

kubectl apply -f secret-smtp.yaml

# In argocd-notifications-cm change the ArgoCDURL i.e. change the IP to latest Public IP.i

kubectl apply -f argocd-notifications-cm.yaml

# In chai-app.yml we add these two annotations:
	1. notifications.argoproj.io/subscribe.on-health-degraded.email: "<receiver@example.com>"
	2. notifications.argoproj.io/subscribe.on-deployed.email: "<receiver@example.com>"

