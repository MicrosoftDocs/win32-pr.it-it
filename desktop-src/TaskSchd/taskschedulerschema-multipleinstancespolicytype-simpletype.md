---
title: Tipo semplice multipleInstancesPolicyType
description: Definisce le costanti dei criteri di istanza per l'elemento MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Tipo semplice multipleInstancesPolicyType Utilità di pianificazione
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e8e847e268486e58bc36bd1bcf9f454b2d8af7b7664d0372613c40c818f932f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758510"
---
# <a name="multipleinstancespolicytype-simple-type"></a>Tipo semplice multipleInstancesPolicyType

Definisce le costanti dei criteri di istanza per [**l'elemento MultipleInstancesPolicy (settingsType).**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

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

Il **tipo semplice multipleInstancesPolicyType** definisce i valori seguenti.



| Valore        | Descrizione                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Parallelo     | Avvia una nuova istanza mentre è in esecuzione un'istanza esistente.<br/>                           |
| Coda        | Avvia una nuova istanza dell'attività al termine di tutte le altre istanze dell'attività.<br/>      |
| IgnoreNew    | Valore predefinito. Non avvia una nuova istanza se è in esecuzione un'istanza esistente dell'attività.<br/> |
| StopExisting | Arresta un'istanza esistente dell'attività prima di avviare la nuova istanza.<br/>                |



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

 

 





