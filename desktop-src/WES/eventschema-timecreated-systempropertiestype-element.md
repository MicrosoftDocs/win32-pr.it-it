---
title: Elemento TimeCreated (SystemPropertiesType)
description: Timestamp che identifica il momento in cui l'evento è stato registrato.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- EventLog elemento TimeCreated
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964406"
---
# <a name="timecreated-systempropertiestype-element"></a>Elemento TimeCreated (SystemPropertiesType)

Timestamp che identifica il momento in cui l'evento è stato registrato.

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

L'elemento **TimeCreated** è definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Attributi



| Nome       | Tipo     | Descrizione                                              |
|------------|----------|----------------------------------------------------------|
| SystemTime | dateTime | Ora di sistema del momento in cui l'evento è stato registrato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





