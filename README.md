# Домашнее задание к занятию «Сетевое взаимодействие в K8S. Часть 1» - Сергей Ситкарёв

## Задание 1. Создать Deployment и обеспечить доступ к контейнерам приложения по разным портам из другого Pod внутри кластера

Создать Deployment приложения, состоящего из двух контейнеров (nginx и multitool), с количеством реплик 3 шт.

[deployment](https://github.com/SSitkarev/1.4-k8s-network/blob/main/src/deployment.yaml)

Создать Service, который обеспечит доступ внутри кластера до контейнеров приложения из п.1 по порту 9001 — nginx 80, по 9002 — multitool 8080.

[service](https://github.com/SSitkarev/1.4-k8s-network/blob/main/src/service.yaml)

Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложения из п.1 по разным портам в разные контейнеры.

[multitool](https://github.com/SSitkarev/1.4-k8s-network/blob/main/src/multitool.yaml)

Продемонстрировать доступ с помощью curl по доменному имени сервиса. Предоставить манифесты Deployment и Service в решении, а также скриншоты или вывод команды п.4.

![Задание1](https://github.com/SSitkarev/1.4-k8s-network/blob/main/img/1.jpg)

## Задание 2. Создать Service и обеспечить доступ к приложениям снаружи кластера

Создать отдельный Service приложения из Задания 1 с возможностью доступа снаружи кластера к nginx, используя тип NodePort.

[nodeport](https://github.com/SSitkarev/1.4-k8s-network/blob/main/src/nodeport.yaml)

Продемонстрировать доступ с помощью браузера или curl с локального компьютера. Предоставить манифест и Service в решении, а также скриншоты или вывод команды п.2.

![Задание2](https://github.com/SSitkarev/1.4-k8s-network/blob/main/img/2-1.jpg)

![Задание2](https://github.com/SSitkarev/1.4-k8s-network/blob/main/img/2-2.jpg)