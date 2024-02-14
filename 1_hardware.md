# Hardware

## Which Raspberry Pi?

My recommendations are

1. Raspberry Pi 4, 400 or 5. 5 is recommended.
2. At least 4GB of RAM. 8GB of RAM is recommend.

Of the Raspberry Pi models, only Pi 4, 400 or 5 is powerful
enough to be a desktop computer.

Pi 5 is about twice as fast as Pi 4 or 400, and Pi 5 only
costs $5 more than the corresponding Pi 4 or 400 models,
with the same amount of RAM. So Pi 5 is recommended if
you're making a new purchase. However, if you have Pi 4
or 400, they'll work just fine.

Pi 4 and 400's speed differences are visible. For example,
Pi 4 and 400 does not play 1080p Youtube videos well, while
Pi 5 does. So you'll most likely have to stick to 720p
Youtube videos with Pi 4 and 400, even when overclocked.

In summary, you'll need a Pi 4, 400 or 5 with at least
4GB of memory. I recommend the 8GB Pi 5 at $80 as of this
writing if you're purchasing one.

I'll discuss overlocking for Pi 4, 400 and 5 in the Pi OS
chapter, and other tuning such as increasing swap space
to 4GB, which is a must for the 4GB RAM models but also
recommended for the 8GB RAM models.

## Storage

### Storage size matters when it comes to performance

In all of the storage formats discussed in the Storage
section, the larger capacity models, i.e., 128GB or larger
models, typically perform much better than the 64GB or
smaller models. So don't choose a model that's smaller
than 128GB.

I'll share performance numbers from Raspberry Pi
Diagnostics tool, which can be found under Accessories,
in the later section of this chapter, after covering all
supported Storage format.

### microSD

Raspberry Pi supports booting from a microSD, in the
smaller Micro SDXC format.

After testing many makes and models of microSDs, I
recommend Samsung Pro Plus microSD, either the 128GB or the
256GB. This model outperforms all other brands and models.

