---
title: Elemento Task
description: Definisce l'attività eseguita dal servizio Utilità di pianificazione.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Utilità di pianificazione elemento attività
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873485"
---
# <a name="task-element"></a>Elemento Task

Definisce l'attività eseguita dal servizio Utilità di pianificazione.

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Tipo                                                                                 | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Azioni**](taskschedulerschema-actions-tasktype-element.md)                   | [**actionsType**](taskschedulerschema-actionstype-complextype.md)                   | Specifica le azioni eseguite dall'attività.<br/>                                                                             |
| [**Data**](taskschedulerschema-data-tasktype-element.md)                         | [**dataType**](taskschedulerschema-datatype-complextype.md)                         | Specifica i dati aggiuntivi associati all'attività, ma in caso contrario non viene utilizzato dal servizio Utilità di pianificazione.<br/>         |
| [**Principals**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Specifica i contesti di sicurezza che possono essere utilizzati per eseguire l'attività.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingsType**](taskschedulerschema-settingstype-complextype.md)                 | Specifica le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/>                                                 |
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggersType**](taskschedulerschema-triggerstype-complextype.md)                 | Specifica i trigger che avviano l'attività.<br/>                                                                              |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).

Per lo sviluppo di script, vedere [**TaskDefinition**](taskdefinition.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





