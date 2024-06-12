k8s_yaml("k8s-specifications/db-dep-svc.yaml")
k8s_yaml("k8s-specifications/redis-dep-svc.yaml")
k8s_yaml("k8s-specifications/result-dep-svc.yaml")
k8s_yaml("k8s-specifications/vote-dep-svc.yaml")
k8s_yaml("k8s-specifications/worker-deployment.yaml")

docker_build('result','result')
docker_build('vote','vote')
docker_build('worker','worker')

k8s_resource('vote',port_forwards='8081:80')
k8s_resource('result',port_forwards='8082:80')