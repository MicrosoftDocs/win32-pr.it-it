---
description: Acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza che usa Schannel.
ms.assetid: 0f006670-a1e5-47ed-baf5-ed55bd42b468
title: Funzione AcquireCredentialsHandle (Schannel) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: d2fb9812817e27576667f7fa0ff5312eea8cea41743cbfc9e5b03267f837011f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101441"
---
# <a name="acquirecredentialshandle-schannel-function"></a>Funzione AcquireCredentialsHandle (Schannel)

La **funzione AcquireCredentialsHandle (Schannel)** acquisisce un handle per le credenziali preesistenti di un'entità [*di sicurezza.*](../secgloss/s-gly.md) Questo handle è richiesto dalle [**funzioni InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) e [**AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md) Possono trattarsi di credenziali *preesistenti,* stabilite tramite un accesso di sistema non descritto qui, oppure il chiamante può fornire credenziali alternative.

> [!Note]  
> Non si tratta di un "accesso alla rete" e non implica la raccolta delle credenziali.

 

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_opt_  SEC_CHAR       *pszPrincipal,
  _In_      SEC_CHAR       *pszPackage,
  _In_      ULONG          fCredentialUse,
  _In_opt_  PLUID          pvLogonID,
  _In_opt_  PVOID          pAuthData,
  _In_opt_  SEC_GET_KEY_FN pGetKeyFn,
  _In_opt_  PVOID          pvGetKeyArgument,
  _Out_     PCredHandle    phCredential,
  _Out_opt_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszPrincipal* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome dell'entità alle cui credenziali farà riferimento l'handle.

Quando si usa SSP Schannel, questo parametro non viene usato e deve essere impostato su **NULL.**

> [!Note]  
> Se il processo che richiede l'handle non ha accesso alle credenziali, la funzione restituisce un errore. Una stringa Null indica che il processo richiede un handle per le credenziali dell'utente nel contesto [*di sicurezza*](../secgloss/s-gly.md) in esecuzione.

 

</dd> <dt>

*pszPackage* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del pacchetto di sicurezza [*con*](../secgloss/s-gly.md) cui verranno usate queste credenziali. Si tratta di [*un nome di pacchetto*](../secgloss/s-gly.md) di sicurezza restituito nel membro **Name** di una [**struttura SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) restituita dalla [**funzione EnumerateSecurityPackages.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) Dopo aver stabilito un contesto, è possibile chiamare [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) con *ulAttribute* impostato su SECPKG ATTR PACKAGE INFO per restituire informazioni sul pacchetto di sicurezza \_ in \_ \_ uso. [](../secgloss/s-gly.md)

Quando si usa SSP Schannel, impostare questo parametro su UNISP \_ NAME.

</dd> <dt>

*fCredentialUse* \[ Pollici\]
</dt> <dd>

Flag che indica come verranno usate queste credenziali. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ CRED \_ IN INGRESSO**</dt> </dl>    | Convalidare le credenziali del server in ingresso. Le credenziali in ingresso possono essere convalidate usando un'autorità di autenticazione quando viene chiamato [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) [**o AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md) Se tale autorità non è disponibile, la funzione avrà esito negativo e restituirà SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY. La convalida è specifica del pacchetto.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ CRED IN \_ USCITA**</dt> </dl> | Consente a una credenziale client locale di preparare un token in uscita.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*pvLogonID* \[ in, facoltativo\]
</dt> <dd>

Puntatore a un [*identificatore univoco locale*](../secgloss/l-gly.md) (LUID) che identifica l'utente. Questo parametro viene fornito per i processi del file system, ad esempio i redirector di rete. Questo parametro può essere **NULL**.

Quando si usa SSP Schannel, questo parametro non viene usato e deve essere impostato su **NULL.**

</dd> <dt>

*pAuthData* \[ in, facoltativo\]
</dt> <dd>

Puntatore a dati specifici del pacchetto. Questo parametro può essere **NULL,** che indica che è necessario usare le credenziali predefinite per il [*pacchetto*](../secgloss/s-gly.md) di sicurezza. Per usare le credenziali fornite, passare una [**struttura SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) che include tali credenziali in questo parametro. Il tempo di esecuzione RPC passa tutto ciò che è stato fornito in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Quando si usa SSP Schannel, specificare una [**struttura**](/windows/win32/api/schannel/ns-schannel-sch_credentials) SCH_CREDENTIALS che indica il protocollo da usare e le impostazioni per varie funzionalità del canale personalizzabili.

