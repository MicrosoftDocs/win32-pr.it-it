---
title: Proprietà TaskSettings. WakeToRun
description: Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Utilità di pianificazione proprietà WakeToRun
- Utilità di pianificazione proprietà WakeToRun, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà WakeToRun
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740802"
---
# <a name="tasksettingswaketorun-property"></a>Proprietà TaskSettings. WakeToRun

Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se true, la proprietà indica che il Utilità di pianificazione riattiverà il computer al momento dell'esecuzione dell'attività.

## <a name="remarks"></a>Commenti

Quando il servizio Utilità di pianificazione riattiva il computer per eseguire un'attività, è possibile che lo schermo rimanga disattivato anche se il computer non è più in modalità di sospensione o di ibernazione. La schermata viene accesa quando Windows Vista rileva che un utente ha restituito l'utilizzo del computer.

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





