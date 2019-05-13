
The generated runtime has defined an interface for all the missing resolvers that we need to provide
`go generate ./...`


- gqlgen.yml — The gqlgen config file, knobs for controlling the generated code.
- generated.go — The GraphQL execution runtime, the bulk of the generated code.
- models_gen.go — Generated models required to build the graph. Often you will override these with your own models. Still very useful for input types.
- resolver.go — This is where your application code lives. generated.go will call into this to get the data the user has requested.
- server/server.go — This is a minimal entry point that sets up an http.Handler to the generated GraphQL server.

start server: `go run server/server.go`