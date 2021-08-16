---
description: Aggiunge un sistema di computer a un dominio o a un gruppo di lavoro.
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
ms.openlocfilehash: b9faf923cf6c771e95a7dfb4f0b04f896c54d79c6b5548e97850d867057b065b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834648"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Metodo JoinDomainOrWorkgroup della classe ComputerSystem Win32 \_

Il **metodo JoinDomainOrWorkgroup** aggiunge un sistema di computer a un dominio o a un gruppo di lavoro.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*Nome* \[ Pollici\]
</dt> <dd>

Specifica il dominio o il gruppo di lavoro da aggiungere. Non può essere **NULL.**

</dd> <dt>

*Password* \[ Pollici\]
</dt> <dd>

Se il *parametro UserName* specifica un nome di account, il *parametro Password* deve puntare alla password da usare per la connessione al controller di dominio. In caso contrario, questo parametro deve essere **NULL.**

</dd> <dt>

*UserName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa di caratteri con terminazione **Null** costante che specifica il nome dell'account da utilizzare per la connessione al controller di dominio. È necessario specificare un nome NetBIOS di dominio e un account utente, ad esempio Utente \\ di dominio. Se questo parametro è **NULL,** vengono usate le informazioni sul chiamante.

È anche possibile usare il nome dell'entità utente (UPPED) nel formato user@domain .

</dd> <dt>

*AccountOU* \[ Pollici\]
</dt> <dd>

Specifica il puntatore a una stringa di caratteri con terminazione **Null** costante contenente il nome di formato [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) dell'unità organizzativa per l'account computer. Se si specifica questo parametro, la stringa deve contenere un percorso completo, in caso contrario *Accent* deve essere **NULL.**

Esempio: "OU=testOU; DC=domain; DC=Dominio; DC=com"

</dd> <dt>

*FJoinOptions* \[ Pollici\]
</dt> <dd>

Set di flag di bit che definiscono le opzioni di join.

<dt>



  (0)


</dt> <dd>

Valore predefinito. Nessuna opzione di join.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP \_ AGGIUNGERE \_ UN DOMINIO** (0x00000001)


</dt> <dd>

Aggiunge il computer a un dominio. Se questo valore non viene specificato, aggiunge il computer a un gruppo di lavoro.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP \_ ACCT \_ CREATE** (0x00000002)


</dt> <dd>

Crea l'account nel dominio.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP \_ AGGIORNAMENTO WIN9X \_** (0x00000010)


</dt> <dd>

L'operazione di join viene eseguita come parte di un aggiornamento.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP \_ AGGIUNTA \_ A UN DOMINIO SE \_ \_ AGGIUNTO** (0x00000020)


</dt> <dd>

Consente l'aggiunta a un nuovo dominio anche se il computer è già aggiunto a un dominio.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP \_ JOIN \_ UNSECURE** (0x00000040)


</dt> <dd>

esegue un join non sicuro.

Questa opzione richiede l'aggiunta di un dominio a un account creato in precedenza senza eseguire l'autenticazione con credenziali utente di dominio. Questa opzione può essere usata insieme **all'opzione NETSETUP \_ MACHINE \_ PWD \_ PASSED.** In questo caso, *Password* è la password dell'account computer creato in precedenza.

Prima di Windows Vista con SP1 e Windows Server 2008, un join non sicuro non eseguiva l'autenticazione al controller di dominio. Tutte le comunicazioni sono state eseguite usando una sessione Null (non autenticata). A partire da Windows Vista con SP1 e Windows Server 2008, il nome dell'account computer e la password vengono usati per l'autenticazione al controller di dominio.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP \_ MACHINE \_ PWD \_ PASSED** (0x00000080)


</dt> <dd>

Indica che il parametro *Password* specifica una password dell'account del computer locale anziché una password utente. Questo flag è valido solo per i join non protetti, che è necessario indicare impostando anche il flag NETSETUP \_ JOIN \_ UNSECURE.

Se si imposta questo flag, al termine dell'operazione di aggiunta, la password del computer verrà impostata sul valore *Password*, se tale valore è una password del computer valida.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP \_ DEFER \_ SPN \_ SET** (0x00000100)


</dt> <dd>

Indica che il nome dell'entità servizio (SPN) e le proprietà DnsHostName nell'oggetto computer non devono essere aggiornati in questo momento.

