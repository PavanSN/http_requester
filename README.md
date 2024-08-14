
Using the native HTTP and cache data and log the responses

## Features

1. Logging Made Easy
2. Caching Made Easy
3. Image uploading Made Easy

## Getting started

flutter pub add http_requester

import "package:http_requester.dart"

## Example

```
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
```

# http_requester
