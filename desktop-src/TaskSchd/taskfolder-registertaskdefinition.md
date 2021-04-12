---
title: TaskFolder. RegisterTaskDefinition, metodo
description: Per lo scripting, registra (Crea) un'attività in una posizione specificata usando l'oggetto TaskDefinition per definire un'attività.
ms.assetid: 198c8848-c89d-4883-b111-4ac0b009b7b3
keywords:
- Utilità di pianificazione del metodo RegisterTaskDefinition
- Metodo RegisterTaskDefinition Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo RegisterTaskDefinition
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616d917dd0bb5516fdf8d474d293ba370775c786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400753"
---
# <a name="taskfolderregistertaskdefinition-method"></a>TaskFolder. RegisterTaskDefinition, metodo

Per lo scripting, registra (Crea) un'attività in una posizione specificata usando l'oggetto [**TaskDefinition**](taskdefinition.md) per definire un'attività.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.RegisterTaskDefinition( _
  ByVal path, _
  ByVal definition, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef task _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*percorso* \[ in\]
</dt> <dd>

Nome dell'attività. Se questo valore è **Nothing**, l'attività verrà registrata nella cartella radice dell'attività e il nome dell'attività sarà un valore GUID creato dal servizio Utilità di pianificazione.

Un nome di attività non può iniziare o terminare con uno spazio. Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .' non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.

</dd> <dt>

*definizione* \[ di in\]
</dt> <dd>

Definizione dell'attività registrata.

</dd> <dt>

*flag* \[ in\]
</dt> <dd>

Costante [**di \_ creazione**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) di un'attività.



| Valore                                                                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <dt>**Attività \_ CONVALIDA \_ solo**</dt> <dt>0x1</dt> </dl>                                                | Il Utilità di pianificazione controlla la sintassi del codice XML che descrive l'attività ma non registra l'attività. Questa costante non può essere combinata con i valori di **\_ creazione**, **\_ aggiornamento** attività **o \_ creazione \_ o \_ aggiornamento** dell'attività.<br/>                                                                                                                            |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <dt>**Attività \_ Crea**</dt> <dt>0x2</dt> </dl>                                                                      | Il Utilità di pianificazione registra l'attività come nuova attività.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <dt>**Attività \_ AGGIORNARE**</dt> <dt>0x4</dt> </dl>                                                                      | Il Utilità di pianificazione registra l'attività come versione aggiornata di un'attività esistente. Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.<br/>                                                                                                                                                                      |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <dt>**Attività \_ Crea \_ o \_ Aggiorna**</dt> <dt>0x6</dt> </dl>                                      | Il Utilità di pianificazione registra l'attività come nuova attività o come versione aggiornata se l'attività esiste già. Equivale a attività di creazione attività di \_ \| \_ aggiornamento.<br/>                                                                                                                                                                                              |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <dt>**Attività \_ DISABILITARE**</dt> <dt>0x8</dt> </dl>                                                                   | Il Utilità di pianificazione Disabilita l'attività esistente.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <dt>**Attività \_ Non \_ aggiungere \_ 0x10 \_ ACE principale**</dt> <dt></dt> </dl>                  | Al Utilità di pianificazione viene impedito di aggiungere la voce di controllo di accesso (ACE) Consenti per l'entità di contesto. Quando viene chiamata la funzione **TaskFolder. RegisterTaskDefinition** con questo flag per aggiornare un'attività, il servizio Utilità di pianificazione non aggiunge la voce ACE per la nuova entità di contesto e non rimuove la voce ACE dall'entità di contesto precedente.<br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <dt>**Attività \_ IGNORARE \_ i \_ trigger di registrazione**</dt> <dt>0x20</dt> </dl> | Il Utilità di pianificazione crea l'attività, ma ignora i trigger di registrazione nell'attività. Ignorando i trigger di registrazione, l'attività non verrà eseguita quando viene registrata, a meno che un trigger basato sul tempo non ne provochi l'esecuzione alla registrazione.<br/>                                                                                                         |



 

</dd> <dt>

*ID utente* \[ in\]
</dt> <dd>

