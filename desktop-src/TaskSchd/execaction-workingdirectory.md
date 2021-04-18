---
title: Proprietà ExecAction. WorkingDirectory
description: Per la creazione di script, ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Utilità di pianificazione proprietà WorkingDirectory
- Utilità di pianificazione proprietà WorkingDirectory, oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione, proprietà WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301342"
---
# <a name="execactionworkingdirectory-property"></a>Proprietà ExecAction. WorkingDirectory

Per la creazione di script, ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.

## <a name="syntax"></a>Sintassi


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Valore proprietà

Directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, la directory di lavoro dell'applicazione viene specificata nell'elemento [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) dello schema utilità di pianificazione.

Il percorso è verificato per assicurarsi che sia valido quando l'attività è registrata, non quando questa proprietà è impostata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





