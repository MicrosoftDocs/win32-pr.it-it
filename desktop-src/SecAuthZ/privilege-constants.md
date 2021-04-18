---
Description: I privilegi determinano il tipo di operazioni di sistema che un account utente può eseguire. Un amministratore assegna privilegi agli account utente e di gruppo. I privilegi di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Costanti Privilege (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 801eccb2f42ccf27b45bc5628a32cee3de994bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331784"
---
# <a name="privilege-constants-authorization"></a>Costanti Privilege (autorizzazione)

I privilegi determinano il tipo di operazioni di sistema che un account utente può eseguire. Un amministratore assegna privilegi agli account utente e di gruppo. I privilegi di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.

Le funzioni che ottengono e regolano i privilegi in un [*token di accesso*](/windows/desktop/SecGloss/a-gly) usano il tipo [*identificatore univoco locale*](/windows/desktop/SecGloss/l-gly) (LUID) per identificare i privilegi. Utilizzare la funzione [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) per determinare il [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) nel sistema locale che corrisponde a una costante Privilege. Usare la funzione [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) per convertire un **LUID** nella costante di stringa corrispondente.

Il sistema operativo rappresenta un privilegio utilizzando la stringa che segue "diritto utente" nella colonna Descrizione della tabella seguente. Il sistema operativo Visualizza le stringhe corrette per l'utente nella colonna **criteri** del nodo **assegnazione diritti utente** dello snap-in impostazioni di protezione locali di Microsoft Management Console (MMC).

## <a name="example"></a>Esempio

```cpp
BOOL EnablePrivilege()
{
    LUID PrivilegeRequired ;
    BOOL bRes = FALSE;
  
    bRes = LookupPrivilegeValue(NULL, SE_DEBUG_NAME, &PrivilegeRequired);

    // ...

    return bRes;
}
```
Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) in GitHub.

