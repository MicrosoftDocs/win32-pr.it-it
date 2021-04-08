---
description: Aggiunge un computer a un dominio o a un gruppo di lavoro.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Metodo JoinDomainOrWorkgroup della classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878170"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Metodo JoinDomainOrWorkgroup della \_ classe ComputerSystem Win32

Il metodo **JoinDomainOrWorkGroup** aggiunge un computer a un dominio o a un gruppo di lavoro.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Specifica il dominio o il gruppo di lavoro da unire. Non può essere **null**.

</dd> <dt>

*Password* \[ di in\]
</dt> <dd>

Se il parametro *username* specifica un nome di account, il parametro *password* deve puntare alla password da usare per la connessione al controller di dominio. In caso contrario, questo parametro deve essere **null**.

</dd> <dt>

*Nome utente* \[ in\]
</dt> <dd>

Puntatore a una stringa di caratteri con terminazione **null** costante che specifica il nome dell'account da utilizzare per la connessione al controller di dominio. È necessario specificare un nome NetBIOS di dominio e un account utente, ad esempio dominio \\ utente. Se questo parametro è **null**, vengono utilizzate le informazioni sul chiamante.

È anche possibile usare il nome dell'entità utente (ALZAto) nel modulo user@domain .

</dd> <dt>

*AccountOU* \[ in\]
</dt> <dd>

Specifica il puntatore a una stringa di caratteri con terminazione **null** costante contenente il nome in formato [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) dell'unità organizzativa (OU) per l'account computer. Se si specifica questo parametro, la stringa deve contenere un percorso completo; in caso contrario, l' *accento* deve essere **null**.

Esempio: "OU = texttesto; DC = dominio; DC = dominio; DC = com "

</dd> <dt>

*FJoinOptions* \[ in\]
</dt> <dd>

Set di flag di bit che definiscono le opzioni di join.

<dt>



  (0)


</dt> <dd>

Valore predefinito. Nessuna opzione di join.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**Netsetup \_ Aggiunta a un \_ dominio** (0x00000001)


</dt> <dd>

Aggiunge il computer a un dominio. Se questo valore non è specificato, aggiunge il computer a un gruppo di lavoro.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**Netsetup \_ \_Creazione Acct** (0x00000002)


</dt> <dd>

Crea l'account nel dominio.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**Netsetup \_ \_Aggiornamento di Win9x** (0x00000010)


</dt> <dd>

L'operazione di join si verifica come parte di un aggiornamento.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**Netsetup \_ \_Aggiunta a un dominio \_ se \_ aggiunto** (0x00000020)


</dt> <dd>

Consente un join a un nuovo dominio anche se il computer è già aggiunto a un dominio.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**Netsetup \_ JOIN non \_ sicuro** (0x00000040)


</dt> <dd>

esegue un join non sicuro.

Questa opzione richiede l'aggiunta di un dominio a un account creato in precedenza senza eseguire l'autenticazione con le credenziali utente di dominio. Questa opzione può essere usata in combinazione con l'opzione **Netsetup \_ Machine \_ pwd \_ passata** . In questo caso, *password* è la password dell'account computer creato in precedenza.

Prima di Windows Vista con SP1 e Windows Server 2008, un join non sicuro non è stato autenticato nel controller di dominio. Tutte le comunicazioni sono state eseguite utilizzando una sessione null (non autenticata). A partire da Windows Vista con SP1 e Windows Server 2008, il nome e la password dell'account del computer vengono utilizzati per l'autenticazione nel controller di dominio.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**Netsetup \_ \_Pwd computer \_ superato** (0x00000080)


</dt> <dd>

Indica che il parametro *password* specifica una password dell'account del computer locale anziché una password utente. Questo flag è valido solo per i join non protetti, che è necessario indicare impostando anche il flag di \_ aggiunta Netsetup join non \_ sicuro.

Se si imposta questo flag, dopo che l'operazione di join ha avuto esito positivo, la password del computer verrà impostata sul valore di *password*, se tale valore è una password del computer valida.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**Netsetup \_ RINVIA \_ \_ set SPN** (0x00000100)


</dt> <dd>

Indica che il nome dell'entità servizio (SPN) e le proprietà DnsHostName dell'oggetto computer non devono essere aggiornati in questo momento.

In genere, queste proprietà vengono aggiornate durante l'operazione di join. Al contrario, queste proprietà devono essere aggiornate durante una chiamata successiva al metodo [**Rename**](rename-method-in-class-win32-computersystem.md) . Queste proprietà vengono sempre aggiornate durante l'operazione di ridenominazione.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**Netsetup \_ Unisci \_ \_ account controller** di dominio (0x00000200)


