# HTTP SERVER JSON

This is a simple node http server that accepts only json.
It has been published cause I don't need to repeat this code in every simple http based service

You can install it in this way:

    npm install --save http-server-json

You can use it in this way:

    const server = require('http-server-json')

    # res is an http.ServerResponse
    function handleData(json, res) {
        res.writeHead(200, "OK", { 'Content-Type': 'text/plain' })
        res.end()
    }

    server.start(8080, '0.0.0.0', handleData)