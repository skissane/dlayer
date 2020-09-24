# dlayer
dlayer is docker layer analyzer.

## Installation
```bash
go get github.com/orisano/dlayer
```
or
```
docker pull orisano/dlayer
```

## How to use
```bash
$ dlayer -h
Usage of dlayer:
  -a	show details
  -d int
    	depth (default 8)
  -f string
    	layer.tar path (default "-")
  -i	interactive mode
  -l int
    	screen line width (default 100)
  -n int
    	max files (default 100)
```

```bash
# recommended
docker save image:tag | dlayer -i
```
or
```bash 
docker save image:tag | dlayer -n 100 | less
```
or
```bash
docker save -o image.tar image:tag
dlayer -f image.tar -n 1000 -d 10 | less
```

![screenshot](https://github.com/orisano/dlayer/raw/images/images/screenshot.png)

## Related Projects
* [orisano/bctx](https://github.com/orisano/bctx) - for build context analysis

## Author
Nao Yonashiro (@orisano)

## License
MIT
