# Guardian Lock [![Cult Of Martians][cult-img]][cult]

<img src=".icons/app_icon.png" align="right"
     title="Icon by tawtsvenz" width="120" height="178">

Size Limit is a tool to prevent JavaScript libraries bloat.
With it, you know exactly for how many kilobytes your JS library
increases the user bundle.

You can add Size Limit to your continuous integration service
(such as Travis CI) and set the limit. If you accidentally
add a massive dependency, Size Limit will throw an error.

<p align="center">
  <img src="./icons/example.png" alt="Size Limit example"
       width="654" height="450">
</p>

Size Limit could tell you not only library size. With `--why` argument it can
tell you *why* your library has this size and show real cost of all your
internal dependencies.

<p align="center">
  <img src="./img/why.png" alt="Bundle Analyzer example"
       width="650" height="335">
</p>

<p align="center">
  <a href="https://evilmartians.com/?utm_source=size-limit">
    <img src="https://evilmartians.com/badges/sponsored-by-evil-martians.svg"
         alt="Sponsored by Evil Martians" width="236" height="54">
  </a>
</p>

[Size Limit: Make the Web lighter]: https://evilmartians.com/chronicles/size-limit-make-the-web-lighter
[cult-img]:                         http://cultofmartians.com/assets/badges/badge.svg
[cult]:                             http://cultofmartians.com/tasks/size-limit-config.html

## Who Uses Size Limit

* [MobX](https://github.com/mobxjs/mobx)


## How It Works

You can find more examples in **[Size Limit: Make the Web lighter]** article.

To be really specific, Size Limit creates an empty webpack project in memory.
Then, it adds your library as a dependency to the project and calculates
the real cost of your libraries, including all dependencies, webpack’s polyfills
for process, etc.


## Usage

First, install `size-limit`:



## Config

Size Limits supports 3 ways to define config.

1. `size-limit` section to `package.json`:

   ```json
     "size-limit": [
       {
         "path": "index.js",
         "limit": "9 KB"
       }
     ]
   ```