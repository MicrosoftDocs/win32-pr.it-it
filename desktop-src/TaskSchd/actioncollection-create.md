---
title: Metodo ActionCollection. Create
description: Per lo scripting, crea e aggiunge una nuova azione alla raccolta.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Utilità di pianificazione Crea metodo
- Metodo Create Utilità di pianificazione, oggetto ActionCollection
- Oggetto ActionCollection Utilità di pianificazione, metodo create
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
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518232"
---
# <a name="actioncollectioncreate-method"></a>Metodo ActionCollection. Create

Per lo scripting, crea e aggiunge una nuova azione alla raccolta.

## <a name="syntax"></a>Sintassi


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo* \[ di in\]
</dt> <dd>

Questo parametro è impostato su una delle seguenti costanti di enumerazione del [**\_ \_ tipo di azione attività**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Attività \_ AZIONE \_ Exec**</dt> <dt>0</dt> </dl>                          | L'azione esegue un'operazione della riga di comando. Ad esempio, l'azione può eseguire uno script, avviare un eseguibile o, se il nome di un documento viene fornito, trovare l'applicazione associata e avviare l'applicazione con il documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Attività \_ \_ \_ Gestore com azione**</dt> <dt>5</dt> </dl>    | L'azione genera un gestore.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Attività \_ AZIONE \_ inviare un \_ messaggio di posta elettronica**</dt> <dt>6</dt> </dl>       | Questa azione Invia un messaggio di posta elettronica.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Attività \_ AZIONE \_ Mostra \_ messaggio**</dt> <dt>7</dt> </dl> | Questa azione Visualizza una finestra di messaggio.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**azione**](action.md) che rappresenta la nuova azione.

## <a name="remarks"></a>Commenti

Non è possibile aggiungere più di 32 azioni alla raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tipo di azione attività \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
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

 

 





