# chirpstack-kube
This is a repository of yaml files that will deploy chirpstack on your kubenetes. To use, simply clone the repository and run:

kubectl create -f $PATH_TO_CLONED_RESPOSITORY

Please note that the gateway bridge is conigured to AU915 region. To change that, modify chirpstack-gatway-bridge.yaml, change "au915_0" in those three lines to correct region.

    event_topic_template="au915_0/gateway/{{ .GatewayID }}/event/{{ .EventType }}"
    state_topic_template="au915_0/gateway/{{ .GatewayID }}/state/{{ .StateType }}"
    command_topic_template="au915_0/gateway/{{ .GatewayID }}/command/#"