In genere, queste proprietà vengono aggiornate durante l'operazione di join. Queste proprietà devono invece essere aggiornate durante una chiamata successiva al [**metodo Rename.**](rename-method-in-class-win32-computersystem.md) Queste proprietà vengono sempre aggiornate durante l'operazione di ridenominazione.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP \_ JOIN \_ DC \_ ACCOUNT** (0x00000200)


</dt> <dd>

Consentire l'aggiunta al dominio se l'account esistente è un controller di dominio.

> [!Note]  
> Questo flag è supportato in Windows Vista e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP \_ CONTROLLER \_ AMBIGUO** (0x00001000)


</dt> <dd>

Quando si esegue l'aggiunta al dominio, non provare a impostare il controller di dominio preferito nel Registro di sistema.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP \_ NO \_ NETLOGON \_ CACHE** (0x00002000)


</dt> <dd>

Quando si esegue l'aggiunta al dominio, non creare la cache netlogon.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP \_ SERVIZI DI CONTROLLO DONT \_ \_** (0x00004000)


</dt> <dd>

Quando si esegue l'aggiunta al dominio, non forzare l'avvio del servizio Accesso rete.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP \_ SET \_ MACHINE \_ NAME** (0x00008000)


</dt> <dd>

Quando si aggiunge il dominio solo per l'aggiunta offline, impostare il nome host del computer di destinazione e il nome NetBIOS.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP \_ FORCE \_ SPN \_ SET** (0x00010000)


</dt> <dd>

Quando si aggiunge il dominio, eseguire l'override di altre impostazioni durante l'aggiunta al dominio e impostare il nome dell'entità servizio (SPN).

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP \_ NO \_ ACCT \_ REUSE** (0x00020000)


</dt> <dd>

Quando si esegue l'aggiunta al dominio, non riutilizzare un account esistente.

> [!Note]  
> Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP \_ IGNORA \_ FLAG NON \_ SUPPORTATI** (0x10000000)


</dt> <dd>

Se questo bit è impostato, i flag non riconosciuti verranno ignorati dalla funzione **JoinDomainOrWorkgroup** e [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) si comporterà come se i flag non fossero impostati.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un [codice di errore di](/windows/desktop/Debug/system-error-codes)sistema che può includere uno dei valori numerici seguenti. Qualsiasi altro numero indica un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

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

impossibile aprire l'oggetto specificato.

</dd> <dt>

**1323**
</dt> <dd>

Impossibile aggiornare la password.

</dd> <dt>

**1326**
</dt> <dd>

Errore di accesso: nome utente sconosciuto o password non valida.

</dd> <dt>

**1355**
</dt> <dd>

Il dominio specificato non esiste o non è stato possibile contattarci.

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

**CONNESSIONE \_ CRITTOGRAFATA WBEM E \_ \_ \_ OBBLIGATORIA**
</dt> <dd>

0x80041087

*Password* e *UserName sono* specificati, ma il livello di autenticazione non è **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Ad Visual Basic, viene restituito **wbemErrEncryptedConnectionRequired.**

</dd> <dt>

**Altri**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si sposta un computer da un dominio a un gruppo di lavoro, è necessario rimuovere il computer dal dominio (con una chiamata a [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) prima di chiamare questo metodo per aggiungere un gruppo di lavoro (con una chiamata a **JoinDomainOrWorkgroup**). Dopo aver chiamato questo metodo, riavviare il computer interessato per applicare le modifiche.

*UserName* e *Password* possono essere lasciati **null.** Tuttavia, l'autenticazione della connessione a WMI deve essere 6 nello script o **WbemAuthenticationLevelPktPrivacy** in Visual Basic e in altri linguaggi che possono usare la libreria [wbemdisp.dll.](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) Per altre informazioni, vedere [Impostazione del livello di sicurezza del processo predefinito tramite VBScript.](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript)

In C++ impostare l'autenticazione su **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), per l'intero processo o in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), per una connessione al proxy [**IWbemServices.**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) Per altre informazioni, vedere [Impostazione dell'autenticazione tramite C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) e Impostazione della sicurezza in [IWbemServices e altri proxy.](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies)

## <a name="examples"></a>Esempio

L'esempio di PowerShell Aggiungere un [computer a un](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) dominio aggiunge un computer a un dominio.

L'esempio di codice VBScript seguente aggiunge un computer a un dominio e crea l'account del computer in Active Directory.


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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ ComputerSystem**](win32-computersystem.md)
</dt> <dt>

[**Metodo UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

