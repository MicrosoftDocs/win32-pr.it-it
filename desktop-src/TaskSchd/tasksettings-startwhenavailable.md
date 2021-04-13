---
title: Proprietà TaskSettings. StartWhenAvailable
description: Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il tempo pianificato.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Utilità di pianificazione proprietà StartWhenAvailable
- Utilità di pianificazione proprietà StartWhenAvailable, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478364"
---
# <a name="tasksettingsstartwhenavailable-property"></a>Proprietà TaskSettings. StartWhenAvailable

Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il tempo pianificato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se true, la proprietà indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il tempo pianificato. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo alle attività basate sul tempo con un limite finale o attività basate sul tempo impostate per la ripetizione infinita.

Le attività avviate dopo il passaggio dell'ora pianificata, a causa della proprietà [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) impostata su true, vengono accodate nella coda delle attività del servizio Utilità di pianificazione e vengono avviate dopo un ritardo. Il ritardo predefinito è di 10 minuti.

Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) dello schema utilità di pianificazione.

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

 

 





