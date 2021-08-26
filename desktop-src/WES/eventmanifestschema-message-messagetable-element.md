---
title: Elemento message (messageTable)
description: Contiene un riferimento a una stringa nella sezione di localizzazione del manifesto. | Elemento message (messageTable)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- Elemento message EventLog
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79020fa18717a3a2338a8ac243bb95e0fa14de47f0e434fb52c475c956afa101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865671"
---
# <a name="message-messagetable-element"></a>Elemento message (messageTable)

Contiene un riferimento a una stringa nella sezione di localizzazione del manifesto.

``` syntax
<xs:element name="message">
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
```

**L'elemento** message è definito dall'elemento [**messageTable.**](eventmanifestschema-messagetable-instrumentationtype-element.md)

## <a name="attributes"></a>Attributi



| Nome    | Tipo   | Descrizione                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Riferimento alla stringa localizzata nella tabella di stringhe.<br/>                                |
| mid     | string | Non usato.<br/>                                                                               |
| simbolo  | string | Nome simbolico che si desidera che il compilatore di messaggi crei per questa stringa di messaggio.<br/> |
| Valore   | string | Numero da utilizzare come identificatore del messaggio.<br/>                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elementi padre**
</dt> <dt>

[**messageTable (EventsType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**messageTable (MetadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





