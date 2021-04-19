---
title: Tipo complesso triggersType
description: Definisce il gruppo (triggerGroup) per tutti gli elementi trigger.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- Utilità di pianificazione di tipo complesso triggersType
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302676"
---
# <a name="triggerstype-complex-type"></a>Tipo complesso triggersType

Definisce il gruppo ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) per tutti gli elementi trigger. Il gruppo [**triggerGroup**](taskschedulerschema-triggergroup-group.md) contiene l'elenco dei trigger che possono essere usati in un'attività.

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





