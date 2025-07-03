
Example of record of license vs dataset level license: 

```

@prefix odrl: <http://www.w3.org/ns/odrl/2/> .
@prefix cc:   <http://creativecommons.org/ns#> .
@prefix dct:  <http://purl.org/dc/terms/> .
@prefix ex:   <http://example.org/record/> .
@prefix ds:   <http://example.org/dataset/> .

# Dataset-level policy (CC BY-NC)
ds:inat-dataset a dct:Dataset ;
    dct:title "iNaturalist Aggregated Observations" ;
    odrl:hasPolicy [
        a odrl:Policy ;
        odrl:profile <http://www.w3.org/ns/odrl/2/> ;
        odrl:permission [
            odrl:action odrl:use ;
            odrl:constraint [
                odrl:leftOperand odrl:purpose ;
                odrl:operator odrl:eq ;
                odrl:rightOperand <http://example.org/purpose/nonCommercial>
            ]
        ] ;
        odrl:prohibition [
            odrl:action odrl:commercialUse ;
        ] ;
        dct:license <https://creativecommons.org/licenses/by-nc/4.0/> ;
    ] ;
    dct:hasPart ex:record1, ex:record2 .

# Record 1 - CC0
ex:record1 a dct:PhysicalResource ;
    dct:identifier "record1" ;
    dct:title "Observation of Danaus plexippus" ;
    odrl:hasPolicy [
        a odrl:Policy ;
        odrl:permission [
            odrl:action odrl:use ;
        ] ;
        dct:license <https://creativecommons.org/publicdomain/zero/1.0/>
    ] .

# Record 2 - CC BY
ex:record2 a dct:PhysicalResource ;
    dct:identifier "record2" ;
    dct:title "Observation of Pieris rapae" ;
    odrl:hasPolicy [
        a odrl:Policy ;
        odrl:permission [
            odrl:action odrl:use ;
            odrl:constraint [
                odrl:leftOperand odrl:attribution ;
                odrl:operator odrl:eq ;
                odrl:rightOperand "Jane Doe (iNaturalist contributor)"
            ]
        ] ;
        dct:license <https://creativecommons.org/licenses/by/4.0/>
    ] .

```

JSON-LD 
```


{
  "@context": {
    "odrl": "http://www.w3.org/ns/odrl/2/",
    "dct": "http://purl.org/dc/terms/",
    "cc": "http://creativecommons.org/ns#",
    "ex": "http://example.org/record/",
    "ds": "http://example.org/dataset/",
    "id": "@id",
    "type": "@type"
  },
  "id": "ds:inat-dataset",
  "type": "dct:Dataset",
  "dct:title": "iNaturalist Aggregated Observations",
  "odrl:hasPolicy": {
    "type": "odrl:Policy",
    "odrl:permission": {
      "odrl:action": "odrl:use",
      "odrl:constraint": {
        "odrl:leftOperand": "odrl:purpose",
        "odrl:operator": "odrl:eq",
        "odrl:rightOperand": "http://example.org/purpose/nonCommercial"
      }
    },
    "odrl:prohibition": {
      "odrl:action": "odrl:commercialUse"
    },
    "dct:license": "https://creativecommons.org/licenses/by-nc/4.0/"
  },
  "dct:hasPart": [
    {
      "id": "ex:record1",
      "type": "dct:PhysicalResource",
      "dct:title": "Observation of Danaus plexippus",
      "odrl:hasPolicy": {
        "type": "odrl:Policy",
        "odrl:permission": {
          "odrl:action": "odrl:use"
        },
        "dct:license": "https://creativecommons.org/publicdomain/zero/1.0/"
      }
    },
    {
      "id": "ex:record2",
      "type": "dct:PhysicalResource",
      "dct:title": "Observation of Pieris rapae",
      "odrl:hasPolicy": {
        "type": "odrl:Policy",
        "odrl:permission": {
          "odrl:action": "odrl:use",
          "odrl:constraint": {
            "odrl:leftOperand": "odrl:attribution",
            "odrl:operator": "odrl:eq",
            "odrl:rightOperand": "Jane Doe (iNaturalist contributor)"
          }
        },
        "dct:license": "https://creativecommons.org/licenses/by/4.0/"
      }
    }
  ]
}
```

```
