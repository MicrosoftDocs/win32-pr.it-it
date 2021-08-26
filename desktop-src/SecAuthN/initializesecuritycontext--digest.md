---
description: Avvia il contesto di sicurezza in uscita [*sul*](../secgloss/s-gly.md) lato client da un handle di credenziali usando la delega [*vincolata digest.*](../secgloss/s-gly.md)
ms.assetid: 4b482dcc-3878-4bc6-85e4-229a1726cecc
title: Funzione InitializeSecurityContext (Digest) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f09baebb4419da9b90dd6b0585788c5c7993c09d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467318"
---
# <a name="initializesecuritycontext-digest-function"></a>Funzione InitializeSecurityContext (Digest)

La **funzione InitializeSecurityContext (Digest)** avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali. La funzione viene usata per compilare un [*contesto di sicurezza*](../secgloss/s-gly.md) tra l'applicazione client e un peer remoto. **InitializeSecurityContext (Digest)** restituisce un token che il client deve passare al peer remoto, che il peer a sua volta invia all'implementazione della sicurezza locale tramite la chiamata [**AcceptSecurityContext (Digest).**](acceptsecuritycontext--digest.md) Il token generato deve essere considerato opaco da tutti i chiamanti.

In genere, la **funzione InitializeSecurityContext (Digest)** viene chiamata in un ciclo fino a quando non viene stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) sufficiente.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phCredential* \[ in, facoltativo\]
</dt> <dd>

Handle per le credenziali restituite da [**AcquireCredentialsHandle (Digest).**](acquirecredentialshandle--digest.md) Questo handle viene utilizzato per compilare il [*contesto di sicurezza*](../secgloss/s-gly.md). La **funzione InitializeSecurityContext (Digest)** richiede almeno credenziali OUTBOUND.

</dd> <dt>

*phContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata a **InitializeSecurityContext (Digest)**, questo puntatore è **NULL.** Nella seconda chiamata questo parametro è un puntatore all'handle al contesto parzialmente formato restituito nel parametro *phNewContext* dalla prima chiamata.

Questo parametro è facoltativo e può essere impostato su **NULL.**

</dd> <dt>

*pszTargetName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica in modo univoco l'URI della risorsa richiesta. La stringa deve essere composta da caratteri consentiti in un URI e deve essere rappresentabile dal set di codice ASCII degli Stati Uniti. La codifica percentuale può essere usata per rappresentare i caratteri esterni al set di codice ASCII degli Stati Uniti.

</dd> <dt>

*fContextReq* \[ Pollici\]
</dt> <dd>

Flag di bit che indicano le richieste per il contesto. Non tutti i pacchetti possono supportare tutti i requisiti. I flag usati per questo parametro sono preceduti dal prefisso ISC \_ \_ REQ, ad esempio ISC \_ REQ \_ DELEGATE. Questo parametro può essere uno o più dei flag di attributi seguenti.




