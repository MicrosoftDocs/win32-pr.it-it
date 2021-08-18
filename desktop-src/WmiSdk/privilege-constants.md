---
description: Il parametro strPrivilege del metodo SWbemPrivilegeSet.AddAsString e il parametro iPrivilege per SWbemPrivilegeSet.Add richiedono stringhe di privilegi da WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Costanti dei privilegi (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 38d104c99885d4328ce8b12413e91607655ab1e260a61b511e3ea4a600b80b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131023"
---
# <a name="privilege-constants"></a>Costanti dei privilegi

Il *parametro strPrivilege* del metodo [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) e il parametro *iPrivilege* per [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) richiedono stringhe di privilegi [da WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). Per altre informazioni su come usare le costanti dei privilegi, vedere [Esecuzione di operazioni con privilegi](executing-privileged-operations.md).

Le costanti seguenti sono definite in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). L'elenco seguente include le costanti equivalenti per C++ e le stringhe per lo scripting. Per formare il nome breve dello scripting, rimuovere "Se" e "Privilege" dal nome della costante C++.

Nell'esempio di codice VBScript seguente viene illustrato come abilitare il privilegio RemoteShutdown in uno script.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



Molti metodi WMI richiedono che sia abilitata una o più autorizzazioni. Se a un account non è stato concesso un privilegio, non può essere abilitato per la chiamata al metodo .

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Costante C++: **edizione Standard \_ CREATE TOKEN \_ \_ NAME:** **SeCreateTokenPrivilege**

Nome breve di scripting: **CreateToken**

Obbligatorio per creare un oggetto token primario.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Costante C++: **Stringa SeAssignPrimaryTokenPrivilege:** **SeAssignPrimaryTokenPrivilege**

Nome breve di scripting: **AssignPrimaryToken**

Obbligatorio per sostituire un token a livello di processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Costante C++: **edizione Standard \_ LOCK MEMORY \_ \_ NAME** string: **SeLockMemoryPrivilege**

Nome breve dello scripting: **LockMemory**

Obbligatorio per bloccare le pagine in memoria.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Costante C++: **edizione Standard \_ INCREASE QUOTA \_ \_ NAME** stringa: **SeIncreaseQuotaPrivilege**

Nome breve dello scripting: **IncreaseQuotaPrivilege**

Obbligatorio per modificare le quote di memoria per un processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Costante C++: **edizione Standard \_ MACINE \_ ACCOUNT \_ NAME** string: **SeMachineAccountPrivilege**

Nome breve dello scripting: **MachineAccount**

Obbligatorio per aggiungere workstation a un dominio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Costante C++: **edizione Standard \_ stringa TCB \_ NAME:** **SeTcbPrivilege**

Nome breve dello scripting: **Tcb**

Necessario per fungere da parte del sistema operativo. Il titolare fa parte della base di computer attendibili.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Costante C++: **edizione Standard \_ SECURITY \_ NAME** stringa: **SeSecurityPrivilege**

Nome breve dello scripting: **Sicurezza**

Obbligatorio per gestire il controllo e il registro di sicurezza NT.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Costante C++: **edizione Standard \_ STRINGA NOME TAKE \_ OWNERSHIP: \_** **SeTakeOwnershipPrivilege**

Nome breve dello scripting: **TakeOwnership**

Obbligatorio per assumere la proprietà di [](/windows/desktop/SecGloss/a-gly) file o altri oggetti senza avere una voce di controllo di accesso (ACE) nell'elenco di controllo di accesso discrezionale (DACL). 


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Costante C++: **edizione Standard \_ LOAD \_ DRIVER:** **SeLoadDriverPrivilege**

Nome breve dello scripting: **LoadDriver**

Obbligatorio per caricare o scaricare un driver di dispositivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



Costante C++: **edizione Standard \_ SYSTEM PROFILE \_ \_ NAME** string: **SeSystemProfilePrivilege**

Nome breve dello scripting: **SystemProfile**

Obbligatorio per raccogliere informazioni sul profilo sulle prestazioni del sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Costante C++: **edizione Standard \_ SYSTEMTIME** \_ NAME string: **SeSystemtimePrivilege**

Nome breve dello scripting: **Systemtime**

