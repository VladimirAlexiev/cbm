# LOD CBMAA Objects_formatted.csv

## Add Column

## Add Node/Literal
#### Literal Node: `http://vocab.getty.edu/aat/300264237`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300266036`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300026687`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300404621`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300179869`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`

#### Literal Node: `http://vocab.getty.edu/aat/300404670`
Literal Type: ``
<br/>Language: ``
<br/>isUri: `true`


## PyTransforms
#### _ObjectURI_
From column: _ObjectID_
``` python
return "object/" + getValue("ObjectID")
```

#### _MediumURI_
From column: _Medium_
``` python
if getValue("Medium"):
    return getValue("ObjectURI")+"/medium"
```

#### _DimensionURI_
From column: _Dimensions_
``` python
if getValue("Dimensions"):
    return getValue("ObjectURI")+"/dimensions"
```

#### _ClassificationURI_
From column: _Classification_
``` python
if getValue("Classification"):
    return "thesauri/classification/"+getValue("Classification").replace(" ","-")
else:
    return ""
```

#### _ProductionURI_
From column: _ObjectURI_
``` python
return getValue("ObjectURI")+"/production"
```

#### _ProductionDateURI_
From column: _ProductionURI_
``` python
return getValue("ObjectURI")+"/production/date"
```

#### _DateBeginValid_
From column: _DateBegin_
``` python
if getValue("DateBegin") == '0':
    return ""
else:
    return getValue("DateBegin")
```

#### _DateEndValid_
From column: _DateEnd_
``` python
if getValue("DateEnd") == '0':
    return ""
else:
    return getValue("DateEnd")
```

#### _MarkingsURI_
From column: _Markings_
``` python
if getValue("Markings") != "":
    return getValue("ObjectURI") + "/markings"
```

#### _ProvenanceURI_
From column: _Provenance_
``` python
if getValue("Provenance"):
    return getValue("ObjectURI") + "/provenance"
```

#### _InscribedURI_
From column: _Inscribed_
``` python
if getValue("Inscribed") != "":
    return getValue("ObjectURI") + "/inscribed"
```

#### _SignedURI_
From column: _Signed_
``` python
if getValue("Signed") != "":
    return getValue("ObjectURI") + "/signed"
```

#### _BibliographyURI_
From column: _Bibliography_
``` python
if getValue("Bibliography"):
    return getValue("ObjectURI") + "/bibliography"
```

#### _CreditLineURI_
From column: _CreditLine_
``` python
if getValue("CreditLine"):
    return getValue("ObjectURI")+"/credit_line"
```

#### _ObjectLabel_
From column: _ObjectID_
``` python
return getValue("ObjectID")
```

#### _ObjectID_URI_
From column: _ObjectLabel_
``` python
return "object/id/" + getValue("ObjectID")
```

#### _TypeAssignmentURI_
From column: _ClassificationURI_
``` python
return getValue("ObjectURI") + "/type_assigned"
```

#### _ExhibitionEventURI_
From column: _Exhibitions_
``` python
return getValue("ObjectURI") + "/exhibition_event"
```

