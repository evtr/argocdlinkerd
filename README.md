# argocdlinkerd

Dette projekt viser, hvordan argocd kan bruges som "deployment agent" på et Kitkube miljø.

## Prerequisites
Du skal bruge:
 * Et Kubernetes cluster 
 
Du kan f.eks. følge opsætningen her: https://github.com/KvalitetsIT/ff-parent-infrastructure/tree/master/kubespray

## Installation
For at komme igang skal argocd installeres. Der er endnu ikke ansible scripts til dette, så du skal stå et sted, hvor du kan bruge kubectl.

1. Installér Argocd: I https://argoproj.github.io/argo-cd/getting_started/ skal du udføre trin 1 i vedledningen dvs. "Install Argo CD". I dette punkt oprettes et namespace og argocd installeres.
2. Opret ingress regel: 
