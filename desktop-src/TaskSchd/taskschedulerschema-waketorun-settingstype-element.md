---
title: Elemento WakeToRun (settingsType)
description: Specifica che Utilità di pianificazione riattivazione del computer quando è il momento di eseguire l'attività.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Elemento WakeToRun Utilità di pianificazione
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12d16f9f06685a427a8f3e7c4f2356dff0bc6415e50379ba752a4bc3a3fec8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872061"
---
# <a name="waketorun-settingstype-element"></a>Elemento WakeToRun (settingsType)

Specifica che Utilità di pianificazione riattivazione del computer quando è il momento di eseguire l'attività.

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

**L'elemento WakeToRun** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Quando il Utilità di pianificazione riattiva il computer per eseguire un'attività, è possibile che lo schermo rimanga spento anche se il computer non è più in modalità sospensione o ibernazione. La schermata si accende quando Windows Vista rileva che un utente è tornato a usare il computer.

Per lo sviluppo C++, vedere [**Proprietà WakeToRun di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).

Per lo sviluppo di script, vedere [**TaskSettings.WakeToRun**](tasksettings-waketorun.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





