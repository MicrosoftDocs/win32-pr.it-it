---
title: Tipo complesso actionBaseType
description: Definisce l'attributo ID per tutti gli elementi di questo tipo.
ms.assetid: adc7117f-881f-4a32-8578-0530f2a0c179
keywords:
- Utilità di pianificazione di tipo complesso actionBaseType
topic_type:
- apiref
api_name:
- actionBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8091456b2f09e6be5a332930d68960b2473acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121243"
---
# <a name="actionbasetype-complex-type"></a>Tipo complesso actionBaseType

Definisce l'attributo ID per tutti gli elementi di questo tipo.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi complessi dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





