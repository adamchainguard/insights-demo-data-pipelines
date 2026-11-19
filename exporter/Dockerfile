FROM cgr.dev/0-cve.com/go:latest AS build
WORKDIR /src
COPY main.go go.mod ./
RUN CGO_ENABLED=0 go build -o /out/exporter .

FROM cgr.dev/0-cve.com/static:latest
COPY --from=build /out/exporter /exporter
ENTRYPOINT ["/exporter"]
