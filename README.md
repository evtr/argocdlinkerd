# argocdlinkerd

Dette projekt viser, hvordan argocd kan bruges som "deployment agent" på et Kitkube miljø. Dette projekt er kun tiltænkt udviklinsmiljøet.

## Prerequisites
Du skal bruge:
 * Et kitkube Kubernetes cluster. Du kan med fordel følge opsætningen her: https://github.com/KvalitetsIT/ff-parent-infrastructure/tree/master/kubespray

## Installation
For at komme igang skal argocd installeres. Der er endnu ikke ansible scripts til dette, så du skal stå et sted, hvor du kan bruge kubectl.

1. Installér Argocd: I https://argoproj.github.io/argo-cd/getting_started/ skal du udføre trin 1 i vedledningen dvs. "Install Argo CD". I dette punkt oprettes et namespace og argocd installeres.
2. Opret ingress regel: kubectl apply -n argocd -f https://raw.githubusercontent.com/evtr/argocdlinkerd/master/argocdbootstrap/argocd-ingress.yml

Argo CD er derefter tilgængelig her: https://argocd.kitkube.dk/
Brugernavn er "admin" og password er pod navnet for Argo CD API serveren (kan også hentes ud med: kubectl get pods -n argocd -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2).
