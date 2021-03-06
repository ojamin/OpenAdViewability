OpenAdViewability
======

This JavaScript SDK is an open source version to track viewability metric for any ad element based on the MRC Viewability guidelines - http://mediaratingcouncil.org/081815%20Viewable%20Ad%20Impression%20Guideline_v2.0_Final.pdf. This implementation is extended from OpenVV - https://github.com/InteractiveAdvertisingBureau/openvv and developed by AdsNative. The purpose of this SDK vs. OpenVV is to provide an ability to track viewability of an ad element as a whole instead for just video ads. 

## Features
* According to MRC guidelines it tracks the viewability of an ad if the ad is at least 50% viewable for at least for 1 second.
* If the ad unit is larger than 242,500 pixel area then it considers only at least 30% ad viewable for at least for 1 second.
* Unlike OpenVV it doesn't require Flash support from the browser. It tracks the viewability across all web browser platforms.
* It tracks viewability even if the ad element is within the friendly-iframe. 

Note: It does not track 'Viewable Video Impression'. It only tracks viewable impressions for the ad element as a whole.

## Usage

```javascript
oav = new OpenAdViewability();
oav.checkViewability(ad_element, function(check){
  if(check.viewabilityStatus){
    // Your code here
  }
});
```

## Demo

Demo: http://preview.adsnative.com/viewability_demo/


