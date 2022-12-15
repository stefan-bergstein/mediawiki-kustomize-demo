# mediawiki-kustomize-demo
Mediawiki demo deployment with kustomize


# Notes
[OpenShift GitOps sync is failing in user namespace - Red Hat Customer Portal](https://access.redhat.com/solutions/6012601)
[Cannot sync application in OpenShift GitOps - Red Hat Customer Portal](https://access.redhat.com/solutions/6331341)

## Workaround for the ArgoCD demo
Create projet and permissions first:

```
oc new-project decv-mediawiki

oc new-project prod-mediawiki

oc adm policy add-role-to-user admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller -n dev-mediawiki

oc adm policy add-role-to-user admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller -n prod-mediawiki 
```