Obbligatorio per modificare l'ora di sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Costante C++: **edizione Standard STRINGA NOME PROCESSO \_ \_ SINGOLO \_ \_ PROF:** **SeProfileSingleProcessPrivilege**

Nome breve dello scripting: **ProfileSingleProcess**

Obbligatorio per raccogliere informazioni sul profilo per un singolo processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Costante C++: **edizione Standard \_ STRINGA NOME PRIORITÀ \_ BASE \_ \_ INC:** **SeIncreaseBasePriorityPrivilege**

Nome breve dello scripting: **IncreaseBasePriority**

Obbligatorio per aumentare la priorità di pianificazione.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Costante C++: **edizione Standard \_ CREATE \_ PAGEFILE \_ NAME** stringa: **SeCreatePagefilePrivilege**

Nome breve di scripting: **CreatePagefile**

Obbligatorio per creare un file di paging.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Costante C++: **edizione Standard \_ CREATE PERMANENT \_ \_ NAME** stringa: **SeCreatePermanentPrivilege**

Nome breve dello scripting: **CreatePermanent**

Obbligatorio per creare oggetti condivisi permanenti.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Costante C++: **edizione Standard \_ BACKUP \_ NAME** stringa: **SeBackupPrivilege**

Nome breve di scripting: **Backup**

Obbligatorio per eseguire il backup di file e directory, indipendentemente dall'ACL specificato per il file.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Costante C++: **edizione Standard \_ RESTORE \_ NAME** stringa: **SeRestorePrivilege**

Nome breve dello scripting: **Ripristino**

Obbligatorio per ripristinare file e directory, indipendentemente dall'ACL specificato per il file.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Costante C++: **edizione Standard \_ SHUTDOWN \_ NAME** stringa: **SeShutdownPrivilege**

Nome breve script: **Shutdown**

Necessario per arrestare il sistema locale.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Costante C++: **edizione Standard \_ DEBUG \_ NAME** string: **SeDebugPrivilege**

Nome breve script: **Debug**

Necessario per eseguire il debug e modificare la memoria di un processo di proprietà di un altro account.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Costante C++: **edizione Standard \_ AUDIT \_ NAME** string: **SeAuditPrivilege**

Nome breve script: **Audit**

Necessario per generare voci di controllo nel registro di sicurezza NT. Solo i server protetti devono avere questo privilegio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Costante C++: **edizione Standard \_ SYSTEM ENVIRONMENT \_ \_ NAME** string: **SeSystemEnvironmentPrivilege**

Nome breve dello script: **SystemEnvironment**

Necessario per modificare la RAM non volatile dei sistemi che usano questo tipo di memoria per archiviare i dati di configurazione.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Costante C++: **edizione Standard \_ \_ CHANGE NOTIFY \_ NAME** string: **SeChangeNotifyPrivilege**

Nome breve script: **ChangeNotify**

Necessario per ricevere notifiche di modifiche a file o directory e ignorare i controlli di accesso di attraversamento. Questo privilegio è abilitato per impostazione predefinita per tutti gli utenti.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Costante C++: **edizione Standard \_ REMOTE SHUTDOWN \_ \_ NAME** string: **SeRemoteShutdownPrivilege**

Nome breve script: **RemoteShutdown**

Necessario per arrestare un computer remoto.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Costante C++: **edizione Standard \_ UNDOCK \_ NAME** string: **SeUndockPrivilege**

Nome breve script: **Disanco**

Necessario per rimuovere un portatile da un docking station.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Costante C++: **edizione Standard \_ SYNC AGENT \_ \_ NAME** string: **SeSyncAgentPrivilege**

Nome breve dello script: **SyncAgent**

Obbligatorio per sincronizzare i dati del servizio directory.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Costante C++: **edizione Standard \_ ENABLE DELEGATION \_ \_ NAME** string: **SeEnableDelegationPrivilege**

Nome breve dello script: **EnableDelegation**

Necessario per abilitare gli account computer e utente come attendibili per la delega.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Costante C++: **edizione Standard \_ MANAGE VOLUME \_ \_ NAME** string: **SeManageVolumePrivilege**

Nome breve script: **ManageVolume**

Obbligatorio per eseguire attività di manutenzione dei volumi.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti api di scripting](scripting-api-constants.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

