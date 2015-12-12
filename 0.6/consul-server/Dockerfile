FROM geniousphp/consul-agent
ADD ./config /config/
ADD https://releases.hashicorp.com/consul/0.6.0/consul_0.6.0_web_ui.zip /tmp/webui.zip
RUN mkdir /ui && cd /tmp && unzip webui.zip -d /ui && rm webui.zip
ENTRYPOINT ["/bin/consul", "agent", "-server", "-config-dir=/config"]