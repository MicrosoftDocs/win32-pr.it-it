---
description: Consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza tra il server e un client remoto.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: Funzione AcceptSecurityContext (CredSSP)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 681e03ea15729cc8726d63551e8b7b0a2b39ecac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312829"
---
# <a name="acceptsecuritycontext-credssp-function"></a>Funzione AcceptSecurityContext (CredSSP)

La funzione **AcceptSecurityContext (CredSSP)** consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza tra il server e un client remoto. Il client remoto chiama la funzione [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) per avviare il processo di creazione di un contesto di sicurezza. Il server può richiedere uno o più token di risposta dal client remoto per completare la creazione del contesto di sicurezza.

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

Handle per le credenziali del server. Per recuperare questo handle, il server chiama la funzione [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) con SECPKG cred in \_ \_ ingresso o SECPKG \_ cred \_ entrambi impostati flag.

*phContext* \[ in, facoltativo\]

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **AcceptSecurityContext (CredSSP)**, questo puntatore è **null**. Nelle chiamate successive, *phContext* specifica il contesto parzialmente formato restituito nel parametro *phNewContext* dalla prima chiamata.

*Pinput* \[ in, facoltativo\]

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generata da una chiamata client a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). La struttura contiene il descrittore del buffer di input.

Il primo buffer deve essere di tipo **\_ token SECBUFFER** e contenere il token di sicurezza ricevuto dal client. Il secondo buffer deve essere di tipo **SECBUFFER \_ vuoto**.

*fContextReq* \[ in\]

-Flag di bit che specificano gli attributi necessari al server per stabilire il contesto. I flag di bit possono essere combinati usando **operazioni OR bit per** bit. Il parametro può essere costituito da uno o più dei valori seguenti.

| Valore                          | Significato                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ASC \_ req \_ alloca \_ memoria** | Credential Security Support Provider (CredSSP) assegnerà i buffer di output. Al termine dell'utilizzo dei buffer di output, è possibile liberarli chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) . |
| **\_connessione ASC req \_**       | Il contesto di sicurezza non gestirà i messaggi di formattazione.                                                                                                                                                      |
| **\_delega ASC req \_**         | Il server può rappresentare il client. Ignorare questo flag per la delega vincolata.                                                         |
| **\_ \_ errore esteso di ASC req \_**  | Quando si verificano errori, viene inviata una notifica all'entità remota.                                                                                                                                                          |
| **\_ \_ rilevamento riesecuzione di ASC req \_**   | Rilevare i pacchetti riprodotti.                                                                                                                                                                                       |
| **\_ \_ rilevamento sequenza ASC \_ req** | Rilevare i messaggi ricevuti fuori sequenza.                                                                                                                                                                      |
| **flusso di ASC \_ req \_**           | Supportare una connessione orientata al flusso.                                                                                                                                                                          |

Per i flag di attributo possibili e i relativi significati, vedere [requisiti di contesto](context-requirements.md). I flag usati per questo parametro sono preceduti dal prefisso ASC \_ req, ad esempio, ASC \_ req \_ delegate.

Gli attributi richiesti potrebbero non essere supportati dal client. Per ulteriori informazioni, vedere il parametro *pfContextAttr* .

*TargetDataRep* \[ in\]

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, sulla destinazione. Questo parametro può essere una **sicurezza \_ nativa \_ DREP** o **\_ \_ DREP della rete di sicurezza**.

*phNewContext* \[ in, out, facoltativo\]

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **AcceptSecurityContext (CredSSP)**, questo puntatore riceve il nuovo handle di contesto. Nelle chiamate successive, *phNewContext* può corrispondere all'handle specificato nel parametro *phContext* .

*pOutput* \[ in, out, facoltativo\]

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene il descrittore del buffer di output. Questo buffer viene inviato al client per l'input in chiamate aggiuntive a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). Un buffer di output può essere generato anche se la funzione restituisce SEC \_ E \_ OK. Qualsiasi buffer generato deve essere restituito all'applicazione client.

Nell'output questo buffer riceve un token per il contesto di sicurezza. Il token deve essere inviato al client. La funzione può anche restituire un buffer di tipo SECBUFFER \_ extra.

*pfContextAttr* \[ out\]

Puntatore a un set di flag di bit che indicano gli attributi del contesto stabilito. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md). I flag usati per questo parametro sono preceduti dal prefisso ASC \_ RET, ad esempio ASC \_ ret \_ delegate.

Non controllare gli attributi correlati alla sicurezza finché la chiamata di funzione finale non viene completata correttamente. I flag di attributo non correlati alla sicurezza, ad esempio \_ il \_ flag ASC RET allocazioned \_ Memory, possono essere controllati prima della restituzione finale.

