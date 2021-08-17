---
description: Consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza tra il server e un client remoto che utilizza Schannel. [](../secgloss/s-gly.md)
ms.assetid: 03fd5272-8476-4c93-8590-0d00acf6a130
title: Funzione AcceptSecurityContext (Schannel) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 2700704c9fc1c40fc2d5648306147c5091a318e5c8bd4383bb32bc5416c8d069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141644"
---
# <a name="acceptsecuritycontext-schannel-function"></a>Funzione AcceptSecurityContext (Schannel)

La **funzione AcceptSecurityContext (Schannel)** consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza [*tra*](../secgloss/s-gly.md) il server e un client remoto. Il client remoto usa la [**funzione InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) per avviare il processo di definizione di un contesto [*di sicurezza.*](../secgloss/s-gly.md) Il server può richiedere uno o più token di risposta dal client remoto per completare la definizione del contesto [*di sicurezza*](../secgloss/s-gly.md).

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

Handle per le credenziali del server. Il server chiama la [**funzione AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md) con il \_ flag SECPKG CRED INBOUND o \_ SECPKG CRED BOTH impostato per recuperare \_ questo \_ handle.

</dd> <dt>

*phContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata ad **AcceptSecurityContext (Schannel)** questo puntatore è **NULL.** Nelle chiamate *successive, phContext* è l'handle per il contesto parzialmente formato restituito nel *parametro phNewContext* dalla prima chiamata.

</dd> <dt>

*pInput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generata da una chiamata client a [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) che contiene il descrittore del buffer di input.

Quando si usa SSP [*(Security Support Provider)*](../secgloss/s-gly.md) Schannel, il primo buffer deve essere di tipo SECBUFFER TOKEN e contenere il \_ token di sicurezza ricevuto dal client. Il secondo buffer deve essere di tipo SECBUFFER \_ EMPTY.

</dd> <dt>

*fContextReq* \[ Pollici\]
</dt> <dd>

Flag di bit che specificano gli attributi richiesti dal server per stabilire il contesto. I flag di bit possono essere combinati usando operazioni **OR** bit per bit. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ REQ \_ ALLOCATE \_ MEMORY**</dt> </dl> | Digest e Schannel allocano automaticamente i buffer di output. Dopo aver terminato di usare i buffer di output, liberarli chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**RISERVATEZZA DI ASC \_ REQ \_**</dt> </dl>  | Crittografare e decrittografare i messaggi.<br/> Digest SSP supporta questo flag solo per SASL.<br/>                                                                                                    |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**CONNESSIONE ASC \_ \_ REQ**</dt> </dl>                 | Il [*contesto di sicurezza non*](../secgloss/s-gly.md) gestirà i messaggi di formattazione.<br/>                                                                                                                                    |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ASC \_ REQ \_ EXTENDED \_ ERROR**</dt> </dl>    | Quando si verificano errori, l'entità remota riceverà una notifica.<br/>                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**AUTENTICAZIONE RECIPROCA \_ ASC REQ \_ \_**</dt> </dl>             | Il client deve fornire un certificato da usare per l'autenticazione client.<br/>                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>       | Rilevare i pacchetti riprodotti.<br/>                                                                                                                                                                     |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl> | Rilevare i messaggi ricevuti fuori sequenza.<br/>                                                                                                                                                    |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**FLUSSO \_ REQ ASC \_**</dt> </dl>                             | Supportare una connessione orientata al flusso.<br/> Questo flag è supportato solo da Schannel.<br/>                                                                                                    |



 

Per i flag di attributo possibili e i relativi significati, vedere [Requisiti di contesto.](context-requirements.md) I flag usati per questo parametro sono preceduti dal prefisso ASC \_ REQ, ad esempio ASC \_ REQ \_ DELEGATE.

Gli attributi richiesti potrebbero non essere supportati dal client. Per altre informazioni, vedere il *parametro pfContextAttr.*

</dd> <dt>

*TargetDataRep* \[ Pollici\]
</dt> <dd>

