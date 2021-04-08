---
title: Proprietà ExecAction. Path
description: Per lo scripting, ottiene o imposta il percorso di un file eseguibile.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Utilità di pianificazione proprietà Path
- Utilità di pianificazione proprietà Path, oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione, proprietà Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740858"
---
# <a name="execactionpath-property"></a>Proprietà ExecAction. Path

Per lo scripting, ottiene o imposta il percorso di un file eseguibile.

## <a name="syntax"></a>Sintassi


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>Valore proprietà

Percorso del file eseguibile che deve essere eseguito dall'azione.

## <a name="remarks"></a>Commenti

Questa azione esegue un'operazione della riga di comando. Ad esempio, l'azione potrebbe eseguire uno script o avviare un file eseguibile.

Durante la lettura o la scrittura di codice XML, il percorso dell'operazione della riga di comando viene specificato nell'elemento [**Command**](taskschedulerschema-command-exectype-element.md) dello schema utilità di pianificazione.

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

 

 





