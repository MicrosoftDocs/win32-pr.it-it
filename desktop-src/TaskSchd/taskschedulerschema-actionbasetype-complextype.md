---
title: Tipo complesso actionBaseType
description: Definisce l'attributo Id per tutti gli elementi di questo tipo.
ms.assetid: adc7117f-881f-4a32-8578-0530f2a0c179
keywords:
- Tipo complesso actionBaseType Utilità di pianificazione
topic_type:
- apiref
api_name:
- actionBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a7620696f21054f67c7e654b50c6ce146e1c596a039e9eb74fc2bc72a994114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857974"
---
# <a name="actionbasetype-complex-type"></a>Tipo complesso actionBaseType

Definisce l'attributo Id per tutti gli elementi di questo tipo.

``` syntax
<xs:complexType name="actionBaseType"
    abstract="true"
>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                                        |
|------|------|----------------------------------------------------|
| id   | ID   | ID dell'azione eseguita dall'attività.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





