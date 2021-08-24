---
title: Elemento opcode (TaskEventDefinitionType)
description: Contiene un codice operativo specifico dell'attività per un evento. Si presuppone che tutte le definizioni del codice operativo siano specifiche dell'attività per l'attività che contiene le definizioni degli eventi.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- Elemento opcode EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f3923e0a42375ac7d926d418943af81cc0264e111e6bdc4be56919780dfacf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652151"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>Elemento opcode (TaskEventDefinitionType)

\[A partire dal compilatore di messaggi fornito con la versione Windows 7 di Windows SDK, questo elemento non è più disponibile.\]

Contiene un codice operativo specifico dell'attività per un evento. Si presuppone che tutte le definizioni del codice operativo siano specifiche dell'attività per l'attività che contiene le definizioni degli eventi.

``` syntax
<xs:element name="opcode">
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
```

**L'elemento opcode** è definito dal tipo complesso [**TaskEventDefinitionType.**](eventmanifestschema-taskeventdefinitiontype-complextype.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                   | Tipo                                                                               | Descrizione                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Evento**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Evento pubblicato con un'attività.<br/> |



## <a name="attributes"></a>Attributi



| Nome | Tipo      | Descrizione                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nome del codice operativo specifico dell'attività.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**task (DefinitionType)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





