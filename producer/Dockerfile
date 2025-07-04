# ---------- Stage1: build ----------
FROM golang:1.22-alpine AS builder
WORKDIR /src
COPY go.mod go.sum ./
RUN go mod download
COPY . .
RUN go build -o /app/producer .

# ---------- Stage2: run ----------
FROM alpine:3.20
WORKDIR /app
COPY --from=builder /app/producer .
CMD ["./producer"]
