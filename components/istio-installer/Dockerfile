FROM eu.gcr.io/kyma-project/test-infra/alpine-kubectl:v20200617-32c1f3ff

LABEL source=git@github.com:kyma-project/kyma.git

ENV ISTIOCTL_VERSION 1.4.7
ENV YQ_VERSION 3.1.1

RUN curl -L https://github.com/istio/istio/releases/download/${ISTIOCTL_VERSION}/istioctl-${ISTIOCTL_VERSION}-linux.tar.gz -o istioctl.tar.gz &&\
	tar xvzf istioctl.tar.gz &&\
	chmod +x istioctl &&\
	mv istioctl /usr/local/bin/istioctl &&\
	rm istioctl.tar.gz &&\
	curl -L https://github.com/mikefarah/yq/releases/download/${YQ_VERSION}/yq_linux_amd64 -o yq &&\
	chmod +x yq &&\
	mv yq /usr/local/bin/yq

ENTRYPOINT ["/bin/bash"]
