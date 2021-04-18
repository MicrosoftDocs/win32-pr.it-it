---
description: Consente al componente server di un'applicazione di trasporto di stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) tra il server e un client remoto che utilizza Schannel.
ms.assetid: 03fd5272-8476-4c93-8590-0d00acf6a130
title: Funzione AcceptSecurityContext (Schannel) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: ba353cfbe64d6471230a720680301ebab0da511a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313302"
---
# <a name="acceptsecuritycontext-schannel-function"></a>Funzione AcceptSecurityContext (Schannel)

La funzione **AcceptSecurityContext (Schannel)** consente al componente server di un'applicazione di trasporto di stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) tra il server e un client remoto. Il client remoto utilizza la funzione [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) per avviare il processo di creazione di un [*contesto di sicurezza*](../secgloss/s-gly.md). Il server può richiedere uno o più token di risposta dal client remoto per completare la creazione del [*contesto di sicurezza*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _Inout_opt_ PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsTimeStamp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phCredential* \[ in, facoltativo\]
</dt> <dd>

Handle per le credenziali del server. Il server chiama la funzione [**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md) con il flag SECPKG \_ cred \_ in ingresso o SECPKG \_ cred \_ entrambi impostati per recuperare questo handle.

</dd> <dt>

*phContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **AcceptSecurityContext (Schannel)**, questo puntatore è **null**. Nelle chiamate successive, *phContext* è l'handle per il contesto parzialmente formattato che è stato restituito nel parametro *phNewContext* dalla prima chiamata.

</dd> <dt>

*Pinput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generata da una chiamata client a [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) che contiene il descrittore del buffer di input.

Quando si usa il [*Security Support Provider*](../secgloss/s-gly.md) Schannel (SSP), il primo buffer deve essere di tipo \_ token SECBUFFER e contenere il token di sicurezza ricevuto dal client. Il secondo buffer deve essere di tipo SECBUFFER \_ vuoto.

</dd> <dt>

*fContextReq* \[ in\]
</dt> <dd>

Flag di bit che specificano gli attributi necessari al server per stabilire il contesto. I flag di bit possono essere combinati usando **operazioni OR bit per** bit. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ req \_ alloca \_ memoria**</dt> </dl> | Digest e Schannel assegnerà automaticamente i buffer di output. Al termine dell'utilizzo dei buffer di output, è possibile liberarli chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**\_ \_ riservatezza ASC req**</dt> </dl>  | Crittografare e decrittografare i messaggi.<br/> Il provider SSP digest supporta questo flag solo per SASL.<br/>                                                                                                    |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**\_connessione ASC req \_**</dt> </dl>                 | Il [*contesto di sicurezza*](../secgloss/s-gly.md) non gestirà i messaggi di formattazione.<br/>                                                                                                                                    |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_ \_ errore esteso di ASC req \_**</dt> </dl>    | Quando si verificano errori, viene inviata una notifica all'entità remota.<br/>                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**\_ \_ autenticazione reciproca ASC req \_**</dt> </dl>             | È necessario che il client fornisca un certificato da usare per l'autenticazione client.<br/>                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**\_ \_ rilevamento riesecuzione di ASC req \_**</dt> </dl>       | Rilevare i pacchetti riprodotti.<br/>                                                                                                                                                                     |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**\_ \_ rilevamento sequenza ASC \_ req**</dt> </dl> | Rilevare i messaggi ricevuti fuori sequenza.<br/>                                                                                                                                                    |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**flusso di ASC \_ req \_**</dt> </dl>                             | Supportare una connessione orientata al flusso.<br/> Questo flag è supportato solo da Schannel.<br/>                                                                                                    |



 

Per i flag di attributo possibili e i relativi significati, vedere [requisiti di contesto](context-requirements.md). I flag usati per questo parametro sono preceduti dal prefisso ASC \_ req, ad esempio, ASC \_ req \_ delegate.

Gli attributi richiesti potrebbero non essere supportati dal client. Per ulteriori informazioni, vedere il parametro *pfContextAttr* .

