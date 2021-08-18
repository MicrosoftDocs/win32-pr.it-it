---
description: Acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza che usa Kerberos.
ms.assetid: 2612bbe9-856b-4a81-bffb-6c761035883d
title: Funzione AcquireCredentialsHandle (Kerberos) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: d90cdd211d6c183ab3c405ba131ddc11be5bbab324478887f8cdbd973784852a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141574"
---
# <a name="acquirecredentialshandle-kerberos-function"></a>Funzione AcquireCredentialsHandle (Kerberos)

La **funzione AcquireCredentialsHandle (Kerberos)** acquisisce un handle per le credenziali preesistenti di un'entità [*di sicurezza*](../secgloss/s-gly.md). Questo handle è richiesto dalle [**funzioni InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) [**e AcceptSecurityContext (Kerberos).**](acceptsecuritycontext--kerberos.md) Possono essere credenziali preesistenti, stabilite tramite un accesso al sistema non descritto in questo articolo, oppure il chiamante può fornire credenziali alternative.

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

*pszPrincipal* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome dell'entità alle cui credenziali farà riferimento l'handle.

> [!Note]  
> Se il processo che richiede l'handle non ha accesso alle credenziali, la funzione restituisce un errore. Una stringa Null indica che il processo richiede un handle per le credenziali dell'utente nel cui contesto di [*sicurezza*](../secgloss/s-gly.md) è in esecuzione.

 

</dd> <dt>

*pszPackage* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del pacchetto [*di sicurezza*](../secgloss/s-gly.md) con cui verranno usate queste credenziali. Si tratta di [*un nome di pacchetto*](../secgloss/s-gly.md) di sicurezza restituito nel membro **Name** di una [**struttura SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) restituita dalla [**funzione EnumerateSecurityPackages.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) Dopo aver stabilito un contesto, è possibile chiamare [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) con *ulAttribute* impostato su SECPKG ATTR PACKAGE INFO per restituire informazioni sul pacchetto \_ di sicurezza \_ in \_ uso. [](../secgloss/s-gly.md)

</dd> <dt>

*fCredentialUse* \[ Pollici\]
</dt> <dd>

Flag che indica come verranno usate queste credenziali. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**SECPKG \_ CRED \_ BOTH**</dt> </dl>             | Convalidare una credenziale in ingresso o usare una credenziale locale per preparare un token in uscita. Questo flag abilita entrambi gli altri flag.<br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ CRED \_ INBOUND**</dt> </dl>    | Convalidare le credenziali del server in ingresso. Le credenziali in ingresso possono essere convalidate usando un'autorità di autenticazione quando viene chiamato [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) o [**AcceptSecurityContext (Kerberos).**](acceptsecuritycontext--kerberos.md) Se tale autorità non è disponibile, la funzione avrà esito negativo e restituirà SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY. La convalida è specifica del pacchetto.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ CRED \_ IN USCITA**</dt> </dl> | Consente a una credenziale client locale di preparare un token in uscita.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*pvLogonID* \[ Pollici\]
</dt> <dd>

Puntatore a un [*identificatore univoco locale*](../secgloss/l-gly.md) (LUID) che identifica l'utente. Questo parametro viene fornito per i processi del file system, ad esempio i redirector di rete. Questo parametro può essere **NULL**.

</dd> <dt>

*pAuthData* \[ Pollici\]
</dt> <dd>

Puntatore a dati specifici del pacchetto. Questo parametro può essere **NULL,** a indicare che [](../secgloss/s-gly.md) è necessario utilizzare le credenziali predefinite per il pacchetto di sicurezza. Per usare le credenziali fornite, passare una [**struttura SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) che include tali credenziali in questo parametro. Il tempo di esecuzione RPC passa qualsiasi valore fornito in [**RpcBindingSetAuthInfo.**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)

</dd> <dt>

*pGetKeyFn* \[ Pollici\]
</dt> <dd>

Questo parametro non viene usato e deve essere impostato su **NULL.**

</dd> <dt>

*pvGetKeyArgument* \[ Pollici\]
</dt> <dd>

Questo parametro non viene usato e deve essere impostato su **NULL.**

</dd> <dt>

*phCredential* \[ Cambio\]
</dt> <dd>

Puntatore a una [struttura CredHandle](sspi-handles.md) per ricevere l'handle delle credenziali.

</dd> <dt>

*ptsExpiry* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza delle credenziali restituite. Il valore restituito in questa **struttura TimeStamp** dipende dalla delega [*vincolata*](../secgloss/s-gly.md). Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) deve restituire questo valore nell'ora locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                 | Descrizione                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl> | Memoria insufficiente per completare l'azione richiesta.<br/>                                                                  |
| <dl> <dt>**SEC \_ E \_ ERRORE \_ INTERNO**</dt> </dl>      | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>      | Nessuna credenziale disponibile nella delega [*vincolata*](../secgloss/s-gly.md).<br/> |
| <dl> <dt>**SEC \_ E \_ NOT \_ OWNER**</dt> </dl>           | Il chiamante della funzione non dispone delle credenziali necessarie.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG \_ NON \_ TROVATO**</dt> </dl>   | Il pacchetto [*di sicurezza richiesto*](../secgloss/s-gly.md) non esiste.<br/>                                                                                          |
| <dl> <dt>**SEC \_ E \_ CREDENZIALI \_ SCONOSCIUTE**</dt> </dl> | Le credenziali fornite al pacchetto non sono state riconosciute.<br/>                                                                            |



 

## <a name="remarks"></a>Commenti

La **funzione AcquireCredentialsHandle (Kerberos)** restituisce un handle alle credenziali di un'entità, ad esempio un utente o un client, usato da una delega [*vincolata specifica.*](../secgloss/s-gly.md) Può trattarsi dell'handle per le credenziali preesistenti oppure la funzione può creare un nuovo set di credenziali e restituirlo. Questo handle può essere usato nelle chiamate successive alle funzioni [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) e [**InitializeSecurityContext (Kerberos).**](initializesecuritycontext--kerberos.md)

In generale, **AcquireCredentialsHandle (Kerberos)** non consente a un processo di ottenere un handle per le credenziali di altri utenti connessi allo stesso computer. Tuttavia, un chiamante con il privilegio TCB NAME di edizione Standard ha la possibilità di specificare l'identificatore di accesso \_ \_ (LUID) [](../secgloss/s-gly.md) [](../secgloss/l-gly.md) di qualsiasi token di sessione di accesso esistente per ottenere un handle per le credenziali della sessione. In genere, viene usato dai moduli in modalità kernel che devono agire per conto di un utente connesso.

Un pacchetto potrebbe chiamare la funzione in *pGetKeyFn* fornito dal trasporto di run-time RPC. Se il trasporto non supporta la nozione di callback per recuperare le credenziali, questo parametro deve essere **NULL.**

Per i chiamanti in modalità kernel, è necessario specificare le differenze seguenti:

-   I due parametri di stringa devono essere [*stringhe Unicode.*](../secgloss/u-gly.md)
-   I valori del buffer devono essere allocati nella memoria virtuale del processo, non dal pool.

Dopo aver usato le credenziali restituite, liberare la memoria usata dalle credenziali chiamando la [**funzione FreeCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (includere Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomi Unicode e ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
