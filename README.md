```
$ hugo version
Hugo Static Site Generator v0.62.0/extended linux/amd64 BuildDate: unknown
```

```
$ git submodule update --init --recursive
$ hugo server
Building sites … panic: runtime error: invalid memory address or nil pointer dereference
[signal SIGSEGV: segmentation violation code=0x1 addr=0x20 pc=0x55e2ee4cea2a]

goroutine 207 [running]:
github.com/gohugoio/hugo/hugolib.(*shortcodeHandler).extractShortcode(0xc000c53980, 0x1, 0x0, 0xc000c5ac40, 0x1, 0x55e2eee13d3a, 0x1)
	/build/hugo/src/hugo-0.62.0/hugolib/shortcode.go:496 +0x89a
github.com/gohugoio/hugo/hugolib.(*pageState).mapContent(0xc000c59d70, 0xc0000e6540, 0xc0005bd180, 0x0, 0xc000c7db88)
	/build/hugo/src/hugo-0.62.0/hugolib/page.go:750 +0xb09
github.com/gohugoio/hugo/hugolib.newPageWithContent.func1(0xc0000e6540, 0x55e2ed9c8f6c, 0xc000c7dbe0)
	/build/hugo/src/hugo-0.62.0/hugolib/page__new.go:233 +0x4d
github.com/gohugoio/hugo/hugolib.(*pagesMap).initPageMeta.func1()
	/build/hugo/src/hugo-0.62.0/hugolib/pages_map.go:77 +0x52
sync.(*Once).doSlow(0xc0003b9920, 0xc000c7dc58)
	/usr/lib/go/src/sync/once.go:66 +0xe5
sync.(*Once).Do(...)
	/usr/lib/go/src/sync/once.go:57
github.com/gohugoio/hugo/hugolib.(*pagesMap).initPageMeta(0xc000c5ab90, 0xc000c59d70, 0xc0000e6540, 0x0, 0x0)
	/build/hugo/src/hugo-0.62.0/hugolib/pages_map.go:75 +0xa3
github.com/gohugoio/hugo/hugolib.(*pagesMap).initPageMetaFor(0xc000c5ab90, 0xc000a43508, 0x6, 0xc0000e6540, 0x1, 0xc000c5ab80)
	/build/hugo/src/hugo-0.62.0/hugolib/pages_map.go:95 +0x42b
github.com/gohugoio/hugo/hugolib.(*pagesMap).assemblePageMeta.func1(0xc000a43508, 0x6, 0x55e2ef7921c0, 0xc0000e6540, 0xc0000e6460)
	/build/hugo/src/hugo-0.62.0/hugolib/pages_map.go:199 +0x68
github.com/armon/go-radix.recursiveWalk(0xc000cc4090, 0xc000c89ea0, 0x55e2ef7921c0)
	/build/go/pkg/mod/github.com/armon/go-radix@v1.0.0/radix.go:519 +0xf2
github.com/armon/go-radix.recursiveWalk(0xc000c59f80, 0xc000c89ea0, 0x0)
	/build/go/pkg/mod/github.com/armon/go-radix@v1.0.0/radix.go:525 +0x80
github.com/armon/go-radix.recursiveWalk(0xc000c59e90, 0xc000c89ea0, 0x0)
	/build/go/pkg/mod/github.com/armon/go-radix@v1.0.0/radix.go:525 +0x80
github.com/armon/go-radix.(*Tree).Walk(...)
	/build/go/pkg/mod/github.com/armon/go-radix@v1.0.0/radix.go:447
github.com/gohugoio/hugo/hugolib.(*pagesMap).assemblePageMeta(0xc000c5ab90, 0xc000477c00, 0x0)
	/build/hugo/src/hugo-0.62.0/hugolib/pages_map.go:196 +0x6e
github.com/gohugoio/hugo/hugolib.(*HugoSites).assemble.func1(0x0, 0x0)
	/build/hugo/src/hugo-0.62.0/hugolib/hugo_sites_build.go:264 +0x101
golang.org/x/sync/errgroup.(*Group).Go.func1(0xc000c59e30, 0xc000c59e60)
	/build/go/pkg/mod/golang.org/x/sync@v0.0.0-20190423024810-112230192c58/errgroup/errgroup.go:57 +0x66
created by golang.org/x/sync/errgroup.(*Group).Go
	/build/go/pkg/mod/golang.org/x/sync@v0.0.0-20190423024810-112230192c58/errgroup/errgroup.go:54 +0x68
```
