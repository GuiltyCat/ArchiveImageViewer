SaltViewer
===============

Now on development.

Why
-------------

I use mcomix for a long time. However,

- mcomix do not support GIF animation.
- mcomix do not support switch rm command and trash command.
- mcomix3 do not support delete command.

Thus I need mcomix alternative.
I need these functions.

- Support many image type
- Support archive like zip, rar, 7z without extraction
- Support animation image like GIF.
- Support delete and trash command.


Feature
------------

- [x] Pure python
- [x] Single script
- [] Support archive
	- [x] Zip
	- [x] Rar
	- [x] 7z
	- [ ] pdf
- [x] Support image type
    - obey pillow
	- svg
- [x] Support dual page mode
- [x] Support animation
	- [x] duration auto adjustment
	- [x] GIF
- [x] Repetition key
- [x] Delete image
- [x] Configure file
- [ ] Cache image for speed

How to use
-----------

### Install Requirements

My envirionment is `python3.9.3`. However it will work on old version of `python`.

Install via pip.

- cairosvg
- natsort
- pdf2python
- pillow
- py7zr
- rarfile
- send2trash

Install via package manager or other method.

- unrar(preferred), unar or bsdtar
- poppler

```
pip install natsort pillow send2trash
```

```
sudo apt install unrar
sudo pacman -S unrar
```

### Run

```
python archived_image_viewer.py <image file | archive file>
```

### Keymap


```
[Keymap]

DoublePage  = d
TrashFile   = Delete

NextPage    = h
PrevPage    = l

# You can use repetition for NextPage and PrevPage.
# For example, 2h means goto next 2 page, type 100h go to next 100 page.
# If you want to reset number, type <Esc>, <Ctrl+[> or simply <[>

NextArchive = j
PrevArchive = k

FitNone     = N
FitWidth    = W
FitHeight   = H
FitBoth     = B

PageOrder   = o

Quit        = q
Head        = g
Tail        = G
```
