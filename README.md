# Golang Web Frameworks Comparison

This documentation provides a brief comparison between top 5 golang web frameworks and it 
shouldn't be considered as a `in depth analysis documentation`. 

Main features and cons of each project plus benchmark!


# Gin
[gin framework](https://github.com/gin-gonic/gin)  is one of the most famous golang frameworks and it provides a lot of features without paying much.
It has a big community with a lot of production ready plugins and extensions like `jwt`, `session`, `health check`, etc. 

Gin provides support for JSON validation. Requesting with a JSON can validate required values, like input data from the client. These values must be validated before saving in memory, so by validating them, developers can avoid saving inaccurate values.

Gin is a simple, easy-to-use framework that, if you are just starting to use Golang, Gin has been voted the most ideal framework because it is minimal and straightforward to use.

It's a perfect choice for your next web project! 

### Features
-   Zero allocation router.
-   Still the fastest http router and framework. From routing to writing.
-   Complete suite of unit tests.
-   Battle tested.
-   API frozen, new releases will not break your code.

# Beego

[Beego](https://beego.me/)  is another Go web framework that is mostly used to build enterprise web applications with rapid development.

Beego has four main parts that make it a viable Go framework:

-   Base modules, which contain  `log`,  `config`, and  `governor`
-   A webserver
-   Tasks, which work similarly to cron jobs
-   A client, which houses the ORM, httplib, and cache modules


Because `Beego` focuses on enterprise applications, which tend to be very large with a lot of code powering a lot of features, a modular structure arranges modules for specific use cases, optimizing performance.

So, the framework provides a great modular structure for things like a configuration module, logging module, and caching module.

It also uses  [a regular MVC architecture](https://github.com/beego/beedoc/tree/master/en-US/mvc)  to handle specific development aspects in an app, which is also beneficial for enterprise applications.



# Irish

Iris is an Express.js-equivalent web framework that is easier to use for people coming from the Node.js community.

It comes with  `Sessions`, API versioning, WebSocket, dependency injection, WebAssembly, the typical MVC architecture, and more, making it very flexible with third-party libraries.

With  [over 20k stars on GitHub](https://github.com/kataras/iris), Iris is most loved because of its simplicity and the ability to extend the framework with personal libraries quickly.

#### Iris general features

As discussed, one of Iris’s main features is that its fully accordant and flexible with external libraries, letting users pick and choose what they want to use with the framework

With a built-in logger for printing and logging server requests, users don’t need to use something external, cutting down the complexity of using Iris.

Like Beego, it provides MVC support for larger applications and its automated API versioning makes adding new integrations convenient by placing them in newer versions of the route.

Iris’s smart and fast compression provides faster performance, and testing is a breeze with the [Ngrok](https://ngrok.com/) integration, which lets developers share a local webserver with other developers for testing.

One great thing about this specific framework is that the author replies to issues on GitHub quickly, making it helpful when running into bugs.

# Echo
[Echo is another promising framework](https://echo.labstack.com/)  created by Labstack with  [20k stars on GitHub](https://github.com/labstack/echo). It is also regarded as a micro framework, which is more of a standard library and a router, and has fully-baked documentation for developers to use and understand.

This framework is great for people who want to learn how to create APIs from scratch, thanks to its extensive documentation.

#### Echo general features

Echo lets developers define their own middleware and has built-in middleware to use as well. This gives developers the ability to create custom middleware to get specific functionalities while having the built-in middleware speeds production.

Echo also supports HTTP/2 for faster performance and an overall better user experience.

Its API also supports a variety of HTTP responses like JSON, XML, stream, blob, file, attachment, inline, and customized central HTTP error handling.

Finally, it supports a variety of templating engines, providing the flexibility and convenience developers need when choosing an engine.

# Fiber

[Fiber is another Express.js-like web framework](https://github.com/gofiber/fiber)  written in Go that boasts low memory usage and rich routing. Built on top of the  [Fasthttp HTTP engine for Go](https://github.com/valyala/fasthttp), which is the fastest HTTP engine for Go, Fiber provides one of the fastest Go frameworks.

Created with the main focus of minimalism and the Unix philosophy to provide simple and modular software technology, the idea for Fiber was to allow new Go developers to begin creating web applications quickly.

### Official features
-   Robust  [routing](https://docs.gofiber.io/routing)
-   Serve  [static files](https://docs.gofiber.io/api/app#static)
-   Extreme  [performance](https://docs.gofiber.io/extra/benchmarks)
-   [Low memory](https://docs.gofiber.io/extra/benchmarks)  footprint
-   [API endpoints](https://docs.gofiber.io/api/ctx)
-   [Middleware](https://docs.gofiber.io/middleware)  &  [Next](https://docs.gofiber.io/api/ctx#next)  support
-   [Rapid](https://dev.to/koddr/welcome-to-fiber-an-express-js-styled-fastest-web-framework-written-with-on-golang-497)  server-side programming
-   [Template engines](https://github.com/gofiber/template)
-   [WebSocket support](https://github.com/gofiber/websocket)
-   [Rate Limiter](https://docs.gofiber.io/api/middleware/limiter)
-   Translated in  [15 languages](https://docs.gofiber.io/)

#### Fiber general features

Fiber boasts of a built-in rate limiter that helps reduce traffic to a particular endpoint. For example, this is helpful if a user tries to sign in to an account continuously and knowing that it might be malicious activity.

Its static files, like style sheets, scripts, and images, can be handled and served from the server, making them easily cached, consuming less memory, and the content remains static upon every request.

And its support for WebSocket bidirectional TCP connections is useful for creating real-time communications, like a chat system.

Like the other Go frameworks we’ve mentioned in this post, it has versatile middleware support, supports a variety of template engines, has low memory usage and footprint, and provides great documentation that is easy and clear for new users.


# Benchmarks

For framework benchmark, [go-framework-benchmark](https://github.com/smallnest/go-web-framework-benchmark) were utilized. 
Unfortunately, this tool doesn't support `Irish` so that `Irish` will be missing in all charts. 

Simple Benchmark  
![Benchmark](https://github.com/sonemaro/gobench/blob/main/benchmark.png)  

Benchmark With Concurrency  
![Concurrency](https://github.com/sonemaro/gobench/blob/main/concurrency.png)  

CPU Usage Benchmark  
![CPU Bound](https://github.com/sonemaro/gobench/blob/main/cpubound_benchmark.png)  

Concurrent CPU Usage Benchmark  
![CPU Bound Concurrency](https://github.com/sonemaro/gobench/blob/main/cpubound_concurrency.png)  

#### Hardware
CPU: Intel(R) Core(TM) i7-8550U CPU @ 1.80GHz  
Mem: Samsung 16G DDR4 2400 MT/s  

# References
https://github.com/smallnest/go-web-framework-benchmark  
https://blog.logrocket.com/5-top-go-web-frameworks/  
https://github.com/beego/beego  
https://github.com/labstack/echo  
https://github.com/gofiber/fiber  
https://github.com/kataras/iris  
https://github.com/gin-gonic/gin  
https://github.com/gin-gonic/gin/blob/master/BENCHMARKS.md  
https://ngrok.com/  
https://golangrepo.com/repo/smallnest-go-web-framework-benchmark-go-web-frameworks  
https://dzone.com/articles/comparison-of-popular-web-frameworks-in-go  
