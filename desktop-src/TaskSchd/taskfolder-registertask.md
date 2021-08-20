---
title: Metodo TaskFolder.RegisterTask
description: Per lo scripting, registra (crea) una nuova attività nella cartella usando XML per definire l'attività.
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- Metodo RegisterTask Utilità di pianificazione
- Metodo RegisterTask Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo RegisterTask
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85321b9dd39e7e7f5e03ff6f4fc828ac94a7d208e673ebf505c07f1687308c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943379"
---
# <a name="taskfolderregistertask-method"></a>Metodo TaskFolder.RegisterTask

Per lo scripting, registra (crea) una nuova attività nella cartella usando XML per definire l'attività.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*path* \[ Pollici\]
</dt> <dd>

Nome dell'attività. Se questo valore è **Nothing**, l'attività verrà registrata nella cartella radice dell'attività e il nome dell'attività sarà un valore GUID creato dal Utilità di pianificazione servizio.

Un nome di attività non può iniziare o terminare con uno spazio. Non è possibile usare il carattere '.' per specificare la cartella attività corrente e '..' Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

</dd> <dt>

*xmlText* \[ Pollici\]
</dt> <dd>

Descrizione in formato XML dell'attività.

Negli argomenti seguenti sono contenute attività definite tramite XML.

-   [Esempio di trigger temporale (XML)](time-trigger-example--xml-.md)
-   [Esempio di trigger di evento (XML)](/previous-versions//aa446889(v=vs.85))
-   [Esempio di trigger giornaliero (XML)](daily-trigger-example--xml-.md)
-   [Esempio di trigger di registrazione (XML)](registration-trigger-example--xml-.md)
-   [Esempio di trigger settimanale (XML)](weekly-trigger-example--xml-.md)
-   [Esempio di trigger Logon (XML)](logon-trigger-example--xml-.md)
-   [Esempio di trigger di avvio (XML)](boot-trigger-example--xml-.md)

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Costante [**TASK \_ CREATION.**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)



| Valore                                                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <dt>**ATTIVITÀ \_ CONVALIDA \_ SOLO**</dt> <dt>0X1</dt> </dl>                                                | Il Utilità di pianificazione controlla la sintassi del codice XML che descrive l'attività, ma non registra l'attività. Questa costante non può essere combinata con i **valori TASK \_ CREATE,** **TASK \_ UPDATE** o **TASK CREATE OR \_ \_ \_ UPDATE.**<br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <dt>**ATTIVITÀ \_ CREATE**</dt> <dt>0x2</dt> </dl>                                                                      | Il Utilità di pianificazione registra l'attività come nuova attività.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <dt>**ATTIVITÀ \_ Aggiornamento**</dt> <dt>0x4</dt> </dl>                                                                      | Il Utilità di pianificazione registra l'attività come versione aggiornata di un'attività esistente. Quando viene aggiornata un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.<br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <dt>**ATTIVITÀ \_ CREATE \_ OR \_ UPDATE**</dt> <dt>0x6</dt> </dl>                                      | Il Utilità di pianificazione registra l'attività come nuova attività o come versione aggiornata se l'attività esiste già. Equivale a TASK \_ CREATE \| TASK \_ UPDATE.<br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <dt>**ATTIVITÀ \_ DISABLE**</dt> <dt>0x8</dt> </dl>                                                                   | Il Utilità di pianificazione disabilita l'attività esistente.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <dt>**ATTIVITÀ \_ DONT \_ ADD \_ PRINCIPAL \_ ACE**</dt> <dt>0x10</dt> </dl>                  | Al Utilità di pianificazione viene impedito di aggiungere la voce di controllo di accesso (ACE) allow per l'entità di contesto. Quando la funzione **TaskFolder.RegisterTask** viene chiamata con questo flag per aggiornare un'attività, il servizio Utilità di pianificazione non aggiunge la ACE per la nuova entità di contesto e non rimuove la ACE dall'entità di contesto precedente.<br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <dt>**ATTIVITÀ \_ IGNORARE \_ I \_ TRIGGER DI**</dt> REGISTRAZIONE <dt>0X20</dt> </dl> | Il Utilità di pianificazione crea l'attività, ma ignora i trigger di registrazione nell'attività. Ignorando i trigger di registrazione, l'attività non verrà eseguita quando viene registrata, a meno che non venga eseguita al momento della registrazione da un trigger basato sul tempo.<br/>                                                                                               |



 

</dd> <dt>

*userId* \[ Pollici\]
</dt> <dd>

Credenziali utente utilizzate per registrare l'attività.

> [!Note]  
> Se l'attività è definita come attività Utilità di pianificazione 1.0, non usare un nome di gruppo (anziché un nome utente specifico) in questo parametro userId. Un'attività viene definita come attività Utilità di pianificazione 1.0 quando l'attributo version dell'elemento Task nel codice XML dell'attività è impostato su 1.1.

 

</dd> <dt>

*password* \[ Pollici\]
</dt> <dd>

Password per l'ID utente usato per registrare l'attività. Quando si utilizza il tipo di accesso TASK LOGON SERVICE ACCOUNT, la password deve essere un valore VARIANT vuoto, ad esempio \_ \_ \_ **VT \_ NULL** o **VT \_ EMPTY.** 

</dd> <dt>

*logonType* \[ Pollici\]
</dt> <dd>

Definisce la tecnica di accesso usata per eseguire l'attività registrata.



| Valore                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**ATTIVITÀ \_ LOGON \_ NONE**</dt> <dt>0</dt> </dl>                                                                               | Il metodo logon non è specificato. Utilizzato per le credenziali non NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**ATTIVITÀ \_ PASSWORD \_ DI ACCESSO**</dt> <dt>1</dt> </dl>                                                                   | Usare una password per l'accesso dell'utente. La password deve essere specificata al momento della registrazione.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**ATTIVITÀ \_ LOGON \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Usare un token interattivo esistente per eseguire un'attività. L'utente deve accedere usando un servizio per l'accesso utente (S4U). Quando si usa un accesso S4U, non viene archiviata alcuna password dal sistema e non è possibile accedere alla rete o ai file crittografati.<br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**ATTIVITÀ \_ LOGON \_ INTERACTIVE \_ TOKEN**</dt> <dt>3</dt> </dl>                                       | L'utente deve essere già connesso. L'attività verrà eseguita solo in una sessione interattiva esistente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**ATTIVITÀ \_ LOGON \_ GROUP**</dt> <dt>4</dt> </dl>                                                                            | Attivazione del gruppo. Il **campo groupId** specifica il gruppo.<br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**ATTIVITÀ \_ ACCOUNT \_ DEL SERVIZIO DI \_ ACCESSO**</dt> <dt>5</dt> </dl>                                             | Indica che un account di sistema locale, servizio locale o servizio di rete viene utilizzato come contesto di sicurezza per eseguire l'attività.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**ATTIVITÀ \_ TOKEN \_ INTERATTIVO DI ACCESSO O \_ \_ \_ PASSWORD**</dt> <dt>6</dt> </dl> | Usare prima di tutto il token interattivo. Se l'utente non è connesso (non è disponibile alcun token interattivo), viene usata la password. La password deve essere specificata quando viene registrata un'attività. Questo flag non è consigliato per le nuove attività perché è meno affidabile di TASK \_ LOGON \_ PASSWORD.<br/> |



 

</dd> <dt>

*sddl* \[ in, facoltativo\]
</dt> <dd>

Descrittore di sicurezza associato all'attività registrata. È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per un'attività per consentire o negare a determinati utenti e gruppi l'accesso a un'attività.

> [!Note]  
> Se all'account di sistema locale viene negato l'accesso a un'attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.

 

</dd> <dt>

*Attività pTask* \[ Cambio\]
</dt> <dd>

Oggetto [**RegisteredTask**](registeredtask.md) che rappresenta la nuova attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività ha un tipo di accesso interattivo. Per impostare il tipo di accesso all'attività su interattivo, specificare 3 (**TASK \_ LOGON INTERACTIVE \_ \_ TOKEN**) o 4 (**TASK LOGON \_ \_ GROUP**) nella proprietà [**LogonType**](principal-logontype.md) dell'entità attività o nel *parametro logonType* di **TaskFolder.RegisterTask** o [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

Solo un membro del gruppo Administrators può creare un'attività con un trigger di avvio.

È possibile registrare correttamente un'attività con un gruppo specificato nel parametro *userId* e 3 (**TASK LOGON INTERACTIVE \_ \_ \_ TOKEN**) specificati nel parametro *logonType* di **TaskFolder.RegisterTask** o [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), ma l'attività non verrà eseguita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**Cartella attività**](taskfolder.md)
</dt> </dl>

 