Questo parametro non viene usato con Schannel. Specificare zero per questo parametro.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata ad **AcceptSecurityContext (Schannel),** questo puntatore riceve il nuovo handle di contesto. Nelle chiamate successive, *phNewContext* può essere uguale all'handle specificato nel *parametro phContext.*

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene il descrittore del buffer di output. Questo buffer viene inviato al client per l'input in chiamate aggiuntive a [**InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md) Un buffer di output può essere generato anche se la funzione restituisce SEC \_ E \_ OK. Qualsiasi buffer generato deve essere inviato nuovamente all'applicazione client.

Nell'output, questo buffer riceve un token per il contesto [*di sicurezza*](../secgloss/s-gly.md). Il token deve essere inviato al client. La funzione può anche restituire un buffer di tipo SECBUFFER \_ EXTRA. Inoltre, il chiamante deve passare un buffer di tipo **SECBUFFER \_ ALERT**. Nell'output, se viene generato un avviso, questo buffer contiene informazioni sull'avviso e la funzione ha esito negativo.

</dd> <dt>

*pfContextAttr* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un set di flag di bit che indicano gli attributi del contesto stabilito. Per una descrizione dei vari attributi, vedere [Requisiti di contesto.](context-requirements.md) I flag usati per questo parametro sono preceduti dal prefisso ASC \_ RET, ad esempio ASC \_ RET \_ DELEGATE.

Non verificare la presenza di attributi correlati alla sicurezza fino a quando la chiamata di funzione finale non viene restituita correttamente. I flag di attributo non correlati alla sicurezza, ad esempio il flag ASC RET ALLOCATED MEMORY, possono essere controllati \_ \_ prima della restituzione \_ finale.

</dd> <dt>

*ptsTimeStamp* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituirà sempre questo valore nell'ora locale.

Questo è facoltativo quando si usa SSP Schannel. Quando l'entità remota ha fornito un certificato da usare per l'autenticazione, questo parametro riceve l'ora di scadenza del certificato. Se non è stato fornito alcun certificato, viene restituito un valore di tempo massimo.

