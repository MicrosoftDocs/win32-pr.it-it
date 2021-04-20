---
title: Elemento Interval (restartType)
description: Specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Elemento Interval Utilità di pianificazione
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734186"
---
# <a name="interval-restarttype-element"></a>Elemento Interval (restartType)

Specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività. Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.

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

L'elemento è definito dal [**tipo complesso restartType.**](taskschedulerschema-restarttype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                               | Derivato da                                                       | Descrizione                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**restartType**](taskschedulerschema-restarttype-complextype.md) | Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività ha esito negativo per qualsiasi motivo.<br/> |



## <a name="remarks"></a>Commenti

Se questo elemento viene specificato, è necessario specificare anche l'elemento [**Count**](taskschedulerschema-count-restarttype-element.md) per indicare al Utilità di pianificazione quante volte deve tentare di riavviare l'attività.

Per lo sviluppo in C++, vedere [**Proprietà RestartInterval di ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)

Per lo sviluppo di script, [**vedere TaskSettings.RestartInterval.**](tasksettings-restartinterval.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





