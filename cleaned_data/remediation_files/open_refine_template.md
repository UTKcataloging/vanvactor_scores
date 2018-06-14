# OpenRefine Template for David Van Vactor Music Collection

---

## Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

## Row Template

```
<mods>
<identifier type="local">{{cells["identifier_adminDB"].value}}</identifier>
{{if(isBlank(cells['title_relatedItem'].value), if(isBlank(cells['identifier_catalog'].value), '', '<identifier type="catalog">' + cells['identifier_catalog'].value + '</identifier>'), '')}}
{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>') + if(isBlank(cells['title_alternative'].value), '', '<titleInfo type="alternative"><title>' + cells['title_alternative'].value + '</title></titleInfo>') + if(isBlank(cells['title_alternative_2'].value), '', '<titleInfo type="alternative"><title>' + cells['title_alternative_2'].value + '</title></titleInfo>') + if(isBlank(cells['title_supplied'].value), '', '<titleInfo supplied="yes"><title>' + cells['title_supplied'].value + '</title></titleInfo>'))}}
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['contents_partNames'].value), '', '<tableOfContents>' + cells['contents_partNames'].value + '</tableOfContents>')}}
{{if(isBlank(cells['instrumentation_all_note'].value), '', '<note type="instrumentation">' + cells['instrumentation_all_note'].value + '</note>')}}
{{'<originInfo>' + if(isBlank(cells['date_created_single'].value), '', '<dateCreated>' + cells['date_created_single'].value + '</dateCreated>') + if(isBlank(cells['date_created_single'].value), '', '<dateCreated encoding="edtf" keyDate="yes">' + cells['date_created_single'].value + '</dateCreated>') + if(isBlank(cells['date_created_range'].value), '', '<dateCreated>' + cells['date_created_range'].value + '</dateCreated>') + if(isBlank(cells['date_created_range_edtf1'].value), '', '<dateCreated encoding="edtf" point="start" keyDate="yes">' + cells['date_created_range_edtf1'].value + '</dateCreated>') + if(isBlank(cells['date_created_range_edtf2'].value), '', '<dateCreated encoding="edtf" point="end" keyDate="yes">' + cells['date_created_range_edtf2'].value + '</dateCreated>') + if(isBlank(cells['date_issued'].value), '', '<dateIssued>' + cells['date_issued'].value + '</dateIssued>') + if(isBlank(cells['date_issued'].value), '', '<dateIssued encoding="edtf" keyDate="yes">' + cells['date_issued'].value + '</dateIssued>') + if(isBlank(cells['date_approximate'].value), '', '<dateCreated qualifier="approximate">' + cells['date_approximate'].value + '</dateCreated>') + if(isBlank(cells['date_approximate'].value), '', '<dateCreated qualifier="approximate" encoding="edtf" keyDate="yes">' + cells['date_approximate'].value + '</dateCreated>') + if(isBlank(cells['date_approximate_range'].value), '', '<dateCreated qualifier="approximate">' + cells['date_approximate_range'].value + '</dateCreated>') + if(isBlank(cells['date_approximate_edtf1'].value), '', '<dateCreated qualifier="approximate" encoding="edtf" point="start" keyDate="yes">' + cells['date_approximate_edtf1'].value + '</dateCreated>') + if(isBlank(cells['date_approximate_edtf2'].value), '', '<dateCreated qualifier="approximate" encoding="edtf" point="end" keyDate="yes">' + cells['date_approximate_edtf2'].value + '</dateCreated>') + if(isBlank(cells['publisher'].value), '', '<publisher>' + cells['publisher'].value + '</publisher>') + if(isBlank(cells['publisher_location'].value), '', '<place><placeTerm valueURI="' + cells['location_URI'].value + '">' + cells['publisher_location'].value + '</placeTerm></place>') + '</originInfo>'}}


{{if(isBlank(cells['first_line'].value), '', '<note type="First line">' + cells['first_line'].value + '</note>')}}
{{if(isBlank(cells['name_composer'].value), '', '<name valueURI="http://id.loc.gov/authorities/names/n82001311"><namePart>Van Vactor, David, 1906-1994</namePart><role>
<roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cmp">Composer</roleTerm></role></name>')}}
{{if(isBlank(cells['name_composer_arranger'].value), '', '<name valueURI="http://id.loc.gov/authorities/names/n82001311"><namePart>' + cells['name_composer_arranger'].value + '</namePart><role>
<roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cmp">Composer</roleTerm><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/arr">Arranger</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist'].value), '', '<name><namePart>' + cells['name_lyricist'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_2'].value), '', '<name><namePart>' + cells['name_lyricist_2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_3'].value), '', '<name><namePart>' + cells['name_lyricist_3'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_4'].value), '', '<name><namePart>' + cells['name_lyricist_4'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_5'].value), '', '<name><namePart>' + cells['name_lyricist_5'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_6'].value), '', '<name><namePart>' + cells['name_lyricist_6'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_7'].value), '', '<name><namePart>' + cells['name_lyricist_7'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_arranger'].value), '', '<name><namePart>' + cells['name_arranger'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/arr">Arranger</roleTerm></role></name>')}}
{{if(isBlank(cells['name_compiler'].value), '', '<name><namePart>' + cells['name_compiler'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/com">Compiler</roleTerm></role></name>')}}
{{if(isBlank(cells['name_musiccopyist'].value), '', '<name><namePart>' + cells['name_musiccopyist'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/mcp">Music copyist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_dedicatee'].value), '', '<name><namePart>' + cells['name_dedicatee'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/dte">Dedicatee</roleTerm></role></name>')}}
{{if(isBlank(cells['name_dedicatee_2'].value), '', '<name><namePart>' + cells['name_dedicatee'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/dte">Dedicatee</roleTerm></role></name>')}}
{{if(isBlank(cells['name_editor'].value), '', '<name><namePart>' + cells['name_editor'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/edt">Editor</roleTerm></role></name>')}}

<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85088762"><topic>Music</topic></subject>

{{if(isBlank(cells['title_relatedItem'].value), '', '<relatedItem type="otherVersion"><titleInfo><title>' + cells['title_relatedItem'].value + '</title></titleInfo>' + if(isBlank(cells['identifier_catalog'].value), '', '<identifier type="catalog">' + cells['identifier_catalog'].value + '</identifier>') + '</relatedItem>'))}}
{{if(isBlank(cells['inscription'].value), '', '<note type="handwritten">' + cells['inscription'].value + '</note>') + if(isBlank(cells['inscription2'].value), '', '<note type="handwritten">' + cells['inscription2'].value + '</note>') + if(isBlank(cells['inscription3'].value), '', '<note type="handwritten">' + cells['inscription3'].value + '</note>') + if(isBlank(cells['inscription4'].value), '', '<note type="handwritten">' + cells['inscription4'].value + '</note>') + if(isBlank(cells['inscription5'].value), '', '<note type="handwritten">' + cells['inscription5'].value + '</note>') + if(isBlank(cells['inscription6'].value), '', '<note type="handwritten">' + cells['inscription6'].value + '</note>') + if(isBlank(cells['inscription7'].value), '', '<note type="handwritten">' + cells['inscription7'].value + '</note>') + if(isBlank(cells['inscription8'].value), '', '<note type="handwritten">' + cells['inscription8'].value + '</note>') + if(isBlank(cells['inscription9'].value), '', '<note type="handwritten">' + cells['inscription9'].value + '</note>') + if(isBlank(cells['inscription10'].value), '', '<note type="handwritten">' + cells['inscription10'].value + '</note>') + if(isBlank(cells['inscription11'].value), '', '<note type="handwritten">' + cells['inscription11'].value + '</note>') + if(isBlank(cells['inscription12'].value), '', '<note type="handwritten">' + cells['inscription12'].value + '</note>')}}



<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300026427">{{cells['form_aat'].value}}</form><internetMediaType>pdf</internetMediaType></physicalDescription>
<typeOfResource>{{cells['item_type'].value}}</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>{{cells['archival_collection'].value}}</title></titleInfo><identifier>{{cells['collection_identifier'].value}}</identifier></relatedItem>
<location><physicalLocation valueURI="{{cells['repository_URI'].value}}">{{cells['repository'].value}}</physicalLocation></location>
<recordInfo><recordContentSource valueURI="{{cells['recordsource_URI'].value}}">{{cells['record_source'].value}}</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>
```

## Row Separator

**LEAVE BLANK**

## Suffix

```
</modsCollection>
```