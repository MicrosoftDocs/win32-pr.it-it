---
title: ExecAction.WorkingDirectory - proprietà
description: Per lo scripting, ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Proprietà WorkingDirectory Utilità di pianificazione
- Proprietà WorkingDirectory Utilità di pianificazione , oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione proprietà , WorkingDirectory
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
ms.openlocfilehash: 362b6cbb977e66a92425da1355f0747660d867f67aec0ad684f7e8e3956edc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139444"
---
# <a name="execactionworkingdirectory-property"></a>ExecAction.WorkingDirectory - proprietà

Per lo scripting, ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.

## <a name="syntax"></a>Sintassi


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Valore proprietà

Directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, la directory di lavoro dell'applicazione viene specificata [**nell'elemento WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) dello schema Utilità di pianificazione dati.

Il percorso viene controllato per verificare che sia valido quando l'attività viene registrata, non quando questa proprietà è impostata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





