# Photo Diary

A simple photo diary using SCSS and static heights to demonstrate rapid CSS scaffolding (uses Bootstrap)

## How to use

`http-server` from the root, and visit the address supplied.

## Rolling your own

1. `gem install compass` to install Compass for SCSS precompilation.
2. `gem install bootstrap-sass` to install the SCSS version of Bootstrap.
3. `compass create photo-diary -r bootstrap-sass --using bootstrap` to roll up the project.

Use the `sass` directory to write your CSS, with the precompilation bonuses of SCSS (such as variables and nesting). Use `compass watch` to watch changes to your SCSS files and output the resulting CSS to the `stylesheets` directory.

Develop in the following order:

- Layout (grids and vertical heights): mostly through Bootstrap classes in your HTML using the [Bootstrap Grid guide](http://getbootstrap.com/css/#grid)
- Typography (text and legibility): mostly through a `_typography.scss` partial and directly targetting elements like `h1` and `p`
- Components (i.e. co-responsible chunks of HTML): mostly through one file per component, i.e. `_photo-diary.scss`. Aim to target `.classes` and eliminate magic numbers using `$variables`
- 'Trumps' (i.e. things that don't fit in the above): mostly through a single file, `_trumps.scss`, and the use of the `!important` flag to override any conflicting styles. Keep this file small.
