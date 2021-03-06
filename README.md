This app demostrates how to use the [Sync](https://github.com/hyperoslo/Sync) library in Objective-C.

![Image](https://raw.githubusercontent.com/3lvis/SyncDesignerNewsDemo/master/Images/app.png)

## [JSON](https://news.layervault.com/?format=json)

```json
{
  "stories":[
    {
      "id":47333,
      "title":"Site Design: Aquest",
      "vote_count":6,
      "created_at":"2015-04-06T13:16:36Z",
      "num_comments":6,
      "submitter_display_name":"Chris A.",
      "comments":[
        {
          "body":"Beautiful.",
          "created_at":"2015-04-06T13:45:20Z",
          "depth":0,
          "user_display_name":"Sam M.",
          "upvotes_count":0,
          "comments":[

          ]
        }
      ]
    }
  ]
}
```

## Model

![Model](https://raw.githubusercontent.com/3lvis/SyncDesignerNewsDemo/master/Images/model.png)

## Sync

```objc
[Sync changes:JSON[@"stories"]
inEntityNamed:@"Story"
    dataStack:dataStack
   completion:^(NSError *error) {
       [UIApplication sharedApplication].networkActivityIndicatorVisible = NO;
   }];
```
