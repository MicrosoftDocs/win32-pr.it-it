---
description: Il parametro strPrivilege del metodo SWbemPrivilegeSet. AddAsString e il parametro iPrivilege per SWbemPrivilegeSet. Add richiedono stringhe di privilegio da WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Costanti Privilege (wbemdisp. h)
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
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759767"
---
# <a name="privilege-constants"></a>Costanti Privilege

Il parametro *strPrivilege* del metodo [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) e il parametro *iPrivilege* per [**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md) richiedono stringhe di privilegio da [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). Per ulteriori informazioni sull'utilizzo delle costanti Privilege, vedere [esecuzione di operazioni con privilegi](executing-privileged-operations.md).

Le costanti seguenti sono definite in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). Nell'elenco seguente sono incluse le costanti equivalenti per C++ e le stringhe per lo scripting. Per creare il nome breve dello scripting, rimuovere "se" e "Privilege" dal nome della costante C++.

Nell'esempio di codice VBScript seguente viene illustrato come abilitare il privilegio RemoteShutdown in uno script.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



Molti metodi WMI richiedono l'abilitazione di una o più autorizzazioni. Se a un account non è stato concesso un privilegio, non è possibile abilitarlo per la chiamata al metodo.

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Costante C++: **se \_ creare \_ il \_ nome del token** stringa: **SeCreateTokenPrivilege**

Nome breve scripting: **creazione Okta**

Obbligatorio per creare un oggetto token primario.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Costante C++: **SeAssignPrimaryTokenPrivilege** stringa: **SeAssignPrimaryTokenPrivilege**

Nome breve scripting: **AssignPrimaryToken**

Obbligatorio per sostituire un token a livello di processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Costante C++: **se si \_ blocca il \_ \_ nome della memoria** stringa: **SeLockMemoryPrivilege**

Nome breve scripting: **LockMemory**

Obbligatorio per bloccare le pagine in memoria.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Costante C++: **se \_ aumenta \_ il \_ nome della quota** stringa: **SeIncreaseQuotaPrivilege**

Nome breve scripting: **IncreaseQuotaPrivilege**

Obbligatorio per modificare le quote di memoria per un processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Costante C++: **se \_ macine \_ \_ nome account** stringa: **SeMachineAccountPrivilege**

Nome breve scripting: **MachineAccount**

Obbligatorio per aggiungere workstation a un dominio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Costante C++: **se \_ TCB \_ nome** stringa: **SeTcbPrivilege**

Nome breve scripting: **TCB**

Obbligatorio per agire come parte del sistema operativo. Il titolare fa parte della base dei computer attendibili.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Costante C++: **se \_ \_ nome sicurezza** stringa: **SeSecurityPrivilege**

Nome breve scripting: **sicurezza**

Necessaria per gestire il controllo e il registro di protezione NT.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Costante C++: **se \_ accetta \_ il \_ nome della proprietà** stringa: **SeTakeOwnershipPrivilege**

Nome breve scripting: **TakeOwnership**

Obbligatorio per assumere la proprietà di file o altri oggetti senza avere una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) nell'elenco di controllo di *accesso discrezionale* (DACL).


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Costante C++: se si carica la stringa del **\_ \_ driver** : **SeLoadDriverPrivilege**

Nome breve scripting: **LoadDriver**

Necessario per caricare o scaricare un driver di dispositivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



Costante C++: **se \_ \_ il \_ nome del profilo di sistema** è stringa: **SeSystemProfilePrivilege**

Nome breve scripting: **systemprofile**

Obbligatorio per raccogliere informazioni sul profilo sulle prestazioni del sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Costante C++: **se \_** è la \_ stringa del nome SYSTEMTIME: **SeSystemTimePrivilege**

Nome breve scripting: **SYSTEMTIME**

Obbligatorio per modificare l'ora di sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Costante C++: **se \_ il \_ \_ \_ nome del singolo processo** è stringa: **SeProfileSingleProcessPrivilege**

