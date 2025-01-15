<h1 float="center">
  <img src="/other/img/hero.jpg" width="96%" /> 
</h1>

**Less, but better.** - Dieter Rams

After seeing the [Ferris Sweep](https://github.com/davidphilipbarr/Sweep) for the first time I've fallen in love, but as a designer I cannot accept the things the way they are. So I've done some experimentation with it.

I changed the overall form of the board so it can be a little bit more compact and be a canvas for expression in the matter of case design

This is a parcial redesign of the [Ferris Sweep 2 half-swept](https://github.com/davidphilipbarr/Sweep). In other words this is a:

- 34 keys.
- Diodeless.
- Low profile.
- Non-hotswap.
- Reversible PCB.
- Column staggered.
- [Tenting puck](https://splitkb.com/products/tenting-puck) compatible.
- Wireless and wired capable.
- Choc MBK spaced (17,5mm x 16,5mm).
- Cheaper than the [cheapino](https://github.com/tompi/cheapino) (at the time of the build).

### What have been done:

- Change PCB overall form.
- Add support screw holes.
- Create an [assembly manual](/other/manuals/k02-assembly-manual.pdf).
- Add teardrop on solder joints.
- Reposition of the reset and power switch.
- Create an alternative version with `USB-C` instead of `TRRS`.
- Add commissioned art by the brazilian artist [Aline Dal Pont](https://www.instagram.com/manifesto.efemero/).
- Remove all the informative silk graphics for a better looking board.

### What I may do<sup>1</sup>:

- Rotate the main switches.
- Change the `USB-C` location.
- Add open hardware logo on silk.
- Make it compatible with choc V2 switches.
- Change the `USB-C` connector to mid-mount 6p.
- Design some _minimalist_ and _low profile_ cases.
- Extend the manual to include [ZMK](https://zmk.dev/) flashing process.
- Create an 36 keys pcb with breakpoints/mousebites.
- Add a variation with choc spacing for [CFX keycaps](https://kbd.news/CFX-keycap-1553.html) (16,5mm x 16,5mm).

> <sup>1</sup> The main reason for not doing this at the moment is the lack of financial motivation. As I have to pay for every prototype and take time off to do the development and iterations I have to be mindful of the tasks I take. If you want to help [contact me](https://www.reddit.com/user/kynikoi_/) :)

## Silk art

I commissioned the work of the brazilian artist [Aline Dal Pont](https://www.instagram.com/manifesto.efemero/) for this board. You can use it as it is (with the credits) for non-commercial ends. You cannot use the work outside of this board, modify it in any way or use it commercially without the express autorization of the artist.

<p float="center">
  <img src="/other/img/photos/img (8).jpg" width="48%" /> 
  <img src="/other/img/photos/img (5).jpg" width="48%" /> 
</p>

## Versions

At the moment this repo contains 2 versions, one with `TRRS` and one with `USB-C` connecting the halves. The `TRRS` connector are objectively worse than the `USB-C` for this use case, due to it introducing a risk of short in the case that the halves are unpluged with the board powered on. On the other side, the `USB-C` if not wired correctly may introduce a [risk of being connected directly to a power supply](https://docs.qmk.fm/features/split_keyboard) by mistake. I've done the bare minimum to prevent it, I wired the `GND` and `VCC` trying to follow the USB protocol. Another problem with the `USB-C` is that this implementation doesn't follow the USB protocol, it just hijack some of the data pins.

The [gerber files are in the release section.](https://github.com/anothermimich/K02/releases)
The list of materials for each version are inside of the respective folder, [USB-C](/USB-C/README.MD) and [TRRS](/TRRS/README.MD).

## Assembly

As the pcb doesn't have any information guiding the assembly, I have done an [manual with visual instructions](/other/manuals/k02-assembly-manual.pdf).

<a href="/other/manuals/k02-assembly-manual.pdf" float="center">
<img src="/other/img/k02-assembly-manual-display.jpg" width="96%" />
</a>

## Keymap

As this redesign have not changed the pin out the [Ferris Sweep](https://github.com/davidphilipbarr/Sweep) you can use any compatible keymap/firmware.

Currenty I'm using the above [zmk](https://zmk.dev/) keymap, you can replicate it with [this files](https://github.com/anothermimich/zmk-config-k02).

<a href="https://github.com/anothermimich/zmk-config-k02" float="center">
<img src="https://github.com/anothermimich/zmk-config-K02/blob/main/other/img/k02-keymap.jpg" width="96%" />
</a>

> I've tried to use the [Miryoku ZMK](https://github.com/manna-harbour/miryoku_zmk) keymap made by [Manna Harbour](https://github.com/manna-harbour), but I was not able to adapt it to my needs. If you want to see my initial setup take a look at the [compiled firmware](/other/old%20miryoku%20keymaps/) or the source [github workflow](https://github.com/anothermimich/miryoku_zmk/blob/master/.github/workflows/workflow-build-k02.yml), [custom_config.h](https://github.com/anothermimich/miryoku_zmk/blob/master/miryoku/custom_config.h), [cradio_left.conf](https://github.com/anothermimich/miryoku_zmk/blob/master/config/cradio_left.conf) and [cradio_right.conf](https://github.com/anothermimich/miryoku_zmk/blob/master/config/cradio_right.conf) files.

## Disclaimer

The files in this repo may contain problems, use them at your own risk.

For the type nerds _(like me)_, the text on the PCB and logo are [FuturaRenner](https://www.fontsquirrel.com/fonts/futura-renner) aka [Formera](https://github.com/noirblancrouge/Formera).

The team behind the design of the incredible [Ferris Sweep](https://github.com/davidphilipbarr/Sweep) are: [Pierre Chevalier](https://github.com/pierrechevalier83), [David Barr](https://github.com/davidphilipbarr), [Ibnu Daru Aji](https://github.com/ibnuda/), [Duccio](https://github.com/duckyb). Without their work this parcial redesign would not be possible.
