Source: https://fairsfair.eu/fairsfair-data-object-assessment-metrics-request-comments

## Generic Digital Object: 

**F** 

1.  Object is assigned a globally unique and persitent ID (FsF-F1-01D and FsF-F1-02D ) (exception: internal Digital Objects that does not need global resolution) 
2.  Includes authoritative data. FsF-R1.3-01M provides guidelines for domain agnostic core metadata (this needs to be aligned with DiSSCo) 
3.  Metadata needs to include the PID of the object (FsF-F3-01M)
4.  Metadata can be retrieved programmatically (FsF-F4-01M)

**A** 

6.  Access and license information (FsF-A1-01M) 
7.  (Meta)data accessible through standard protocol (FsF-A1-03D and FsF-A1-02M)

**I** 

8.  Formal knowledge representation (FsF-I1-01M) 
9.  Semantic resources are identified (vocabularies, name spaces) FsF-I1-02M-1 and FsF-I1-02M-2
10.  Link between data and related entities (FsF-I3-01M) (like prior version, related entities) 

**R** 

11. Object descriptor/Type Data content descriptor (FsF-R1-01MD)
12. License information for data reuse (FsF-R1.1-01M) 
13. Provenance information about data creation and generation (FsF-R1.2-01M) 
14. Follows data standard of target research community (FsF-R1.3-01M) 
15. Associated bit sequence is available in a format recommended by the research community (FsF-R1.3-02D) 


Let's create an object based on the above list. 

1.  Object is assigned a globally unique and persitent ID

In case of a Digital Specimen, it will need a physical specimen identifier 

```
{
  "id": "20.5000.1025/64ae0cf0dacb7bd20ba5",
 "identifiers": [
        {
          "identifier": "https://hdl.handle.net/20.5000.1025/64ae0cf0dacb7bd20ba5",
          "identifierType": "Handle"
        }, 
          {
          "identifier": "MNHN-IM-2013-8488",
          "identifierType": "physicalSpecimenId"
        } 
        ]
 ```
    
 2. Object Includes authoritative data. This is based on FsF-R1.3-01M guideline for domain agnostic core metadata (who, what, when) 
         
 
 ```
 "typeName": "21.T11148/627a5b7620b1471aa945",
  "authoritative": {
    "publication_date": "2021-02-22T14:10:20.824Z", 
    "publisher": "DiSSCo",
    "summary": "Digital Specimen for Pygmaepterys pointieri Garrigues",
    "modified": "2021-02-22T14:10:20.824Z",
        "institution": [
      "MNHN",
      "https://ror.org/03wkt5x30"
    ]
  }
  ```
  3. Metadata needs to include the PID of the object (FsF-F3-01M)

```
        {
          "identifier": "https://hdl.handle.net/20.5000.1025/64ae0cf0dacb7bd20ba5",
          "identifierType": "Handle"
        }

```

4. Metadata can be retrieved programmatically (FsF-F4-01M)

Yes! 

5. Access and license information (FsF-A1-01M)

```
  "rightsList": [
        {
          "rights": "Creative Commons CC 4.0",
          "rightsUri": "http://creativecommons.org/licenses/by/4.0/legalcode"
        }
      ]
     
```

6.  (Meta)data accessible through standard protocol (FsF-A1-03D and FsF-A1-02M)

yes, https 

7. Formal knowledge representation (FsF-I1-01M) 

TBD 

8. Semantic resources are identified (vocabularies, name spaces) FsF-I1-02M-1 and FsF-I1-02M-2

```
 "typeName": "21.T11148/627a5b7620b1471aa945"
 
 ```
 9.  Link between data and related entities (FsF-I3-01M) (like prior version, related entities) 
 TBD
 
 10.  Object descriptor/Type Data content descriptor (FsF-R1-01MD)

```
 "typeName": "21.T11148/627a5b7620b1471aa945"
 ```
 
 
11. License information for data reuse (FsF-R1.1-01M) 

```
 "rightsList": [
        {
          "rights": "Creative Commons CC 4.0",
          "rightsUri": "http://creativecommons.org/licenses/by/4.0/legalcode"
        }
      ]
     
 ```
     
12.  Provenance information about data creation and generation (FsF-R1.2-01M) 

```
{
"publication_date": "2021-02-22T14:10:20.824Z", 
    "publisher": "DiSSCo",
    "modified": "2021-02-22T14:10:20.824Z"
    }
    
```
    
13. Follows data standard of target research community (FsF-R1.3-01M) 

Mention openDS

14. Associated bit sequence is available in a format recommended by the research community (FsF-R1.3-02D) 

```
format 
```


## Digital Specimen 

```
{
  "id": "20.5000.1025/64ae0cf0dacb7bd20ba5",
 "identifiers": [
        {
          "identifier": "https://hdl.handle.net/20.5000.1025/64ae0cf0dacb7bd20ba5",
          "identifierType": "Handle"
        } 
        ],
      "typeName": "21.T11148/627a5b7620b1471aa945",
  "authoritative": {
    "publication_date": "2021-02-22T14:10:20.824Z", 
    "publisher": "DiSSCo",
    "summary": "Digital Specimen for Pygmaepterys pointieri Garrigues",
    "modified": "2021-02-22T14:10:20.824Z",
    "midsLevel": 1,
    "physicalSpecimenId": "MNHN-IM-2013-8488",
    "institution": [
      "MNHN",
      "https://ror.org/03wkt5x30"
    ],
    "materialType": "Alcohol, 95%",
    "name": "Pygmaepterys pointieri Garrigues & Merle, 2014"
  },
  "rightsList": [
        {
          "rights": "Creative Commons CC 4.0",
          "rightsUri": "http://creativecommons.org/licenses/by/4.0/legalcode"
        }
      ]
     
}  
```

## Basic Image Object 
```
{
  "id": "20.5000.1025/64ae0cf0dacb7bd20ba5",
 "identifiers": [
        {
          "identifier": "https://hdl.handle.net/20.5000.1025/64ae0cf0dacb7bd20ba5",
          "identifierType": "Handle"
        } 
        ],
      "typeName": "ODStypeBIO-1901",
  "authoritative": {
    "publication_date": "2021-03-22T14:10:20.824Z", 
    "publisher": "DiSSCo",
    "summary": "Basic Image Object Pygmaepterys pointieri Garrigues",
    "modified": "2021-03-22T14:10:22.824Z",
    "images": [
        {
          "imageName": "hi-res",
          "source": "#/payloads",
          "mediaType": "image/jpeg", 
          "imageWidth": "400",
          "imageHeight": "280",
          "xResolution": "",
          "yResolution": "", 
          "colorSpace": "",
          "iccProfileName": "", 
          "creator": "",
          "created": "",
          "project": "",
          "license": "CC BY 4.0" 
        }
        ],
    "payloads": [
      {
        "name": "hi-res",
        "filename": "1427463506459UAeHPJw9jXoET1sF.jfif",
        "mediaType": "image/jpeg",
        "size": "15063"
      }
    ]
  } ,
"rightsList": [
        {
          "rights": "Creative Commons CC 4.0",
          "rightsUri": "http://creativecommons.org/licenses/by/4.0/legalcode"
        }
      ]
}
```
