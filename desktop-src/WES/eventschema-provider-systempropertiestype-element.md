---
title: Elemento Provider (SystemPropertiesType)
description: Identifica il provider che ha registrato l'evento.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Elemento provider EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5327bc267272942df30044678a96244d957122c9fbf7878a805bfd48433e20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904526"
---
# <a name="provider-systempropertiestype-element"></a>Elemento Provider (SystemPropertiesType)

Identifica il provider che ha registrato l'evento.

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**L'elemento** Provider è definito dal [**tipo complesso SystemPropertiesType.**](eventschema-systempropertiestype-complextype.md)

## <a name="attributes"></a>Attributi



| Nome            | Tipo                                                | Descrizione                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| EventSourceName | string                                              | Nome dell'origine evento che ha pubblicato l'evento (se l'origine evento deriva dall'API [di registrazione eventi](/windows/desktop/EventLog/event-logging) legacy).<br/> |
| Guid            | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica in modo univoco il provider.<br/>                                                                   |
| Nome            | anyURI                                              | Nome del provider di eventi che ha registrato l'evento.<br/>                                                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

