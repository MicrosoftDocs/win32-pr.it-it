---
title: Elemento RestartOnIdle (idleSettingsType)
description: Specifica se l'attività viene riavviata quando il computer scorre una condizione di inattività più volte.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Utilità di pianificazione elemento RestartOnIdle
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302684"
---
# <a name="restartonidle-idlesettingstype-element"></a>Elemento RestartOnIdle (idleSettingsType)

Specifica se l'attività viene riavviata quando il computer scorre una condizione di inattività più volte.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

L'elemento **RestartOnIdle** è definito dal tipo complesso [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.<br/> |



## <a name="remarks"></a>Commenti

Questo elemento viene utilizzato solo se l'elemento [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) è impostato su true.

Per lo sviluppo di script, questa impostazione di attività viene specificata tramite la proprietà [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) .

Per lo sviluppo in C++, questa impostazione di attività viene specificata tramite la proprietà [**IIdleSettings:: RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un'impostazione inattiva che indica che l'attività non deve essere riavviata quando viene ciclita la condizione di inattività.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





