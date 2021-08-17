---
title: Tipo semplice priorityType
description: Definisce i valori minimo e massimo per l'elemento Priority (settingsType).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- tipo semplice priorityType Utilità di pianificazione
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 71bdf8b87a641247ce2064ccf44ee861d79aab0593229e4cd7b38035c5c7c124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424431"
---
# <a name="prioritytype-simple-type"></a>Tipo semplice priorityType

Definisce i valori minimo e massimo per [**l'elemento Priority (settingsType).**](taskschedulerschema-priority-settingstype-element.md)

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il **tipo semplice priorityType** definisce i valori seguenti.



| Valore | Descrizione                         |
|-------|-------------------------------------|
| 0     | Numero intero minimo consentito.<br/> |
| 10    | Numero intero massimo consentito.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione tipi semplici dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