</dt> <dd>

Consentire l'aggiunta a un dominio se l'account esistente è un controller di dominio.

> [!Note]  
> Questo flag è supportato in Windows Vista e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**Netsetup \_ \_DC ambiguo** (0x00001000)


</dt> <dd>

Quando si aggiunge il dominio, non provare a impostare il controller di dominio preferito nel registro di sistema.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**Netsetup \_ Nessuna \_ \_ cache di Netlogon** (0x00002000)


</dt> <dd>

Quando si aggiunge il dominio, non creare la cache di Netlogon.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**Netsetup \_ \_ \_ Servizi di controllo dont** (0x00004000)


</dt> <dd>

Quando si aggiunge il dominio, non forzare l'avvio del servizio Netlogon.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**Netsetup \_ IMPOSTA \_ il \_ nome del computer** (0x00008000)


</dt> <dd>

Quando si aggiunge il dominio solo per il join offline, impostare il nome host del computer di destinazione e il nome NetBIOS.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**Netsetup \_ FORCE \_ \_ set SPN** (0x00010000)


</dt> <dd>

Quando si aggiunge il dominio, eseguire l'override di altre impostazioni durante l'aggiunta a un dominio e impostare il nome dell'entità servizio (SPN).

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**Netsetup \_ Nessun \_ \_ riuso Acct** (0x00020000)


</dt> <dd>

Quando si aggiunge il dominio, non riutilizzare un account esistente.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**Netsetup \_ Ignora \_ \_ flag non supportati** (0x10000000)


</dt> <dd>

Se questo bit è impostato, i flag non riconosciuti verranno ignorati dalla funzione **JoinDomainOrWorkGroup** e [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) si comporterà come se i flag non fossero impostati.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes), che può includere uno dei seguenti valori numerici. Qualsiasi altro numero indica un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Success**
</dt> <dd>

0

</dd> <dt>

**5**
</dt> <dd>

Accesso negato.

</dd> <dt>

**87**
</dt> <dd>

Parametro non corretto.

</dd> <dt>

**110**
</dt> <dd>

il sistema non è in grado di aprire l'oggetto specificato.

</dd> <dt>

**1323**
</dt> <dd>

Non è possibile aggiornare la password.

</dd> <dt>

**1326**
</dt> <dd>

Errore di accesso: nome utente sconosciuto o password errata.

</dd> <dt>

**1355**
</dt> <dd>

Il dominio specificato non esiste o non è possibile contattarlo.

</dd> <dt>

**2224**
</dt> <dd>

L'account esiste già.

</dd> <dt>

**2691**
</dt> <dd>

Il computer è già aggiunto al dominio.

</dd> <dt>

**2692**
</dt> <dd>

Il computer non è attualmente aggiunto a un dominio.

</dd> <dt>

**\_ \_ connessione crittografata WBEM E \_ \_ necessaria**
</dt> <dd>

0x80041087

La *password* e il *nome utente* vengono specificati, ma il livello di autenticazione non è la **\_ \_ \_ \_ \_ privacy PKT a livello** di autenticazione di RPC C. Per Visual Basic, viene restituito **wbemErrEncryptedConnectionRequired** .

</dd> <dt>

**Altri**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si trasferisce un computer da un dominio a un gruppo di lavoro, è necessario rimuovere il computer dal dominio (con una chiamata a [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) prima di chiamare questo metodo per aggiungere un gruppo di lavoro (con una chiamata a **JoinDomainOrWorkGroup**). Dopo aver chiamato questo metodo, riavviare il computer interessato per applicare le modifiche.

Il *nome utente* e la *password* possono essere lasciati **null**. Tuttavia, l'autenticazione della connessione a WMI deve essere 6 in script o **WbemAuthenticationLevelPktPrivacy** in Visual Basic e in altri linguaggi che possono usare la libreria [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) . Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).

In C++, impostare l'autenticazione a **livello di autenticazione RPC \_ C \_ \_ \_ PKT \_ privacy** in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), per l'intero processo o in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)per una connessione al proxy [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Per ulteriori informazioni, vedere [impostazione dell'autenticazione mediante C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) e [impostazione della sicurezza su IWbemServices e altri proxy](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).

## <a name="examples"></a>Esempio

L'esempio [aggiungere un computer a un dominio di](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell aggiunge un computer a un dominio.

Nell'esempio di codice VBScript seguente viene creato un join di un computer a un dominio e viene creato l'account del computer in Active Directory.


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ComputerSystem Win32**](win32-computersystem.md)
</dt> <dt>

[**Metodo UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

