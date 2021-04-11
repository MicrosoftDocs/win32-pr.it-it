---
description: Acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza che utilizza il digest.
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: Funzione AcquireCredentialsHandle (digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1474eef8ad5f5a30fe7d930431185a8ff70f7dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232967"
---
# <a name="acquirecredentialshandle-digest-function"></a>Funzione AcquireCredentialsHandle (digest)

La funzione **AcquireCredentialsHandle (digest)** acquisisce un handle per le credenziali preesistenti di un' [*entità di sicurezza*](../secgloss/s-gly.md). Questo handle è richiesto dalle funzioni [**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md) e [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) . Possono essere *credenziali* preesistenti, stabilite tramite un accesso di sistema non descritto in questo argomento, oppure il chiamante può fornire credenziali alternative.

> [!Note]  
> Non si tratta di un "accesso alla rete" e non implica la raccolta delle credenziali.

 

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszPrincipal* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome dell'entità le cui credenziali faranno riferimento all'handle.

Quando si usa il provider SSP digest, questo parametro è facoltativo.

> [!Note]  
> Se il processo che richiede l'handle non ha accesso alle credenziali, la funzione restituisce un errore. Una stringa null indica che il processo richiede un handle per le credenziali dell'utente con il [*contesto di sicurezza*](../secgloss/s-gly.md) in cui è in esecuzione.

 

</dd> <dt>

*pszPackage* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del [*pacchetto di sicurezza*](../secgloss/s-gly.md) con cui verranno utilizzate queste credenziali. Nome del [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituito nel membro del **nome** di una struttura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) restituita dalla funzione [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) . Dopo aver stabilito un contesto, è possibile chiamare [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) con *ULATTRIBUTE* impostato su SECPKG \_ attr \_ package \_ info per restituire informazioni sul [*pacchetto di sicurezza*](../secgloss/s-gly.md) in uso.

Quando si usa il provider di servizi condivisi del digest, impostare questo parametro su WDIGEST \_ SP \_ Name.

</dd> <dt>

*fCredentialUse* \[ in\]
</dt> <dd>

Flag che indica il modo in cui verranno utilizzate queste credenziali. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ cred in \_ ingresso**</dt> </dl>    | Convalidare le credenziali del server in ingresso. Le credenziali in ingresso possono essere convalidate tramite un'autorità di autenticazione quando viene chiamato [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) o [**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md) . Se tale autorità non è disponibile, la funzione avrà esito negativo e restituirà il secondo \_ e \_ Nessuna \_ autorità di autenticazione \_ . La convalida è specifica del pacchetto.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ cred in \_ uscita**</dt> </dl> | Consentire a una credenziale client locale di preparare un token in uscita.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*pvLogonID* \[ in\]
</dt> <dd>

Puntatore a un [*identificatore univoco locale*](../secgloss/l-gly.md) (LUID) che identifica l'utente. Questo parametro viene fornito per i processi di file System, ad esempio i redirector di rete. Questo parametro può essere **NULL**.

</dd> <dt>

*pAuthData* \[ in\]
</dt> <dd>

Puntatore ai dati specifici del pacchetto. Questo parametro può essere **null**, a indicare che è necessario utilizzare le credenziali predefinite per il [*pacchetto di sicurezza*](../secgloss/s-gly.md) . Per usare le credenziali specificate, passare una struttura di [**\_ \_ \_ identità di autenticazione WinNT in secondi**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) che includa le credenziali in questo parametro. Il tempo di esecuzione RPC passa ciò che è stato fornito in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Quando si usa il provider di servizi condivisi del digest, questo parametro è un puntatore a una struttura di [**\_ \_ \_ identità di autenticazione WinNT sec**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) che contiene le informazioni di autenticazione da usare per individuare le credenziali.

</dd> <dt>

*pGetKeyFn* \[ in\]
</dt> <dd>

Questo parametro non viene utilizzato e deve essere impostato su **null**.

</dd> <dt>

*pvGetKeyArgument* \[ in\]
</dt> <dd>

Questo parametro non viene utilizzato e deve essere impostato su **null**.

</dd> <dt>

*phCredential* \[ out\]
</dt> <dd>

Puntatore a una struttura [CredHandle](sspi-handles.md) per la ricezione dell'handle delle credenziali.

</dd> <dt>

*ptsExpiry* \[ out\]
</dt> <dd>

Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza delle credenziali restituite. Il valore restituito in questa struttura di **timestamp** dipende dalla [*delega vincolata*](../secgloss/s-gly.md). Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) deve restituire questo valore nell'ora locale.

Questo parametro è impostato su un tempo massimo costante. Non esiste alcuna data di scadenza per il [*contesto di sicurezza*](../secgloss/s-gly.md)del digest o per le credenziali o quando si utilizza il provider SSP del digest.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                 | Descrizione                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ memoria insufficiente \_**</dt> </dl> | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                  |
| <dl> <dt>**\_ \_ errore interno sec \_ E**</dt> </dl>      | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ Nessuna \_ credenziale**</dt> </dl>      | Nessuna credenziale disponibile nella [*delega vincolata*](../secgloss/s-gly.md).<br/> |
| <dl> <dt>**SEC \_ E \_ non \_ proprietario**</dt> </dl>           | Il chiamante della funzione non ha le credenziali necessarie.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG \_ non \_ trovati**</dt> </dl>   | Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) richiesto non esiste.<br/>                                                                                          |
| <dl> <dt>**SEC \_ E \_ \_ credenziali sconosciute**</dt> </dl> | Le credenziali fornite al pacchetto non sono state riconosciute.<br/>                                                                            |



 

## <a name="remarks"></a>Commenti

La funzione **AcquireCredentialsHandle (digest)** restituisce un handle per le credenziali di un'entità, ad esempio un utente o un client, come usato da una [*delega vincolata*](../secgloss/s-gly.md)specifica. Può trattarsi dell'handle per le credenziali preesistenti oppure la funzione può creare un nuovo set di credenziali e restituirlo. Questo handle può essere usato nelle chiamate successive alle funzioni [**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md) e [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) .

In generale, **AcquireCredentialsHandle (digest)** non consente a un processo di ottenere un handle per le credenziali di altri utenti connessi allo stesso computer. Tuttavia, un chiamante con \_ \_ [*privilegi*](../secgloss/s-gly.md) per il nome TCB ha la possibilità di specificare l' [*identificatore di accesso*](../secgloss/l-gly.md) (LUID) di qualsiasi token di sessione di accesso esistente per ottenere un handle per le credenziali della sessione. Questa operazione viene in genere utilizzata dai moduli in modalità kernel che devono agire per conto di un utente connesso.

Un pacchetto può chiamare la funzione in *pGetKeyFn* fornita dal trasporto di run-time RPC. Se il trasporto non supporta la nozione di callback per recuperare le credenziali, questo parametro deve essere **null**.

Per i chiamanti in modalità kernel, è necessario notare le differenze seguenti:

-   I due parametri di stringa devono essere stringhe [*Unicode*](../secgloss/u-gly.md) .
-   I valori del buffer devono essere allocati nella memoria virtuale del processo, non dal pool.

Al termine dell'utilizzo delle credenziali restituite, liberare la memoria utilizzata dalle credenziali chiamando la funzione [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomi Unicode e ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
