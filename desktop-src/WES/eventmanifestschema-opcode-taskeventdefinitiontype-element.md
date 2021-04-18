---
title: Elemento Opcode (TaskEventDefinitionType)
description: Contiene un codice operativo specifico dell'attività per un evento. Si presuppone che tutte le definizioni opcode siano specifiche dell'attività per l'attività che contiene le definizioni degli eventi.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- opcode element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302544"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>Elemento Opcode (TaskEventDefinitionType)

\[A partire dal compilatore di messaggi fornito con la versione di Windows 7 del Windows SDK, questo elemento non è più disponibile.\]

Contiene un codice operativo specifico dell'attività per un evento. Si presuppone che tutte le definizioni opcode siano specifiche dell'attività per l'attività che contiene le definizioni degli eventi.

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

L'elemento **OpCode** è definito dal tipo complesso [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                   | Tipo                                                                               | Descrizione                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**evento**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Evento pubblicato con un'attività.<br/> |



## <a name="attributes"></a>Attributi



| Nome | Tipo      | Descrizione                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nome del codice operativo specifico dell'attività.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**attività (DefinitionType)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





