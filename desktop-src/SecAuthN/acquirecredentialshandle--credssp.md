---
description: La funzione AcquireCredentialsHandle (CredSSP) acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza.
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: Funzione AcquireCredentialsHandle (CredSSP)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 0dbece18bc7a7de8ec35764c9879380e29292e92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313299"
---
# <a name="acquirecredentialshandle-credssp-function"></a>Funzione AcquireCredentialsHandle (CredSSP)

La funzione **AcquireCredentialsHandle (CredSSP)** acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza. Questo handle è richiesto dalle funzioni [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) e [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . Possono essere *credenziali* preesistenti, stabilite tramite un accesso di sistema non descritto in questo argomento, oppure il chiamante può fornire credenziali alternative.

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

Puntatore a una stringa con terminazione null che specifica il nome dell'entità le cui credenziali faranno riferimento all'handle.

> [!Note]  
> Se il processo che richiede l'handle non ha accesso alle credenziali, la funzione restituisce un errore. Una stringa null indica che il processo richiede un handle per le credenziali dell'utente con il contesto di sicurezza in cui è in esecuzione.

*pszPackage* \[ in\]

Puntatore a una stringa con terminazione null che specifica il nome del pacchetto di sicurezza con cui verranno utilizzate queste credenziali. Nome del pacchetto di sicurezza restituito nel membro del **nome** di una struttura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) restituita dalla funzione [**EnumerateSecurityPackages**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) . Dopo aver stabilito un contesto, è possibile chiamare [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) con *UlAttribute* impostato su **SECPKG \_ attr \_ package \_ info** per restituire informazioni sul pacchetto di sicurezza in uso.

*fCredentialUse* \[ in\]

Flag che indica il modo in cui verranno utilizzate queste credenziali. Questo parametro può avere uno dei valori seguenti.

| Valore                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECPKG \_ cred in \_ ingresso**<br/>0x1  | Convalidare le credenziali del server in ingresso. Le credenziali in ingresso possono essere convalidate tramite un'autorità di autenticazione quando viene chiamato [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) o [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . Se tale autorità non è disponibile, la funzione avrà esito negativo e restituirà il **secondo \_ e \_ Nessuna \_ \_ autorità di autenticazione**. La convalida è specifica del pacchetto |
| **SECPKG \_ cred in \_ uscita**<br/>0x0 | Consentire a una credenziale client locale di preparare un token in uscita. |

*pvLogonId* \[ in, facoltativo\]

Puntatore a un [*identificatore univoco locale*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) che identifica l'utente. Questo parametro viene fornito per i processi di file System, ad esempio i redirector di rete. Questo parametro può essere **NULL**.

*pAuthData* \[ in, facoltativo\]

Puntatore a una struttura [**CredSSP \_ cred**](/windows/win32/api/credssp/ns-credssp-credssp_cred) che specifica i dati di autenticazione per i pacchetti Schannel e Negotiate.

*pGetKeyFn* \[ in, facoltativo\]

Riservato. Questo parametro non viene utilizzato e deve essere impostato su **null**.

*pvGetKeyArgument* \[ in, facoltativo\]

Riservato. Questo parametro deve essere impostato su **null**.

*phCredential* \[ out\]

Puntatore alla struttura [CredHandle](sspi-handles.md) che riceverà l'handle delle credenziali.

*ptsExpiry* \[ out, facoltativo\]

Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza delle credenziali restituite. Il valore della struttura ricevuto dipende dal pacchetto di sicurezza, che deve specificare il valore nell'ora locale.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **sec \_ E \_ OK**.

Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.

| Codice restituito                      | Descrizione                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **SEC \_ E \_ memoria insufficiente \_** | La memoria disponibile non è sufficiente per completare l'azione richiesta. |
| **\_ \_ errore interno sec \_ E**      | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.                |
| **SEC \_ E \_ Nessuna \_ credenziale**      | Nessuna credenziale disponibile nel pacchetto di sicurezza.                    |
| **SEC \_ E \_ non \_ proprietario**           | Il chiamante della funzione non ha le credenziali necessarie.      |
| **SEC \_ E \_ SECPKG \_ non \_ trovati**   | Il pacchetto di sicurezza richiesto non esiste.                           |
| **SEC \_ E \_ \_ credenziali sconosciute** | Le credenziali fornite al pacchetto non sono state riconosciute.             |

## <a name="remarks"></a>Commenti

La funzione **AcquireCredentialsHandle (CredSSP)** restituisce un handle per le credenziali di un'entità, ad esempio un utente o un client, come usato da un pacchetto di sicurezza specifico. La funzione può restituire l'handle per le credenziali preesistenti o le credenziali appena create e restituirle. Questo handle può essere usato nelle chiamate successive alle funzioni [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) e [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) .

In generale, **AcquireCredentialsHandle (CredSSP)** non fornisce le credenziali di altri utenti connessi allo stesso computer. Tuttavia, un chiamante con \_ privilegio di \_ nome [](../secgloss/p-gly.md#_security_privilege_gly) TCB è in grado di ottenere le credenziali di una sessione di accesso esistente specificando l' [*identificatore di accesso*](../secgloss/l-gly.md#_security_logon_identifier_gly) (LUID) di tale sessione. Questa operazione viene in genere utilizzata dai moduli in modalità kernel che devono agire per conto di un utente connesso.

Un pacchetto può chiamare la funzione in *pGetKeyFn* fornita dal trasporto di run-time RPC. Se il trasporto non supporta la nozione di callback per recuperare le credenziali, questo parametro deve essere **null**.

Per i chiamanti in modalità kernel, è necessario notare le differenze seguenti:

- I due parametri di stringa devono essere stringhe [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) .
- I valori del buffer devono essere allocati nella memoria virtuale del processo, non dal pool.

Al termine dell'utilizzo delle credenziali restituite, liberare la memoria utilizzata dalle credenziali chiamando la funzione [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato | \[Solo app desktop di Windows Vista\]                                              |
| Server minimo supportato | \[Solo app desktop Windows Server 2008\]                                        |
| Intestazione                   | SSPI. h (include Security. h)                                                      |
| Libreria                  | Secur32. lib                                                                      |
| DLL                      | Secur32.dll                                                                      |
| Nomi Unicode e ANSI   | **AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI) |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
- [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
