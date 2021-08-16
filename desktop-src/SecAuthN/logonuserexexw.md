---
description: La funzione LogonUserExExW tenta di accedere a un utente nel computer locale.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Funzione LogonUserExExW (Winbasep.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 8e6b7c5b377ffa7b517ccd19d1dfbffa08d26191af3822f9d9b17cc02c33d055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922336"
---
# <a name="logonuserexexw-function"></a>Funzione LogonUserExExW

La **funzione LogonUserExExW** tenta di accedere a un utente nel computer locale. Il computer locale è il computer da cui **è stato chiamato LogonUserExExW.** Non è possibile **usare LogonUserExExW** per accedere a un computer remoto. Specificare l'utente usando un nome utente e un dominio e [*autenticare*](../secgloss/a-gly.md) l'utente usando una password in testo non crittografato. Se la funzione ha esito positivo, riceve un handle per un token che rappresenta l'utente connesso. È quindi possibile usare questo handle di token per rappresentare l'utente specificato o, nella maggior parte dei casi, per creare un processo eseguito nel contesto dell'utente specificato. [](../secgloss/p-gly.md)

Questa funzione è simile alla funzione [**LogonUserEx,**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) ad eccezione del fatto che accetta il parametro aggiuntivo *pTokenGroups*, ovvero un set di uno o più ID di sicurezza [](../secgloss/s-gly.md) (SID) che vengono aggiunti al token restituito al chiamante quando l'accesso ha esito positivo.

Questa funzione non è dichiarata in un'intestazione pubblica e non ha alcuna libreria di importazione associata. È necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico Advapi32.dll.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszUsername* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome dell'utente. Nome dell'account utente a cui accedere. Se si usa il formato del nome [*dell'entità*](../secgloss/u-gly.md) utente (UPN), il *parametro lpszDomain* deve essere **NULL.**

</dd> <dt>

*lpszDomain* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del dominio o del server il cui database di account contiene *l'account lpszUsername.* Se questo parametro è **NULL,** il nome utente deve essere specificato in formato UPN. Se questo parametro è ".", la funzione convalida l'account usando solo il database dell'account locale.

</dd> <dt>

*lpszPassword* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica la password di testo non crittografato per l'account utente specificato da *lpszUsername*. Al termine dell'uso della password, cancellare la password dalla memoria chiamando la [**funzione SecureZeroMemory.**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) Per altre informazioni sulla protezione delle password, vedere [Gestione delle password](../secbp/handling-passwords.md).

</dd> <dt>

*dwLogonType* \[ Pollici\]
</dt> <dd>

Tipo di operazione di accesso da eseguire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <dt>**LOGON32 \_ ACCESSO \_ INTERATTIVO**</dt> <dt>2</dt> </dl>                    | Questo tipo di accesso è destinato agli utenti che usano il computer in modo interattivo, ad esempio un utente connesso da un server [*terminal,*](../secgloss/t-gly.md) una shell remota o un processo simile. Questo tipo di accesso presenta il costo aggiuntivo della memorizzazione nella cache delle informazioni di accesso per le operazioni disconnesse. pertanto non è appropriato per alcune applicazioni client/server, ad esempio un server di posta elettronica.<br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <dt>**LOGON32 \_ RETE \_ DI ACCESSO**</dt> <dt>3</dt> </dl>                                | Questo tipo di accesso è destinato ai server ad alte prestazioni per autenticare le password in testo non crittografato. La **funzione LogonUserExExW** non memorizza nella cache le credenziali per questo tipo di accesso.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <dt>**LOGON32 \_ BATCH \_ DI ACCESSO**</dt> <dt>4</dt> </dl>                                      | Questo tipo di accesso è destinato ai server batch, in cui i processi possono essere esecutori per conto di un utente senza l'intervento diretto. Questo tipo è anche per i server con prestazioni più elevate che elaborano molti tentativi di autenticazione in testo non crittografato contemporaneamente, ad esempio server di posta elettronica o Web. La **funzione LogonUserExExW** non memorizza nella cache le credenziali per questo tipo di accesso.<br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <dt>**LOGON32 \_ SERVIZIO \_ DI ACCESSO**</dt> <dt>5</dt> </dl>                                | Indica un accesso di tipo servizio. L'account fornito deve avere il privilegio del servizio abilitato.<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <dt>**LOGON32 \_ SBLOCCO \_ DI ACCESSO**</dt> <dt>7</dt> </dl>                                   | Questo tipo di accesso è per [*le DLL GINA*](../secgloss/g-gly.md) che azionano gli utenti che usano il computer in modo interattivo. Questo tipo di accesso può generare un record di controllo univoco che indica quando la workstation è stata sbloccata.<br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <dt>**LOGON32 \_ TESTO \_ NON \_ CRITTOGRAFATO DI RETE DI ACCESSO**</dt> <dt>8</dt> </dl> | Questo tipo di accesso mantiene il nome e la password nel pacchetto di autenticazione [*,*](../secgloss/a-gly.md)che consente al server di effettuare connessioni ad altri server di rete durante la rappresentazione del client. Un server può accettare credenziali in testo non crittografato da un client, chiamare **LogonUserExExW,** verificare che l'utente possa accedere al sistema attraverso la rete e comunque comunicare con altri server. <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <dt>**LOGON32 \_ ACCEDERE \_ ALLE \_ NUOVE CREDENZIALI**</dt> <dt>9</dt> </dl>       | Questo tipo di accesso consente al chiamante di clonare il token corrente e di specificare nuove credenziali per le connessioni in uscita. La nuova sessione di accesso ha lo stesso identificatore locale, ma usa credenziali diverse per altre connessioni di rete.<br/> Questo tipo di accesso è supportato solo dal provider **di accesso LOGON32 \_ PROVIDER \_ WINNT50.**<br/>                                                                                                                                       |



 

