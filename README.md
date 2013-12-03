vendor-prefixes-talk
====================

Notes, examples, and further reading from a December 2013 presentation I gave on CSS Vendor Prefixes and the [grunt-autoprefixer](https://github.com/nDmitry/grunt-autoprefixer) task.

## Autoprefixer Documentation

Refer to the [grunt-autoprefixer GitHub repo](https://github.com/nDmitry/grunt-autoprefixer) for documentation.

## Sample Configuration

```js
// Gruntfile.js

grunt.initConfig({

  autoprefixer: {

    options: {
        browsers: [
            'last 2 version',
            ''> 1%',
            'ie 8',
            'android 4'
            ]
    },

    // Prefix a single file and output it to a new file
    single_file: {
      src: 'src/css/file.css',
      dest: 'dest/css/file.css'
    },

    // Omit the 'dest' parameter to overwrite your source file(s)
    overwrite: {
      src: 'dest/css/file.css' // globbing is also possible here
    }
  }
})
```
## Further Reading

[Autoprefixer: A Postprocessor for Dealing with Vendor Prefixes in the Best Possible Way](http://css-tricks.com/autoprefixer/) by Andrey Sitnik (Autoprefixer author). August 2013.

[How To Deal With Vendor Prefixes](http://css-tricks.com/how-to-deal-with-vendor-prefixes/) by Chris Coyier. December 2012.

Older posts. These posts contain partially outdated information but they're useful if you want more context.

[Vendor Prefixes - about to go south](http://remysharp.com/2012/02/09/vendor-prefixes-about-to-go-south/) by Remy Sharp. February 2012.

[New Proposal Could End the CSS Prefix Madness](http://www.webmonkey.com/2012/05/new-proposal-could-end-the-css-prefix-madness/) by Scott Gilbertson. May 2012.

## License

MIT License • © [Noah Collins](https://twitter.com/noahec)