Here is a link to Samsung Pro Plus 128GB microSD,
[Amazon Samsung Pro Plus 128GB microSD](https://www.amazon.com/dp/B0C1PT9XXS)

I used this microSD daily for several weeks and had not
observed slowness due to the use of this microSD. I had
used 2 other slower and cheaper microSD makes and models,
and I did observe slowness whenever Pi OS is reading or
writing to the swap space.

### USB ports

Raspberry Pi has 2 types of USB ports, supporting USB2 and USB3, and is color coded as black and blue, respectively.

For maximum performance, ensure you plug your USB3 Flash
drive into 1 of the 2 blue USB3 ports!

Use the black USB2 ports for keyboard and mouse.

Raspbery Pi USB3 port only supports 3.0. So plugging
USB 3.1 or 3.2 USB Flash drives into Raspberry Pi USB3
ports cannot obtain the USB 3.1 or 3.2 performance.
Instead these higher performance USB Flash drives
will operate at USB 3.0 performance. Plus
these USB 3.1 or 3.2 Flash drives typically cost more
than twice my recommendation below.

Don't use USB2 Flash drives to run Pi OS.
They are slower than the Samsung Pro Plus microSD.

Lastly, if you need more USB3 ports, get a USB3 hub.
I use the [UGREEN USB 3.0 Hub with 4 Ports](https://www.amazon.com/UGREEN-Ultra-Slim-Supported-multiport-Compatible/dp/B08Y8CJKJC/).

### USB3 Flash Drive

Raspberry Pi also supports booting from USB3 Flash drive.

After testing many makes and models of USB3 Flash drive,
I recommend the
[Samsung BAR Plus 128GB](https://www.amazon.com/dp/B07BPK3XWW)
model. The 256GB model will also work but costs more.

The Samsung BAR Plus 128GB USB3 Flash drive performs
better than Samsung Pro Plus microSD 128GB, and costs
the same.

I recommend USB3 Flash drive over microSD for
Raspberry Pi as the respective Samsung models
costs about the same but the USB3 Flash drive
has higher performance, and is more reliable.

### SATA Drive with USB3 Adapter

Similar to the USB Flash drive, one can attach a 2.5"
SATA SSD drive to Raspberry Pi using a USB3-SATA adapter.

This configuration is the most expensive since you
need to buy a SATA-USB3 adapter and a SATA drive.
However, it's the best option if you need more
than 256GB of storage as the Samsung BAR Plus Flash
drive only goes up to 256GB, whereas a SATA drive
can go up to 2TB, or 8 times the capacity.

I recommend the following 2 SATA-USB3 adapters:

1. [JSAUX SATA-USB Adapter](https://www.amazon.com/dp/B083ZJZGH2)

2. [StarTech SATA-USB Adapter](https://www.amazon.com/dp/B00HJZJI84)

The biggest difference between these 2 SATA-USB3 adapter
is their cable lengths, with JSAUX having shorter length.

As for the SATA drives, I recommend the following:

1. [Kingston A400 480GB SATA SSD drive](https://www.amazon.com/dp/B01N0TQPQB)

2. [TeamGroup AX2 512GB SATA SSD drive](https://www.amazon.com/gp/product/B08CK7T9FG)

### NVMe Drive with NVMe Board for Pi 5

This is only available to Pi 5. It's expected to provide
both the highest performance and capacity.

#### PCIe Gen 2 only

Firstly, while it's possible to force PCIe Gen 3,
Pi 5 officially only support Gen 2. And every NVMe
board I tested so far is unstable running with PCIe
Gen 3 but perfectly stable with PCIe Gen 2.

#### NVMe boards tested

Here are the 4 NVMe boards I tested so far.

1. [Geekworm X1002](https://www.amazon.com/gp/product/B0CQYBBNP5/)

2. [Pimoroni NVMe Base](https://shop.pimoroni.com/products/nvme-base)

3. [52Pi N04 M.2 2280 PCIe to NVMe](https://52pi.com/products/n04-m-2-2280-pcie-to-nvme-top)

4. [Waveshare PCIe to M.2](https://www.waveshare.com/product/raspberry-pi/boards-kits/raspberry-pi-5/pcie-to-m.2-hat-plus.htm)

The Geekworm X1001 did not work. The other 3 all worked.

I like the Pimoroni NVMe Base best because you can buy it
with a compatible NVMe drive. Pimoroni also publishes a
list of compatible NVMe drives, and incompatble NVMe
drives, while other vendors do not publish such info.

For the 52Pi N04 NVMe board, I bought the NVMe drive
as show in their picture, which is a Kingston NV2 250GB
NVMe drive.

The Waveshare NVMe board is currently the only one
that documented to support HAT+ standard but I found
that I still need to configure the appropriate config.txt
flag, so not quite sure what HAT+ standard support means.

I would like to be able to test 2 more NVMe boards or
solutions:

1. Raspberry Pi NVME board

2. [Argon NEO 5 M2. NVMe PCIe Case](https://argon40.com/products/argon-neo-5-m-2-nvme-for-raspberry-pi-5)

The ideal Pi 5 NVMe solution is a case that will
support and enclose both the active cooling solution and NVMe drive.

Currently Argon NEO 5 is the only such solution.

### Storage performance data

Here is a table with performance results from Raspberry
Pi Diagnostics tool, which can be found under Accessories.

NB: I recommend ignoring the right most 2 digits, i.e.,
rounding the rightmost 2 digits to 0. Consider the
rightmost 2 digits as noise.

The performance results are faster when attached to Pi 5,
because Pi 5 has a dedicated RP1 I/O controller.

| Drive | Sequential Write (KB/s) | Random Write (IOPS) | Random Read (IOPS) |
| :------------------------------ | -----: | ---: | ---: |
| Kingston SATA Pi 5              |  68768 | 6382 | 4815 |
| Silicon Power SATA Pi 5         |  62296 | 2596 | 2935 |
| SanDisk 32GB USB Pi 5           |  71312 |  672 | 1775 |
| Samsung BAR Plus 256GB USB Pi 5 | 116819 | 7424 | 3336 |
| Samsung BAR Plus 128GB USB Pi 5 |  62178 | 6229 | 3175 |
| Samsung FIT Plus 256GB USB Pi 5 | 115380 | 7406 | 3369 |
| Samsung Pro Plus 128GB Pi 5     |  54704 | 2371 | 6617 |
| Samsung Pro Plus 128GB Pi 400   |  31922 | 1476 | 4801 |
| Pioneer 64GB Pi 5               |  16129 | 1113 | 3219 |
| Pioneer 64GB Pi 400             |  16761 | 1173 | 3309 | 
| PNY 64GB Pi 5                   |  49164 |  879 | 2323 |
| PNY 64GB Pi 400                 |  31417 |  860 | 2367 |

## Power Suppply

For Pi 5, get the Raspberry Pi's Pi 5 Power Supply.
You'll need this power supply to overclock and power
the SATA or NVMe drive. It's true you can use a Pi 4
Power Supply for Pi 5 but this most likely means you
have to stick to microSD as storage.

For Pi 4 or 400, you can get the Raspberry Pi's Pi 4
Power Supply, but unfortunately it doesn't have a
on/off switch. So as an alternative with on/off
switch, I recommend [iUniker 20W 5V 4A Power Supply](https://www.amazon.com/gp/product/B097P2NLVH).

## Case and Cooling

Since we'll be overclocking, we need active cooling
solutions with large heatsink and quiet fan.

NB: I dislike jet engine sound fans.

The situation for Pi 5 is changing day to day as new case
and cooling solutions become available.

The gap is further exacerbated if you would like an
enclosed case with active cooling that supports NVMe
boards.

Here are my current recommendations for Pi 4 and 5
respectively.

[GeeekPi ABS Case for Pi 5](https://www.amazon.com/dp/B0CP5HXYCK)

The GeeekPi ABS case comes with
Armor Lite V5 heatsink and fan, both the heatsink and
fan are larger and quieter than Raspberry Pi's Active
Cooler. The only downside with this case is it's an
assemble once case, as the 4 screws mars the ABS case when
you tighten the screws.

Similarly for Raspberry Pi 4, an good active cooling
solution is needed to overlock. I find the ICE Tower Cooler
to be the best. However, it's $30.

[GeeekPi Pi 4 Metal Case with Ultra Thin ICE Tower Cooler](https://www.amazon.com/dp/B08CVDRCKT)

Pi 5 case and cooling solutions beats Pi 4 on cost, so
another reason why Pi 5 is preferred over Pi 4, if you
are buying a new Raspberry Pi.

The best Pi 4 passive cooling solution is Pi 400.
Unfortunately Pi 400 only comes with 4GB RAM.
While 4GB RAM is usable, it is less optimal than 8GB of RAM.

The only case with active cooling and NVMe support for
Pi 5 at this time is the
[Argon NEO 5 M2. NVMe PCIe Case](https://argon40.com/products/argon-neo-5-m-2-nvme-for-raspberry-pi-5).

Unfortunately I have not test it so cannot tell you
how well it performs with its active cooling or
NVMe support. I'll update this section once I have
had a chance to test it.

