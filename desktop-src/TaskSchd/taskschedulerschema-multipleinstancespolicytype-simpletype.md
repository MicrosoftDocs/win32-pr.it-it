---
title: Tipo semplice multipleInstancesPolicyType
description: Definisce le costanti dei criteri dell'istanza per l'elemento MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Utilità di pianificazione di tipo semplice multipleInstancesPolicyType
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964435"
---
# <a name="multipleinstancespolicytype-simple-type"></a>Tipo semplice multipleInstancesPolicyType

Definisce le costanti dei criteri dell'istanza per l'elemento [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il tipo semplice **multipleInstancesPolicyType** definisce i valori seguenti.



| Valore        | Descrizione                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Parallelo     | Avvia una nuova istanza di mentre è in esecuzione un'istanza esistente.<br/>                           |
| Coda        | Avvia una nuova istanza dell'attività dopo il completamento di tutte le altre istanze dell'attività.<br/>      |
| IgnoreNew    | Valore predefinito. Non avvia una nuova istanza se è in esecuzione un'istanza esistente dell'attività.<br/> |
| StopExisting | Arresta un'istanza esistente dell'attività prima di avviare una nuova istanza.<br/>                |



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

 

 





