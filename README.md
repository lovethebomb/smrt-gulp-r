# gulp-r

First, install `gulp-r` as a development dependency:

```shell
npm install --save-dev gulp-r
```

Then, use it in your `gulpfile.js`:

```javascript
var rjs = require("gulp-r");

gulp.src("app/scripts/*.js")
    .pipe(rjs({
        "baseUrl": "app/scripts"
    }))
    .pipe(gulp.dest("dist/scripts"));
```

If you want to rename output files use `gulp-rename` plugin.

```JavaScript
var rename = require("gulp-rename"),
    rjs = require("gulp-r");

gulp.src("app/scripts/*.js")
    .pipe(rjs({
        "baseUrl": "app/scripts"
    }))
    .pipe(rename({
        "extname": ".min.js"
    }))
    .pipe(gulp.dest("dist/scripts"));
```

## Status

This fork is maintained independently from its origin.

---

[![Build Status](https://travis-ci.org/smrtlabs/smrt-gulp-r.svg?branch=master)](https://travis-ci.org/smrtlabs/smrt-gulp-r)
[![Code Climate](https://codeclimate.com/github/smrtlabs/smrt-gulp-r.png)](https://codeclimate.com/github/smrtlabs/smrt-gulp-r)
[![Dependency Status](https://david-dm.org/smrtlabs/smrt-gulp-r.svg)](https://david-dm.org/smrtlabs/smrt-gulp-r)
