FROM registry.access.redhat.com/ubi8/ubi-minimal:8.0

EXPOSE 9080

RUN microdnf install nc && microdnf clean all

CMD ncat -kl --sh-exec 'echo -e "HTTP/1.1 200 OK\nContent-Type: application/json\n\n{\"caller\":\"service-a\", \"color\":\"#A00\"}"' 0.0.0.0 9080
