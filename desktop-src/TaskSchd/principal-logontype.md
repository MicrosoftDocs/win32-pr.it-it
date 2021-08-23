---
title: Principal.LogonType - proprietà
description: Per lo scripting, ottiene o imposta il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Proprietà LogonType Utilità di pianificazione
- Proprietà LogonType Utilità di pianificazione, oggetto Principal
- Oggetto Principal Utilità di pianificazione proprietà LogonType
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7db85573072c54a613009c3afec4873a38db4ff7336e487553437967b4c6e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060079"
---
# <a name="principallogontype-property"></a>Principal.LogonType - proprietà

Per lo scripting, ottiene o imposta il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.

## <a name="syntax"></a>Sintassi


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Valore proprietà

Impostare su una delle costanti di [**enumerazione TASK \_ LOGON TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) seguenti.



| Valore                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**ATTIVITÀ \_ LOGON \_ NONE**</dt> <dt>0</dt> </dl>                                                                               | Il metodo logon non è specificato. Utilizzato per le credenziali non NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**ATTIVITÀ \_ PASSWORD \_ DI ACCESSO**</dt> <dt>1</dt> </dl>                                                                   | Usare una password per l'accesso dell'utente. La password deve essere specificata al momento della registrazione.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**ATTIVITÀ \_ LOGON \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Usare un token interattivo esistente per eseguire un'attività. L'utente deve accedere usando un servizio per l'accesso utente (S4U). Quando si usa un accesso S4U, non viene archiviata alcuna password dal sistema e non è possibile accedere alla rete o ai file crittografati.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**ATTIVITÀ \_ LOGON \_ INTERACTIVE \_ TOKEN**</dt> <dt>3</dt> </dl>                                       | L'utente deve essere già connesso. L'attività verrà eseguita solo in una sessione interattiva esistente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**ATTIVITÀ \_ LOGON \_ GROUP**</dt> <dt>4</dt> </dl>                                                                            | Attivazione del gruppo. Il campo userId specifica il gruppo.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**ATTIVITÀ \_ ACCOUNT \_ DEL SERVIZIO DI \_ ACCESSO**</dt> <dt>5</dt> </dl>                                             | Indica che un account di sistema locale, servizio locale o servizio di rete viene utilizzato come contesto di sicurezza per eseguire l'attività.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**ATTIVITÀ \_ TOKEN \_ INTERATTIVO DI ACCESSO O \_ \_ \_ PASSWORD**</dt> <dt>6</dt> </dl> | Usare prima di tutto il token interattivo. Se l'utente non è connesso (non è disponibile alcun token interattivo), viene usata la password. La password deve essere specificata quando viene registrata un'attività. Questo flag non è consigliato per le nuove attività perché è meno affidabile di TASK \_ LOGON \_ PASSWORD.<br/> |



 

## <a name="remarks"></a>Commenti

Questa proprietà è valida solo quando un identificatore utente viene specificato dalla [**proprietà UserId.**](principal-userid.md)

Durante la lettura o la scrittura di codice XML per un'attività, il tipo logon viene specificato [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) nell'elemento dello schema Utilità di pianificazione.

Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività ha un tipo di accesso interattivo. Per impostare il tipo di accesso all'attività su interattivo, specificare 3 (**TASK \_ LOGON INTERACTIVE \_ \_ TOKEN**) o 4 (**TASK LOGON \_ \_ GROUP**) nella proprietà **LogonType** dell'entità attività o nel *parametro logonType* di [**TaskFolder.RegisterTask**](taskfolder-registertask.md) o [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

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

[**Principale**](principal.md)
</dt> </dl>

 

 





