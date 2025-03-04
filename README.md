
## <p style="text-align: center;">ОТЧЕТ</p> <p style="text-align: center;">по домашним заданиям к занятию «Сетевое взаимодействие в K8S. Часть 2»</p>
## <p style="text-align: right;">Выполнил: студент Порсев И.С.</p>

### Цель задания

В тестовой среде Kubernetes необходимо обеспечить доступ к двум приложениям снаружи кластера по разным путям.

------

### Чеклист готовности к домашнему заданию

1. Установленное k8s-решение (например, MicroK8S).
2. Установленный локальный kubectl.
3. Редактор YAML-файлов с подключённым Git-репозиторием.

------

### Инструменты и дополнительные материалы, которые пригодятся для выполнения задания

1. [Инструкция](https://microk8s.io/docs/getting-started) по установке MicroK8S.
2. [Описание](https://kubernetes.io/docs/concepts/services-networking/service/) Service.
3. [Описание](https://kubernetes.io/docs/concepts/services-networking/ingress/) Ingress.
4. [Описание](https://github.com/wbitt/Network-MultiTool) Multitool.

------

### Задание 1. Создать Deployment приложений backend и frontend

1. Создать Deployment приложения _frontend_ из образа nginx с количеством реплик 3 шт.
2. Создать Deployment приложения _backend_ из образа multitool. 
3. Добавить Service, которые обеспечат доступ к обоим приложениям внутри кластера. 
4. Продемонстрировать, что приложения видят друг друга с помощью Service.
5. Предоставить манифесты Deployment и Service в решении, а также скриншоты или вывод команды п.4.


## Решение
> по пунктам 1-5
![localImage](./screen_VII.05_1.png)        

## Ссылки на файлы:
>[frontend](./conf/frontend.yaml);    
>[backend](./conf/backend.yaml);  
>[Service](./conf/service_1.yaml).  

![localImage](./Yes.png)

------

### Задание 2. Создать Ingress и обеспечить доступ к приложениям снаружи кластера

1. Включить Ingress-controller в MicroK8S.
2. Создать Ingress, обеспечивающий доступ снаружи по IP-адресу кластера MicroK8S так, чтобы при запросе только по адресу открывался _frontend_ а при добавлении /api - _backend_.
3. Продемонстрировать доступ с помощью браузера или `curl` с локального компьютера.
4. Предоставить манифесты и скриншоты или вывод команды п.2.

## Решение
> по пунктам 1-3
![localImage](./screen_VII.05_2.png)        
> по пункту 3
![localImage](./screen_VII.05_2.png)      
> по пункту 4
![localImage](./screen_VII.05_3.png)      

## Ссылки на файлы:
>[Deploy](./conf/deploy_1.yaml);    
>[Service](./conf/service_1.yaml);   
>[Pod](./conf/pod.yaml).   

![localImage](./Yes.png)