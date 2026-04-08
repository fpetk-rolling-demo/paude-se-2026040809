FROM quay.io/bbrowning/paude-base-centos10:0.15.0
ENV PAUDE_AGENT_NAME=claude

COPY entrypoint.sh /usr/local/bin/entrypoint.sh
COPY entrypoint-session.sh /usr/local/bin/entrypoint-session.sh
COPY entrypoint-lib-base.sh /usr/local/bin/entrypoint-lib-base.sh
COPY credential-watchdog.sh /usr/local/bin/credential-watchdog.sh
COPY patch-agent.sh /usr/local/bin/patch-agent.sh
COPY tmux.conf /etc/tmux.conf

RUN chmod +x /usr/local/bin/entrypoint.sh \
              /usr/local/bin/entrypoint-session.sh \
              /usr/local/bin/entrypoint-lib-base.sh \
              /usr/local/bin/credential-watchdog.sh \
              /usr/local/bin/patch-agent.sh

ENTRYPOINT ["tini", "--", "entrypoint.sh"]
