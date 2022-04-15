![](https://github.com/MirageAIO/quicktask-documentation/blob/main/miragebanner.jpeg)
## Mirage Quicktask Documentation
This repository outlines the usage of the Mirage quicktask system, meaning that any monitor company etc, can use our quicktasks system easily.

## UPDATE 12/04/2022
As of 12/04/2022, remote quicktasks are now available to our users. To use this feature, users must be logged in to the [Mirage Dashboard](https://dashboard.miragebots.io/dashboard), before launching a quicktask.

## Format
The format of the quicktask url is as follows; `http://dashboard.miragebots.io/dashboard?quicktask=true&module={MODULE}&site={SITE}&items={PRODUCTS}`. We support multi product quicktasks, by comma seperating the `items` query, e.g. `...&items=product1,product2,product3`. For each different site we have a `module` and a `site` - more info below. Please note that we handle the modes that are ran for the user in-bot, so there is no need to worry about that.

## Mesh
Mesh quicktasks are done using the backend store identifier, and mesh quicktasks support PID's and SKU's - we would recommend using SKU's if possible due to checkout speed being lower when using them. An example of a mesh quicktask is `http://dashboard.miragebots.io/dashboard?quicktask=true&module=mesh&site=jdsportsuk&items=16071417.0194953243086,16071417.0194953243093,16071417.0194953243109,16071417.0194953243116`, as shown, this is using comma seperated size sku's - the bot will pick a random one for each task. For mesh quicktasks, the `module` will always be `mesh` and the `site` can be any store on any region, e.g. `footpatrolgb`, `sizefr`, `jdsportsfr`.

## Offspring / Office
Offspring / Office quicktasks both use the `module` as `office`, and can use the `site` as `office` or `offspring` depending on if you're running offspring or office, the `items` field uses the productid, we do not support size sku's for the office module

## SNS / YME / Naked
These sites all use their own site for the `module` field aswell as the `site` field; e.g. `http://dashboard.miragebots.io/dashboard?quicktask=true&module=sns&site=sns&items=46826:1317422,46826:1317423,46826:1317425` would be an sns quicktask, also another feature about this specific store is that we support size sku quicktasks (along with base pid), by doing BASEPID:SIZEPID. These can also be comma seperated.

## Slamjam
Slamjam also has implemtation for BASEPID:SIZEPID quicktasks (recommended), e.g. `http://dashboard.miragebots.io/dashboard?quicktask=true&module=slamjam&site=slamjam&items=J230350:2000216694107`, again the `site` and `module` are both `slamjam`, we also support base pid quicktasks, but please note it will make the bot have a slower checkout time.

## OFF---WHITE / AMBUSH DESIGN
These modules are both for the drops.... domains, the `module` for both of these is `farfetch` and the store for off---white is `owd` and the store for ambush is `amd`, an example quicktask link is `http://dashboard.miragebots.io/dashboard?quicktask=true&module=farfetch&site=owd&items=17606488`

## Footasylum
For footasylum, the `module` is `asylum` and the `site`is `footasylum`, we support size pids for quicktasks, an example of a quicktask link would be `http://dashboard.miragebots.io/dashboard?quicktask=true&module=asylum&site=footasylum&items=4051961101,4051961105`

## KithEU
For kith, the `module` and `site` would both be `kith`, and we use the end part of the product url in the `items` field. e.g. if the product is `https://eu.kith.com/products/nkda3940-010`, then the quicktask url would be `http://dashboard.miragebots.io/dashboard?quicktask=true&module=kith&site=kith&items=nkda3940-010`, we only support base pids

This is examples for all sites supported currently, updated 21/12/2021, if you have any questions regarding this, please feel free to dm either Vastid#0001, Austin.#1111 or WILL#9999