*ptsExpiry* \[ out, facoltativo\]

Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il pacchetto di sicurezza restituisca sempre questo valore nell'ora locale.

> [!Note]  
> Fino all'ultima chiamata del processo di autenticazione, l'ora di scadenza per il contesto può non essere corretta perché verranno fornite ulteriori informazioni durante le fasi successive della negoziazione. Pertanto, *ptsTimeStamp* deve essere **null** fino all'ultima chiamata alla funzione.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei valori seguenti.

| Codice/valore restituito                                   | Descrizione                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | Funzione completata. I dati nel buffer di input sono incompleti. L'applicazione deve leggere i dati aggiuntivi dal client e chiamare di nuovo [<strong>AcceptSecurityContext (CredSSP)</strong>](acceptsecuritycontext--credssp.md) . |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | La funzione non è riuscita. La memoria disponibile non è sufficiente per completare l'azione richiesta.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | La funzione non è riuscita. Si è verificato un errore che non è stato mappato a un codice di errore SSPI.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | La funzione non è riuscita. L'handle passato alla funzione non è valido.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | La funzione non è riuscita. Il token passato alla funzione non è valido.                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030CL                | Accesso non riuscito.                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311L | La funzione non è riuscita. Non è stato possibile contattare un'autorità per l'autenticazione. Questo problema può essere dovuto alle condizioni seguenti:<br/><ul><li>Il nome di dominio dell'entità di autenticazione non è corretto.</li><li>Il dominio non è disponibile.</li><li>Relazione di trust non riuscita. |
| SEC_E_NO_CREDENTIALS <br/>0x8009030EL               | La funzione non è riuscita. L'handle delle credenziali specificato nel parametro *phCredential* non è valido.                            |
| SEC_E_OK <br/> 0x00000000L                          | Funzione completata. Il contesto di sicurezza ricevuto dal client è stato accettato. Se la funzione ha generato un token di output, il token deve essere inviato al processo client. |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302L        | La funzione non è riuscita. Il parametro *fContextReq* ha specificato un flag di attributo di contesto (ASC_REQ_DELEGATE o ASC_REQ_PROMPT_FOR_CREDS) non valido.                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314L       | Funzione completata. Il server deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e passare il token di output al client. Il server deve quindi attendere un token restituito dal client prima di effettuare un'altra chiamata a [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md). |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313L             | Funzione completata. Il server deve terminare la compilazione del messaggio dal client prima di chiamare [ **CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312L             | Funzione completata. Il server deve inviare il token di output al client e attendere un token restituito. Il token restituito deve essere passato in *Pinput* per un'altra chiamata a [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md).


## <a name="remarks"></a>Commenti

La funzione **AcceptSecurityContext (CredSSP)** è la controparte del server della funzione [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) .

Quando il server riceve una richiesta da un client, usa il parametro *fContextReq* per specificare cosa richiede la sessione. In questo modo, un server può richiedere che i client siano in grado di usare una sessione riservata o controllata dall' [*integrità*](../secgloss/i-gly.md). può rifiutare i client che non sono in grado di soddisfare tale richiesta. In alternativa, un server può non essere necessario. qualsiasi cosa il client richiede o può fornire viene restituito nel parametro *pfContextAttr* .

I parametri *fContextReq* e *pfContextAttr* sono maschere di maschera che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md).

> [!Note]  
> Anche se il parametro *pfContextAttr* è valido in caso di esito positivo, è necessario esaminare i flag relativi agli aspetti di sicurezza del contesto solo per la restituzione finale riuscita. I ritorni intermedi possono impostare, ad esempio, \_ il \_ flag di memoria allocata RET di ISC \_ .

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza (crittografia) ma non è stato possibile stabilirla, è possibile che alcune applicazioni decidano di arrestare immediatamente la connessione. Se non è possibile stabilire il contesto di sicurezza, il server deve liberare il contesto parzialmente creato chiamando la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Per informazioni sul momento in cui chiamare la funzione **DeleteSecurityContext** , vedere **DeleteSecurityContext**.

Una volta stabilito il contesto di sicurezza, l'applicazione server può utilizzare la funzione [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) per recuperare un handle per l'account utente a cui è stato eseguito il mapping del certificato client. Inoltre, il server può utilizzare la funzione [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) per rappresentare l'utente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------|
| Client minimo supportato | \[Solo app desktop di Windows Vista\]       |
| Server minimo supportato | \[Solo app desktop Windows Server 2008\] |
| Intestazione                   | SSPI. h (include Security. h)               |
| Libreria                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vedi anche

- [Funzioni SSPI](authentication-functions.md#sspi-functions)
- [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
