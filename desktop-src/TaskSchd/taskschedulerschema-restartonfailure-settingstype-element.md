---
title: Elemento RestartOnFailure (settingsType)
description: Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività ha esito negativo per qualsiasi motivo.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Elemento RestartOnFailure Utilità di pianificazione
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfe29be7dd329def41e8a6726f141a850eb2daecd05e05d6b5988f543f64864c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072441"
---
# <a name="restartonfailure-settingstype-element"></a>Elemento RestartOnFailure (settingsType)

Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività ha esito negativo per qualsiasi motivo.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

**L'elemento RestartOnFailure** è definito dal [**tipo complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                              | Tipo         | Descrizione                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Conteggio**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Specifica il numero di tentativi di riavvio Utilità di pianificazione'attività.<br/> |
| [**Intervallo**](taskschedulerschema-interval-restarttype-element.md) | duration     | Specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.<br/>                 |



## <a name="remarks"></a>Commenti

Quando un'applicazione specifica le impostazioni dell'attività, queste informazioni sono accessibili tramite le proprietà [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) e [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) dell'interfaccia [**ITaskSettings.**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) Per lo scripting, queste informazioni sono accessibili tramite le [**proprietà TaskSettings.RestartCount**](tasksettings-restartcount.md) [**e TaskSettings.RestartInterval.**](tasksettings-restartinterval.md)

Entrambi gli elementi figlio devono essere impostati per specificare il modo in Utilità di pianificazione riavvio dell'attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