</dd> <dt>

*TargetDataRep* \[ in\]
</dt> <dd>

Questo parametro non viene usato con Schannel. Specificare zero per questo parametro.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **AcceptSecurityContext (Schannel)**, questo puntatore riceve il nuovo handle di contesto. Nelle chiamate successive, *phNewContext* può corrispondere all'handle specificato nel parametro *phContext* .

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene il descrittore del buffer di output. Questo buffer viene inviato al client per l'input in chiamate aggiuntive a [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md). Un buffer di output può essere generato anche se la funzione restituisce SEC \_ E \_ OK. Qualsiasi buffer generato deve essere restituito all'applicazione client.

Nell'output questo buffer riceve un token per il [*contesto di sicurezza*](../secgloss/s-gly.md). Il token deve essere inviato al client. La funzione può anche restituire un buffer di tipo SECBUFFER \_ extra. Inoltre, il chiamante deve passare un buffer di tipo **SECBUFFER \_ Alert**. Nell'output, se viene generato un avviso, questo buffer contiene informazioni sull'avviso e la funzione ha esito negativo.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un set di flag di bit che indicano gli attributi del contesto stabilito. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md). I flag usati per questo parametro sono preceduti dal prefisso ASC \_ RET, ad esempio ASC \_ ret \_ delegate.

Non controllare gli attributi correlati alla sicurezza finché la chiamata di funzione finale non viene completata correttamente. I flag di attributo non correlati alla sicurezza, ad esempio \_ il \_ flag ASC RET allocazioned \_ Memory, possono essere controllati prima della restituzione finale.

</dd> <dt>

*ptsTimeStamp* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituisca sempre questo valore nell'ora locale.

Questa opzione è facoltativa quando si usa SSP Schannel. Quando la parte remota ha fornito un certificato da usare per l'autenticazione, questo parametro riceve l'ora di scadenza per il certificato. Se non è stato fornito alcun certificato, viene restituito un valore di tempo massimo.