</dd> <dt>

*pGetKeyFn* \[ in, facoltativo\]
</dt> <dd>

Questo parametro non viene usato e deve essere impostato su **NULL.**

</dd> <dt>

*pvGetKeyArgument* \[ in, facoltativo\]
</dt> <dd>

Questo parametro non viene usato e deve essere impostato su **NULL.**

</dd> <dt>

*phCredential* \[ Cambio\]
</dt> <dd>

Puntatore a una [struttura CredHandle](sspi-handles.md) per ricevere l'handle delle credenziali.

</dd> <dt>

*ptsExpiry* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza delle credenziali restituite. Il valore restituito in questa **struttura TimeStamp** dipende dalla delega [*vincolata*](../secgloss/s-gly.md). Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) deve restituire questo valore nell'ora locale.

Quando si usa SSP Schannel, questo parametro è facoltativo. Quando la credenziale da usare per l'autenticazione è un certificato, questo parametro riceve l'ora di scadenza per il certificato. Se non è stato fornito alcun certificato, viene restituito un valore di tempo massimo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                 | Descrizione                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl> | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                  |
| <dl> <dt>**SEC \_ E \_ ERRORE \_ INTERNO**</dt> </dl>      | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ NESSUNA \_ CREDENZIALE**</dt> </dl>      | Nella delega vincolata non sono disponibili [*credenziali*](../secgloss/s-gly.md).<br/> |
| <dl> <dt>**SEC \_ E \_ NON \_ PROPRIETARIO**</dt> </dl>           | Il chiamante della funzione non dispone delle credenziali necessarie.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG \_ NON \_ TROVATO**</dt> </dl>   | Il pacchetto [*di sicurezza richiesto*](../secgloss/s-gly.md) non esiste.<br/>                                                                                          |
| <dl> <dt>**SEC \_ E \_ CREDENZIALI \_ SCONOSCIUTE**</dt> </dl> | Le credenziali fornite al pacchetto non sono state riconosciute.<br/>                                                                            |



 

## <a name="remarks"></a>Commenti

La **funzione AcquireCredentialsHandle (Schannel)** restituisce un handle per le credenziali di un'entità, ad esempio un utente o un client, usato da una specifica [*delega vincolata.*](../secgloss/s-gly.md) Può trattarsi dell'handle per le credenziali preesistenti oppure la funzione può creare un nuovo set di credenziali e restituirlo. Questo handle può essere usato nelle chiamate successive alle funzioni [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) e [**InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md)

In generale, **AcquireCredentialsHandle (Schannel)** non consente a un processo di ottenere un handle per le credenziali di altri utenti connessi allo stesso computer. Tuttavia, un chiamante con edizione Standard TCB NAME ha la possibilità di specificare l'identificatore di accesso \_ \_ (LUID) [](../secgloss/s-gly.md) [](../secgloss/l-gly.md) di qualsiasi token di sessione di accesso esistente per ottenere un handle per le credenziali della sessione. In genere, viene usato dai moduli in modalità kernel che devono agire per conto di un utente connesso.

Un pacchetto potrebbe chiamare la funzione in *pGetKeyFn* fornita dal trasporto in fase di esecuzione RPC. Se il trasporto non supporta la nozione di callback per recuperare le credenziali, questo parametro deve essere **NULL.**

Per i chiamanti in modalità kernel, è necessario specificare le differenze seguenti:

-   I due parametri di stringa devono essere [*stringhe Unicode.*](../secgloss/u-gly.md)
-   I valori del buffer devono essere allocati nella memoria virtuale del processo, non dal pool.

Al termine dell'uso delle credenziali restituite, liberare la memoria usata dalle credenziali chiamando la [**funzione FreeCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomi Unicode e ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

[**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
</dt> <dt>

[**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials)
</dt> <dt>

[**Funzioni SSPI**](authentication-functions.md#sspi-functions)
</dt> <dt>
 

 
