# Nox Custom Loading Page

Looks stupid, but yeah..\
Maybe you're bored and want to mess your nox emulator a little?\
Not messing the emulator itself tho, but its loading screen.

Some days ago i was browsing aimlessly, and find out this thing is actually a local file downloaded from certain place, so i decided to edit this file called `ads` a bit.

Im not sure whether nox can load this when there is no `ads` file located in the said folder below in the first place.\
I think it needs to actually load the original `ads` file then you can overwrite it with this file for this custom page to load.

Oh right, idk maybe you already know this, but the user agent string for this nox loading screen is:
`Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/538.1 (KHTML, like Gecko) Nox Safari/538.1`
Windows NT and WOW64 since im running on windows 7 64 bit (maybe), but i cant figure out what browser is AppleWebKit 538.1.\
Looks like some old browser but im not sure.

## Features

Some features (if you can call it features):
- custom background images
- random background images from danbooru
- play video from danbooru (well, if you want tho?)

## Configuring

You can change everything if you want it.

### JavaScript

For standard configuration, you can change these variables value. These variables available from line 237 to 247.

- `var turnonrandom = 1;`

change the value to 0 to completely disable random background and use default supplied from css, 1 to enable random background.

- `var fetchdanbooru = 1;`

change the value to 0 to disable random background fetched from danboru, 1 to enable random from predefined images and danbooru, 2 to enable random from danbooru only (ignore predefined images).

- `var disablevideo = 1;`

change the value to 0 to enable playing video (if available), 1 to disable playing video.

- `var enablerandomtags = 1;`

change the value to 0 to disable random tags from your defined random tags, 1 to enable random.

- `var danbooruutags = 'tags';`

your single danbooru tags. you may include another tag, but iirc danbooru only accept two tags simulatenously. example: 'blazblue jin_kisaragi'. works like usual 
danbooru tags

- `var randomtags = ['tags', 'tags'];`

if you enable random tags, insert your desired tags to the array. separate every strings with comma. you can insert two tags simultaneously like danboorutags too. 
example: ['tag1', 'tag2 another_tag'];

- `var danboorupage = null;`

accepts integer (example: 1000) and null. change the value to any integer (1 to 1000). if you change it to null, it will set to 200 by default. used to define maximum page fetch from danbooru.

- `var booruver = 'danbooru';`

accepts string 'safebooru' and 'danbooru'. well, maybe you dont want any graphic suddenly popped out from these, so its better to use safebooru. the default is safebooru.

- `var enableheader = 1;`

change the value to 1 to enable header & random messages, 0 to disable.

- `var rands = ['texts'];`

insert your random message here if youre bored. separate your sentence with comma. example: ['this is sentence 1', 'this is sentence 2'];

You can change predefined image by changing `widebg` array that starts from line 254 and `narrowbg` array that starts from line 275.

### CSS

The default image is still somehow heavy, or maybe not in your favor? You can change that too! Im too lazy to compress that rascal.\
Wait. Did you just say something about my sopdoge?

For tablet resolution, you can change the background image source on `li.page0` and `li.page-actived0`.
For phone resolution, you can change that on `html.mb li.page0` and `html.mb li.page-actived0`.

## How to use the sauce

When you choose random, it provides some sauce for the background too.\
Take a look to the bottom left corner and you will find `danbooru: <danbooru id> | pixiv: <pixiv id>`.\
For danbooru, just go straight to `https://danbooru.donmai.us/posts/<danbooru id>` and `https://pixiv.net/artworks/<pixiv id>` for pixiv.

## How to install

Just go straight to `C:\Users\[Your User name]\AppData\Local\Nox\loading` folder, place this `ads` file on that folder (overwrite if there is a file named `ads` too).\
Right click the `ads` file you just copy or move, choose properties, **tick `Read-only` on Attributes** so it will survive since nox sometimes would overwrite this file too.


## Important, maybe

- If you turn on `fetchdanbooru` but not turn on `turnonrandom`, it wont work since you dont accept random background in the first place.
- I think if your pc is that darn slow, you need to disable video playback on this. Or just place a blank page. Idk, maybe just dual boot with x86 android.
- No, im not filtering any input. its on your own machine.
- I dont know why, but the nox loading browser cant play video on loop. im trying many things but it still not working so i guess its browser things. surprisingly, it would play video automatically even when im not clicking it. Still can't loop sop junyaa tho.
- Im keeping the click ability from the original page to play video on this just in case the video can't run automatically. Can't figure another use of that thing, so im using it as a button to change the background if random background enabled. feel free to modify the line 692-700.
- You may as well [check this out](https://gist.github.com/Log1x/12d330ef7685d6fbc611d1d57efb5c29) too to find out about debloating nox.
- Its better to not have a loading screen at all? [try this.](https://gist.github.com/Log1x/12d330ef7685d6fbc611d1d57efb5c29#gistcomment-2931821)
- Again, don't forget to **make this `ads` file read-only**. It happened to me lol

## The last

Its all messed up, just like my life.\
Thanks to everyone, and (for sure) you too.