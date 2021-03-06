# Overview

**Module Name**: Platform.io Bidder Adapter  
**Module Type**: Bidder Adapter  
**Maintainer**: siarhei.kasukhin@platform.io  

# Description

Connects to Platform.io demand source to fetch bids.  
Banner, Native, Video formats are supported.  
Please use ```platformio``` as the bidder code.

# Test Parameters
```
  var adUnits = [{
          code: 'dfp-native-div',
          mediaType: 'native',
          mediaTypes: {
              native: {
                  title: {
                      required: true,
                      len: 75
                  },
                  image: {
                      required: true
                  },
                  body: {
                      len: 200
                  },
                  icon: {
                      required: false
                  }
              }
          },
          bids: [{
              bidder: 'platformio',
              params: {
                  pubId: '29521',
                  siteId: '26048',
                  placementId: '123',
              }
          }]
      },
      {
          code: 'dfp-banner-div',
          mediaTypes: {
              banner: {
                  sizes: [
                      [300, 250]
                  ],
              }
          },
          bids: [{
              bidder: 'platformio',
              params: {
                  pubId: '29521',
                  siteId: '26049',
                  size: '300X250',
                  placementId: '123',
              }
          }]
      },
      {
          code: 'dfp-video-div',
          sizes: [640, 480],
          mediaTypes: {
              video: {
                  context: "instream"
              }
          },
          bids: [{
              bidder: 'platformio',
              params: {
                  pubId: '29521',
                  siteId: '26049',
                  size: '640X480',
                  placementId: '123',
                  video: {
                      skippable: true,
                  }
              }
          }]
      }
  ];
```
