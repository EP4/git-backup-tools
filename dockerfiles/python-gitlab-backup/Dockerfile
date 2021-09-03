FROM alpine:3.9

RUN apk add --update --no-cache tzdata git python3 && ln -sf python3 /usr/bin/python
RUN python3 -m ensurepip
RUN pip3 install gitlab-backup

COPY gitlabbackup.py /srv/gitlabbackup.py
COPY exec.sh /srv/exec.sh

RUN chmod +x /srv/exec.sh

CMD ["/srv/exec.sh"]