---
title: Proprietà TaskSettings. RestartInterval
description: Per gli script, ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Utilità di pianificazione proprietà RestartInterval
- Utilità di pianificazione proprietà RestartInterval, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740423"
---
# <a name="tasksettingsrestartinterval-property"></a>Proprietà TaskSettings. RestartInterval

Per gli script, ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valore proprietà

Valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività. Se questa proprietà è impostata, è necessario impostare anche la proprietà [**RestartCount**](tasksettings-restartcount.md) . Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> (ad esempio, "PT5M" è 5 minuti, "PT1H" è 1 ora e "PT20M" è di 20 minuti). Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è pari a 1 minuto.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) dello schema utilità di pianificazione.

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

 

 





