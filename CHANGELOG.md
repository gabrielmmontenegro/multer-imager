4.0.0 / 2019-06-22
==================
  * Upgrade s3rver
  * Fix js-yaml security issue
  * Drop support NodeJS < 8.x

3.3.3 / 2019-01-12
==================
  * Update dependencies: mime, aws-sdk

3.3.2 / 2018-10-20
==================
  * Update dependencies

3.3.0 / 2018-07-11
==================
  * Update dependencies
  * Add crop option

3.2.0 / 2018-01-26
==================
  * Update dependencies
  * Min. NodeJS >= 6.0
  
3.1.1 / 2017-02-27
==================
  * Setup Greenkeeper

3.1.0 / 2017-01-16
==================
  * Feature: Support s3 options (custom metadata, etc...)

3.0.0 / 2017-01-11
==================
  * Feature: replace graphicsmagick-stream by gm
  * Fix: Content-Type not set in AWS S3
  * Update dev. dependencies

**BREAKING CHANGE:**
## Setup
Before:
```
apt-get install build-essential libgraphicsmagick++1-dev libarchive-dev
```
After:
```
apt-get install graphicsmagick
```

## gm options
Before:
```
gm: {
      pool: 5,             // how many graphicsmagick processes to use
      format: 'png',       // format to convert to
      scale: {
        width: 200,        // scale input to this width
        height: 200,       // scale input this height
        type: 'contain'    // scale type (either contain/cover/fixed)
      },
      crop: {
        width: 200,        // crop input to this width
        height: 200,       // crop input this height
        x: 0,              // crop using this x offset
        y: 0               // crop using this y offset
      },
      rotate: 'auto',      // auto rotate image based on exif data
                           // or use rotate:degrees 
      density: 300,        // set the image density. useful when converting pdf to images
   }
```
After:
```
gm: {                          // [Optional]: define graphicsmagick options
      width: 200,              // doc: http://aheckmann.github.io/gm/docs.html#resize
      height: 200,
      options: '!',
      format: 'png'            // Default: jpg
    }
```

2.1.3 / 2016-02-21
==================
  * Update dev. supertest

2.1.2 / 2015-12-06
==================
  * Update dev. dependencies

2.1.1 / 2015-12-06
==================
  * fix code style issues 

2.1.0 / 2015-11-04
==================
  * Update s3fs 2.3->2.4
  * Update dev. dependencies

2.0.0 / 2015-11-04
==================
  * BREAKING CHANGE: option reqfilename replaced by filename (function)
  * Update dependencies

1.2.0 / 2015-09-17
==================
  * Remove global variables
  * Update dependencies
  * Tests NodeJS 2-4

1.1.0 / 2015-07-30
==================
  * Addd Travis tests with nodejs 4.0

1.1.0 / 2015-07-30
==================
  * Update dependencies
  * Add Travis build

1.0.0 / 2015-07-20
==================
  * First release