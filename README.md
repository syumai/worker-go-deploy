# worker-go

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https%3A%2F%2Fgithub.com%2Fsyumai%2Fworker-go-deploy)

- A template for starting a Cloudflare Worker project with Go.
- This template uses [`workers`](https://github.com/syumai/workers) package to run an HTTP server.

## Notice

- Go (not TinyGo) with many dependencies may exceed the size limit of the Worker (3MB for free plan, 10MB for paid plan). In that case, you can use the [TinyGo template](https://github.com/syumai/workers/tree/main/_templates/cloudflare/worker-tinygo) instead.

## Usage

- `main.go` includes simple HTTP server implementation. Feel free to edit this code and implement your own HTTP server.

## Requirements

- Node.js
- Go 1.23.0 or later

## Getting Started

- Create a new worker project from [deploy link](https://deploy.workers.cloudflare.com/?url=https%3A%2F%2Fgithub.com%2Fsyumai%2Fworker-go-deploy).

## Development

### Commands

```
npm start      # run dev server
# or
go run .       # run dev server without Wrangler (Cloudflare-related features are not available)
npm run build  # build Go Wasm binary
npm run deploy # deploy worker
```

### Testing dev server

- Just send HTTP request using some tools like curl.

```
$ curl http://localhost:8787
Hello, Go!
```
