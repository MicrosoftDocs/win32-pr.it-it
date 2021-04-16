---
title: Proprietà Action. Type
description: Per lo scripting, ottiene il tipo dell'azione.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Utilità di pianificazione proprietà di tipo
- Utilità di pianificazione proprietà tipo, oggetto azione
- Oggetto Action Utilità di pianificazione, proprietà Type
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
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477812"
---
# <a name="actiontype-property"></a>Proprietà Action. Type

Per lo scripting, ottiene il tipo dell'azione.

## <a name="syntax"></a>Sintassi


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà restituisce una delle seguenti costanti di enumerazione del [**\_ \_ tipo di azione dell'attività**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) .



| Valore                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Attività \_ AZIONE \_ Exec**</dt> <dt>0</dt> </dl>                          | Questa azione esegue un'operazione della riga di comando. Ad esempio, l'azione può eseguire uno script, avviare un eseguibile o, se il nome di un documento viene fornito, trovare l'applicazione associata e avviare l'applicazione con il documento.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Attività \_ \_ \_ Gestore com azione**</dt> <dt>5</dt> </dl>    | Questa azione attiva un gestore.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Attività \_ AZIONE \_ inviare un \_ messaggio di posta elettronica**</dt> <dt>6</dt> </dl>       | Questa azione Invia un messaggio di posta elettronica.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Attività \_ AZIONE \_ Mostra \_ messaggio**</dt> <dt>7</dt> </dl> | Questa azione Visualizza una finestra di messaggio.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il tipo di azione viene definito quando viene creata l'azione e non può essere modificato in un secondo momento. Per informazioni sulla creazione di un'azione, vedere [**ActionCollection. Create**](actioncollection-create.md).

Per informazioni sul funzionamento combinato di azioni e attività, vedere [azioni attività](task-actions.md).

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

[**Azione**](action.md)
</dt> </dl>

 

 





