---
title: Metodo RegisteredTask.Run
description: Per lo scripting, esegue immediatamente l'attività registrata.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Eseguire il metodo Utilità di pianificazione
- Eseguire il metodo Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione , metodo Run
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
ms.openlocfilehash: e747688ba80c08a39b0336fda126ae7d85a558f53c97aab230bc5d3d0113b360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681621"
---
# <a name="registeredtaskrun-method"></a>Metodo RegisteredTask.Run

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

*parametri* \[ Pollici\]
</dt> <dd>

Parametri utilizzati come valori nelle azioni dell'attività. Per non specificare valori di parametro per le azioni dell'attività, impostare questo parametro su **Nothing**. In caso contrario, è possibile specificare un singolo valore stringa o una matrice di valori stringa.

I valori stringa specificati vengono associati ai nomi e archiviati come coppie nome-valore. Se si specifica un singolo valore stringa, Arg0 sarà il nome assegnato al valore. Il valore può essere usato nell'azione dell'attività in cui la variabile $(Arg0) viene usata nelle proprietà dell'azione.

Se si passano valori come "0", "100" e "250" come matrice di valori stringa, "0" sostituirà le variabili $(Arg0), "100" sostituirà le variabili $(Arg1) e "250" sostituirà le variabili $(Arg2) usate nelle proprietà dell'azione.

È possibile specificare un massimo di 32 valori stringa.

Per altre informazioni e un elenco delle proprietà dell'azione che possono usare le variabili $(Arg0), $(Arg1), ..., $(Arg32) nei relativi valori, vedere [Azioni attività](task-actions.md).

</dd> <dt>

*ppRunningTask* \[ Cambio\]
</dt> <dd>

Oggetto [**RunningTask**](runningtask.md) che definisce la nuova istanza dell'attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La **funzione RegisteredTask.Run** equivale alla funzione [**RegisteredTask.RunEx**](registeredtask-runex.md) con il parametro flags uguale a 0 e nessun valore specificato per il parametro user.

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

 

 





