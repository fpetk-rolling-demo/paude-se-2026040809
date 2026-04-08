FROM quay.io/bbrowning/paude-base-centos10:0.15.0
ENV PAUDE_AGENT_NAME=claude

COPY --chmod=755 entrypoint.sh /usr/local/bin/entrypoint.sh
COPY --chmod=755 entrypoint-session.sh /usr/local/bin/entrypoint-session.sh
COPY --chmod=755 entrypoint-lib-base.sh /usr/local/bin/entrypoint-lib-base.sh
COPY --chmod=755 credential-watchdog.sh /usr/local/bin/credential-watchdog.sh
COPY --chmod=755 patch-agent.sh /usr/local/bin/patch-agent.sh
COPY tmux.conf /etc/tmux.conf

ENTRYPOINT ["tini", "--", "entrypoint.sh"]
