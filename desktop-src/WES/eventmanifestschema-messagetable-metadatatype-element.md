---
title: Elemento messageTable (MetadataType)
description: Contiene riferimenti alle stringhe utilizzate nella sezione relativa ai metadati del manifesto di strumentazione eventi. Le stringhe vengono archiviate in un gruppo di elementi messaggio e ID abbinati.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
keywords:
- EventLog elemento messageTable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119187"
---
# <a name="messagetable-metadatatype-element"></a>Elemento messageTable (MetadataType)

Contiene riferimenti alle stringhe utilizzate nella sezione relativa ai metadati del manifesto di strumentazione eventi. Le stringhe vengono archiviate in un gruppo di elementi [**messaggio**](eventmanifestschema-message-messagetable-element.md) e ID abbinati.

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
                <xs:complexType>
                    <xs:attribute name="value"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="mid"
                        type="string"
                        use="optional"
                     />
                    <xs:attribute name="message"
                        type="string"
                        use="required"
                     />
                    <xs:attribute name="symbol"
                        type="string"
                        use="optional"
                     />
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L'elemento **messageTable** è definito dal tipo complesso [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                             | Tipo | Descrizione                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**message**](eventmanifestschema-message-messagetable-element.md) |      | Specifica un riferimento a una stringa nella sezione localizzazione del manifesto.<br/> |



## <a name="attributes"></a>Attributi



| Nome    | Tipo   | Descrizione                                                              |
|---------|--------|--------------------------------------------------------------------------|
| message | string | Riferimento alla stringa localizzata nella tabella di stringhe.<br/>      |
| mid     | string | Non usato.<br/>                                                     |
| simbolo  | string | Simbolo utilizzato per fare riferimento al messaggio.<br/>                     |
| Valore   | string | Numero da utilizzare come identificatore del messaggio per questo messaggio.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MetadataType**](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**metadati (instrumentationManifest)**](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





