---
title: triggersType Tipo complesso
description: Definisce il gruppo (triggerGroup) per tutti gli elementi trigger.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- triggersType tipo complesso Utilità di pianificazione
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c2bd6fa4011841958ad08239640024f9878528aecb1307487c3354ac74e31db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610538"
---
# <a name="triggerstype-complex-type"></a>triggersType Tipo complesso

Definisce il gruppo ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) per tutti gli elementi trigger. Il [**gruppo triggerGroup**](taskschedulerschema-triggergroup-group.md) contiene l'elenco di trigger che è possibile usare in un'attività.

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





