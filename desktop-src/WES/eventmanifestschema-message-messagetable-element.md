---
title: Message (messageTable)-elemento
description: Contiene un riferimento a una stringa nella sezione localizzazione del manifesto. | Message (messageTable)-elemento
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- EventLog elemento messaggio
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321286"
---
# <a name="message-messagetable-element"></a>Message (messageTable)-elemento

Contiene un riferimento a una stringa nella sezione localizzazione del manifesto.

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

L'elemento **Message** è definito dall'elemento [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) .

## <a name="attributes"></a>Attributi



| Nome    | Tipo   | Descrizione                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Riferimento alla stringa localizzata nella tabella di stringhe.<br/>                                |
| mid     | string | Non usato.<br/>                                                                               |
| simbolo  | string | Nome simbolico che si desidera venga creato dal compilatore di messaggi per questa stringa di messaggio.<br/> |
| Valore   | string | Numero da utilizzare come identificatore del messaggio per questo messaggio.<br/>                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elementi padre**
</dt> <dt>

[**messageTable (EventsType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**messageTable (MetadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





