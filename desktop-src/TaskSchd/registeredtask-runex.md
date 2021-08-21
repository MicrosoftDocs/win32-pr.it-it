---
title: Metodo RegisteredTask.RunEx
description: Per lo scripting, esegue immediatamente l'attività registrata usando i flag specificati e un identificatore di sessione.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Metodo RunEx Utilità di pianificazione
- Il metodo RunEx Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione , metodo RunEx
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
ms.openlocfilehash: ecea66d57bf473b5000e84c707e652f1c49431a840da5cc50e43f9e091c3eefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943393"
---
# <a name="registeredtaskrunex-method"></a>Metodo RegisteredTask.RunEx

Per lo scripting, esegue immediatamente l'attività registrata usando i flag specificati e un identificatore di sessione.

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

*parametri* \[ Pollici\]
</dt> <dd>

Parametri utilizzati come valori nelle azioni dell'attività. Per non specificare valori di parametro per le azioni dell'attività, impostare questo parametro su **Nothing**. In caso contrario, è possibile specificare un singolo valore stringa o una matrice di valori stringa.

I valori stringa specificati vengono associati ai nomi e archiviati come coppie nome-valore. Se si specifica un singolo valore stringa, Arg0 sarà il nome assegnato al valore. Il valore può essere usato nell'azione dell'attività in cui la variabile $(Arg0) viene usata nelle proprietà dell'azione.

Se si passano valori come "0", "100" e "250" come matrice di valori stringa, "0" sostituirà le variabili $(Arg0), "100" sostituirà le variabili $(Arg1) e "250" sostituirà le variabili $(Arg2) usate nelle proprietà dell'azione.

È possibile specificare un massimo di 32 valori stringa.

Per altre informazioni e un elenco delle proprietà dell'azione che possono usare le variabili $(Arg0), $(Arg1), ..., $(Arg32) nei relativi valori, vedere [Azioni attività](task-actions.md).

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Costante [TASK \_ RUN \_ FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) che definisce la modalità di esecuzione dell'attività.

</dd> <dt>

*sessionID* \[ Pollici\]
</dt> <dd>

Sessione del server terminal in cui si desidera avviare l'attività.

Se la costante TASK RUN USE SESSION ID (0x4) non viene passata nel parametro flags, il valore specificato \_ in questo parametro viene \_ \_ \_ ignorato.  Se la costante TASK RUN USE SESSION ID viene passata nel parametro flags e il valore sessionID è minore o uguale a 0, verrà restituito un errore di \_ \_ argomento non \_ \_ valido. 

Se la costante TASK RUN USE SESSION ID viene passata nel parametro flags e il valore sessionID è un ID di sessione valido maggiore di 0 e non viene specificato alcun valore per il parametro user, il servizio Utilità di pianificazione tenterà di avviare l'attività in modo interattivo come utente connesso alla \_ \_ sessione \_ \_ specificata.  

Se la costante TASK RUN USE SESSION ID viene passata nel parametro flags e il valore sessionID è un ID di sessione valido maggiore di 0 e se nel parametro user è specificato un utente, il servizio Utilità di pianificazione tenterà di avviare l'attività in modo interattivo come utente specificato nel parametro \_ \_ \_ \_ *user.*  

</dd> <dt>

*runningTask* \[ Cambio\]
</dt> <dd>

Oggetto [**RunningTask**](runningtask.md) che definisce la nuova istanza dell'attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo restituirà senza errori, ma l'attività non verrà eseguita se la proprietà [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) è impostata su false per l'attività registrata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





