---
Description: I privilegi determinano il tipo di operazioni di sistema che un account utente può eseguire. Un amministratore assegna privilegi agli account utente e di gruppo. I privilegi di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Costanti di privilegio (Winnt.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: cd33cf947f6425d717b4d41524fe7cf0fed14cef
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327156"
---
# <a name="privilege-constants-authorization"></a>Costanti di privilegio (autorizzazione)

I privilegi determinano il tipo di operazioni di sistema che un account utente può eseguire. Un amministratore assegna privilegi agli account utente e di gruppo. I privilegi di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.

Le funzioni che ottengono e modificano i privilegi in un token di [*accesso*](/windows/desktop/SecGloss/a-gly) usano il tipo LUID [*(Local Unique Identifier)*](/windows/desktop/SecGloss/l-gly) per identificare i privilegi. Usare la [**funzione LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) per determinare [**il LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) nel sistema locale che corrisponde a una costante di privilegi. Usare la [**funzione LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) per convertire un **LUID** nella costante stringa corrispondente.

Il sistema operativo rappresenta un privilegio usando la stringa che segue "Diritto utente" nella colonna Descrizione della tabella seguente. Il sistema operativo visualizza le  stringhe dei  diritti utente nella colonna Criteri del nodo Assegnazione diritti utente dello snap-in Impostazioni di sicurezza locali Microsoft Management Console (MMC).

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
Esempio di [esempi classici di Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) in GitHub.

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
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt> <dt>TEXT( &quot; SeAssignPrimaryTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per <a href="/windows/desktop/SecGloss/p-gly"><em>assegnare il token primario</em></a> di un processo. <br/> Diritto utente: sostituire un token a livello di processo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong>SE_AUDIT_NAME</strong></dt> <dt>TEXT( &quot; SeAuditPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per generare le voci del log di controllo. Concedere questo privilegio ai server protetti. <br/> Diritto utente: generare controlli di sicurezza.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong>SE_BACKUP_NAME</strong></dt> <dt>TEXT( &quot; SeBackupPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per eseguire operazioni di backup. Questo privilegio fa sì che il sistema concedi <a href="/windows/desktop/SecGloss/a-gly"><em></em></a> tutto il controllo di accesso in lettura a qualsiasi file, indipendentemente dall'elenco di controllo di accesso (ACL) specificato per il file. Qualsiasi richiesta di accesso diversa da read viene comunque valutata con l'ACL. Questo privilegio è richiesto dalle <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>funzioni RegSaveKey</strong></a> <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>e RegSaveKeyEx.</strong></a> Se si dispone di questo privilegio, vengono concessi i diritti di accesso seguenti:<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Diritto utente: eseguire il backup di file e directory.<br/>Se il file si trova in un'unità rimovibile ed è abilitata l'opzione "Controlla archivi rimovibili", il SE_SECURITY_NAME deve avere ACCESS_SYSTEM_SECURITY.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt> <dt>TEXT( &quot; SeChangeNotifyPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per ricevere notifiche relative alle modifiche apportate a file o directory. Questo privilegio fa inoltre in modo che il sistema ignorare tutti i controlli di accesso di attraversamento. È abilitata per impostazione predefinita per tutti gli utenti. <br/> Diritto utente: ignorare il controllo di attraversamento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt> <dt>TEXT( &quot; SeCreateGlobalPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per creare oggetti mapping di file denominati nello spazio dei nomi globale durante le sessioni di Servizi terminal. Questo privilegio è abilitato per impostazione predefinita per gli amministratori, i servizi e l'account di sistema locale.<br/> Diritto utente: creare oggetti globali.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt> <dt>TEXT( &quot; SeCreatePagefilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare un file di paging. <br/> Diritto utente: creare un file di paging.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt> <dt>TEXT( &quot; SeCreatePermanentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare un oggetto permanente. <br/> Diritto utente: creare oggetti condivisi permanenti.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt> <dt>TEXT( &quot; SeCreateSymbolicLinkPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare un collegamento simbolico.<br/> Diritto utente: creare collegamenti simbolici.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong>SE_CREATE_TOKEN_NAME</strong></dt> <dt>TEXT( &quot; SeCreateTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare un token primario. <br/> Diritto utente: creare un oggetto token.<br/> Non è possibile aggiungere questo privilegio a un account utente con &quot; i criteri Creare un oggetto &quot; token. Inoltre, non è possibile aggiungere questo privilegio a un processo di proprietà usando le API di Windows. <strong>Windows Server 2003 e Windows XP con SP1 e versioni precedenti:</strong> Le API di Windows possono aggiungere questo privilegio a un processo di proprietà.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong>SE_DEBUG_NAME</strong></dt> <dt>TEXT( &quot; SeDebugPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per eseguire il debug e modificare la memoria di un processo di proprietà di un altro account. <br/> Diritto utente: Eseguire il debug dei programmi.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt> <dt>TEXT( &quot; SeDelegateSessionUserImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per ottenere un token di rappresentazione per un altro utente nella stessa sessione. <br/> Diritto utente: rappresenta altri utenti.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt> <dt>TEXT( &quot; SeEnableDelegationPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per contrassegnare gli account utente e computer come trusted per la delega.<br/> Diritto utente: abilitare gli account computer e utente come attendibili per la delega.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong>SE_IMPERSONATE_NAME</strong></dt> <dt>TEXT( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per la rappresentazione.<br/> Diritto utente: rappresenta un client dopo l'autenticazione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseBasePriorityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per aumentare la priorità di base di un processo. <br/> Diritto utente: aumentare la priorità di pianificazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseQuotaPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per aumentare la quota assegnata a un processo. <br/> Diritto utente: regolare le quote di memoria per un processo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong>SE_INC_WORKING_SET_NAME</strong></dt> <dt>TEXT( &quot; SeIncreaseWorkingSetPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per allocare più memoria per le applicazioni eseguite nel contesto degli utenti.<br/> Diritto utente: aumentare il numero di processi working set.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong>SE_LOAD_DRIVER_NAME</strong></dt> <dt>TEXT( &quot; SeLoadDriverPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per caricare o scaricare un driver di dispositivo. <br/> Diritto utente: caricare e scaricare i driver di dispositivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong>SE_LOCK_MEMORY_NAME</strong></dt> <dt>TEXT( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per bloccare le pagine fisiche in memoria. <br/> Diritto utente: bloccare le pagine in memoria.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt> <dt>TEXT( &quot; SeMachineAccountPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per creare un account computer. <br/> Diritto utente: aggiungere workstation al dominio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt> <dt>TEXT( &quot; SeManageVolumePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per abilitare i privilegi di gestione dei volumi. <br/> Diritto utente: gestire i file in un volume.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt> <dt>TEXT( &quot; SeProfileSingleProcessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per raccogliere informazioni di profilatura per un singolo processo. <br/> Diritto utente: profilare un singolo processo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong>SE_RELABEL_NAME</strong></dt> <dt>TEXT( &quot; SeRelabelPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per modificare il livello di integrità obbligatorio di un oggetto.<br/> Diritto utente: modificare l'etichetta di un oggetto.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt> <dt>TEXT( &quot; SeRemoteShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per arrestare un sistema usando una richiesta di rete. <br/> Diritto utente: forzare l'arresto da un sistema remoto.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong>SE_RESTORE_NAME</strong></dt> <dt>TEXT( &quot; SeRestorePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per eseguire operazioni di ripristino. Questo privilegio fa sì che il sistema concedi tutto il controllo di accesso in scrittura a qualsiasi file, indipendentemente dall'ACL specificato per il file. Qualsiasi richiesta di accesso diversa dalla scrittura viene comunque valutata con l'ACL. Inoltre, questo privilegio consente di impostare qualsiasi SID utente o gruppo valido come proprietario di un file. Questo privilegio è richiesto dalla <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>funzione RegLoadKey.</strong></a> Se si dispone di questo privilegio, vengono concessi i diritti di accesso seguenti:<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>DELETE</li>
</ul>
Diritto utente: ripristinare file e directory.<br/>Se il file si trova in un'unità rimovibile ed è abilitata l'opzione "Controlla archivi rimovibili", il SE_SECURITY_NAME deve avere ACCESS_SYSTEM_SECURITY.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong>SE_SECURITY_NAME</strong></dt> <dt>TEXT( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per eseguire una serie di funzioni correlate alla sicurezza, ad esempio il controllo e la visualizzazione dei messaggi di controllo. Questo privilegio identifica il titolare come operatore di sicurezza. <br/> Diritto utente: gestire il log di controllo e di sicurezza.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong>SE_SHUTDOWN_NAME</strong></dt> <dt>TEXT( &quot; SeShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per arrestare un sistema locale. <br/> Diritto utente: arrestare il sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong>SE_SYNC_AGENT_NAME</strong></dt> <dt>TEXT( &quot; SeSyncAgentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per l'utilizzo dei servizi di sincronizzazione <a href="/windows/desktop/SecGloss/l-gly"><em>Lightweight Directory Access Protocol</em></a> directory da parte di un controller di dominio. Questo privilegio consente al titolare di leggere tutti gli oggetti e le proprietà nella directory, indipendentemente dalla protezione per gli oggetti e le proprietà. Per impostazione predefinita, viene assegnato agli account Administrator e LocalSystem nei controller di dominio. <br/> Diritto utente: sincronizzare i dati del servizio directory.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong>SE_SYSTEM_ENVIRONMENT_NAME</strong></dt> <dt>TEXT( &quot; SeSystemEnvironmentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per modificare la RAM non volatile dei sistemi che usano questo tipo di memoria per archiviare le informazioni di configurazione. <br/> Diritto utente: modificare i valori dell'ambiente del firmware.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong>SE_SYSTEM_PROFILE_NAME</strong></dt> <dt>TEXT( &quot; SeSystemProfilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per raccogliere informazioni di profilatura per l'intero sistema. <br/> Diritto utente: profilare le prestazioni del sistema.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong>SE_SYSTEMTIME_NAME</strong></dt> <dt>TEXT( &quot; SeSystemtimePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per modificare l'ora di sistema. <br/> Diritto utente: modificare l'ora di sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong>SE_TAKE_OWNERSHIP_NAME</strong></dt> <dt>TEXT( &quot; SeTakeOwnershipPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per assumere la proprietà di un oggetto senza concedere l'accesso discrezionale. Questo privilegio consente di impostare il valore del proprietario solo su tali valori che il titolare può assegnare legittimamente come proprietario di un oggetto. <br/> Diritto utente: assumere la proprietà di file o altri oggetti.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong>SE_TCB_NAME</strong></dt> <dt>TEXT( &quot; SeTcbPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Questo privilegio identifica il titolare come parte della base di computer attendibili. Ad alcuni sottosistemi protetti attendibili viene concesso questo privilegio. <br/> Diritto utente: funge da parte del sistema operativo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong>SE_TIME_ZONE_NAME</strong></dt> <dt>TEXT( &quot; SeTimeZonePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per regolare il fuso orario associato all'orologio interno del computer.<br/> Diritto utente: modificare il fuso orario.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong>SE_TRUSTED_CREDMAN_ACCESS_NAME</strong></dt> <dt>TEXT( &quot; SeTrustedCredManAccessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per accedere Gestione credenziali come chiamante attendibile.<br/> Diritto utente: accesso Gestione credenziali come chiamante attendibile.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong>SE_UNDOCK_NAME</strong></dt> <dt>TEXT( &quot; SeUndockPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessario per disanciare un portatile.<br/> Diritto utente: rimuovere il computer dall'alloggiamento di espansione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong>SE_UNSOLICITED_INPUT_NAME</strong></dt> <dt>TEXT( &quot; SeUnsolicitedInputPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Obbligatorio per leggere l'input non richiesto da un <a href="/windows/desktop/SecGloss/t-gly"><em>dispositivo terminale.</em></a><br/> Diritto utente: non applicabile.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Le costanti di privilegio sono definite come stringhe in Winnt.h. Ad esempio, la costante SE \_ AUDIT NAME è definita come \_ "SeAuditPrivilege".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Privilegi](privileges.md)
</dt> </dl>

