---
title: Elemento messageTable (EventsType)
description: Contiene un riferimento a una stringa nella sezione localizzazione del manifesto. | Elemento messageTable (EventsType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
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
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321285"
---
# <a name="messagetable-eventstype-element"></a>Elemento messageTable (EventsType)

Contiene un riferimento a una stringa nella sezione localizzazione del manifesto.

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

L'elemento **messageTable** è definito dal tipo complesso [**EventsType**](eventmanifestschema-eventstype-complextype.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                             | Tipo | Descrizione                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**message**](eventmanifestschema-message-messagetable-element.md) |      | Specifica un riferimento a una stringa nella sezione localizzazione del manifesto.<br/> |



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

[**Elemento Events (InstrumentationType)**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