> [!Note]  
> Fino all'ultima chiamata del processo di autenticazione, l'ora di scadenza del contesto può non essere corretta perché verranno fornite altre informazioni durante le fasi successive della negoziazione. Pertanto, *ptsTimeStamp* deve essere **NULL** fino all'ultima chiamata alla funzione.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei valori seguenti.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Codice/valore restituito</th><th>Descrizione</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318L</dt> </dl></td><td>Funzione completata. I dati nel buffer di input sono incompleti. L'applicazione deve leggere dati aggiuntivi dal client e chiamare di nuovo [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md).<br/> Quando viene restituito questo valore, il buffer <em>pInput</em> contiene una struttura [<strong>SecBuffer</strong>](/windows/win32/api/sspi/ns-sspi-secbuffer) con un membro <strong>BufferType</strong> <strong>di SECBUFFER_MISSING</strong>. Il <strong>membro cbBuffer</strong> di <strong>SecBuffer</strong> contiene un valore che indica il numero di byte aggiuntivi che la funzione deve leggere dal client prima che questa funzione riesca. Anche se questo numero non è sempre accurato, l'uso di questo valore può migliorare le prestazioni evitando più chiamate a questa funzione.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>La funzione non è riuscita. Memoria insufficiente per completare l'azione richiesta.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>La funzione non è riuscita. Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>La funzione non è riuscita. L'handle passato alla funzione non è valido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>La funzione non è riuscita. Il token passato alla funzione non è valido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Accesso non riuscito.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>La funzione non è riuscita. Non è stato possibile contattare alcuna autorità per l'autenticazione. Ciò potrebbe essere dovuto alle condizioni seguenti:<br/><ul><li>Il nome di dominio dell'entità di autenticazione non è corretto.</li><li>Il dominio non è disponibile.</li><li>La relazione di trust non è riuscita.</li></ul></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>La funzione non è riuscita. L'handle di credenziali specificato <em>nel parametro phCredential</em> non è valido. Questo valore può essere restituito quando si usa lo SSP Digest o Schannel.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Funzione completata. Il [*contesto di*](../secgloss/s-gly.md) sicurezza ricevuto dal client è stato accettato. Se un token di output è stato generato dalla funzione, deve essere inviato al processo client.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>La funzione non è riuscita. Un flag di attributo di contesto non valido (ASC_REQ_DELEGATE o ASC_REQ_PROMPT_FOR_CREDS) è stato specificato nel <em>parametro fContextReq.</em><br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_APPLICATION_PROTOCOL_MISMATCH</strong></dt> <dt>0x80090367L</dt> </dl></td><td>Non esiste alcun protocollo applicativo comune tra il client e il server.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Funzione completata. Il server deve chiamare [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e passare il token di output al client. Il server attende quindi un token restituito dal client e quindi esegue un'altra chiamata a [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md). <br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Funzione completata. Il server deve completare la compilazione del messaggio dal client e quindi chiamare la funzione [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Funzione completata. Il server deve inviare il token di output al client e attendere un token restituito. Il token restituito deve essere passato in <em>pInput</em> per un'altra chiamata a [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>La funzione non è riuscita. La funzione [<strong>AcceptSecurityContext (Schannel)</strong>](acceptsecuritycontext--schannel.md) è stata chiamata dopo che è stato stabilito il contesto specificato. Questo valore può essere restituito quando si usa il provider di servizi di servizi di gestione digest.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Commenti

La **funzione AcceptSecurityContext (Schannel)** è la controparte server della [**funzione InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md)

Quando il server riceve una richiesta da un client, usa il parametro *fContextReq* per specificare gli elementi necessari per la sessione. In questo modo, un server può specificare che i [](../secgloss/i-gly.md)client devono essere in grado di utilizzare una sessione riservata o verificata dall'integrità e può rifiutare i client che non possono soddisfare tale richiesta. In alternativa, un server non può richiedere nulla e qualsiasi elemento che il client può fornire o richiede viene restituito nel *parametro pfContextAttr.*

Per un pacchetto che supporta l'autenticazione a più livelli, ad esempio l'autenticazione reciproca, la sequenza di chiamata è la seguente:

1.  Il client trasmette un token al server.
2.  Il server chiama **AcceptSecurityContext (Schannel)** la prima volta, che genera un token di risposta che viene quindi inviato al client.
3.  Il client riceve il token e lo passa a [**InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md) Se **InitializeSecurityContext (Schannel)** restituisce SEC \_ E OK, l'autenticazione reciproca è stata completata e può iniziare \_ una sessione protetta. Se **InitializeSecurityContext (Schannel) restituisce un** codice di errore, la negoziazione dell'autenticazione reciproca termina. In caso contrario, il token di sicurezza restituito da **InitializeSecurityContext (Schannel)** viene inviato al client e i passaggi 2 e 3 vengono ripetuti.

I *parametri fContextReq* e *pfContextAttr* sono maschera di bit che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [Requisiti di contesto.](context-requirements.md)

> [!Note]  
> Il *parametro pfContextAttr* è valido in caso di esito positivo, ma solo in caso di esito positivo finale è necessario esaminare i flag relativi agli aspetti di sicurezza del contesto. I valori restituiti intermedi possono impostare, ad esempio, il flag ISC \_ RET \_ ALLOCATED \_ MEMORY.

 

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, la riservatezza (crittografia) è stata richiesta, ma non è stato possibile stabilirlo, alcune applicazioni potrebbero scegliere di arrestare immediatamente la connessione. Se non [*è possibile*](../secgloss/s-gly.md) stabilire il contesto di sicurezza, il server deve liberare il contesto creato parzialmente chiamando la [**funzione DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) Per informazioni su quando chiamare la **funzione DeleteSecurityContext,** vedere **DeleteSecurityContext.**

Dopo aver [*stabilito il contesto*](../secgloss/s-gly.md) di sicurezza, l'applicazione server può usare la funzione [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) per recuperare un handle per l'account utente a cui è stato eseguito il mapping del certificato client. Inoltre, il server può usare la [**funzione ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) per rappresentare l'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (includere Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
</dt> </dl>

 

 
