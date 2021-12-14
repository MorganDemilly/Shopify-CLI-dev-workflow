# Shopify Theme Development workflow with Shopify CLI, Sass, Gulp, Github

## Set up Shopify CLI
- https://shopify.dev/themes/tools/cli/installation
- Authenticate
```curl
shopify login --store johns-apparel.myshopify.com
```
- Create a new theme
```curl
shopify theme init
```
- Preview, test, and share your theme
```curl
shopify theme serve
```

## Set up Sass and Gulp
- Init
```curl
npm init
```
- Install gulp
```curl
npm install gulp
```
- Add node_modules in .gitignore
- Install sass
```curl
npm install sass node-sass gulp-sass
```
- Create a gulpfile
```js
const gulp = require('gulp');
const sass = require('gulp-sass')(require('sass'));

gulp.task('sass', function() {
    return gulp.src('styles/*.scss')
    .pipe(sass())
    .pipe(gulp.dest('assets'))
});

gulp.task('watch', function() {
    gulp.watch('styles/**/*.scss', gulp.series('sass'));
});
```
- Compile scss to css
```curl
gulp watch
```

## Set up Git
- Create Git Repository with [Github](https://github.com)
```curl
git init
```
- [Sync Folder to Git Repository](https://docs.github.com/en/github/getting-started-with-github/managing-remote-repositories)
```curl
git remote add origin [repository url]
```
- Commit Progress
```curl
git add -A
git commit -m "initial commit"
git push origin master
```