| valore | Significato | 
|-------|---------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl><dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt></dl> | Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) alloca automaticamente i buffer di output. Dopo aver terminato di usare i buffer di output, liberarli chiamando la [<strong>funzione FreeContextBuffer.</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br /> | 
| <span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl><dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt></dl> | Crittografare i messaggi [<strong>usando la funzione EncryptMessage.</strong>](encryptmessage--general.md)<br /> | 
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl><dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt></dl> | Quando si verificano errori, l'entità remota riceverà una notifica.<br /> | 
| <span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl><dt><strong>ISC_REQ_HTTP</strong></dt></dl> | Usare digest per HTTP. Omettere questo flag per usare digest come meccanismo SASL.<br /> | 
| <span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl><dt><strong>ISC_REQ_INTEGRITY</strong></dt></dl> | Firmare i messaggi e verificare le firme usando [<strong>le funzioni EncryptMessage</strong>](encryptmessage--general.md) [<strong>e MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl><dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt></dl> | Verranno soddisfatti i criteri di autenticazione reciproca del servizio.<br /><blockquote>[!Caution]<br />Ciò non significa necessariamente che viene eseguita l'autenticazione reciproca, ma solo che vengono soddisfatti i criteri di autenticazione del servizio. Per assicurarsi che l'autenticazione reciproca sia eseguita, chiamare [<strong>la funzione QueryContextAttributes (Digest).</strong>](querycontextattributes--digest.md)</blockquote><br /> | 
| <span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl><dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt></dl> | Rilevare i messaggi riprodotti che sono stati codificati usando le [<strong>funzioni EncryptMessage</strong>](encryptmessage--general.md) [<strong>o MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl><dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt></dl> | Rilevare i messaggi ricevuti fuori sequenza.<br /> | 
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl><dt><strong>ISC_REQ_STREAM</strong></dt></dl> | Supportare una connessione orientata al flusso.<br /> | 




 

Gli attributi richiesti potrebbero non essere supportati dal client. Per altre informazioni, vedere il *parametro pfContextAttr.*

Per altre descrizioni dei vari attributi, vedere Requisiti [di contesto.](context-requirements.md)

</dd> <dt>

*Riservato1* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*TargetDataRep* \[ Pollici\]
</dt> <dd>

Questo parametro non viene usato con digest. Impostarlo su zero.

</dd> <dt>

*pInput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a [**una struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori ai buffer forniti come input per il pacchetto. A meno che il contesto client non sia stato avviato dal server, il valore di questo parametro deve essere **NULL** alla prima chiamata alla funzione. Nelle chiamate successive alla funzione o quando il contesto client è stato avviato dal server, il valore di questo parametro è un puntatore a un buffer allocato con memoria sufficiente per contenere il token restituito dal computer remoto.

Per informazioni sulla configurazione del buffer, vedere [Buffer di input per la risposta alla richiesta di digest.](input-buffers-for-the-digest-challenge-response.md)

</dd> <dt>

*Riservato2* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata a **InitializeSecurityContext (Digest)** questo puntatore riceve il nuovo handle di contesto. Nella seconda chiamata, *phNewContext* può essere uguale all'handle specificato nel *parametro phContext.*

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori alla [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che riceve i dati di output. Se un buffer è stato digitato come SEC \_ READWRITE nell'input, sarà presente nell'output. Il sistema alloca un buffer per il token di sicurezza, se richiesto (tramite ISC REQ ALLOCATE MEMORY) e inserisce l'indirizzo nel descrittore del buffer per \_ \_ il token di \_ sicurezza.

Questo parametro riceve la risposta alla richiesta di richiesta che deve essere inviata al server.

</dd> <dt>

*pfContextAttr* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile per ricevere un set di flag di bit che indicano [*gli attributi*](../secgloss/a-gly.md#_security_attribute_gly) del contesto stabilito. Per una descrizione dei vari attributi, vedere [Requisiti di contesto.](context-requirements.md)

I flag usati per questo parametro sono preceduti dal prefisso ISC \_ RET, ad esempio ISC \_ RET \_ DELEGATE. Per un elenco di valori validi, vedere il *parametro fContextReq.*

Non verificare la presenza di attributi correlati alla sicurezza fino a quando la chiamata di funzione finale non viene restituita correttamente. I flag di attributo non correlati alla sicurezza, ad esempio il flag ASC RET ALLOCATED MEMORY, possono essere controllati \_ \_ prima della restituzione \_ finale.

> [!Note]  
> Particolari attributi di contesto possono cambiare durante la negoziazione con un peer remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza del contesto.

Non esiste alcuna scadenza per le credenziali Microsoft Digest contesto [*di*](../secgloss/s-gly.md)sicurezza SSP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce uno dei codici di esito positivo seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Il [*contesto di sicurezza*](../secgloss/s-gly.md) è stato inizializzato correttamente. Non è necessaria [**un'altra chiamata InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Se la funzione restituisce un token di output, ad esempio se IL TOKEN SECBUFFER \_ in *pOutput* è di lunghezza diversa da zero, tale token deve essere inviato al server.<br/> |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Il client deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e quindi passare l'output al server. Il client attende quindi un token restituito e lo passa, in un'altra chiamata, a [**InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md)<br/>                                                                                                                                  |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | Il client deve completare la compilazione del messaggio e quindi chiamare [**la funzione CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Il client deve inviare il token di output al server e attendere un token restituito. Il token restituito viene quindi passato in un'altra chiamata [**a InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Il token di output può essere vuoto.<br/>                                                                                                                                                       |
| <dl> <dt>**SEC \_ I \_ CREDENZIALI INCOMPLETE \_**</dt> </dl> | Usare con Schannel. Il server ha richiesto l'autenticazione client e le credenziali fornite non includono un certificato o il certificato non è stato emesso da un'autorità di certificazione (CA) attendibile dal server. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                            |



 

Se la funzione ha esito negativo, la funzione restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl>          | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERRORE \_ INTERNO SEC E \_ \_**</dt> </dl>               | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**HANDLE \_ SEC E NON \_ \_ VALIDO**</dt> </dl>               | L'handle passato alla funzione non è valido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**TOKEN \_ SEC E NON \_ \_ VALIDO**</dt> </dl>                | L'errore è dovuto a un token di input in formato non valido, ad esempio un token danneggiato in transito, un token di dimensioni non corrette o un token passato nella delega [*vincolata errata.*](../secgloss/s-gly.md) Il passaggio di un token al pacchetto errato può verificarsi se il client e il server non hanno negoziato la delega [*vincolata appropriata.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                 | L'accesso non è riuscito.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E NESSUNA AUTORITÀ DI \_ \_ \_ AUTENTICAZIONE**</dt> </dl> | Non è stato possibile contattare alcuna autorità per l'autenticazione. Il nome di dominio dell'entità autenticante potrebbe non essere corretto, il dominio potrebbe non essere raggiungibile o potrebbe esserci stato un errore di relazione di trust.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NESSUNA \_ CREDENZIALE**</dt> </dl>               | Nella delega vincolata non sono disponibili [*credenziali*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**DESTINAZIONE \_ SEC E \_ \_ SCONOSCIUTA**</dt> </dl>               | La destinazione non è stata riconosciuta.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E FUNZIONE NON \_ \_ SUPPORTATA**</dt> </dl>         | Nel parametro fContextReq è stato specificato un flag di attributo di contesto non \_ valido (ISC REQ DELEGATE o \_ ISC \_ REQ \_ PROMPT FOR \_ \_ CREDS). <br/>                                                                                                                                            |
| <dl> <dt>**ENTITÀ \_ SEC E \_ \_ ERRATO**</dt> </dl>              | L'entità che ha ricevuto la richiesta di autenticazione non corrisponde a quella passata nel *parametro pszTargetName.* Ciò indica un errore nell'autenticazione reciproca.<br/>                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, la riservatezza è stata richiesta, ma non è stato possibile stabilirlo, alcune applicazioni possono scegliere di arrestare immediatamente la connessione.

Se gli attributi del [*contesto di sicurezza*](../secgloss/s-gly.md) non sono sufficienti, il client deve liberare il contesto creato parzialmente chiamando la funzione [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

La **funzione InitializeSecurityContext (Digest)** viene usata da un client per inizializzare un contesto in uscita.

Per un contesto di [*sicurezza a due*](../secgloss/s-gly.md)tratta, la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione con *phContext* impostato su **NULL** e compila il descrittore del buffer con il messaggio di input.
2.  Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) esamina i parametri e costruisce un token opaco, inserendolo nell'elemento TOKEN nella matrice di buffer. Se il *parametro fContextReq* include il flag ISC REQ ALLOCATE MEMORY, il pacchetto di sicurezza alloca la memoria e restituisce il \_ \_ \_ puntatore nell'elemento TOKEN. [](../secgloss/s-gly.md)
3.  Il client invia il token restituito nel buffer *pOutput* al server di destinazione. Il server passa quindi il token come argomento di input in una chiamata alla [**funzione AcceptSecurityContext (Digest).**](acceptsecuritycontext--digest.md)
4.  [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) può restituire un token che il server invia al client per una seconda chiamata a **InitializeSecurityContext (Digest)** se la prima chiamata ha restituito SEC \_ I CONTINUE \_ \_ NEEDED.

Per i contesti [*di sicurezza a più*](../secgloss/s-gly.md)livelli, ad esempio l'autenticazione reciproca, la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione come descritto in precedenza, ma il pacchetto restituisce il codice di esito positivo SEC \_ I \_ CONTINUE \_ NEEDED.
2.  Il client invia il token di output al server e attende la risposta del server.
3.  Al momento della ricezione della risposta del server, il client chiama nuovamente **InitializeSecurityContext (Digest),** con *phContext* impostato sull'handle restituito dall'ultima chiamata. Il token ricevuto dal server viene fornito nel *parametro pInput.*

Se il server ha risposto correttamente, il pacchetto [*di sicurezza*](../secgloss/s-gly.md) restituisce SEC E OK e viene stabilita una \_ sessione \_ protetta.

Se la funzione restituisce una delle risposte di errore, la risposta del server non viene accettata e la sessione non viene stabilita.

Se la funzione restituisce SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED o SEC I COMPLETE AND CONTINUE, i passaggi \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2 e 3 vengono ripetuti.

Per [*inizializzare*](../secgloss/s-gly.md)un contesto di sicurezza, possono essere necessarie più chiamate a questa funzione, a seconda del meccanismo di autenticazione sottostante e delle scelte specificate nel *parametro fContextReq.*

I *parametri fContextReq* e *pfContextAttributes* sono maschera di bit che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [Requisiti di contesto](context-requirements.md). Il *parametro pfContextAttributes* è valido in caso di esito positivo, ma solo in caso di esito positivo finale è necessario esaminare i flag relativi agli aspetti di sicurezza del contesto. I valori restituiti intermedi possono impostare, ad esempio, il flag ISC \_ RET \_ ALLOCATED \_ MEMORY.

Se il flag ISC REQ USE SUPPLIED CREDS è impostato, il pacchetto di sicurezza deve cercare un tipo \_ \_ di buffer \_ \_ [](../secgloss/s-gly.md) \_ SECBUFFER PKG PARAMS nel buffer di \_ input *pInput.* Non si tratta di una soluzione generica, ma consente un accoppiamento sicuro del pacchetto [*di sicurezza*](../secgloss/s-gly.md) e dell'applicazione quando appropriato.

Se è stato specificato \_ ISC REQ \_ ALLOCATE \_ MEMORY, il chiamante deve liberare la memoria chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Ad esempio, il token di input potrebbe essere la richiesta di un LAN Manager. In questo caso, il token di output sarà la risposta crittografata NTLM alla richiesta.

L'azione eseguita dal client dipende dal codice restituito da questa funzione. Se il codice restituito è SEC E OK, non sarà presente alcuna seconda chiamata \_ \_ a **InitializeSecurityContext (Digest)** e non è prevista alcuna risposta dal server. Se il codice restituito è SEC I CONTINUE NEEDED, il client prevede un token in risposta dal server e lo passa in una seconda chiamata \_ \_ a \_ **InitializeSecurityContext (Digest).** Il codice restituito SEC I COMPLETE NEEDED indica che il client deve completare la compilazione del \_ messaggio e chiamare la funzione \_ \_ [**CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) Il codice SEC \_ I COMPLETE AND CONTINUE incorpora \_ \_ \_ entrambe queste azioni.

Se **InitializeSecurityContext (Digest)** restituisce l'esito positivo alla prima (o solo) chiamata, il chiamante deve chiamare alla fine la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sull'handle restituito, anche se la chiamata ha esito negativo in una fase successiva dello scambio di autenticazione.

Il client può chiamare **nuovamente InitializeSecurityContext (Digest)** dopo che è stato completato correttamente. Ciò indica al pacchetto [*di sicurezza che*](../secgloss/s-gly.md) è necessario eseguire una riautenticazione.

I chiamanti in modalità kernel hanno le differenze seguenti: il nome di destinazione è una stringa [*Unicode*](../secgloss/u-gly.md) che deve essere allocata nella memoria virtuale tramite [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc). non deve essere allocato dal pool. I buffer passati e forniti in *pInput* *e pOutput* devono essere nella memoria virtuale, non nel pool.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**AcquireCredentialsHandle (digest)**](acquirecredentialshandle--digest.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
