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
{{if(isBlank(cells['identifier_catalog'].value), '', '<identifier type="catalog">' + cells['identifier_catalog'].value + '</identifier>')}}
<titleInfo><title>{{cells["title"].value}}</title></titleInfo>
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['date_text', 'season'].value), '', '<originInfo>') + if(isBlank(cells['date_text'].value), '', '<dateIssued>' + cells['date_text'].value + '</dateIssued>') + if(isBlank(cells['date'].value), '', '<dateIssued encoding="edtf">' + cells['date'].value + '</dateIssued>') + if(isBlank(cells['season'].value), '', '<dateOther encoding="edtf">' + cells['season'].value + '</dateOther>') + if(isBlank(cells['place'].value), '', '<place><placeTerm valueURI="http://id.loc.gov/authorities/names/n80003889">' + cells['place'].value + '</placeTerm></place>') +
if(isBlank(cells['department'].value), '', '<publisher>' + cells['department'].value + '</publisher>') + '</originInfo>')}}
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
{{if(isBlank(cells['creator'].value), '', '<name'+ if(isBlank(cells['creator_URI'].value), '', ' valueURI="' + cells['creator_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['creator'].value + '</namePart>' + if(isBlank(cells['role'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['role'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['creator2'].value), '', '<name'+ if(isBlank(cells['creator2_URI'].value), '', ' valueURI="' + cells['creator2_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['creator2'].value + '</namePart>' + if(isBlank(cells['creator2'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['role'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['creator3'].value), '', '<name'+ if(isBlank(cells['creator3_URI'].value), '', ' valueURI="' + cells['creator3_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['creator3'].value + '</namePart>' + if(isBlank(cells['creator3'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['role'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['creator4'].value), '', '<name'+ if(isBlank(cells['creator4_URI'].value), '', ' valueURI="' + cells['creator4_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['creator4'].value + '</namePart>' + if(isBlank(cells['creator4'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['role'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['creator5'].value), '', '<name'+ if(isBlank(cells['creator5_URI'].value), '', ' valueURI="' + cells['creator5_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['creator5'].value + '</namePart>' + if(isBlank(cells['creator5'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['role'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['creator6'].value), '', '<name'+ if(isBlank(cells['creator6_URI'].value), '', ' valueURI="' + cells['creator6_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['creator6'].value + '</namePart>' + if(isBlank(cells['creator6'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['role'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['director'].value), '', '<name'+ if(isBlank(cells['director_URI'].value), '', ' valueURI="' + cells['director_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['director'].value + '</namePart>' + if(isBlank(cells['director'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role2_URI'].value + '">' + cells['role2'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['director2'].value), '', '<name'+ if(isBlank(cells['director2_URI'].value), '', ' valueURI="' + cells['director2_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['director2'].value + '</namePart>' + if(isBlank(cells['director2'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['director2_role_URI'].value + '">' + cells['director2_role'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['director3'].value), '', '<name'+ if(isBlank(cells['director3_URI'].value), '', ' valueURI="' + cells['director3_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['director3'].value + '</namePart>' + if(isBlank(cells['director3'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role2_URI'].value + '">' + cells['role2'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['director4'].value), '', '<name'+ if(isBlank(cells['director4_URI'].value), '', ' valueURI="' + cells['director4_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['director4'].value + '</namePart>' + if(isBlank(cells['director4'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['role2_URI'].value + '">' + cells['role2'].value + '</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['production_company'].value), '', '<name><namePart>' + cells['production_company'].value + '</namePart>' + if(isBlank(cells['production_company'].value), '', '<role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/prn">Production company</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['subject_LCSH'].value), '', '<subject><topic' + if(isBlank(cells['subject_URI'].value), '>', ' valueURI="' + cells['subject_URI'].value + '">') + cells['subject_LCSH'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2_LCSH'].value), '', '<subject><topic' + if(isBlank(cells['subject2_URI'].value), '>', ' valueURI="' + cells['subject2_URI'].value + '">') + cells['subject2_LCSH'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3_LCSH'].value), '', '<subject><topic' + if(isBlank(cells['subject3_URI'].value), '>', ' valueURI="' + cells['subject3_URI'].value + '">') + cells['subject3_LCSH'].value + '</topic></subject>')}}
{{if(isBlank(cells['location'].value), '', '<subject><geographic>' + cells['location'].value + '</geographic></subject>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><internetMediaType>{{cells['format'].value}}</internetMediaType></physicalDescription>
<typeOfResource>{{cells['type'].value}}</typeOfResource>
<typeOfResource>{{cells['type2'].value}}</typeOfResource>
<language><languageTerm type="code" authority="iso639-2b">eng</languageTerm></language>
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