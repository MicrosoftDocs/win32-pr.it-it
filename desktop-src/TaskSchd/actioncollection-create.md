---
title: Metodo ActionCollection.Create
description: Per lo scripting, crea e aggiunge una nuova azione alla raccolta.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Creare il metodo Utilità di pianificazione
- Creare il metodo Utilità di pianificazione, oggetto ActionCollection
- Oggetto ActionCollection Utilità di pianificazione, metodo Create
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce517ae33681fcb106e83720fc5ddd7685f26f673c466e24162ce95e9ca442
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072701"
---
# <a name="actioncollectioncreate-method"></a>Metodo ActionCollection.Create

Per lo scripting, crea e aggiunge una nuova azione alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* \[ Pollici\]
</dt> <dd>

Questo parametro è impostato su una delle costanti di [**enumerazione TASK \_ ACTION \_ TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) seguenti.



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**ATTIVITÀ \_ ACTION \_ EXEC**</dt> <dt>0</dt> </dl>                          | L'azione esegue un'operazione della riga di comando. Ad esempio, l'azione potrebbe eseguire uno script, avviare un eseguibile oppure, se viene specificato il nome di un documento, trovare l'applicazione associata e avviare l'applicazione con il documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**ATTIVITÀ \_ ACTION \_ COM \_ HANDLER**</dt> <dt>5</dt> </dl>    | L'azione genera un gestore.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**ATTIVITÀ \_ AZIONE INVIA \_ \_ MESSAGGIO DI POSTA ELETTRONICA**</dt> <dt>6</dt> </dl>       | Questa azione invia un messaggio di posta elettronica.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**ATTIVITÀ \_ AZIONE \_ MOSTRA \_ MESSAGGIO**</dt> <dt>7</dt> </dl> | Questa azione visualizza una finestra di messaggio.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**Action**](action.md) che rappresenta la nuova azione.

## <a name="remarks"></a>Commenti

Non è possibile aggiungere più di 32 azioni alla raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TIPO \_ DI AZIONE \_ ATTIVITÀ**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**Actioncollection**](actioncollection.md)
</dt> <dt>

[**Azione**](action.md)
</dt> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





