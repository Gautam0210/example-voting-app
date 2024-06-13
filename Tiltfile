load('ext://kubectl_build', 'kubectl_build')

k8s_yaml("k8s-specifications/db-dep-svc.yaml")
k8s_yaml("k8s-specifications/redis-dep-svc.yaml")
k8s_yaml("k8s-specifications/result-dep-svc.yaml")
k8s_yaml("k8s-specifications/vote-dep-svc.yaml")
k8s_yaml("k8s-specifications/worker-deployment.yaml")

kubectl_build('result', 'result')

# docker_build('result','result')
# docker_build('vote','vote')
# docker_build('worker','worker')

# custom_build('result','docker build -t $EXPECTED_REF result', tag= disable_push = False , skips_local_docker = true, deps=['result'])
# custom_build(ref: str, command: Union[str, List[str]], deps: List[str], tag: str = "", disable_push: bool = False, skips_local_docker: bool = False, live_update: List[LiveUpdateStep]=[], match_in_env_vars: bool = False, ignore: Union[str, List[str]] = [], entrypoint: Union[str, List[str]] = [], command_bat_val: str = "", outputs_image_ref_to: str = "", command_bat: Union[str, List[str]] = "", image_deps: List[str] = [], env: Dict[str, str] = {}, dir: str = "")

# k8s_resource('vote',port_forwards='8081:80')
# k8s_resource('result',port_forwards='8082:80')

allow_k8s_contexts('arn:aws:eks:ap-south-1:590183817564:cluster/prod-eks-cluster')
k8s_context('arn:aws:eks:ap-south-1:590183817564:cluster/prod-eks-cluster')