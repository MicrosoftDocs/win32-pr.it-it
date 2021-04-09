---
title: RegisteredTask. RunEx, metodo
description: Per gli script, esegue l'attività registrata immediatamente usando i flag specificati e un identificatore di sessione.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Utilità di pianificazione del metodo RunEx
- Metodo RunEx Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo RunEx
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120426"
---
# <a name="registeredtaskrunex-method"></a>RegisteredTask. RunEx, metodo

Per gli script, esegue l'attività registrata immediatamente usando i flag specificati e un identificatore di sessione.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
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

*flag* \[ in\]
</dt> <dd>

Costante [dei \_ \_ flag di esecuzione](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) di un'attività che definisce la modalità di esecuzione dell'attività.

</dd> <dt>

*ID sessione* \[ in\]
</dt> <dd>

Sessione di Terminal Server in cui si desidera avviare l'attività.

Se l'esecuzione dell'attività \_ \_ Usa la \_ \_ costante ID di sessione (0x4) non viene passata nel parametro *Flags* , il valore specificato in questo parametro viene ignorato. Se l'esecuzione dell'attività \_ \_ Usa la \_ \_ costante ID sessione viene passata nel parametro *Flags* e il valore SessionID è minore o uguale a 0, verrà restituito un errore di argomento non valido.

Se l'esecuzione dell'attività \_ \_ Usa la \_ \_ costante ID sessione viene passata nel parametro *Flags* e il valore SessionID è un ID di sessione valido maggiore di 0 e se non viene specificato alcun valore per il parametro *User* , il servizio Utilità di pianificazione tenterà di avviare l'attività in modo interattivo quando l'utente è connesso alla sessione specificata.

Se l'esecuzione dell'attività \_ \_ Usa la \_ \_ costante ID sessione viene passata nel parametro *Flags* e il valore SessionID è un ID di sessione valido maggiore di 0 e se un utente viene specificato nel parametro *User* , il servizio Utilità di pianificazione tenterà di avviare l'attività in modo interattivo come l'utente specificato nel parametro *User* .

</dd> <dt>

*runningTask* \[ out\]
</dt> <dd>

Oggetto [**RunningTask**](runningtask.md) che definisce la nuova istanza dell'attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

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

 

 





