---
title: Tipo semplice dayOfMonthType
description: Definisce i valori possibili per specificare un giorno del mese.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- Tipo semplice dayOfMonthType Utilità di pianificazione
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c3d3d549f2d84c292ad1dbdf3c03965bd6e4265559b57c41016811834167a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309354"
---
# <a name="dayofmonthtype-simple-type"></a>Tipo semplice dayOfMonthType

Definisce i valori possibili per specificare un giorno del mese.

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice dayOfMonthType** è una **stringa** limitata dal modello seguente:

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    Specifica il primo e il 31° giorno del mese o sempre l'ultimo giorno del mese.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione semplici dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





