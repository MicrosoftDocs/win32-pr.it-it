---
title: Elemento Security (SystemPropertiesType)
description: Identifica l'utente che ha registrato l'evento.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- EventLog dell'elemento di sicurezza
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20aef5465b8790bdba92c50181c0550ca5989c29d66fd53b9ec7ed0f760a2129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588287"
---
# <a name="security-systempropertiestype-element"></a>Elemento Security (SystemPropertiesType)

Identifica l'utente che ha registrato l'evento.

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**L'elemento** Security è definito dal [**tipo complesso SystemPropertiesType.**](eventschema-systempropertiestype-complextype.md)

## <a name="attributes"></a>Attributi



| Nome   | Tipo   | Descrizione                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | string | ID di sicurezza (SID) dell'utente in formato stringa.<br/> |



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

 

 





