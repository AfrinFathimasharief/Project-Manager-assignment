1.Install Minikube:

bash
Minikube Start


2.Install Kubescape:

curl -s https://raw.githubusercontent.com/kubescape/kubescape/master/install.sh | /bin/bash


3.Run security scan:

kubescape scan framework nsa --output json --format json -o k8s-findings.json


4.Sample output:

{
  "kind": "KubernetesSecurityScan",
  "summary": {
    "critical": 2,
    "high": 5,
    "medium": 10
  },
  "resources": [
    {
      "name": "kube-apiserver",
      "severity": "Critical",
      "issue": "Anonymous authentication enabled"
    },
    ...
  ]
}