Nome breve scripting: **ProfileSingleProcess**

Obbligatorio per raccogliere informazioni sul profilo per un singolo processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Costante C++: **se \_ Inc \_ base \_ \_ nome priorità** stringa: **SeIncreaseBasePriorityPrivilege**

Nome breve scripting: **IncreaseBasePriority**

Obbligatorio per aumentare la priorità di pianificazione.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Costante C++: **se \_ creare \_ il \_ nome del file di paging** stringa: **SeCreatePagefilePrivilege**

Nome breve scripting: **CreatePagefile**

Necessario per creare un pagefile.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Costante C++: **se crea una stringa di \_ \_ \_ nome permanente** : **SeCreatePermanentPrivilege**

Nome breve scripting: **CreatePermanent**

Obbligatorio per creare oggetti condivisi permanenti.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Costante C++: **se \_ \_ nome backup** stringa: **SeBackupPrivilege**

Nome breve scripting: **backup**

Obbligatorio per eseguire il backup di file e directory, indipendentemente dall'ACL specificato per il file.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Costante C++: **se \_ ripristinare il \_ nome** stringa: **SeRestorePrivilege**

Nome breve scripting: **Restore**

Obbligatorio per ripristinare i file e le directory, indipendentemente dall'ACL specificato per il file.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Costante C++: **se si \_ Arresta il \_ nome** stringa: **SeShutdownPrivilege**

Nome breve scripting: **Shutdown**

Necessario per arrestare il sistema locale.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Costante C++: **se \_ il \_ nome di debug** stringa: **SeDebugPrivilege**

Nome breve scripting: **debug**

Necessario per eseguire il debug e la modifica della memoria di un processo di proprietà di un altro account.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Costante C++: **se \_ controllo \_ nome** stringa: **SeAuditPrivilege**

Nome breve scripting: **Audit**

Obbligatorio per generare voci di controllo nel registro di sicurezza di NT. Solo i server protetti devono disporre di questo privilegio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Costante C++: **se \_ il \_ \_ nome dell'ambiente di sistema** è stringa: **SeSystemEnvironmentPrivilege**

Nome breve scripting: **SystemEnvironment**

Obbligatorio per modificare la RAM non volatile dei sistemi che usano questo tipo di memoria per archiviare i dati di configurazione.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Costante C++: **se la \_ modifica \_ notifica il \_ nome** stringa: **SeChangeNotifyPrivilege**

Nome breve scripting: **ChangeNotify**

Necessaria per ricevere notifiche delle modifiche a file o directory e ignorare i controlli di accesso attraversati. Questo privilegio è abilitato per impostazione predefinita per tutti gli utenti.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Costante C++: se la stringa del **\_ \_ \_ nome di arresto remoto** è: **SeRemoteShutdownPrivilege**

Nome breve scripting: **RemoteShutdown**

Necessario per arrestare un computer remoto.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Costante C++: se la stringa del **\_ \_ nome viene disancorata** : **SeUndockPrivilege**

Nome breve dello script: **Undock**

Necessario per rimuovere un computer portatile da una stazione di ancoraggio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Costante C++: **se \_ il \_ \_ nome dell'agente di sincronizzazione** è stringa: **SeSyncAgentPrivilege**

Nome breve scripting: **SyncAgent**

Obbligatorio per sincronizzare i dati del servizio directory.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Costante C++: **se \_ Abilita \_ il \_ nome della delega** stringa: **SeEnableDelegationPrivilege**

Nome breve scripting: **EnableDelegation**

Necessario per consentire l'attendibilità degli account computer e utente per la delega.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Costante C++: **se \_ Gestisci \_ \_ nome volume** stringa: **SeManageVolumePrivilege**

Nome breve scripting: **ManageVolume**

Obbligatorio per eseguire le attività di manutenzione del volume.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esecuzione di script di costanti API](scripting-api-constants.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

