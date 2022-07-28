# OpenFriday Workshop

**Kurzes Intro:**
Es ist nicht notwendig alle Tools zu installieren, aber wer mag: Feel free.

Was wir definitiv benötigen ist einen lokalen Kubernetes Cluster.
Die jenigen, die ohne VirtualBox auskommen, dürfen gerne WSL2 installieren (Siehe weiter unten). 
Beides zusammen funktioniert unter Windows leider nicht.

Daher, wenn nicht anders möglich, bitte Minikube installieren. (Siehe weiter Unten)

Was wir hauptsächlich machen möchten, ist ein Kubernetes Cluster mit FluxCD zu bestücken - ist einfacher Art und Weise.
Hierfür benötigen wir ein Repo (welches ich bereitgestellt habe und geforked werden kann) und einen Personal Access Token.
Wie man daran kommt, werde ich während des Workshops zeigen.

## Voraussetzungen / Vorbereitungen

- GitHub Account
  -  Folgende GitHub Repo forken:
  - https://github.com/PatrickLaabs/spinning-k8s-with-flux


### Einrichtung auf Windows

**Wenn WSL2 vorhanden ist:**
Wichtig: WSL2 und VirtualBox funktionieren NICHT zusammen.
- WSL2 Installieren (Sobald wir WSL2 Installiert haben, arbeiten wir auf einer Linux Distro)
  - https://docs.microsoft.com/en-us/windows/wsl/install

- Rancher Desktop
  - https://github.com/rancher-sandbox/rancher-desktop/releases/download/v1.4.1/Rancher.Desktop.Setup.1.4.1.exe


**Ohne WSL2:**
- Minikube installieren
  - https://minikube.sigs.k8s.io/docs/start/

**Diese Schritte sind allgemein für beide Varianten möglich. Entweder mit Brew.sh oder Chocolatey:**
- Helm CLI
  - Binaries selber downloaden, extracten und kopieren:
    - **Linux:** https://github.com/helm/helm/releases/tag/v3.9.0 (Abschnitt: Installation and Upgrading)
    - Binary in das Verzeichnis '/usr/local/bin/' kopieren/verschieben && ausführbar machen (chmod +x)
    - **Windows:** https://github.com/helm/helm => In der README.md unter 'Install'

- Chart Tester CLI
  - Binaries selber downloaden, extracten und kopieren:
    - Linux: https://github.com/helm/chart-testing/releases/download/v3.7.0/chart-testing_3.7.0_linux_amd64.tar.gz
    - Windows: https://github.com/helm/chart-testing/releases/download/v3.7.0/chart-testing_3.7.0_windows_amd64.zip

- Chart Releaser CLI
  - Binaries selber downloaden, extracten und kopieren:
    - Linux: https://github.com/helm/chart-releaser/releases/download/v1.4.0/chart-releaser_1.4.0_linux_amd64.tar.gz
    - Windows: https://github.com/helm/chart-releaser/releases/download/v1.4.0/chart-releaser_1.4.0_windows_amd64.zip

- FluxCD CLI
  - https://fluxcd.io/docs/installation/

- kubectl (wird mit Rancher Desktop)
  -  Für Minikube:
    - minikube kubectl -- get po -A
    - (Docu ab 'Interact with your cluster') => https://minikube.sigs.k8s.io/docs/start/

- Lens oder K9s installieren
  - Lens: https://k8slens.dev/
  - K9s: https://github.com/derailed/k9s
