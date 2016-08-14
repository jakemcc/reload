# reload

A Clojure Ring middleware that uses
[tools.namespace](https://github.com/clojure/tools.namespace) for
detecting and reloading changed namespaces.

## Usage

Require `com.jakemccrary.middleware.reload` and wrap your handler with `wrap-reload`.

```clojure
(ns example
  (:require
   ;; more deps
   [com.jakemccrary.middleware.reload :as reload]))

;; wherever you are setting up your middleware stack
(reload/wrap-reload routes)
```

`reload/wrap-reload` optionally takes a list of directories to monitor
as a second parameter. By default it the `src` directory.

## License

Copyright © 2016 Jake McCrary

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
