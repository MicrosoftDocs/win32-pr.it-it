---
title: Elemento MaintenanceSettings (maintenanceSettingsType)
description: Specifica il modo in cui il Utilità di pianificazione esegue le attività durante la manutenzione automatica.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Utilità di pianificazione elemento MaintenanceSettings
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120795"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>Elemento MaintenanceSettings (maintenanceSettingsType)

Specifica il modo in cui il Utilità di pianificazione esegue le attività durante la manutenzione automatica.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

L'elemento **MaintenanceSettings** è definito dal tipo complesso [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                    | Tipo    | Descrizione                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Scadenza**](taskschedulerschema-deadline-element.md)   |         | Specifica il periodo di tempo dopo il quale l'utilità di pianificazione tenterà di avviare l'attività durante la manutenzione automatica di emergenza, se non è stata completata durante la normale manutenzione. <br/> |
| [**Esclusivo**](taskschedulerschema-exclusive-element.md) | boolean | Se è impostato su true, l'attività verrà avviata esclusivamente tra le altre attività di manutenzione. <br/>                                                                                                 |
| [**Periodo**](taskschedulerschema-period-element.md)       |         | Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica. <br/>                                                                                                      |



## <a name="remarks"></a>Commenti

Per la programmazione in C++, questa impostazione di inattività viene specificata tramite la proprietà [**ITaskSettings3:: MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) .

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento Settings che indica Utilità di pianificazione eseguire un'attività una volta in 5 giorni durante la manutenzione automatica normale e se non riesce per 15 giorni, avviare il tentativo di esecuzione dell'attività durante la manutenzione automatica di emergenza.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





