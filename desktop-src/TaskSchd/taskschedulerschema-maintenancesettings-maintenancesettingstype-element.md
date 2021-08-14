---
title: Elemento MaintenanceSettings (maintenanceSettingsType)
description: Specifica il modo in cui Utilità di pianificazione attività durante la manutenzione automatica.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Elemento MaintenanceSettings Utilità di pianificazione
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5724a5dff942377af783970e5d011e8f8a1ce9123039112917a3f652372495d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309341"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>Elemento MaintenanceSettings (maintenanceSettingsType)

Specifica il modo in cui Utilità di pianificazione attività durante la manutenzione automatica.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

**L'elemento MaintenanceSettings** è definito dal tipo complesso [**maintenanceSettingsType.**](taskschedulerschema-maintenancesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                    | Tipo    | Descrizione                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Scadenza**](taskschedulerschema-deadline-element.md)   |         | Specifica l'intervallo di tempo dopo il quale l'Utilità di pianificazione tenterà di avviare l'attività durante la manutenzione automatica di emergenza, se non è stato possibile completarla durante la manutenzione regolare. <br/> |
| [**Esclusivo**](taskschedulerschema-exclusive-element.md) | boolean | Se impostato su true, l'attività verrà avviata esclusivamente tra le altre attività di manutenzione. <br/>                                                                                                 |
| [**Periodo**](taskschedulerschema-period-element.md)       |         | Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica. <br/>                                                                                                      |



## <a name="remarks"></a>Commenti

Per la programmazione C++, questa impostazione di inattività viene specificata usando la [**proprietà ITaskSettings3::MaintenanceSettings.**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento settings che indica a Utilità di pianificazione di eseguire l'attività una volta ogni 5 giorni durante la normale manutenzione automatica e, in caso di esito negativo per 15 giorni, avviare il tentativo di eseguire l'attività durante la manutenzione automatica di emergenza.


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>           |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





