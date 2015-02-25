# **Short SASS**
---------------

Just another SASS library to simplify the way you use SASS.

We're trying to create shorthand for many CSS properties, like `@include absolute-top-left;` as `position: absolute; top: 0; left: 0;`.
Beautiful? Let's get see how it's works!

### **Example**
***

```sass
// Import normalize and resetter without think more.
@include normalize;
@include reset;


// Lets start with font-face generator. Really simple!
@include font-faces('arial' 'assets/fonts/arial', regular bold italic);


// Forget about regular things.
body {
    // With this one:
    @include font-smoothing;

    // You don't need to write:
    speak: none;
    font-variant: normal;

    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

// A lot of use display, width and height? Try this.
.simple-box {
    // With this one:
    @include block(100% 500px);

    // You don't need to write:
    display: block;
    width: 100%;
    height: 500px;
}

// What about positioning? Try this.
.simple-position {
    // With this one:
    @include absolute-middle-center;

    // You don't need to write
    position: absolute;
    top: 50%;
    left: 50%;
    -webkit-transform: translate(-50%, -50%);
    -moz-transform: translate(-50%, -50%);
    -mz-transform: translate(-50%, -50%);
    -o-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
}

// More hard things? Let's try!
.complex-gradient {
    // With these simple breath, the possibility to combine values:
    @include linear-gradient((-90deg, #fff, #ff8), true);   // Append values.
    @include linear-gradient((-90deg, #dff, #3d8), true);
    @include radial-gradient((center, #ae9, #d38), true);
    @include linear-gradient((-90deg, #73d, #f83), true);
    @include radial-gradient((center, #dd9, #88d), true);
    @include radial-gradient((center, #a9f, #ff1), true);
    @include linear-gradient((-90deg, #99d, #1f0));         // Write the styles!

    // You're freem from these things :P
    background-image: -webkit-linear-gradient(-90deg, #fff, #ff8), -webkit-linear-gradient(-90deg, #dff, #3d8), -webkit-radial-gradient(center, #ae9, #d38), -webkit-linear-gradient(-90deg, #73d, #f83), -webkit-radial-gradient(center, #dd9, #88d), -webkit-radial-gradient(center, #a9f, #ff1), -webkit-linear-gradient(-90deg, #99d, #1f0);
    background-image: -moz-linear-gradient(-90deg, #fff, #ff8), -moz-linear-gradient(-90deg, #dff, #3d8), -moz-radial-gradient(center, #ae9, #d38), -moz-linear-gradient(-90deg, #73d, #f83), -moz-radial-gradient(center, #dd9, #88d), -moz-radial-gradient(center, #a9f, #ff1), -moz-linear-gradient(-90deg, #99d, #1f0);
    background-image: -ms-linear-gradient(-90deg, #fff, #ff8), -ms-linear-gradient(-90deg, #dff, #3d8), -ms-radial-gradient(center, #ae9, #d38), -ms-linear-gradient(-90deg, #73d, #f83), -ms-radial-gradient(center, #dd9, #88d), -ms-radial-gradient(center, #a9f, #ff1), -ms-linear-gradient(-90deg, #99d, #1f0);
    background-image: -o-linear-gradient(-90deg, #fff, #ff8), -o-linear-gradient(-90deg, #dff, #3d8), -o-radial-gradient(center, #ae9, #d38), -o-linear-gradient(-90deg, #73d, #f83), -o-radial-gradient(center, #dd9, #88d), -o-radial-gradient(center, #a9f, #ff1), -o-linear-gradient(-90deg, #99d, #1f0);
}

// Or want to be free at anywhere?
.simple-box {
    // It's default media
    @include inline-block(320px 240px);

    // Let's drive to mobile
    @include mobile-portrait {
        @include block(100% auto);
    }
}
```

### **Download**
***

You can choose the download option above, or use `NPM` or `Bower`

```
bower install short-sass
```
```
npm install short-sass
```

### **Notes**
***

We still working on documentation and trying to add more shorthand. Feel free to try this. ;)

### **Release History**
***

* 2015-02-25          v1.0.0          "First release."