## <a name="constants"></a>Costanti


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_ASSIGNPRIMARYTOKEN_NAME ( &quot; SeAssignPrimaryTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per assegnare il <a href="/windows/desktop/SecGloss/p-gly"><em>token primario</em></a> di un processo. <br/> Diritto utente: sostituire un token a livello di processo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong></strong></dt> <dt>Testo se_audit_name ( &quot; SeAuditPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per generare le voci del log di controllo. Assegnare questo privilegio ai server protetti. <br/> Diritto utente: genera controlli di sicurezza.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_BACKUP_NAME ( &quot; SeBackupPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per eseguire operazioni di backup. Questo privilegio fa in modo che il sistema conceda tutto il controllo di accesso in lettura a qualsiasi file, indipendentemente dall' <a href="/windows/desktop/SecGloss/a-gly"><em>elenco di controllo di accesso</em></a> (ACL) specificato per il file. Qualsiasi richiesta di accesso diversa da Read viene comunque valutata con l'ACL. Questo privilegio è richiesto dalle funzioni <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a> e <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>. Se questo privilegio viene mantenuto, vengono concessi i diritti di accesso seguenti:<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Diritto utente: backup di file e directory.<br/>Se il file si trova in un'unità rimovibile ed è abilitata la funzionalità di controllo dell'archiviazione rimovibile, è necessario che il SE_SECURITY_NAME disponga di ACCESS_SYSTEM_SECURITY.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_CHANGE_NOTIFY_NAME ( &quot; SeChangeNotifyPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessaria per ricevere notifiche delle modifiche apportate ai file o alle directory. Questo privilegio fa anche in modo che il sistema ignori tutti i controlli di accesso attraversati. È abilitata per impostazione predefinita per tutti gli utenti. <br/> Right utente: ignorare il controllo incrociato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_CREATE_GLOBAL_NAME ( &quot; SeCreateGlobalPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare oggetti mapping di file denominati nello spazio dei nomi globale durante le sessioni di Servizi terminal. Questo privilegio è abilitato per impostazione predefinita per gli amministratori, i servizi e l'account di sistema locale.<br/> Diritto utente: creare oggetti globali.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_CREATE_PAGEFILE_NAME ( &quot; SeCreatePagefilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare un file di paging. <br/> Diritto utente: creare un pagefile.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_CREATE_PERMANENT_NAME ( &quot; SeCreatePermanentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare un oggetto permanente. <br/> Diritto utente: creare oggetti condivisi permanenti.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_CREATE_SYMBOLIC_LINK_NAME ( &quot; SeCreateSymbolicLinkPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare un collegamento simbolico.<br/> Diritto utente: creare collegamenti simbolici.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_CREATE_TOKEN_NAME ( &quot; SeCreateTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per creare un token primario. <br/> Diritto utente: creare un oggetto token.<br/> Non è possibile aggiungere questo privilegio a un account utente con il &quot; criterio creare un oggetto token &quot; . Non è inoltre possibile aggiungere questo privilegio a un processo di proprietà usando le API di Windows. <strong>Windows Server 2003 e Windows XP con SP1 e versioni precedenti:</strong> Le API di Windows possono aggiungere questo privilegio a un processo di proprietà.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_DEBUG_NAME ( &quot; SeDebugPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per eseguire il debug e la modifica della memoria di un processo di proprietà di un altro account. <br/> Diritto utente: debug di programmi.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME ( &quot; SeDelegateSessionUserImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per ottenere un token di rappresentazione per un altro utente nella stessa sessione. <br/> Diritto utente: rappresentare altri utenti.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_ENABLE_DELEGATION_NAME ( &quot; SeEnableDelegationPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per contrassegnare gli account utente e computer come trusted per la delega.<br/> Diritto utente: consentire l'attendibilità degli account computer e utente per la delega.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_IMPERSONATE_NAME ( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per la rappresentazione.<br/> Diritto utente: rappresenta un client dopo l'autenticazione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_INC_BASE_PRIORITY_NAME ( &quot; SeIncreaseBasePriorityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per aumentare la priorità di base di un processo. <br/> Diritto utente: aumento della priorità di pianificazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_INCREASE_QUOTA_NAME ( &quot; SeIncreaseQuotaPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per aumentare la quota assegnata a un processo. <br/> Diritto utente: modificare le quote di memoria per un processo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_INC_WORKING_SET_NAME ( &quot; SeIncreaseWorkingSetPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per allocare ulteriore memoria per le applicazioni eseguite nel contesto degli utenti.<br/> Diritto utente: aumentare un processo working set.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_LOAD_DRIVER_NAME ( &quot; SeLoadDriverPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per caricare o scaricare un driver di dispositivo. <br/> Diritto utente: caricare e scaricare i driver di dispositivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_LOCK_MEMORY_NAME ( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per bloccare le pagine fisiche in memoria. <br/> Diritto utente: blocco di pagine in memoria.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_MACHINE_ACCOUNT_NAME ( &quot; SeMachineAccountPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per creare un account computer. <br/> Diritto utente: aggiungere le workstation al dominio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_MANAGE_VOLUME_NAME ( &quot; SeManageVolumePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per abilitare i privilegi di gestione del volume. <br/> Diritto utente: gestire i file in un volume.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_PROF_SINGLE_PROCESS_NAME ( &quot; SeProfileSingleProcessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per raccogliere le informazioni di profilatura per un singolo processo. <br/> Diritto utente: profilo singolo processo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_RELABEL_NAME ( &quot; SeRelabelPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per modificare il livello di integrità obbligatorio di un oggetto.<br/> Diritto utente: modificare l'etichetta di un oggetto.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_REMOTE_SHUTDOWN_NAME ( &quot; SeRemoteShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per arrestare un sistema utilizzando una richiesta di rete. <br/> Diritto utente: forza l'arresto da un sistema remoto.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_RESTORE_NAME ( &quot; SeRestorePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per eseguire operazioni di ripristino. Questo privilegio fa in modo che il sistema conceda tutti i controlli di accesso in scrittura a qualsiasi file, indipendentemente dall'ACL specificato per il file. Qualsiasi richiesta di accesso diversa da Write viene comunque valutata con l'ACL. Questo privilegio consente inoltre di impostare qualsiasi SID utente o gruppo valido come proprietario di un file. Questo privilegio è richiesto dalla funzione <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegLoadKey</strong></a> . Se questo privilegio viene mantenuto, vengono concessi i diritti di accesso seguenti:<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>DELETE</li>
</ul>
Diritto utente: ripristino di file e directory.<br/>Se il file si trova in un'unità rimovibile ed è abilitata la funzionalità di controllo dell'archiviazione rimovibile, è necessario che il SE_SECURITY_NAME disponga di ACCESS_SYSTEM_SECURITY.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_SECURITY_NAME ( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per eseguire numerose funzioni correlate alla sicurezza, ad esempio il controllo e la visualizzazione dei messaggi di controllo. Questo privilegio identifica il proprio titolare come operatore di sicurezza. <br/> Diritto utente: gestire il registro di controllo e di sicurezza.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_SHUTDOWN_NAME ( &quot; SeShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per arrestare un sistema locale. <br/> Diritto utente: arrestare il sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_SYNC_AGENT_NAME ( &quot; SeSyncAgentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per il controller di dominio per l'utilizzo dei servizi di sincronizzazione directory <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight Directory Access Protocol</em></a> . Questo privilegio consente al titolare di leggere tutti gli oggetti e le proprietà nella directory, indipendentemente dalla protezione degli oggetti e delle proprietà. Per impostazione predefinita, viene assegnato agli account Administrator e LocalSystem nei controller di dominio. <br/> Diritto utente: sincronizzare i dati del servizio directory.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_SYSTEM_ENVIRONMENT_NAME ( &quot; SeSystemEnvironmentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per modificare la RAM non volatile dei sistemi che usano questo tipo di memoria per archiviare le informazioni di configurazione. <br/> Diritto utente: modificare i valori dell'ambiente del firmware.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_SYSTEM_PROFILE_NAME ( &quot; SeSystemProfilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per raccogliere le informazioni di profilatura per l'intero sistema. <br/> Diritto utente: profilare le prestazioni del sistema.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_SYSTEMTIME_NAME ( &quot; SeSystemTimePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per modificare l'ora di sistema. <br/> Diritto utente: modificare l'ora di sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_TAKE_OWNERSHIP_NAME ( &quot; SeTakeOwnershipPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per assumere la proprietà di un oggetto senza che venga concesso l'accesso discrezionale. Questo privilegio consente l'impostazione del valore proprietario solo per i valori che il titolare può assegnare legittimamente come proprietario di un oggetto. <br/> Diritto utente: assumere la proprietà di file o di altri oggetti.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_TCB_NAME ( &quot; SeTcbPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Questo privilegio identifica il proprio titolare come parte della base del computer attendibile. A alcuni sottosistemi protetti attendibili viene concesso questo privilegio. <br/> Diritto utente: agire come parte del sistema operativo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_TIME_ZONE_NAME ( &quot; SeTimeZonePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per modificare il fuso orario associato al clock interno del computer.<br/> Diritto utente: modificare il fuso orario.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_TRUSTED_CREDMAN_ACCESS_NAME ( &quot; SeTrustedCredManAccessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per accedere a gestione credenziali come chiamante attendibile.<br/> Diritto utente: accedere a gestione credenziali come chiamante attendibile.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_UNDOCK_NAME ( &quot; SeUndockPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per disancorare un portatile.<br/> Diritto utente: rimuovere il computer dalla stazione di ancoraggio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong></strong></dt> <dt>Testo SE_UNSOLICITED_INPUT_NAME ( &quot; SeUnsolicitedInputPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per leggere l'input non richiesto da un dispositivo <a href="/windows/desktop/SecGloss/t-gly"><em>Terminal</em></a> .<br/> Diritto utente: non applicabile.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Le costanti di privilegio sono definite come stringhe in Winnt. h. Ad esempio, la \_ costante del nome del controllo se \_ è definita come "SeAuditPrivilege".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Privilegi](privileges.md)
</dt> </dl>