Le credenziali utente utilizzate per registrare l'attività. Se presenti, queste credenziali hanno la priorità sulle credenziali specificate nell'oggetto definizione di attività a cui punta il parametro della *definizione* .

> [!Note]  
> Se l'attività è definita come un'attività Utilità di pianificazione 1,0, non usare il nome di un gruppo (anziché un nome utente specifico) in questo parametro userId. Un'attività è definita come un'attività Utilità di pianificazione 1,0 quando la proprietà [**compatibilità**](tasksettings-compatibility.md) è impostata su 1 nelle impostazioni dell'attività.

 

</dd> <dt>

*password* \[ di in\]
</dt> <dd>

Password per l'ID utente usato per registrare l'attività. Quando \_ viene usato il tipo di accesso dell'account del servizio di accesso all'attività \_ \_ , la password deve essere un valore **Variant** vuoto, ad esempio **VT \_ null** o **VT \_ vuoto**.

</dd> <dt>

*LogonType* \[ in\]
</dt> <dd>

Definisce quale tecnica di accesso viene utilizzata per eseguire l'attività registrata.



| Valore                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Attività \_ \_Nessun accesso**</dt> <dt>0</dt> </dl>                                                                               | Metodo di accesso non specificato. Utilizzato per le credenziali non NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Attività \_ \_Password di accesso**</dt> <dt>1</dt> </dl>                                                                   | Usare una password per la registrazione dell'utente. La password deve essere fornita in fase di registrazione.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Attività \_ \_S4U di accesso**</dt> <dt>2</dt> </dl>                                                                                  | Usare un token interattivo esistente per eseguire un'attività. L'utente deve accedere utilizzando un servizio per l'accesso utente (S4U). Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.<br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Attività \_ \_ \_ Token interattivo di accesso**</dt> <dt>3</dt> </dl>                                       | L'utente deve essere già connesso. L'attività verrà eseguita solo in una sessione interattiva esistente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Attività \_ \_Gruppo di accesso**</dt> <dt>4</dt> </dl>                                                                            | Attivazione del gruppo. Il campo **GroupID** specifica il gruppo.<br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Attività \_ \_ \_ Account del servizio di accesso**</dt> <dt>5</dt> </dl>                                             | Indica che un account di sistema locale, servizio locale o servizio di rete viene utilizzato come contesto di sicurezza per eseguire l'attività.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Attività \_ \_Token interattivo di accesso \_ \_ o \_ password**</dt> <dt>6</dt> </dl> | Usare prima il token interattivo. Se l'utente non è connesso (non è disponibile alcun token interattivo), viene utilizzata la password. Quando un'attività è registrata, è necessario specificare la password. Questo flag non è consigliato per le nuove attività perché è meno affidabile rispetto alla \_ password di accesso dell'attività \_ .<br/> |



 

</dd> <dt>

*SDDL* \[ in, facoltativo\]
</dt> <dd>

Descrittore di sicurezza associato all'attività registrata. È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per un'attività per consentire o negare a determinati utenti e gruppi l'accesso a un'attività.

> [!Note]  
> Se all'account di sistema locale viene negato l'accesso a un'attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.

 

</dd> <dt>

*attività* \[ out\]
</dt> <dd>

Oggetto [**RegisteredTask**](registeredtask.md) che rappresenta la nuova attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo. Per impostare il tipo di accesso dell'attività su interattivo, specificare 3 (**\_ \_ \_ token interattivo accesso attività**) o 4 (**\_ \_ gruppo di accesso attività**) nella proprietà [**LogonType**](principal-logontype.md) dell'entità attività oppure nel parametro *LogonType* di [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o **TaskFolder. RegisterTaskDefinition**.

Solo un membro del gruppo Administrators può creare un'attività con un trigger di avvio.

È possibile registrare correttamente un'attività con un gruppo specificato nel parametro *userid* e 3 (**\_ \_ \_ token interattivo accesso attività**) specificato nel parametro *LogonType* di [**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o **TaskFolder. RegisterTaskDefinition**, ma l'attività non viene eseguita.

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
</dt> <dt>

[**TaskFolder**](taskfolder.md)
</dt> </dl>

 

 





