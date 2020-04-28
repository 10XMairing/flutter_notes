
  ## Providers

|Type|Function|
|--|--|
|Provider|to provide a value (usually a data model object) to anywhere in the widget tree. However, it won’t help you update the widget tree when that value changes.|
|ChangeNotifierProvider|Unlike the basic `Provider` widget, `ChangeNotifierProvider` listens for changes in the model object. When there are changes, it will rebuild any widgets under the `Consumer`.|
|ListenableProvider||
|ValueListenableProvider||
|StreamProvider|`StreamProvider` is basically a wrapper around a `StreamBuilder`. You provide a stream and then then the Consumers get rebuilt when there is an event in the stream.|
|FutureProvider|`FutureProvider` is basically just a wrapper around the [FutureBuilder](https://api.flutter.dev/flutter/widgets/FutureBuilder-class.html)` widget. You give it some initial data to show in the UI and also provide it a Future of the value that you want to provide. The `FutureProvider` listens for when the Future completes and then notifies the Consumers to rebuild their widgets.|
|MultiProvider|If you need to provide a second type of model object, you could nest the providers. However, all that nesting is messy. A neater way to do it is to use a `MultiProvider`.|
|ProxyProvider|if you have two models that you want to provide, but one of the models depends on the other one? In that case you can use a `ProxyProvider`. A `ProxyProvider` takes the value from one provider and lets it be injected into another provider.|
