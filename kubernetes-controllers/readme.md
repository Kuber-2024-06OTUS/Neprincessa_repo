1. Необходимо создать манифест namespace.yaml для namespace с именем homework
2. Необходимо создать манифест deployment.yaml. Он должен описывать deployment, который:
    - будет создаваться в namespace homework 
    - запускает 3 экземпляяра пода, полностью аналогичных по спецификации прошлому дз 
    - в дополнение к этому будет иметь readiness пробу, проверяющую наличие файла /homework/index.html
    - будет иметь стратегию обновления RollingUpdate настроенную так, что в процессе обновления может быть не доступен максимум 1 под 

Задание с *: 
Добавить к манифесту deployment-а спецификацию, обеспечивающую запуск подов деплоймента только на нодах кластера, имеющих метку homework=true