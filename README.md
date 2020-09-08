# kubernetes-config project

## Images used

This cluster uses two images:
- martinhelmich/typo3:9.5
- mariadb:10.5-focal

The first image offers the [TYPO3 CMS](https://typo3.org/). **TYPO3** is a Content Management System like Drupal or Wordpress. It was really popular between 2000 and 2015 and lost some market shares in recent years. However, it is still a great CMS!

The **TYPO3** version used here is the v9. This is not the latest but you can still enjoy this version.

To launch the cluster, you can use Minikube.

```
$ kubectl create -f path/to/typo3-v9.yanl
```

Then, do a port-forward to reach the **TYPO3** backend and frontend.

```
kubectl port-forward typo3-v9-starter 8080:80
```

Then, go to http://localhost:8080 and start the installation.