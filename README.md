# Bulgarian Colemak
Colemak based on Bulgarian Phonetic

## Installation 

1. Add the content of *bg* to `/usr/share/X11/xkb/symbols/bg`.

```bash
cat bg >> /usr/share/X11/xkb/symbols/bg
```

2. Add the content of `evdev.xml` to `/usr/share/X11/xkb/rules/evdev.xml` in section `<variantList>` of the Bulgarian layout. The section should look like this at the end:

```xml
    <layout>
      <configItem>
        <name>bg</name>
        <shortDescription>bg</shortDescription>
        <description>Bulgarian</description>
        <languageList>
          <iso639Id>bul</iso639Id>
        </languageList>
      </configItem>
      <variantList>
        <variant>
          <configItem>
            <name>phonetic</name>
            <description>Bulgarian (traditional phonetic)</description>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>bas_phonetic</name>
            <description>Bulgarian (new phonetic)</description>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>bulmak</name>
            <description>Bulgarian (Colemak)</description>
          </configItem>
        </variant>
      </variantList>
    </layout>
```

3. Gnome's language layout will now have Bulgarian (Colemak) to chose. (Tested on Gnome only)
