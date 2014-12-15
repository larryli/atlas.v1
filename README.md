Atlas API
=========

[![GoDoc](https://godoc.org/github.com/larryli/atlas.v1?status.png)](https://godoc.org/github.com/larryli/atlas.v1)

This is the documentation and guide for the Atlas API.
You can use it to create and update boxes, versions and providers.

	import "github.com/larryli/atlas.v1"

 	api := atlas.New("--replace-your-access-token--")
	box := api.Box("yourname", "boxname")
	if box.New() == nil {
		version := box.Version(0)
		version.Version = "0.0.1"
		if version.New() == nil {
			provider := version.Provider(atlas.ProviderVirtualbox)
			provider.OriginalUrl = "http://your.box.url"
			if provider.New() == nil {
				version.Release()
			}
		}
	}
