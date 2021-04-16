---
title: Tipo semplice dayOfMonthType
description: Definisce i valori possibili per specificare un giorno del mese.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- Utilità di pianificazione di tipo semplice dayOfMonthType
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517505"
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

Il tipo semplice **dayOfMonthType** è una **stringa** limitata dal modello seguente:

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    Specifica il primo e il 31 ° giorno del mese o sempre l'ultimo giorno del mese.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi semplici dello schema Utilità di pianificazione](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





