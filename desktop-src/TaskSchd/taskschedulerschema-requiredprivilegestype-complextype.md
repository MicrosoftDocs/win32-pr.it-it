---
title: Tipo complesso requiredPrivilegesType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento RequiredPrivileges (requiredPrivilegesType).
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- Tipo complesso requiredPrivilegesType Utilità di pianificazione
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d79b75a4d4bb44aded7367fd4acfd758887815bba6fc6fcfd965f9123ac58c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658791"
---
# <a name="requiredprivilegestype-complex-type"></a>Tipo complesso requiredPrivilegesType

Definisce gli elementi figlio e le informazioni di sequenziazione per [**l'elemento RequiredPrivileges (requiredPrivilegesType).**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md)

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Tipo                                                                  | Descrizione                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [**Privilegio**](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [**privilegeType**](taskschedulerschema-privilegetype-simpletype.md) | Specifica i privilegi necessari per l'attività. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





