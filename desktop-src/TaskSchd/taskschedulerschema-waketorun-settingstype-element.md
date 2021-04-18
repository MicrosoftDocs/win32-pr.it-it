---
title: Elemento WakeToRun (settingsType)
description: Specifica che Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Utilità di pianificazione elemento WakeToRun
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302486"
---
# <a name="waketorun-settingstype-element"></a>Elemento WakeToRun (settingsType)

Specifica che Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

L'elemento **WakeToRun** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Quando il servizio Utilità di pianificazione riattiva il computer per eseguire un'attività, è possibile che lo schermo rimanga disattivato anche se il computer non è più in modalità di sospensione o di ibernazione. La schermata viene accesa quando Windows Vista rileva che un utente ha restituito l'utilizzo del computer.

Per lo sviluppo in C++, vedere [**la proprietà WakeToRun di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).

Per lo sviluppo di script, vedere [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).

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

 

 





