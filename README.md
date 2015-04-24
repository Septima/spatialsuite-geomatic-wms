# spatialsuite-geomatic-wms
Dette er et modul til Spatial Suite, der giver adgang til Geomatic WMS tjenester

Udviklingen af modulet er drevet af Spatial Suite kunder.  

###Installation

Udpak filen til  /config/modules/thirdparty/septima

Tilføj modulet til din modules_xxx.xml

<module name="spatialsuite-geomatic-wms" dir="thirdparty/septima/spatialsuite-geomatic-wms" permissionlevel="public"/>

Indsæt følgende i din profils **themegroups** element:

```xml

<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/*" mustexist="false"/>


```
Indsæt dette i **themes** elementet i profilen:

```xml

<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themes/*" mustexist="false"/>

```

Indsæt dit burgernavn og password i CBinfo.xml

```xml
<param name="module.spatiasluite.geomatic.wms.username">USER</param>
<param name="module.spatiasluite.geomatic.wms.password">PASSWORD</param>
```


