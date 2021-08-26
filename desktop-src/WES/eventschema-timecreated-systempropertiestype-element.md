---
title: Elemento TimeCreated (SystemPropertiesType)
description: Timestamp che identifica quando è stato registrato l'evento.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- Elemento TimeCreated EventLog
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5026bed56e3e065a403c0e6076daa0ec478223c4d742db0a35109a41cc98d5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005301"
---
# <a name="timecreated-systempropertiestype-element"></a>Elemento TimeCreated (SystemPropertiesType)

Timestamp che identifica quando è stato registrato l'evento.

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

**L'elemento TimeCreated** è definito dal [**tipo complesso SystemPropertiesType.**](eventschema-systempropertiestype-complextype.md)

## <a name="attributes"></a>Attributi



| Nome       | Tipo     | Descrizione                                              |
|------------|----------|----------------------------------------------------------|
| SystemTime | dateTime | Ora di sistema in cui è stato registrato l'evento.<br/> |



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

 

 





