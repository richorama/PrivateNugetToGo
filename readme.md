# Private NuGet To Go

Get your own NuGet feed on Azure Websites with the click of a button.

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)

Once deployed, if you go the azure portal and set `username` and `password` settings, basic authorization will be enabled.

You can also set `requireApiKey` to `true`, and provide an API Key with the `apiKey` setting.

## Consuming the feed

1. In the Visual Studio menu, go to `Tools` -> `Options`
1. In the settings go to `NuGet Package Manager` -> `Package Sources`
1. Add a feed with the url `https://YOUR_WEBSITE_NAME.azurewebsites.net/nuget`

You will be prompted for the username and password when you access the feed.

## Publishing to the feed

```
$ nuget push MY_PROJECT.nupkg -Source https://YOUR_WEBSITE_NAME.azurewebsites.net
```

## Acknowledgements

* [Devbridge](https://www.devbridge.com) for the basic auth code.
* [Brady Gaster](http://www.bradygaster.com/) for the Azure Web Sites button

## License

MIT
