<!--- Readme Title : MY_NEW_MODULE_NAME -->
<!--- Readme Subtitle: DataDome MY_NEW_MODULE_NAME module detects and protects against bot activity -->

<!--- Generic description -->

This Datadome module is to be used on TECHNO_NAME with SERVICE_NAME_AND_LINK / This module is developed in LANGUAGE and integrates smoothly with TECHNO_NAME.

Before the regular MY_NEW_MODULE_NAME process starts, the module makes a call to the the closest DataDome Regional Endpoint /using a KeepAlive connection.

Depending on the API response, the module will either block the query or let MY_NEW_MODULE_NAME proceed with the regular process.

The module has been developed to protect the users' experience: if any errors were to occur during the process, or if the timeout is reached, the module will automatically disable its blocking process and allow those requests.


# Compatibility

The DataDome module supports the following versions / runtimes

- Apache 2.4 / .NET 6.0 / ...
- Apache 2.2 / .NET 5.0 / ...

<!--- OS versions : alphabetical order if applicable -->

Every new release of the module is thoroughly tested on the following distributions:

- CentOS 1/2/3
- Debian 8/9/10
- Ubuntu 20/22

# Installation

1. Step 1.

```shell
sudo blablabla
```

2. Step 2.

tblablablbala

Y. Replace `DATADOME_LICENSE_KEY` with your own License Key, available in your [DataDome dashboard](https://app.datadome.co/). / Enter your own License Key, available in your [DataDome dashboard](https://app.datadome.co/).

Z. blabla

Congrats! You can now see your traffic in your [DataDome dashboard](https://app.datadome.co/dashboard/).


# Configuration

By default, the configuration is located in _/usr/local/openresty/nginx/conf/nginx.conf_.

Refer to the next Settings section for the full list of possible configuration settings.

## Settings

| Setting      | Description | Required | Default Value |
| :---        |    :----:   |    :----:     |      ---: |
| datadome_server_side_key      | Your DataDome server side key, found in your [dashboard](https://app.datadome.co/dashboard/management/integrations)  | Yes   | - |
| datadome_url_pattern_exclusion   | Regular expression to exclude URLs from the DataDome protection        | No    | List of excluded static assets below |
| datadome_url_pattern_inclusion   | Regular expression to include URLs in the DataDome protected traffic       | No    | - |
| datadome_timeout   | Timeout for regular API calls	| No    | 150ms /100 for edge modules |
| datadome_endpoint   | Host of the API Server: available [endpoints](https://docs.datadome.co/docs/api-server)| No  | api.datadome.co |


```shell Excluded file extensions for static assets (default values)
"\\.(avi|flv|mka|mkv|mov|mp4|mpeg|mpg|mp3|flac|ogg|ogm|opus|wav|webm|webp|bmp|gif|ico|jpeg|jpg|png|svg|svgz|swf|eot|otf|ttf|woff|woff2|css|less|js|map|json)$"
```



# FAQ (debug, enriched headers, proxy, timeouts...)

## How do I...?