vendor-prefixes-talk
====================

Notes, examples, and further reading from a December 2013 presentation I gave on CSS Vendor Prefixes and the [grunt-autoprefixer](https://github.com/nDmitry/grunt-autoprefixer) task. I welcome your questions and feedback. Create an issue or send me pull request.

#### Outline

 - CSS vendor prefixes come and go regularly; keeping them current requires research and upkeep. 

 - Preprocessors and mixin libraries are excellent tools, but they still require some maintenance.

 - Autoprefixer takes a supplied configuration, references the Can I Use API, and outputs only the prefixes you need.

 - Your source CSS files no longer need prefixes, so they're easier to maintain. Prefixes are added/removed automatically, based on your configuration and current browser market share.

## Slides

[The slides from this talk](https://speakerdeck.com/noahcollins/smarter-css-prefixes-with-autoprefixer).

## More Documentation

To see more details about using the grunt-autoprefixer task, refer to the [grunt-autoprefixer GitHub repo](https://github.com/nDmitry/grunt-autoprefixer).

For more details about configuring specific browser support, see the Browsers section of the [autoprefixer docs](https://github.com/ai/autoprefixer#browsers).

## Sample Configuration

```js
// Gruntfile.js

grunt.initConfig({

  autoprefixer: {

    options: {
        browsers: [
            'last 2 version',
            '> 1%',
            'ie 8',
            'android 4'
            ]
    },

    // Prefix a single file and output it to a new file
    single_file: {
      src: 'src/css/file.css',
      dest: 'dest/css/file.css'
    },

    // Omit the `dest` parameter to overwrite your source file(s)
    overwrite: {
      src: 'dest/css/file.css' // globbing is also possible here
    }
  }
})
```
## Further Reading

[Autoprefixer: A Postprocessor for Dealing with Vendor Prefixes in the Best Possible Way](http://css-tricks.com/autoprefixer/) by Andrey Sitnik (Autoprefixer author). August 2013.

[How To Deal With Vendor Prefixes](http://css-tricks.com/how-to-deal-with-vendor-prefixes/) by Chris Coyier. December 2012.

### Older posts

These posts contain partially outdated information but they're useful if you want more context.

[Vendor Prefixes - about to go south](http://remysharp.com/2012/02/09/vendor-prefixes-about-to-go-south/) by Remy Sharp. February 2012.

[New Proposal Could End the CSS Prefix Madness](http://www.webmonkey.com/2012/05/new-proposal-could-end-the-css-prefix-madness/) by Scott Gilbertson. May 2012.


## License

MIT License © [Noah Collins](https://twitter.com/noahec)