#### _ExhibitionEventAppellationURI_
From column: _ExhibitionEventURI_
``` python
return getValue("ObjectURI") + "/exhibition_event/appellation"
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _Bibliography_ | `crm:P3_has_note` | `crm:E33_Linguistic_Object2`|
| _BibliographyURI_ | `uri` | `crm:E33_Linguistic_Object2`|
| _Classification_ | `rdfs:label` | `crm:E55_Type1`|
| _ClassificationURI_ | `uri` | `crm:E55_Type1`|
| _CreditLine_ | `rdf:value` | `crm:E33_Linguistic_Object5`|
| _CreditLineURI_ | `uri` | `crm:E33_Linguistic_Object5`|
| _DateBeginValid_ | `crm:P82a_begin_of_the_begin` | `crm:E52_Time-Span1`|
| _DateEndValid_ | `crm:P82b_end_of_the_end` | `crm:E52_Time-Span1`|
| _DimensionURI_ | `uri` | `crm:E33_Linguistic_Object4`|
| _Dimensions_ | `rdf:value` | `crm:E33_Linguistic_Object4`|
| _ExhibitionEventAppellationURI_ | `uri` | `crm:E41_Appellation1`|
| _ExhibitionEventURI_ | `uri` | `crm:E5_Event1`|
| _Exhibitions_ | `rdf:value` | `crm:E41_Appellation1`|
| _Inscribed_ | `crm:P3_has_note` | `crm:E34_Inscription1`|
| _InscribedURI_ | `uri` | `crm:E34_Inscription1`|
| _Markings_ | `crm:P3_has_note` | `crm:E37_Mark1`|
| _MarkingsURI_ | `uri` | `crm:E37_Mark1`|
| _Medium_ | `rdf:value` | `crm:E33_Linguistic_Object3`|
| _MediumURI_ | `uri` | `crm:E33_Linguistic_Object3`|
| _ObjectID_ | `rdf:value` | `crm:E42_Identifier1`|
| _ObjectID_URI_ | `uri` | `crm:E42_Identifier1`|
| _ObjectLabel_ | `rdfs:label` | `crm:E42_Identifier1`|
| _ObjectURI_ | `uri` | `crm:E22_Man-Made_Object1`|
| _ProductionDateURI_ | `uri` | `crm:E52_Time-Span1`|
| _ProductionURI_ | `uri` | `crm:E12_Production1`|
| _Provenance_ | `crm:P3_has_note` | `crm:E33_Linguistic_Object1`|
| _ProvenanceURI_ | `uri` | `crm:E33_Linguistic_Object1`|
| _Signed_ | `crm:P3_has_note` | `crm:E37_Mark3`|
| _SignedURI_ | `uri` | `crm:E37_Mark3`|
| _TypeAssignmentURI_ | `uri` | `crm:E17_Type_Assignment1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `crm:E12_Production1` | `crm:P4_has_time-span` | `crm:E52_Time-Span1`|
| `crm:E17_Type_Assignment1` | `crm:P21_had_general_purpose` | `xsd:http://vocab.getty.edu/aat/300179869`|
| `crm:E17_Type_Assignment1` | `crm:P42_assigned` | `crm:E55_Type1`|
| `crm:E22_Man-Made_Object1` | `crm:P108i_was_produced_by` | `crm:E12_Production1`|
| `crm:E22_Man-Made_Object1` | `crm:P129i_is_subject_of` | `crm:E33_Linguistic_Object1`|
| `crm:E22_Man-Made_Object1` | `crm:P129i_is_subject_of` | `crm:E33_Linguistic_Object2`|
| `crm:E22_Man-Made_Object1` | `crm:P12i_was_present_at` | `crm:E5_Event1`|
| `crm:E22_Man-Made_Object1` | `crm:P1_is_identified_by` | `crm:E42_Identifier1`|
| `crm:E22_Man-Made_Object1` | `crm:P41i_was_classified_by` | `crm:E17_Type_Assignment1`|
| `crm:E22_Man-Made_Object1` | `crm:P65_shows_visual_item` | `crm:E34_Inscription1`|
| `crm:E22_Man-Made_Object1` | `crm:P65_shows_visual_item` | `crm:E37_Mark1`|
| `crm:E22_Man-Made_Object1` | `crm:P65_shows_visual_item` | `crm:E37_Mark3`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object3`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object4`|
| `crm:E22_Man-Made_Object1` | `crm:P67i_is_referred_to_by` | `crm:E33_Linguistic_Object5`|
| `crm:E22_Man-Made_Object1` | `crm:P2_has_type` | `crm:E55_Type1`|
| `crm:E33_Linguistic_Object3` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300264237`|
| `crm:E33_Linguistic_Object4` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300266036`|
| `crm:E33_Linguistic_Object5` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300026687`|
| `crm:E41_Appellation1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300404670`|
| `crm:E42_Identifier1` | `crm:P2_has_type` | `xsd:http://vocab.getty.edu/aat/300404621`|
| `crm:E5_Event1` | `crm:P1_is_identified_by` | `crm:E41_Appellation1`|
