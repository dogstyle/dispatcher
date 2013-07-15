dispatcher
==========


call this method like so.

```javaScript

;(function() {

 // var dispatcher = PAGE.Modules.Dispatcher
 var dispatcher = Dispatcher
 
 var name = dispatcher.random()
 var name2 = dispatcher.random()
 var name3 = dispatcher.random()

 dispatcher.makeRunner(name, function() {
  // your aysnc stuff here like
  setTimeout(function() {
    dispatcher.finish(name)
  }, 1000)
 })
 
 dispatcher.makeRunner(name2, function() {
  // your aysnc stuff here like
  setTimeout(function() {
    dispatcher.finish(name2)
  }, 500)
 })
 
 dispatcher.makeRunner(name3, function() {
  // your aysnc stuff here like
  setTimeout(function() {
    dispatcher.finish(name3)
  }, 1000)
 })

}())

```
