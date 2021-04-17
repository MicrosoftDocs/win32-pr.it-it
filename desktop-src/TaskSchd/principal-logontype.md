---
title: Proprietà Principal. LogonType
description: Per lo scripting, ottiene o imposta il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Utilità di pianificazione proprietà LogonType
- Utilità di pianificazione proprietà LogonType, oggetto Principal
- Utilità di pianificazione oggetto principale, proprietà LogonType
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
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477200"
---
# <a name="principallogontype-property"></a>Proprietà Principal. LogonType

Per lo scripting, ottiene o imposta il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.

## <a name="syntax"></a>Sintassi


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Valore proprietà

Impostare su una delle costanti di enumerazione dei [**\_ tipi di accesso alle attività**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) seguenti.



| Valore                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Attività \_ \_Nessun accesso**</dt> <dt>0</dt> </dl>                                                                               | Metodo di accesso non specificato. Utilizzato per le credenziali non NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Attività \_ \_Password di accesso**</dt> <dt>1</dt> </dl>                                                                   | Usare una password per la registrazione dell'utente. La password deve essere fornita in fase di registrazione.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Attività \_ \_S4U di accesso**</dt> <dt>2</dt> </dl>                                                                                  | Usare un token interattivo esistente per eseguire un'attività. L'utente deve accedere utilizzando un servizio per l'accesso utente (S4U). Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Attività \_ \_ \_ Token interattivo di accesso**</dt> <dt>3</dt> </dl>                                       | L'utente deve essere già connesso. L'attività verrà eseguita solo in una sessione interattiva esistente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Attività \_ \_Gruppo di accesso**</dt> <dt>4</dt> </dl>                                                                            | Attivazione del gruppo. Il campo userId specifica il gruppo.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Attività \_ \_ \_ Account del servizio di accesso**</dt> <dt>5</dt> </dl>                                             | Indica che un account di sistema locale, servizio locale o servizio di rete viene utilizzato come contesto di sicurezza per eseguire l'attività.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Attività \_ \_Token interattivo di accesso \_ \_ o \_ password**</dt> <dt>6</dt> </dl> | Usare prima il token interattivo. Se l'utente non è connesso (non è disponibile alcun token interattivo), viene utilizzata la password. Quando un'attività è registrata, è necessario specificare la password. Questo flag non è consigliato per le nuove attività perché è meno affidabile rispetto alla \_ password di accesso dell'attività \_ .<br/> |



 

## <a name="remarks"></a>Commenti

Questa proprietà è valida solo quando un identificatore utente viene specificato dalla proprietà [**userid**](principal-userid.md) .

Durante la lettura o la scrittura di codice XML per un'attività, il tipo di accesso viene specificato nell' [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) elemento dello schema utilità di pianificazione.

Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo. Per impostare il tipo di accesso dell'attività su interattivo, specificare 3 (**\_ \_ \_ token interattivo accesso attività**) o 4 (**\_ \_ gruppo di accesso attività**) nella proprietà **LogonType** dell'entità attività oppure nel parametro *LogonType* di [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

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

[**Principale**](principal.md)
</dt> </dl>

 

 





