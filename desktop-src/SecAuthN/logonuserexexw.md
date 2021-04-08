---
description: La funzione LogonUserExExW tenta di registrare un utente nel computer locale.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Funzione LogonUserExExW (Winbasep. h)
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
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058037"
---
# <a name="logonuserexexw-function"></a>LogonUserExExW (funzione)

La funzione **LogonUserExExW** tenta di registrare un utente nel computer locale. Il computer locale è il computer da cui è stato chiamato **LogonUserExExW** . Non è possibile usare **LogonUserExExW** per accedere a un computer remoto. Specificare l'utente utilizzando un nome utente e un dominio e [*autenticare*](../secgloss/a-gly.md) l'utente utilizzando una password in testo non crittografato. Se la funzione ha esito positivo, riceve un handle per un token che rappresenta l'utente connesso. È quindi possibile usare questo handle di token per rappresentare l'utente specificato o, nella maggior parte dei casi, per creare un [*processo*](../secgloss/p-gly.md) che viene eseguito nel contesto dell'utente specificato.

Questa funzione è simile alla funzione [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , ma accetta il parametro aggiuntivo, *pTokenGroups*, che è un set di uno o più [*identificatori di sicurezza*](../secgloss/s-gly.md) (SID) aggiunti al token restituito al chiamante quando l'accesso ha esito positivo.

Questa funzione non è dichiarata in un'intestazione pubblica e non dispone di librerie di importazione associate. È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Advapi32.dll.

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

*lpszUsername* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome dell'utente. Si tratta del nome dell'account utente a cui accedere. Se si usa il formato del [*nome dell'entità utente*](../secgloss/u-gly.md) (UPN), il parametro *LpszDomain* deve essere **null**.

</dd> <dt>

*lpszDomain* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del dominio o del server il cui database di account contiene l'account *lpszUsername* . Se questo parametro è **null**, il nome utente deve essere specificato in formato UPN. Se questo parametro è ".", la funzione convalida l'account utilizzando solo il database di account locale.

</dd> <dt>

*lpszPassword* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica la password in testo non crittografato per l'account utente specificato da *lpszUsername*. Al termine dell'utilizzo della password, cancellare la password dalla memoria chiamando la funzione [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) . Per ulteriori informazioni sulla protezione delle password, vedere [gestione delle password](../secbp/handling-passwords.md).

</dd> <dt>

*dwLogonType* \[ in\]
</dt> <dd>

Tipo di operazione di accesso da eseguire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <dt>**LOGON32 \_ ACCESSO \_ interattivo**</dt> <dt>2</dt> </dl>                    | Questo tipo di accesso è destinato agli utenti che utilizzano in modo interattivo il computer, ad esempio un utente connesso da un server [*Terminal*](../secgloss/t-gly.md) , una shell remota o un processo simile. Questo tipo di accesso comporta le spese aggiuntive per la memorizzazione nella cache delle informazioni di accesso per le operazioni disconnesse. Pertanto, non è appropriato per alcune applicazioni client/server, ad esempio un server di posta elettronica.<br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <dt>**LOGON32 \_ \_Rete di accesso**</dt> <dt>3</dt> </dl>                                | Questo tipo di accesso è destinato ai server ad alte prestazioni per l'autenticazione di password in testo non crittografato. La funzione **LogonUserExExW** non memorizza nella cache le credenziali per questo tipo di accesso.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <dt>**LOGON32 \_ \_Batch di accesso**</dt> <dt>4</dt> </dl>                                      | Questo tipo di accesso è destinato ai server batch, in cui i processi possono essere eseguiti per conto di un utente senza l'intervento diretto. Questo tipo è anche per i server con prestazioni più elevate che elaborano molti tentativi di autenticazione in testo non crittografato alla volta, ad esempio posta elettronica o server Web. La funzione **LogonUserExExW** non memorizza nella cache le credenziali per questo tipo di accesso.<br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <dt>**LOGON32 \_ \_Servizio di accesso**</dt> <dt>5</dt> </dl>                                | Indica un accesso del tipo di servizio. Per l'account specificato deve essere abilitato il privilegio servizio.<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <dt>**LOGON32 \_ \_Sblocco di accesso**</dt> <dt>7</dt> </dl>                                   | Questo tipo di accesso è per le dll [*Gina*](../secgloss/g-gly.md) che accedono agli utenti che utilizzeranno il computer in modo interattivo. Questo tipo di accesso può generare un record di controllo univoco che indica quando la workstation è stata sbloccata.<br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <dt>**LOGON32 \_ Rete di accesso non \_ \_ crittografata**</dt> <dt>8</dt> </dl> | Questo tipo di accesso conserva il nome e la password nel [*pacchetto di autenticazione*](../secgloss/a-gly.md), che consente al server di stabilire connessioni ad altri server di rete durante la rappresentazione del client. Un server può accettare le credenziali in testo non crittografato da un client, chiamare **LogonUserExExW**, verificare che l'utente possa accedere al sistema attraverso la rete e continuare a comunicare con altri server. <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <dt>**LOGON32 \_ \_Nuove \_ credenziali di accesso**</dt> <dt>9</dt> </dl>       | Questo tipo di accesso consente al chiamante di clonare il token corrente e di specificare nuove credenziali per le connessioni in uscita. La nuova sessione di accesso ha lo stesso identificatore locale ma usa credenziali diverse per altre connessioni di rete.<br/> Questo tipo di accesso è supportato solo dal provider di accesso **\_ \_ WINNT50 del provider LOGON32** .<br/>                                                                                                                                       |



 

</dd> <dt>

*dwLogonProvider* \[ in\]
</dt> <dd>

Provider di accesso. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                           | Significato                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <dt>**\_Impostazione predefinita del provider LOGON32 \_**</dt> </dl> | Utilizzare il provider di accesso standard per il sistema. Il [*provider di sicurezza*](../secgloss/s-gly.md) predefinito è NTLM.<br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <dt>**\_Provider LOGON32 \_ WINNT50**</dt> </dl> | Utilizzare il provider di accesso Negotiate. <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <dt>**\_Provider LOGON32 \_ WINNT40**</dt> </dl> | Utilizzare il provider di accesso NTLM.<br/>                                                                                                                                                               |



 

</dd> <dt>

*pTokenGroups* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**di \_ gruppi di token**](/windows/win32/api/winnt/ns-winnt-token_groups) che specifica un elenco di SID di gruppo che vengono aggiunti al token che questa funzione riceve al completamento dell'accesso. Eventuali SID aggiunti al token hanno effetto anche sull'espansione del gruppo. Se, ad esempio, i SID aggiunti sono membri dei gruppi locali, anche tali gruppi vengono aggiunti al token di accesso ricevuto.

Se questo parametro non è **null**, il chiamante di questa funzione deve avere il privilegio di **\_ \_ privilegio se TCB** concesso e abilitato.

</dd> <dt>

*phToken* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile dell'handle che riceve un handle per un token che rappresenta l'utente specificato.

È possibile usare l'handle restituito nelle chiamate alla funzione [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .

Nella maggior parte dei casi, l'handle restituito è un [*token primario*](../secgloss/p-gly.md) che è possibile usare nelle chiamate alla funzione [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Tuttavia, se si specifica il \_ \_ flag di rete di accesso LOGON32, **LogonUserExExW** restituisce un [*token di rappresentazione*](../secgloss/i-gly.md) che non è possibile utilizzare in **CreateProcessAsUser ha** a meno che non si chiami [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) per convertire il token di rappresentazione in un token primario.

Quando questo handle non è più necessario, chiuderlo chiamando la funzione [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

</dd> <dt>

*ppLogonSid* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un puntatore a un SID che riceve il SID dell'utente connesso.

Al termine dell'utilizzo del SID, liberarlo chiamando la funzione [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .

</dd> <dt>

*ppProfileBuffer* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un puntatore che riceve l'indirizzo di un buffer che contiene il profilo dell'utente connesso.

</dd> <dt>

*pdwProfileLength* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un **valore DWORD** che riceve la lunghezza del buffer del profilo.

</dd> <dt>

*pQuotaLimits* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**di \_ limiti di quota**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) che riceve informazioni sulle quote per l'utente che ha eseguito l'accesso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce un valore diverso da zero.

Se la funzione ha esito negativo, viene restituito zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Il tipo di accesso alla **\_ \_ rete di accesso LOGON32** è più veloce, ma presenta le limitazioni seguenti:

-   La funzione restituisce un [*token di rappresentazione*](../secgloss/i-gly.md), non un token primario. Non è possibile usare questo token direttamente nella funzione [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Tuttavia, è possibile chiamare la funzione [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) per convertire il token in un token primario e quindi usarlo in **CreateProcessAsUser ha**.
-   Se si converte il token in un token primario e lo si usa in [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per avviare un processo, il nuovo processo non può accedere ad altre risorse di rete, ad esempio server remoti o stampanti, tramite il redirector. Un'eccezione è che se la risorsa di rete non è controllata dall'accesso, il nuovo processo sarà in grado di accedervi.

L'account specificato da *lpszUsername* deve disporre dei diritti di account necessari. Ad esempio, per accedere a un utente con il **flag \_ \_ interattivo accesso LOGON32** , l'utente o un gruppo a cui appartiene l'utente deve disporre dell'account **\_ \_ \_ nome di accesso interattivo se** . Per un elenco dei diritti dell'account che interessano le varie operazioni di accesso, vedere [diritti di accesso agli oggetti account](../secmgmt/account-object-access-rights.md).

Un utente viene considerato connesso se esiste almeno un token. Se si chiama [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) e si chiude il token, l'utente viene comunque connesso fino al termine del processo e di tutti i processi figlio.

Se viene specificato il parametro facoltativo *pTokenGroups* , LSA non aggiungerà automaticamente il SID locale o il SID di accesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                  |
| Versione<br/>                  | LogonUserExExW è disponibile anche in Windows Server 2003 o Windows XPwith la versione di distribuzione generale.<br/> |
| Intestazione<br/>                   | <dl> <dt>Winbasep. h</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di accesso client/server](../secauthz/client-server-access-control.md)
</dt> <dt>

[Funzioni di controllo di accesso client/server](../secauthz/authorization-functions.md)
</dt> <dt>

[**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[**limiti di QUOTA \_**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
