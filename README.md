
<!---

This README is automatically generated from the comments in these files:
super-patternset-svg.html

Edit those files, and our readme bot will duplicate them over here!
Edit this file, and the bot will squash your changes :)

The bot does some handling of markdown. Please file a bug if it does the wrong
thing! https://github.com/PolymerLabs/tedium/issues

-->

[![Build status](https://travis-ci.org/oneezy/super-patternset-svg.svg?branch=master)](https://travis-ci.org/oneezy/super-patternset-svg)

_[Demo and API docs](https://elements.polymer-project.org/elements/super-patternset-svg)_


##&lt;super-patternset-svg&gt;

The `super-patternset-svg` element allows users to define their own pattern sets
that contain svg patterns. The svg pattern elements should be children of the
`super-patternset-svg` element. Multiple patterns should be given distinct id's.

Using svg elements to create patterns has a few advantages over traditional
bitmap graphics like jpg or png. patterns that use svg are vector based so
they are resolution independent and should look good on any device. They
are stylable via css. patterns can be themed, colorized, and even animated.

Example:

```html
<super-patternset-svg name="my-svg-patterns" size="24">
  <svg>
    <defs>
      <g id="shape">
        <rect x="12" y="0" width="12" height="24" />
        <circle cx="12" cy="12" r="12" />
      </g>
    </defs>
  </svg>
</super-patternset-svg>
```

This will automatically register the pattern set "my-svg-patterns" to the patternset
database.  To use these patterns from within another element, make a
`super-patternset` element and call the `byId` method
to retrieve a given patternset. To apply a particular pattern inside an
element use the `applypattern` method. For example:

```javascript
patternset.applypattern(patternNode, 'car');
```


