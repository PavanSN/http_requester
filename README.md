<!--
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/tools/pub/writing-package-pages).

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/to/develop-packages).
-->

TODO: Put a short description of the package here that helps potential users
know whether this package might be useful for them.

## Features

1. Logging Made Easy
2. Caching Made Easy
3. Image uploading Made Easy

## Getting started

flutter pub add http_requester

import "package:http_requester.dart"

## Example

test() async {
  HttpRequesterPayload payload = HttpRequesterPayload(
    url: 'https://example/com/abc',
    body: {'key': 'value'},
    headers: {'key': 'value'},
    requestType: RequestType.get,
    shouldCache: true,
    invalidateCachesAfter: Duration(days: 1),
  );

  HttpRequesterResponse response =
      await HttpRequester.i.request(payload: payload);

  MyModel model = MyModel.fromJson(response.decodedResponse);
}
# http_requester
