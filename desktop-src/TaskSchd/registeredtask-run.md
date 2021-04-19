---
title: Metodo RegisteredTask. Run
description: Per lo scripting, esegue immediatamente l'attività registrata.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Metodo Run Utilità di pianificazione
- Metodo Run Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo Run
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302229"
---
# <a name="registeredtaskrun-method"></a>Metodo RegisteredTask. Run

Per lo scripting, esegue immediatamente l'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*parametri* \[ in\]
</dt> <dd>

Parametri utilizzati come valori nelle azioni dell'attività. Per non specificare i valori dei parametri per le azioni dell'attività, impostare questo parametro su **Nothing**. In caso contrario, è possibile specificare un solo valore stringa o una matrice di valori stringa.

I valori stringa specificati sono associati a nomi e archiviati come coppie nome-valore. Se si specifica un solo valore stringa, Arg0 sarà il nome assegnato al valore. Il valore può essere utilizzato nell'azione dell'attività in cui la variabile $ (Arg0) viene utilizzata nelle proprietà dell'azione.

Se si passano valori quali "0", "100" e "250" come matrice di valori stringa, "0" sostituirà le variabili $ (Arg0), "100" sostituiranno le variabili $ (arg1) e "250" sostituiranno le variabili $ (arg2) utilizzate nelle proprietà dell'azione.

È possibile specificare un massimo di 32 valori di stringa.

Per ulteriori informazioni e per un elenco delle proprietà dell'azione che possono usare variabili $ (Arg0), $ (arg1),..., $ (Arg32) nei rispettivi valori, vedere [azioni attività](task-actions.md).

</dd> <dt>

*ppRunningTask* \[ out\]
</dt> <dd>

Oggetto [**RunningTask**](runningtask.md) che definisce la nuova istanza dell'attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La funzione **RegisteredTask. Run** è equivalente alla funzione [**RegisteredTask. RunEx**](registeredtask-runex.md) con il parametro flags uguale a 0 e non è stato specificato alcun valore per il parametro User.

Questo metodo restituirà senza errori, ma l'attività non verrà eseguita se la proprietà [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) è impostata su false per l'attività registrata.

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
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