> [!Note]  
> Fino all'ultima chiamata del processo di autenticazione, l'ora di scadenza per il contesto può non essere corretta perché verranno fornite ulteriori informazioni durante le fasi successive della negoziazione. Pertanto, *ptsTimeStamp* deve essere **null** fino all'ultima chiamata alla funzione.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei valori seguenti.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Codice/valore restituito</th><th>Descrizione</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318L</dt> </dl></td><td>Funzione completata. I dati nel buffer di input sono incompleti. L'applicazione deve leggere i dati aggiuntivi dal client e chiamare di nuovo [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD).<br/> Quando viene restituito questo valore, il buffer <em>Pinput</em> contiene una struttura [<strong>SecBuffer</strong>] (/Windows/Win32/API/SSPI/NS-SSPI-SecBuffer) con un membro <strong>BufferType</strong> di <strong>SECBUFFER_MISSING</strong>. Il membro <strong>cbBuffer</strong> di <strong>SecBuffer</strong> contiene un valore che indica il numero di byte aggiuntivi che la funzione deve leggere dal client prima che questa funzione abbia esito positivo. Sebbene questo numero non sia sempre accurato, l'uso di questo numero può aiutare a migliorare le prestazioni evitando più chiamate a questa funzione.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>La funzione non è riuscita. La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>La funzione non è riuscita. Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>La funzione non è riuscita. L'handle passato alla funzione non è valido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>La funzione non è riuscita. Il token passato alla funzione non è valido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Accesso non riuscito.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>La funzione non è riuscita. Non è stato possibile contattare un'autorità per l'autenticazione. Questo problema può essere dovuto alle condizioni seguenti:<br/><ul><li>Il nome di dominio dell'entità di autenticazione non è corretto.</li><li>Il dominio non è disponibile.</li><li>Relazione di trust non riuscita.</li></ul></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>La funzione non è riuscita. L'handle delle credenziali specificato nel parametro <em>phCredential</em> non è valido. Questo valore può essere restituito quando si utilizza SSP digest o Schannel.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Funzione completata. Il [*contesto di sicurezza*](../secgloss/s-gly.md) ricevuto dal client è stato accettato. Se è stato generato un token di output dalla funzione, è necessario inviarlo al processo client.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>La funzione non è riuscita. Flag di attributo di contesto non valido (ASC_REQ_DELEGATE o ASC_REQ_PROMPT_FOR_CREDS) specificato nel parametro <em>fContextReq</em> .<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_APPLICATION_PROTOCOL_MISMATCH</strong></dt> <dt>0x80090367L</dt> </dl></td><td>Non esiste alcun protocollo applicativo comune tra il client e il server.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Funzione completata. Il server deve chiamare [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) e passare il token di output al client. Il server attende quindi un token restituito dal client e quindi effettua un'altra chiamata a [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD). <br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Funzione completata. Il server deve terminare la compilazione del messaggio dal client, quindi chiamare la funzione [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Funzione completata. Il server deve inviare il token di output al client e attendere un token restituito. Il token restituito deve essere passato in <em>Pinput</em> per un'altra chiamata a [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>La funzione non è riuscita. La funzione [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD) è stata chiamata dopo che è stato stabilito il contesto specificato. Questo valore può essere restituito quando si utilizza SSP del digest.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Commenti

La funzione **AcceptSecurityContext (Schannel)** è la controparte del server della funzione [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) .

Quando il server riceve una richiesta da un client, il server usa il parametro *fContextReq* per specificare cosa richiede la sessione. In questo modo, un server può specificare che i client devono essere in grado di usare una sessione riservata o controllata dall' [*integrità*](../secgloss/i-gly.md)e rifiutare i client che non sono in grado di soddisfare tale richiesta. In alternativa, un server può non richiedere alcun elemento e qualsiasi altro elemento che il client può fornire o richiede viene restituito nel parametro *pfContextAttr* .

Per un pacchetto che supporta l'autenticazione a più gambe, ad esempio l'autenticazione reciproca, la sequenza chiamante è la seguente:

1.  Il client trasmette un token al server.
2.  Il server chiama **AcceptSecurityContext (Schannel)** la prima volta, che genera un token di risposta che viene quindi inviato al client.
3.  Il client riceve il token e lo passa a [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md). Se **InitializeSecurityContext (Schannel)** restituisce sec \_ e \_ OK, l'autenticazione reciproca è stata completata ed è possibile avviare una sessione protetta. Se **InitializeSecurityContext (Schannel)** restituisce un codice di errore, termina la negoziazione di autenticazione reciproca. In caso contrario, il token di sicurezza restituito da **InitializeSecurityContext (Schannel)** viene inviato al client e i passaggi 2 e 3 vengono ripetuti.

I parametri *fContextReq* e *pfContextAttr* sono maschere di maschera che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md).

> [!Note]  
> Il parametro *pfContextAttr* è valido in caso di esito positivo, ma solo in caso di esito positivo finale è possibile esaminare i flag relativi agli aspetti di sicurezza del contesto. I ritorni intermedi possono impostare, ad esempio, \_ il \_ flag di memoria allocata RET di ISC \_ .

 

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza (crittografia) ma non è stato possibile stabilirla, è possibile che alcune applicazioni decidano immediatamente di arrestare la connessione. Se non è possibile stabilire il [*contesto di sicurezza*](../secgloss/s-gly.md) , il server deve liberare il contesto parzialmente creato chiamando la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Per informazioni sul momento in cui chiamare la funzione **DeleteSecurityContext** , vedere **DeleteSecurityContext**.

Una volta stabilito il [*contesto di sicurezza*](../secgloss/s-gly.md) , l'applicazione server può utilizzare la funzione [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) per recuperare un handle per l'account utente a cui è stato eseguito il mapping del certificato client. Inoltre, il server può utilizzare la funzione [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) per rappresentare l'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                           |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
</dt> </dl>

 

 
