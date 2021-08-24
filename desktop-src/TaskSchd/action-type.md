---
title: Action.Type - proprietà
description: Per lo scripting, ottiene il tipo di azione.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Proprietà type Utilità di pianificazione
- Proprietà Type Utilità di pianificazione , oggetto Action
- Action object Utilità di pianificazione proprietà Type
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499c7e42b5b2578928796e6f878219e0c53612e454948d390cdb631dcaccd64c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739031"
---
# <a name="actiontype-property"></a>Action.Type - proprietà

Per lo scripting, ottiene il tipo di azione.

## <a name="syntax"></a>Sintassi


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà restituisce una delle costanti di enumerazione [**TASK \_ ACTION \_ TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) seguenti.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**ATTIVITÀ \_ AZIONE \_ EXEC**</dt> <dt>0</dt> </dl>                          | Questa azione esegue un'operazione della riga di comando. Ad esempio, l'azione può eseguire uno script, avviare un file eseguibile oppure, se viene specificato il nome di un documento, trovare l'applicazione associata e avviare l'applicazione con il documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**ATTIVITÀ \_ GESTORE \_ COM \_ DI AZIONE**</dt> <dt>5</dt> </dl>    | Questa azione genera un gestore.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**ATTIVITÀ \_ AZIONE \_ INVIA MESSAGGIO DI POSTA \_ ELETTRONICA**</dt> <dt>6</dt> </dl>       | Questa azione invia un messaggio di posta elettronica.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**ATTIVITÀ \_ AZIONE \_ MOSTRA \_ MESSAGGIO**</dt> <dt>7</dt> </dl> | Questa azione mostra una finestra di messaggio.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il tipo di azione viene definito quando l'azione viene creata e non può essere modificata in un secondo momento. Per informazioni sulla creazione di un'azione, vedere [**ActionCollection.Create**](actioncollection-create.md).

Per informazioni sul funzionamento di azioni e attività, vedere [Azioni attività](task-actions.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO \_ DI AZIONE \_ ATTIVITÀ**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**Azione**](action.md)
</dt> </dl>

 

 





