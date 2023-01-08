# uoeia -- Universally Open Every Image Available

A small utility script which displays the specified image(s), image url(s) or image gallery url(s) using your preferred image viewer.

Basically, point it to something containing images and it should open it in your image viewer.

## Usage

`uoeia [OPTION]... [FILE|URL]`

Displays the specified image using your preferred image viewer.

Can open remote urls of individual images, galleries, as well as local files at the same time.
Uses gallery-dl for remote gallery opening - so if gallery-dl can open it, so can your image viewer.

Options:

  `-v`, `--viewer`       Specify the image viewer to use.

  `-q`, `--quiet`        Don't display any output during normal operation.

  `-g`, `--gdlopts`      Pass through options to gallery-dl. Take care to fully quote each passed option.

  `-r`, `--replace`      Url patterns to replace in the format `'mypattern:::myreplacement'`

  `-h`, `--help`         Show this help message and exit.

## Examples

`uoeia my-image.jpg`

Display a local image file.

`uoeia https://example.com/image`

Display an image/image gallery from a URL.

`uoeia -v imv https://example.com/image`

Display an image from a URL using imv.

`uoeia -g \"--range 1-10\" https://reddit.com/r/earthporn`

Download and display the first 10 results.

`uoeia -r 'nitter.net:::twitter.com' https://nitter.net/donttrythis/`

Display images from twitter directly instead of its
open source interface nitter.

## Issues

If you spot a bug or have an idea feel free to open an issue.

Pull requests are always warmly welcomed.

Thanks for using my software ❤️
