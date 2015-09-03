# spatialsuite-geomatic-wms
Dette er et modul til Spatial Suite, der giver adgang til Geomatic WMS tjenester

Udviklingen af modulet er drevet af Spatial Suite kunder.  

###Installation

Udpak filen til  /config/modules/thirdparty/septima

Fjern endelsen "-master" fra den udpakkede folder
Tilføj modulet til din modules_xxx.xml

<module name="spatialsuite-geomatic-wms" dir="thirdparty/septima/spatialsuite-geomatic-wms" permissionlevel="public"/>

Indsæt følgende i din profils **themegroups** element:

```xml
<themegroup displayname="Adresser og grundejere" expanded="false" name="adresser" selectable="true" type="checkbutton"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='geomatic_klassifikation']" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='faktorer']" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='beskaeftigelse']" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='ejerforhold']" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='indkomst_og_formue']" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='uddannelse']" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='civilstand']" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='alder']" mustexist="false"/>



```
Indsæt dette i **themes** elementet i profilen:

```xml
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_klassifikation.xml" nodes="/themes/*" mustexist="false"/>
        <include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_faktorer.xml" nodes="/themes/*" mustexist="false"/>
        <include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_beskaeftigelse.xml" nodes="/themes/*" mustexist="false"/>
        <include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_ejerforhold.xml" nodes="/themes/*" mustexist="false"/>
        <include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_indkomst_formue.xml" nodes="/themes/*" mustexist="false"/>
        <include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_uddannelse.xml" nodes="/themes/*" mustexist="false"/>
        <include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_civilstand.xml" nodes="/themes/*" mustexist="false"/>
        <include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_alder.xml" nodes="/themes/*" mustexist="false"/>
```

Har du kun adgang til **klassifikation** og **faktorer**:

Indsæt dettet i **themegroups** elementet i profilen:

```xml
        <themegroup displayname="Adresser og grundejere" expanded="false" name="adresser" selectable="true" type="checkbutton"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='geomatic_klassifikation']" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/profile.xml" nodes="/profile/themegroups/themegroup[@name='faktorer']" mustexist="false"/>
```

Indsæt dette i **themes** elementet i profilen:

```xml
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_klassifikation.xml" nodes="/themes/*" mustexist="false"/>
<include src="[module:spatialsuite-geomatic-wms.dir]/profiles/includes/themes-geomatic_faktorer.xml" nodes="/themes/*" mustexist="false"/>
``

Indsæt dit burgernavn og password i CBinfo.xml

```xml
<param name="module.spatiasluite.geomatic.wms.username">USER</param>
<param name="module.spatiasluite.geomatic.wms.password">PASSWORD</param>
```


