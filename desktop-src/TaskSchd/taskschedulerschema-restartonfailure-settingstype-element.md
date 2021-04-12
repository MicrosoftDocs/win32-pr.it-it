---
title: Elemento RestartOnFailure (settingsType)
description: Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Utilità di pianificazione elemento RestartOnFailure
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225242"
---
# <a name="restartonfailure-settingstype-element"></a>Elemento RestartOnFailure (settingsType)

Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

L'elemento **RestartOnFailure** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                              | Tipo         | Descrizione                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Conteggio**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Specifica il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.<br/> |
| [**Interval**](taskschedulerschema-interval-restarttype-element.md) | duration     | Specifica il periodo di tempo durante il quale il Utilità di pianificazione tenterà di riavviare l'attività.<br/>                 |



## <a name="remarks"></a>Commenti

Quando un'applicazione specifica le impostazioni delle attività, queste informazioni sono accessibili tramite le proprietà [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) e [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) dell'interfaccia [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) . Per gli script, è possibile accedere a queste informazioni tramite le proprietà [**TaskSettings. RestartCount**](tasksettings-restartcount.md) e [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .

È necessario impostare entrambi gli elementi figlio per specificare il modo in cui il Utilità di pianificazione riavvia l'attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





