---
description: Consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza tra il server e un client remoto.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: Funzione AcceptSecurityContext (CredSSP)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: df4c87274c3a19d9e4a028cde813801688ce1927d1a0b89dbe3a7e8633ce8b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141694"
---
# <a name="acceptsecuritycontext-credssp-function"></a>Funzione AcceptSecurityContext (CredSSP)

La **funzione AcceptSecurityContext (CredSSP)** consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza tra il server e un client remoto. Il client remoto chiama la [**funzione InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) per avviare il processo di definizione di un contesto di sicurezza. Il server può richiedere uno o più token di risposta dal client remoto per completare la definizione del contesto di sicurezza.

## <a name="syntax"></a>Sintassi

```C++
SECURITY_STATUS SEC_ENTRY AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        unsigned long  fContextReq,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Parametri

*phCredential* \[ in, facoltativo\]

Handle per le credenziali del server. Per recuperare questo handle, il server chiama la funzione [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) con il set di flag SECPKG \_ CRED INBOUND o \_ SECPKG \_ CRED \_ BOTH.

*phContext* \[ in, facoltativo\]

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Nella prima chiamata ad **AcceptSecurityContext (CredSSP)** questo puntatore è **NULL.** Nelle chiamate successive, *phContext* specifica il contesto parzialmente formato restituito nel *parametro phNewContext* dalla prima chiamata.

*pInput* \[ in, facoltativo\]

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generata da una chiamata client a [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) La struttura contiene il descrittore del buffer di input.

Il primo buffer deve essere di tipo **SECBUFFER \_ TOKEN** e contenere il token di sicurezza ricevuto dal client. Il secondo buffer deve essere di tipo **SECBUFFER \_ EMPTY.**

*fContextReq* \[ Pollici\]

Flag di bit che specificano gli attributi richiesti dal server per stabilire il contesto. I flag di bit possono essere combinati usando operazioni **OR** bit per bit. Questo parametro può essere uno o più dei valori seguenti.

| Valore                          | Significato                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ASC \_ REQ \_ ALLOCATE \_ MEMORY** | Credential Security Support Provider (CredSSP) alloca i buffer di output. Dopo aver terminato di usare i buffer di output, liberarli chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) |
| **CONNESSIONE ASC \_ \_ REQ**       | Il contesto di sicurezza non gestirà i messaggi di formattazione.                                                                                                                                                      |
| **DELEGATO ASC \_ REQ \_**         | Il server può rappresentare il client. Ignorare questo flag per la delega vincolata.                                                         |
| **ASC \_ REQ \_ EXTENDED \_ ERROR**  | Quando si verificano errori, l'entità remota riceverà una notifica.                                                                                                                                                          |
| **ASC \_ REQ \_ REPLAY \_ DETECT**   | Rilevare i pacchetti riprodotti.                                                                                                                                                                                       |
| **ASC \_ REQ \_ SEQUENCE \_ DETECT** | Rilevare i messaggi ricevuti fuori sequenza.                                                                                                                                                                      |
| **FLUSSO \_ REQ ASC \_**           | Supportare una connessione orientata al flusso.                                                                                                                                                                          |

Per i flag di attributo possibili e i relativi significati, vedere [Requisiti di contesto.](context-requirements.md) I flag usati per questo parametro sono preceduti dal prefisso ASC \_ REQ, ad esempio ASC \_ REQ \_ DELEGATE.

Gli attributi richiesti potrebbero non essere supportati dal client. Per altre informazioni, vedere il *parametro pfContextAttr.*

*TargetDataRep* \[ Pollici\]

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, nella destinazione. Questo parametro può essere **SECURITY \_ NATIVE \_ DREP** o **SECURITY NETWORK \_ \_ DREP.**

*phNewContext* \[ in, out, facoltativo\]

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata ad **AcceptSecurityContext (CredSSP),** questo puntatore riceve il nuovo handle di contesto. Nelle chiamate successive, *phNewContext* può essere uguale all'handle specificato nel *parametro phContext.*

*pOutput* \[ in, out, facoltativo\]

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene il descrittore del buffer di output. Questo buffer viene inviato al client per l'input in chiamate aggiuntive a [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) Un buffer di output può essere generato anche se la funzione restituisce SEC \_ E \_ OK. Qualsiasi buffer generato deve essere inviato nuovamente all'applicazione client.

Nell'output questo buffer riceve un token per il contesto di sicurezza. Il token deve essere inviato al client. La funzione può anche restituire un buffer di tipo SECBUFFER \_ EXTRA.

*pfContextAttr* \[ Cambio\]

Puntatore a un set di flag di bit che indicano gli attributi del contesto stabilito. Per una descrizione dei vari attributi, vedere [Requisiti di contesto.](context-requirements.md) I flag usati per questo parametro sono preceduti dal prefisso ASC \_ RET, ad esempio ASC \_ RET \_ DELEGATE.

Non verificare la presenza di attributi correlati alla sicurezza fino a quando la chiamata di funzione finale non viene restituita correttamente. I flag di attributo non correlati alla sicurezza, ad esempio il flag ASC RET ALLOCATED MEMORY, possono essere controllati \_ \_ prima della restituzione \_ finale.

*ptsExpiry* \[ out, facoltativo\]

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il pacchetto di sicurezza restituirà sempre questo valore nell'ora locale.

> [!Note]  
> Fino all'ultima chiamata del processo di autenticazione, l'ora di scadenza del contesto può non essere corretta perché verranno fornite altre informazioni durante le fasi successive della negoziazione. Pertanto, *ptsTimeStamp* deve essere **NULL** fino all'ultima chiamata alla funzione.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei valori seguenti.

| Codice/valore restituito                                   | Descrizione                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | Funzione completata. I dati nel buffer di input sono incompleti. L'applicazione deve leggere dati aggiuntivi dal client e [<strong>chiamare di nuovo AcceptSecurityContext (CredSSP).</strong>](acceptsecuritycontext--credssp.md) |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | La funzione non è riuscita. Memoria insufficiente per completare l'azione richiesta.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | La funzione non è riuscita. Si è verificato un errore che non è stato mappato a un codice di errore SSPI.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | La funzione non è riuscita. L'handle passato alla funzione non è valido.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | La funzione non è riuscita. Il token passato alla funzione non è valido.                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030CL                | Accesso non riuscito.                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311L | La funzione non è riuscita. Non è stato possibile contattare alcuna autorità per l'autenticazione. Ciò potrebbe essere dovuto alle condizioni seguenti:<br/><ul><li>Il nome di dominio dell'entità di autenticazione non è corretto.</li><li>Il dominio non è disponibile.</li><li>La relazione di trust non è riuscita. |
| SEC_E_NO_CREDENTIALS <br/>0x8009030EL               | La funzione non è riuscita. L'handle di credenziali specificato *nel parametro phCredential* non è valido.                            |
| SEC_E_OK <br/> 0x00000000L                          | Funzione completata. Il contesto di sicurezza ricevuto dal client è stato accettato. Se la funzione ha generato un token di output, il token deve essere inviato al processo client. |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302L        | La funzione non è riuscita. Il *parametro fContextReq* ha specificato un flag di attributo di contesto (ASC_REQ_DELEGATE o ASC_REQ_PROMPT_FOR_CREDS) non valido.                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314L       | Funzione completata. Il server deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e passare il token di output al client. Il server deve quindi attendere un token restituito dal client prima di effettuare un'altra chiamata ad [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md) |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313L             | Funzione completata. Il server deve completare la compilazione del messaggio dal client prima di [ **chiamare CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312L             | Funzione completata. Il server deve inviare il token di output al client e attendere un token restituito. Il token restituito deve essere passato in *pInput per* un'altra chiamata ad [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md)


## <a name="remarks"></a>Commenti

La **funzione AcceptSecurityContext (CredSSP)** è la controparte server della [**funzione InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md)

Quando il server riceve una richiesta da un client, usa il parametro *fContextReq* per specificare gli elementi necessari per la sessione. In questo modo, un server può richiedere che i client siano in grado di usare una sessione riservata [*o verificata*](../secgloss/i-gly.md)dall'integrità; può rifiutare i client che non possono soddisfare tale richiesta. In alternativa, un server non può richiedere nulla. qualsiasi elemento richiesto o fornito dal client viene restituito nel *parametro pfContextAttr.*

I *parametri fContextReq* e *pfContextAttr* sono maschera di bit che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [Requisiti di contesto.](context-requirements.md)

> [!Note]  
> Anche se *il parametro pfContextAttr* è valido in caso di esito positivo, è consigliabile esaminare i flag relativi agli aspetti di sicurezza del contesto solo sul risultato finale con esito positivo. I valori restituiti intermedi possono impostare, ad esempio, il flag ISC \_ RET \_ ALLOCATED \_ MEMORY.

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Ad esempio, se la riservatezza (crittografia) è stata richiesta ma non è stato possibile stabilire, alcune applicazioni possono scegliere di arrestare immediatamente la connessione. Se non è possibile stabilire il contesto di sicurezza, il server deve liberare il contesto creato parzialmente chiamando la [**funzione DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) Per informazioni su quando chiamare la **funzione DeleteSecurityContext,** vedere **DeleteSecurityContext.**

Dopo aver stabilito il contesto di sicurezza, l'applicazione server può usare la [**funzione QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) per recuperare un handle per l'account utente a cui è stato eseguito il mapping del certificato client. Inoltre, il server può usare la [**funzione ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) per rappresentare l'utente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | Windows solo \[ app desktop vista\]       |
| Server minimo supportato | Windows Solo app desktop di Server 2008 \[\] |
| Intestazione                   | Sspi.h (includere Security.h)               |
| Libreria                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
