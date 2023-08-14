# build
custom_build(
    ref = 'cnsa-config-service',
    command = './gradlew bootBuildImage --imageName $EXPECTED_REF',
    deps = ['build.gradle', 'src']
)

# deploy
k8s_yaml(['kubernetes/deployment.yaml', 'kubernetes/service.yaml'])

# manage
k8s_resource('cnsa-config-service', port_forwards=['8888'])
