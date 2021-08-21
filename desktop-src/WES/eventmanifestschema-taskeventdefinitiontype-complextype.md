---
title: Tipo complesso TaskEventDefinitionType
description: Definisce un evento specifico dell'attività che il provider può registrare. | Tipo complesso TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- EventLog di tipo complesso TaskEventDefinitionType
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44a4fc7ca8784b3472fea3b0d4f4e657ce615fae05a8cc7372aa3cca0fedb431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055839"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Tipo complesso TaskEventDefinitionType

\[A partire dal compilatore di messaggi fornito con la versione Windows 7 di Windows SDK, il tipo complesso TaskEventDefinitionType non è più disponibile. Usare invece opcode specifici dell'attività per fornire la stessa funzionalità.\]

Definisce un evento specifico dell'attività che il provider può registrare.

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="event"
                        type="EventDefinitionType"
                        maxOccurs="unbounded"
                     />
                </xs:sequence>
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
            </xs:complexType>
        </xs:element>
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                      | Tipo                                                                               | Descrizione                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Evento specifico dell'attività pubblicato con un'attività.<br/> |
| [**Opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Codice operativo specifico dell'attività per un evento. <br/>   |



## <a name="attributes"></a>Attributi



| Nome | Tipo      | Descrizione                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nome del codice operativo specifico dell'attività.<br/> |
| name | anyURI    | Nome dell'attività.<br/>                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





