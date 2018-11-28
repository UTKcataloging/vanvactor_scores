# OpenRefine Template for David Van Vactor Music Collection

---

## Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

## Row Template

```
remember to add PID once all are ingested.
<identifier type="pid">{{cells['PID'].value}}</identifier>

<mods>
<identifier type="local">{{cells["identifier_adminDB"].value}}</identifier>
{{if(isBlank(cells['title_relatedItem'].value), if(isBlank(cells['identifier_catalog'].value), '', '<identifier type="catalog">' + cells['identifier_catalog'].value + '</identifier>'), '')}}
{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>') + if(isBlank(cells['title_alternative'].value), '', '<titleInfo type="alternative"><title>' + cells['title_alternative'].value + '</title></titleInfo>') + if(isBlank(cells['title_alternative_2'].value), '', '<titleInfo type="alternative"><title>' + cells['title_alternative_2'].value + '</title></titleInfo>') + if(isBlank(cells['title_supplied'].value), '', '<titleInfo supplied="yes"><title>' + cells['title_supplied'].value + '</title></titleInfo>'))}}
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['contents_partNames'].value), '', '<tableOfContents>' + cells['contents_partNames'].value + '</tableOfContents>')}}
{{if(isBlank(cells['instrumentation_all_note'].value), '', '<note type="instrumentation">' + cells['instrumentation_all_note'].value + '</note>')}}

{{if(isBlank(cells['instrumentation'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_URI'].value + '">' + cells['instrumentation'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_2'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_2_URI'].value + '">' + cells['instrumentation_2'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_3'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_3_URI'].value + '">' + cells['instrumentation_3'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_4'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_4_URI'].value + '">' + cells['instrumentation_4'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_5'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_5_URI'].value + '">' + cells['instrumentation_5'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_6'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_6_URI'].value + '">' + cells['instrumentation_6'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_7'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_7_URI'].value + '">' + cells['instrumentation_7'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_8'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_8_URI'].value + '">' + cells['instrumentation_8'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_9'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_9_URI'].value + '">' + cells['instrumentation_9'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_10'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_10_URI'].value + '">' + cells['instrumentation_10'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_11'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_11_URI'].value + '">' + cells['instrumentation_11'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_12'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_12_URI'].value + '">' + cells['instrumentation_12'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_13'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_13_URI'].value + '">' + cells['instrumentation_13'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_14'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_14_URI'].value + '">' + cells['instrumentation_14'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_15'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_15_URI'].value + '">' + cells['instrumentation_15'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_16'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_16_URI'].value + '">' + cells['instrumentation_16'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_17'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_17_URI'].value + '">' + cells['instrumentation_17'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_18'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_18_URI'].value + '">' + cells['instrumentation_18'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_19'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_19_URI'].value + '">' + cells['instrumentation_19'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_20'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_20_URI'].value + '">' + cells['instrumentation_20'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_21'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_21_URI'].value + '">' + cells['instrumentation_21'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_22'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_22_URI'].value + '">' + cells['instrumentation_22'].value + '</genre>')}}
{{if(isBlank(cells['instrumentation_23'].value), '', '<genre authority="lcmpt" valueURI="' + cells['instrumentation_23_URI'].value + '">' + cells['instrumentation_23'].value + '</genre>')}}

{{'<originInfo>' + if(isBlank(cells['date_created'].value), '', '<dateCreated>' + cells['date_created'].value + '</dateCreated>') + if(isBlank(cells['date_created'].value), '', '<dateCreated encoding="edtf" keyDate="yes">' + cells['date_created'].value + '</dateCreated>') + if(isBlank(cells['date_created_range'].value), '', '<dateCreated>' + cells['date_created_range'].value + '</dateCreated>') + if(isBlank(cells['date_created_range1'].value), '', '<dateCreated encoding="edtf" point="start" keyDate="yes">' + cells['date_created_range1'].value + '</dateCreated>') + if(isBlank(cells['date_created_range2'].value), '', '<dateCreated encoding="edtf" point="end">' + cells['date_created_range2'].value + '</dateCreated>') + if(isBlank(cells['date_issued'].value), '', '<dateIssued>' + cells['date_issued'].value + '</dateIssued>') + if(isBlank(cells['date_issued'].value), '', '<dateIssued encoding="edtf" keyDate="yes">' + cells['date_issued'].value + '</dateIssued>') + if(isBlank(cells['date_approximate'].value), '', '<dateCreated qualifier="approximate">' + cells['date_approximate'].value + '</dateCreated>') + if(isBlank(cells['date_approximate'].value), '', '<dateCreated qualifier="approximate" encoding="edtf" keyDate="yes">' + cells['date_approximate'].value + '</dateCreated>') + if(isBlank(cells['date_approximate_range'].value), '', '<dateCreated qualifier="approximate">' + cells['date_approximate_range'].value + '</dateCreated>') + if(isBlank(cells['date_approximate_range1'].value), '', '<dateCreated qualifier="approximate" encoding="edtf" point="start" keyDate="yes">' + cells['date_approximate_range1'].value + '</dateCreated>') + if(isBlank(cells['date_approximate_range2'].value), '', '<dateCreated qualifier="approximate" encoding="edtf" point="end">' + cells['date_approximate_range2'].value + '</dateCreated>') + if(isBlank(cells['publisher'].value), '', '<publisher>' + cells['publisher'].value + '</publisher>') + if(isBlank(cells['publisher_location'].value), '', '<place><placeTerm valueURI="' + cells['location_URI'].value + '">' + cells['publisher_location'].value + '</placeTerm></place>') + '</originInfo>'}}
<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300026427">{{cells['form_aat'].value}}</form><extent>{{cells['extent'].value}}</extent><internetMediaType>pdf</internetMediaType></physicalDescription>
{{if(isBlank(cells['first_line'].value), '', '<note type="First line">' + cells['first_line'].value + '</note>')}}
{{if(isBlank(cells['name_composer'].value), '', '<name valueURI="http://id.loc.gov/authorities/names/n82001311"><namePart>Van Vactor, David, 1906-1994</namePart><role>
<roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cmp">Composer</roleTerm></role></name>')}}
{{if(isBlank(cells['name_composer_arranger'].value), '', '<name valueURI="http://id.loc.gov/authorities/names/n82001311"><namePart>' + cells['name_composer_arranger'].value + '</namePart><role>
<roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cmp">Composer</roleTerm><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/arr">Arranger</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist'].value), '', '<name' + if(isBlank(cells['name_lyricist_URI'].value), '', ' authority="naf" valueURI="' + cells['name_lyricist_URI'].value + '"') + '><namePart>' + cells['name_lyricist'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_2'].value), '', '<name' + if(isBlank(cells['name_lyricist_2_URI'].value), '', ' authority="naf" valueURI="' + cells['name_lyricist_2_URI'].value + '"') + '><namePart>' + cells['name_lyricist_2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_3'].value), '', '<name' + if(isBlank(cells['name_lyricist_3_URI'].value), '', ' authority="naf" valueURI="' + cells['name_lyricist_3_URI'].value + '"') + '><namePart>' + cells['name_lyricist_3'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_4'].value), '', '<name' + if(isBlank(cells['name_lyricist_4_URI'].value), '', ' authority="naf" valueURI="' + cells['name_lyricist_4_URI'].value + '"') + '><namePart>' + cells['name_lyricist_4'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_5'].value), '', '<name' + if(isBlank(cells['name_lyricist_5_URI'].value), '', ' authority="naf" valueURI="' + cells['name_lyricist_5_URI'].value + '"') + '><namePart>' + cells['name_lyricist_5'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_6'].value), '', '<name' + if(isBlank(cells['name_lyricist_6_URI'].value), '', ' authority="naf" valueURI="' + cells['name_lyricist_6_URI'].value + '"') + '><namePart>' + cells['name_lyricist_6'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_lyricist_7'].value), '', '<name' + if(isBlank(cells['name_lyricist_7_URI'].value), '', ' authority="naf" valueURI="' + cells['name_lyricist_7_URI'].value + '"') + '><namePart>' + cells['name_lyricist_7'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/lyr">Lyricist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_compiler'].value), '', '<name' + if(isBlank(cells['name_compiler_URI'].value), '', ' authority="naf" valueURI="' + cells['name_compiler_URI'].value + '"') + '><namePart>' + cells['name_compiler'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/com">Compiler</roleTerm></role></name>')}}
{{if(isBlank(cells['name_musiccopyist'].value), '', '<name><namePart>' + cells['name_musiccopyist'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/mcp">Music copyist</roleTerm></role></name>')}}
{{if(isBlank(cells['name_dedicatee'].value), '', '<name' + if(isBlank(cells['name_dedicatee_URI'].value), '', ' authority="naf" valueURI="' + cells['name_dedicatee_URI'].value + '"') + '><namePart>' + cells['name_dedicatee'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/dte">Dedicatee</roleTerm></role></name>')}}
{{if(isBlank(cells['name_dedicatee_2'].value), '', '<name' + if(isBlank(cells['name_dedicatee_2_URI'].value), '', ' authority="naf" valueURI="' + cells['name_dedicatee_2_URI'].value + '"') + '><namePart>' + cells['name_dedicatee'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/dte">Dedicatee</roleTerm></role></name>')}}
{{if(isBlank(cells['name_editor'].value), '', '<name' + if(isBlank(cells['name_editor_URI'].value), '', ' authority="naf" valueURI="' + cells['name_editor_URI'].value + '"') + '><namePart>' + cells['name_editor'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/edt">Editor</roleTerm></role></name>')}}
{{if(isBlank(cells['name_associated'].value), '', '<name' + if(isBlank(cells['name_associated_URI'].value), '', ' authority="naf" valueURI="' + cells['name_associated_URI'].value + '"') + '><namePart>' + cells['name_associated'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/asn">Associated name</roleTerm></role></name>')}}

{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_2_URI'].value + '"><topic>' + cells['subject_topic_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_3_URI'].value + '"><topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geographic'].value), '', '<subject authority="naf" valueURI="' + cells['subject_geographic_URI'].value + '"><geographic>' + cells['subject_geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_name'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_URI'].value + '"><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name_2'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_2_URI'].value + '"><name><namePart>' + cells['subject_name_2'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['genre'].value), '', '<genre authority="lcgft" valueURI="' + cells['genre_URI'].value + '">' + cells['genre'].value + '</genre>')}}
{{if(isBlank(cells['genre_2'].value), '', '<genre authority="lcgft" valueURI="' + cells['genre_2_URI'].value + '">' + cells['genre_2'].value + '</genre>')}}
{{if(isBlank(cells['genre_3'].value), '', '<genre authority="lcgft" valueURI="' + cells['genre_3_URI'].value + '">' + cells['genre_3'].value + '</genre>')}}
{{if(isBlank(cells['genre_4'].value), '', '<genre authority="lcgft" valueURI="' + cells['genre_4_URI'].value + '">' + cells['genre_4'].value + '</genre>')}}

{{if(isBlank(cells['title_relatedItem'].value), '', '<relatedItem type="otherVersion"><titleInfo><title>' + cells['title_relatedItem'].value + '</title></titleInfo>' + if(isBlank(cells['identifier_catalog'].value), '', '<identifier type="catalog">' + cells['identifier_catalog'].value + '</identifier>') + '</relatedItem>'))}}
{{if(isBlank(cells['inscription'].value), '', '<note type="handwritten">' + cells['inscription'].value + '</note>') + if(isBlank(cells['inscription2'].value), '', '<note type="handwritten">' + cells['inscription2'].value + '</note>') + if(isBlank(cells['inscription3'].value), '', '<note type="handwritten">' + cells['inscription3'].value + '</note>') + if(isBlank(cells['inscription4'].value), '', '<note type="handwritten">' + cells['inscription4'].value + '</note>') + if(isBlank(cells['inscription5'].value), '', '<note type="handwritten">' + cells['inscription5'].value + '</note>') + if(isBlank(cells['inscription6'].value), '', '<note type="handwritten">' + cells['inscription6'].value + '</note>') + if(isBlank(cells['inscription7'].value), '', '<note type="handwritten">' + cells['inscription7'].value + '</note>') + if(isBlank(cells['inscription8'].value), '', '<note type="handwritten">' + cells['inscription8'].value + '</note>') + if(isBlank(cells['inscription9'].value), '', '<note type="handwritten">' + cells['inscription9'].value + '</note>') + if(isBlank(cells['inscription10'].value), '', '<note type="handwritten">' + cells['inscription10'].value + '</note>') + if(isBlank(cells['inscription11'].value), '', '<note type="handwritten">' + cells['inscription11'].value + '</note>') + if(isBlank(cells['inscription12'].value), '', '<note type="handwritten">' + cells['inscription12'].value + '</note>')}}

<typeOfResource>{{cells['item_type'].value}}</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>{{cells['archival_collection'].value}}</title></titleInfo><identifier>{{cells['collection_identifier'].value}}</identifier><location><url>{{cells['ARK'].value}}</url></location></relatedItem>
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