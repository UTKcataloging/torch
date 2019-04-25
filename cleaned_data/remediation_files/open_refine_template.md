# Open Refine Template for Torchbearer


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="issn">{{cells['ISSN'].value}}</identifier>
<identifier type="filename">{{cells["identifier"].value}}</identifier>
<identifier type="pid">{{cells["PID"].value}}</identifier>
<titleInfo supplied="yes"><title>{{cells['title'].value}}</title></titleInfo>
<abstract>{{cells['abstract'].value}}</abstract>
<name authority="naf" valueURI="{{cells['subject1_URI'].value}}"><namePart>{{cells['subject1'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm></role></name>
<originInfo><dateIssued>{{cells['dateIssued'].value}}</dateIssued><dateIssued encoding="edtf" keyDate="yes">{{cells['dateIssued_edtf'].value}}</dateIssued><publisher>{{cells['publisher'].value}}</publisher>
{{if(isBlank(cells['publisher2'].value), '', '<publisher>' + cells['publisher2'].value + '</publisher>')}}
<place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm></place></originInfo>
<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300026657">periodicals</form></physicalDescription>
{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85141147"><topic>Universities and colleges--Periodicals</topic></subject>
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh89003052"><topic>College students--United States</topic></subject>
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85141093"><topic>Universities and colleges--Alumni and alumnae</topic></subject>
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85028338"><topic>College sports</topic></subject>
<subject authority="naf" valueURI="{{cells['subject1_URI'].value}}"><name><namePart>{{cells['subject1'].value}}</namePart></name></subject>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<typeOfResource>text</typeOfResource>
<classification authority="lcc">{{cells['classification'].value}}</classification>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Torchbearer</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource><languageOfCataloging><languageTerm type="text" authority="iso639-2b">English</languageTerm></languageOfCataloging><recordOrigin>
Created and edited in general conformance to MODS Guidelines (Version 3.5).
</recordOrigin></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```