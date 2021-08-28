---
description: La funzione AcquireCredentialsHandle (CredSSP) acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza.
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: Funzione AcquireCredentialsHandle (CredSSP)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 22ab5b4f9696e266e6d07b3085cafe10384e8b6b266c9e20672021fa04e97998
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101481"
---
# <a name="acquirecredentialshandle-credssp-function"></a>Funzione AcquireCredentialsHandle (CredSSP)

La **funzione AcquireCredentialsHandle (CredSSP)** acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza. Questo handle è richiesto dalle [**funzioni InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) [**e AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md) Possono essere credenziali preesistenti, stabilite tramite un accesso al sistema non descritto in questo articolo, oppure il chiamante può fornire credenziali alternative.

> [!Note]  
> Non si tratta di un "accesso alla rete" e non implica la raccolta delle credenziali.

## <a name="syntax"></a>Sintassi

```C++
SECURITY_STATUS SEC_ENTRY AcquireCredentialsHandle(
  _In_opt_   SEC_CHAR       *pszPrincipal,
  _In_       SEC_CHAR       *pszPackage,
  _In_       unsigned long  fCredentialUse,
  _In_opt_   void           *pvLogonID,
  _In_opt_   void           *pAuthData,
  _In_opt_   SEC_GET_KEY_FN pGetKeyFn,
  _Reserved_ void           *pvGetKeyArgument,
  _Out_      PCredHandle    phCredential,
  _Out_opt_  PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Parametri

*pszPrincipal* \[ in, facoltativo\]

Puntatore a una stringa con terminazione Null che specifica il nome dell'entità alle cui credenziali farà riferimento l'handle.

> [!Note]  
> Se il processo che richiede l'handle non ha accesso alle credenziali, la funzione restituisce un errore. Una stringa Null indica che il processo richiede un handle per le credenziali dell'utente nel cui contesto di sicurezza è in esecuzione.

*pszPackage* \[ Pollici\]

Puntatore a una stringa con terminazione Null che specifica il nome del pacchetto di sicurezza con cui verranno usate queste credenziali. Si tratta di un nome di pacchetto di sicurezza restituito nel **membro Name** di una [**struttura SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) restituita dalla [**funzione EnumerateSecurityPackages.**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) Dopo aver stabilito un contesto, è possibile chiamare [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) con *ulAttribute* impostato su **SECPKG \_ ATTR \_ PACKAGE \_ INFO** per restituire informazioni sul pacchetto di sicurezza in uso.

*fCredentialUse* \[ Pollici\]

Flag che indica come verranno usate queste credenziali. Questo parametro può avere uno dei valori seguenti.

| Valore                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECPKG \_ CRED \_ INBOUND**<br/>0x1  | Convalidare le credenziali del server in ingresso. Le credenziali in ingresso possono essere convalidate usando un'autorità di autenticazione quando viene chiamato [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) o [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md) Se tale autorità non è disponibile, la funzione avrà esito negativo e restituirà **SEC \_ E NO \_ \_ AUTHENTICATING \_ AUTHORITY**. La convalida è specifica del pacchetto |
| **SECPKG \_ CRED \_ IN USCITA**<br/>0x0 | Consente a una credenziale client locale di preparare un token in uscita. |

*pvLogonId* \[ in, facoltativo\]

Puntatore a un [*identificatore univoco locale*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) che identifica l'utente. Questo parametro viene fornito per i processi del file system, ad esempio i redirector di rete. Questo parametro può essere **NULL**.

*pAuthData* \[ in, facoltativo\]

Puntatore a una [**struttura \_ CRED CRED CRED che**](/windows/win32/api/credssp/ns-credssp-credssp_cred) specifica i dati di autenticazione per i pacchetti Schannel e Negotiate.

*pGetKeyFn* \[ in, facoltativo\]

Riservato. Questo parametro non viene usato e deve essere impostato su **NULL.**

*pvGetKeyArgument* \[ in, facoltativo\]

Riservato. Questo parametro deve essere impostato su **NULL.**

*phCredential* \[ Cambio\]

Puntatore alla struttura [CredHandle](sspi-handles.md) che riceverà l'handle delle credenziali.

*ptsExpiry* \[ out, facoltativo\]

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza delle credenziali restituite. Il valore della struttura ricevuto dipende dal pacchetto di sicurezza, che deve specificare il valore nell'ora locale.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **SEC \_ E \_ OK**.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                      | Descrizione                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **SEC \_ E \_ MEMORIA \_ INSUFFICIENTE** | Memoria insufficiente per completare l'azione richiesta. |
| **SEC \_ E \_ ERRORE \_ INTERNO**      | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.                |
| **SEC \_ E \_ NO \_ CREDENTIALS**      | Nel pacchetto di sicurezza non sono disponibili credenziali.                    |
| **SEC \_ E \_ NOT \_ OWNER**           | Il chiamante della funzione non dispone delle credenziali necessarie.      |
| **SEC \_ E \_ SECPKG \_ NON \_ TROVATO**   | Il pacchetto di sicurezza richiesto non esiste.                           |
| **SEC \_ E \_ CREDENZIALI \_ SCONOSCIUTE** | Le credenziali fornite al pacchetto non sono state riconosciute.             |

## <a name="remarks"></a>Commenti

La **funzione AcquireCredentialsHandle (CredSSP)** restituisce un handle alle credenziali di un'entità, ad esempio un utente o un client, usato da un pacchetto di sicurezza specifico. La funzione può restituire l'handle per le credenziali preesistenti o le credenziali appena create e restituirlo. Questo handle può essere usato nelle chiamate successive alle funzioni [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) e [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md)

In generale, **AcquireCredentialsHandle (CredSSP)** non fornisce le credenziali di altri utenti connessi allo stesso computer. Tuttavia, un chiamante edizione Standard il privilegio TCB NAME può ottenere le credenziali di una sessione di accesso esistente specificando l'identificatore di accesso \_ \_ (LUID) di tale sessione. [](../secgloss/p-gly.md#_security_privilege_gly) [](../secgloss/l-gly.md#_security_logon_identifier_gly) In genere, viene usato dai moduli in modalità kernel che devono agire per conto di un utente connesso.

Un pacchetto potrebbe chiamare la funzione in *pGetKeyFn* fornito dal trasporto di run-time RPC. Se il trasporto non supporta la nozione di callback per recuperare le credenziali, questo parametro deve essere **NULL.**

Per i chiamanti in modalità kernel, è necessario specificare le differenze seguenti:

- I due parametri di stringa devono essere [*stringhe Unicode.*](../secgloss/u-gly.md#_security_unicode_gly)
- I valori del buffer devono essere allocati nella memoria virtuale del processo, non dal pool.

Dopo aver usato le credenziali restituite, liberare la memoria usata dalle credenziali chiamando la [**funzione FreeCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato | Windows Solo \[ app desktop Vista\]                                              |
| Server minimo supportato | Windows Solo app desktop di Server 2008 \[\]                                        |
| Intestazione                   | Sspi.h (include Security.h)                                                      |
| Libreria                  | Secur32.lib                                                                      |
| DLL                      | Secur32.dll                                                                      |
| Nomi Unicode e ANSI   | **AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI) |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
- [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