</dd> <dt>

*dwLogonProvider* \[ Pollici\]
</dt> <dd>

Provider di accesso. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                           | Significato                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <dt>**IMPOSTAZIONE PREDEFINITA DEL PROVIDER LOGON32 \_ \_**</dt> </dl> | Usare il provider di accesso standard per il sistema. Il [*provider di sicurezza predefinito*](../secgloss/s-gly.md) è NTLM.<br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <dt>**LOGON32 \_ PROVIDER \_ WINNT50**</dt> </dl> | Usare il provider di accesso negotiate. <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <dt>**LOGON32 \_ PROVIDER \_ WINNT40**</dt> </dl> | Usare il provider di accesso NTLM.<br/>                                                                                                                                                               |



 

</dd> <dt>

*pTokenGroups* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura TOKEN \_ GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) che specifica un elenco di SID di gruppo che vengono aggiunti al token ricevuto da questa funzione al momento dell'accesso riuscito. Anche i SID aggiunti al token hanno effetto sull'espansione del gruppo. Ad esempio, se i SID aggiunti sono membri di gruppi locali, tali gruppi vengono aggiunti anche al token di accesso ricevuto.

Se questo parametro non è **NULL,** al chiamante di questa funzione deve essere concesso **edizione Standard \_ privilegio TCB \_ PRIVILEGE** concesso e abilitato.

</dd> <dt>

*phToken* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile handle che riceve un handle per un token che rappresenta l'utente specificato.

È possibile usare l'handle restituito nelle chiamate alla [**funzione ImpersonateLoggedOnUser.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)

Nella maggior parte dei casi, l'handle restituito è un [*token*](../secgloss/p-gly.md) primario che è possibile usare nelle chiamate alla [**funzione CreateProcessAsUser.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Tuttavia, se si specifica il flag LOGON32 \_ LOGON \_ NETWORK, **LogonUserExExW** restituisce un [*token*](../secgloss/i-gly.md) di rappresentazione che non è possibile usare in **CreateProcessAsUser** a meno che non si chiami [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) per convertire il token di rappresentazione in un token primario.

Quando questo handle non è più necessario, chiuderlo chiamando la [**funzione CloseHandle.**](/windows/win32/api/handleapi/nf-handleapi-closehandle)

</dd> <dt>

*ppLogonSid* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un puntatore a un SID che riceve il SID dell'utente connesso.

Al termine dell'uso del SID, liberarlo chiamando la [**funzione LocalFree.**](/windows/win32/api/winbase/nf-winbase-localfree)

</dd> <dt>

*ppProfileBuffer* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un puntatore che riceve l'indirizzo di un buffer che contiene il profilo dell'utente connesso.

</dd> <dt>

*pdwProfileLength* \[ out, facoltativo\]
</dt> <dd>

Puntatore a **un valore DWORD** che riceve la lunghezza del buffer del profilo.

</dd> <dt>

*pQuotaLimits* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura QUOTA \_ LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) che riceve informazioni sulle quote per l'utente connesso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce un valore diverso da zero.

Se la funzione ha esito negativo, restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Il **tipo di accesso \_ LOGON32 LOGON \_ NETWORK** è più veloce, ma presenta le limitazioni seguenti:

-   La funzione restituisce un [*token di rappresentazione,*](../secgloss/i-gly.md)non un token primario. Non è possibile usare questo token direttamente nella [**funzione CreateProcessAsUser.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Tuttavia, è possibile chiamare la [**funzione DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) per convertire il token in un token primario e quindi usarlo in **CreateProcessAsUser**.
-   Se si converte il token in un token primario e lo si usa in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per avviare un processo, il nuovo processo non può accedere ad altre risorse di rete, ad esempio server remoti o stampanti, tramite il redirector. Un'eccezione è che se la risorsa di rete non è controllata dall'accesso, il nuovo processo sarà in grado di accedervi.

L'account specificato da *lpszUsername* deve disporre dei diritti di account necessari. Ad esempio, per accedere a un utente con il flag **LOGON32 \_ LOGON \_ INTERACTIVE,** l'utente (o un gruppo a cui appartiene l'utente) deve avere il diritto edizione Standard **INTERACTIVE LOGON \_ \_ \_ NAME.** Per un elenco dei diritti di account che influiscono sulle diverse operazioni di accesso, vedere [Diritti di accesso agli oggetti account](../secmgmt/account-object-access-rights.md).

Un utente viene considerato connesso se esiste almeno un token. Se si chiama [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) e quindi si chiude il token, l'utente rimane connesso fino al termine del processo (e di tutti i processi figlio).

Se viene specificato *il parametro facoltativo pTokenGroups,* LSA non aggiungerà automaticamente il SID locale o il SID di accesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                  |
| Versione<br/>                  | LogonUserExExW è disponibile anche in Windows Server 2003 o Windows XPcon la versione di distribuzione generale.<br/> |
| Intestazione<br/>                   | <dl> <dt>Winbasep.h</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di accesso client/server](../secauthz/client-server-access-control.md)
</dt> <dt>

[Funzioni di controllo di accesso client/server](../secauthz/authorization-functions.md)
</dt> <dt>

[**Closehandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[**Createprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[**LIMITI DI \_ QUOTA**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
