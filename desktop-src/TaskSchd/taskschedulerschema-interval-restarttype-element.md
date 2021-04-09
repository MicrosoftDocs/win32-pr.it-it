---
title: Elemento Interval (restartType)
description: Specifica il periodo di tempo durante il quale il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Utilità di pianificazione dell'elemento Interval
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963859"
---
# <a name="interval-restarttype-element"></a>Elemento Interval (restartType)

Specifica il periodo di tempo durante il quale il Utilità di pianificazione tenterà di riavviare l'attività. Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> (ad esempio, "PT5M" è 5 minuti, "PT1H" è 1 ora e "PT20M" è di 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è pari a 1 minuto.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dal tipo complesso [**restartType**](taskschedulerschema-restarttype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                               | Derivato da                                                       | Descrizione                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**restartType**](taskschedulerschema-restarttype-complextype.md) | Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.<br/> |



## <a name="remarks"></a>Commenti

Se questo elemento viene specificato, è necessario specificare anche l'elemento [**count**](taskschedulerschema-count-restarttype-element.md) per indicare al utilità di pianificazione il numero di tentativi di riavvio dell'attività.

Per lo sviluppo in C++, vedere [**la proprietà RestartInterval di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).

Per lo sviluppo di script, vedere [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





