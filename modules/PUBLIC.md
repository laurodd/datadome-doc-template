<!--- Readme Title : MY_NEW_MODULE_NAME -->
<!--- Readme Subtitle: DataDome MY_NEW_MODULE_NAME module detects and protects against bot activity -->

<!--- Generic description -->

Before the regular MY_NEW_MODULE_NAME process starts, the module makes a call to the DataDome API using a KeepAlive connection.

Depending on the API response, the module will either block the query or let MY_NEW_MODULE_NAME proceed with the regular process.

The module has been developed to protect the users' experience: if any errors were to occur during the process, or if the timeout is reached, the module will automatically disable its blocking process and allow those hits.


# Compatibility

The DataDome module supports the following versions

- Apache 2.4 / .NET 6.0 / ...
- Apache 2.2 / .NET 5.0 / ...

<!--- OS versions : alphabetical order if applicable -->

Every new release of the module is thoroughly tested on the following distributions:

- CentOS 1/2/3
- Debian 8/9/10
- Ubuntu 20/22

# Installation

1. Step 1

```shell
sudo blablabla
```

2. Step 2

tblablablbala

# Configuration

1. **Add the DataDome configuration below to the http block.**  
   By default, the configuration is located on `/usr/local/openresty/nginx/conf/nginx.conf`

- Make sure to replace the `datadome_server_side_key`


# Settings

[block:parameters]
{
  "data": {
    "h-0": "Setting",
    "h-1": "Description",
    "h-2": "Required",
    "h-3": "Default Value",
    "0-0": "datadome_server_side_key",
    "0-1": "Your DataDome server side key, found in your [dashboard](https://app.datadome.co/dashboard/management/integrations)",
    "0-2": "yes",
    "0-3": "-",
    "1-0": "datadome_endpoint",
    "1-1": "Host of the API Server  \n[Available endpoints](doc:api-server)",
    "1-2": "no",
    "1-3": "`api.datadome.co`",
    "2-0": "datadome_timeout",
    "2-1": "Timeout for regular API calls",
    "2-2": "no",
    "2-3": "`150` (in milliseconds)",
    "3-0": "datadome_url_pattern_inclusion",
    "3-1": "Regular expression to include URLs",
    "3-2": "no",
    "3-3": "-",
    "4-0": "datadome_url_pattern_exclusion",
    "4-1": "Regular expression to exclude URLs",
    "4-2": "no",
    "4-3": "List of excluded static assets below"
  },
  "cols": 4,
  "rows": 5,
  "align": [
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


```shell Excluded file extensions for static assets (default values)
"\\.(avi|flv|mka|mkv|mov|mp4|mpeg|mpg|mp3|flac|ogg|ogm|opus|wav|webm|webp|bmp|gif|ico|jpeg|jpg|png|svg|svgz|swf|eot|otf|ttf|woff|woff2|css|less|js|map|json)$"
```



# FAQ (debug, enrichied headers, proxy, timeouts...)
## Subitem