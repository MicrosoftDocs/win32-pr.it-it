---
title: Proprietà TaskSettings. AllowHardTerminate
description: Per la creazione di script, ottiene o imposta un valore booleano che indica che l'attività può essere terminata dal servizio Utilità di pianificazione usando TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Utilità di pianificazione proprietà AllowHardTerminate
- Utilità di pianificazione proprietà AllowHardTerminate, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà AllowHardTerminate
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742415"
---
# <a name="tasksettingsallowhardterminate-property"></a>Proprietà TaskSettings. AllowHardTerminate

Per la creazione di script, ottiene o imposta un valore booleano che indica che l'attività può essere terminata dal servizio Utilità di pianificazione usando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Il servizio tenterà di chiudere l'attività in esecuzione inviando la notifica di [**\_ chiusura WM**](../winmsg/wm-close.md) . se l'attività non risponde, l'attività verrà terminata solo se questa proprietà è impostata su true.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se true, l'attività può essere terminata usando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Se false, l'attività non può essere terminata utilizzando **TerminateProcess**.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

