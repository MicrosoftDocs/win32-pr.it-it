---
description: Avvia il contesto di sicurezza in uscita [*sul*](../secgloss/s-gly.md) lato client da un handle di credenziali usando la delega [*vincolata*](../secgloss/s-gly.md)Kerberos.
ms.assetid: b5c968dc-9343-44ed-acbc-a89c58c14e4a
title: Funzione InitializeSecurityContext (Kerberos) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f2a88fd930e58be418afa9d508adf9cda73912a8c0c5ea6731c06af5ec41a997
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482601"
---
# <a name="initializesecuritycontext-kerberos-function"></a>Funzione InitializeSecurityContext (Kerberos)

La **funzione InitializeSecurityContext (Kerberos)** avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali. La funzione viene usata per compilare un [*contesto di sicurezza*](../secgloss/s-gly.md) tra l'applicazione client e un peer remoto. **InitializeSecurityContext (Kerberos)** restituisce un token che il client deve passare al peer remoto, che il peer a sua volta invia all'implementazione della sicurezza locale tramite la chiamata [**AcceptSecurityContext (Kerberos).**](acceptsecuritycontext--kerberos.md) Il token generato deve essere considerato opaco da tutti i chiamanti.

In genere, la **funzione InitializeSecurityContext (Kerberos)** viene chiamata in un ciclo fino a quando non viene stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) sufficiente.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_        SEC_CHAR       *pszTargetName,
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

Handle per le credenziali restituite da [**AcquireCredentialsHandle (Kerberos).**](acquirecredentialshandle--kerberos.md) Questo handle viene utilizzato per compilare il [*contesto di sicurezza*](../secgloss/s-gly.md). La **funzione InitializeSecurityContext (Kerberos)** richiede almeno credenziali OUTBOUND.

</dd> <dt>

*phContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata a **InitializeSecurityContext (Kerberos)** questo puntatore è **NULL.** Nella seconda chiamata questo parametro è un puntatore all'handle al contesto parzialmente formato restituito nel parametro *phNewContext* dalla prima chiamata.

</dd> <dt>

*pszTargetName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che indica il nome dell'entità servizio (SPN) o il contesto [*di sicurezza*](../secgloss/s-gly.md) del server di destinazione.

Usare un nome di destinazione completo perché i nomi brevi non sono supportati nelle foreste.

</dd> <dt>

*fContextReq* \[ Pollici\]
</dt> <dd>

Flag di bit che indicano le richieste per il contesto. Non tutti i pacchetti possono supportare tutti i requisiti. I flag usati per questo parametro sono preceduti dal prefisso ISC \_ \_ REQ, ad esempio ISC \_ REQ \_ DELEGATE. Questo parametro può essere uno o più dei flag di attributi seguenti.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) alloca automaticamente i buffer di output. Dopo aver terminato di usare i buffer di output, liberarli chiamando la funzione [<strong>FreeContextBuffer</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Crittografare i messaggi usando la funzione [<strong>EncryptMessage</strong>](encryptmessage--general.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Il [*contesto di sicurezza non*](../secgloss/s-gly.md) gestirà i messaggi di formattazione. Questo è il valore predefinito.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>Il server può utilizzare il contesto per l'autenticazione ad altri server come client. Il ISC_REQ_MUTUAL_AUTH deve essere impostato per il funzionamento di questo flag. Valido per Kerberos. Ignorare questo flag per la [*delega vincolata.*](../secgloss/c-gly.md)<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Quando si verificano errori, l'entità remota riceverà una notifica.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Firmare i messaggi e verificare le firme usando le funzioni [<strong>EncryptMessage</strong>](encryptmessage--general.md) e [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Verranno soddisfatti i criteri di autenticazione reciproca del servizio.<br/><blockquote>[!Caution]<br />
Ciò non significa necessariamente che viene eseguita l'autenticazione reciproca, ma solo che vengono soddisfatti i criteri di autenticazione del servizio. Per assicurarsi che l'autenticazione reciproca sia eseguita, chiamare la funzione [<strong>QueryContextAttributes (Kerberos)</strong>](querycontextattributes--kerberos.md).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Se questo flag è impostato, il flag <strong>ISC_REQ_INTEGRITY</strong> viene ignorato.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Rilevare i messaggi riprodotti codificati usando le funzioni [<strong>EncryptMessage</strong>](encryptmessage--general.md) o [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Rilevare i messaggi ricevuti fuori sequenza.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Supportare una connessione orientata al flusso.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>È necessario [*negoziare una*](../secgloss/s-gly.md) nuova chiave di sessione.<br/></td></tr></tbody></table>



 

Gli attributi richiesti potrebbero non essere supportati dal client. Per altre informazioni, vedere il *parametro pfContextAttr.*

Per altre descrizioni dei vari attributi, vedere Requisiti [di contesto.](context-requirements.md)

</dd> <dt>

*Riservato1* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*TargetDataRep* \[ Pollici\]
</dt> <dd>

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, nella destinazione. Questo parametro può essere SECURITY \_ NATIVE \_ DREP o SECURITY \_ NETWORK \_ DREP.

</dd> <dt>

*pInput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a [**una struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori ai buffer forniti come input per il pacchetto. A meno che il contesto client non sia stato avviato dal server, il valore di questo parametro deve essere **NULL** alla prima chiamata alla funzione. Nelle chiamate successive alla funzione o quando il contesto client è stato avviato dal server, il valore di questo parametro è un puntatore a un buffer allocato con memoria sufficiente per contenere il token restituito dal computer remoto.

</dd> <dt>

*Riservato2* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata a **InitializeSecurityContext (Kerberos)** questo puntatore riceve il nuovo handle di contesto. Nella seconda chiamata, *phNewContext* può essere uguale all'handle specificato nel *parametro phContext.*

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori alla [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che riceve i dati di output. Se un buffer è stato digitato come SEC \_ READWRITE nell'input, sarà presente nell'output. Il sistema alloca un buffer per il token di sicurezza, se richiesto (tramite ISC REQ ALLOCATE MEMORY) e inserisce l'indirizzo nel descrittore del buffer per \_ \_ il token di \_ sicurezza.

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

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituirà sempre questo valore nell'ora locale. Poiché questo parametro è facoltativo, è necessario passare **NULL** per i client di breve durata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce uno dei codici di esito positivo seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Il [*contesto di sicurezza*](../secgloss/s-gly.md) è stato inizializzato correttamente. Non è necessaria [**un'altra chiamata a InitializeSecurityContext (Kerberos).**](initializesecuritycontext--kerberos.md) Se la funzione restituisce un token di output, ad esempio se il TOKEN SECBUFFER \_ in *pOutput* è di lunghezza diversa da zero, tale token deve essere inviato al server.<br/> |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Il client deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e quindi passare l'output al server. Il client attende quindi un token restituito e lo passa, in un'altra chiamata, a [**InitializeSecurityContext (Kerberos).**](initializesecuritycontext--kerberos.md)<br/>                                                                                                                                  |
| <dl> <dt>**SEC \_ COMPLETATO \_ \_ NECESSARIO**</dt> </dl>        | Il client deve completare la compilazione del messaggio e quindi chiamare la [**funzione CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Il client deve inviare il token di output al server e attendere un token restituito. Il token restituito viene quindi passato in un'altra chiamata a [**InitializeSecurityContext (Kerberos).**](initializesecuritycontext--kerberos.md) Il token di output può essere vuoto.<br/>                                                                                                                                                       |
| <dl> <dt>**SEC \_ I \_ CREDENZIALI INCOMPLETE \_**</dt> </dl> | Usare con Schannel. Il server ha richiesto l'autenticazione client e le credenziali fornite non includono un certificato o il certificato non è stato emesso da un'autorità di certificazione (CA) attendibile dal server. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                |



 

Se la funzione ha esito negativo, la funzione restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl>          | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERRORE \_ INTERNO SEC E \_ \_**</dt> </dl>               | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**HANDLE \_ SEC E NON \_ \_ VALIDO**</dt> </dl>               | L'handle passato alla funzione non è valido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**TOKEN \_ SEC E NON \_ \_ VALIDO**</dt> </dl>                | L'errore è dovuto a un token di input in formato non valido, ad esempio un token danneggiato in transito, un token di dimensioni non corrette o un token passato nella delega [*vincolata errata.*](../secgloss/s-gly.md) Il passaggio di un token al pacchetto errato può verificarsi se il client e il server non negoziano la delega [*vincolata appropriata.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                 | L'accesso non è riuscito.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E NESSUNA AUTORITÀ DI \_ \_ \_ AUTENTICAZIONE**</dt> </dl> | Non è stato possibile contattare alcuna autorità per l'autenticazione. Il nome di dominio dell'entità autenticante potrebbe non essere corretto, il dominio potrebbe non essere raggiungibile o potrebbe esserci stato un errore di relazione di trust.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NESSUNA \_ CREDENZIALE**</dt> </dl>               | Nella delega vincolata non sono disponibili [*credenziali*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**DESTINAZIONE \_ SEC E \_ \_ SCONOSCIUTA**</dt> </dl>               | La destinazione non è stata riconosciuta.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E FUNZIONE NON \_ \_ SUPPORTATA**</dt> </dl>         | Nel parametro fContextReq è stato specificato un flag di attributo di contesto non \_ valido (ISC REQ DELEGATE o \_ ISC \_ REQ \_ PROMPT FOR \_ \_ CREDS). <br/>                                                                                                                                            |
| <dl> <dt>**ENTITÀ \_ SEC E \_ \_ ERRATO**</dt> </dl>              | L'entità che ha ricevuto la richiesta di autenticazione non corrisponde a quella passata nel *parametro pszTargetName.* Ciò indica un errore nell'autenticazione reciproca.<br/>                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, la riservatezza è stata richiesta, ma non è stato possibile stabilirlo, alcune applicazioni possono scegliere di arrestare immediatamente la connessione.

Se gli attributi del [*contesto di sicurezza*](../secgloss/s-gly.md) non sono sufficienti, il client deve liberare il contesto creato parzialmente chiamando la funzione [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

La **funzione InitializeSecurityContext (Kerberos)** viene usata da un client per inizializzare un contesto in uscita.

Per un contesto di [*sicurezza a due*](../secgloss/s-gly.md)tratta, la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione con *phContext* impostato su **NULL** e compila il descrittore del buffer con il messaggio di input.
2.  Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) esamina i parametri e costruisce un token opaco, inserendolo nell'elemento TOKEN nella matrice di buffer. Se il *parametro fContextReq* include il flag ISC REQ ALLOCATE MEMORY, il pacchetto di sicurezza alloca la memoria e restituisce il \_ \_ \_ puntatore nell'elemento TOKEN. [](../secgloss/s-gly.md)
3.  Il client invia il token restituito nel buffer *pOutput* al server di destinazione. Il server passa quindi il token come argomento di input in una chiamata alla funzione [**AcceptSecurityContext (Kerberos).**](acceptsecuritycontext--kerberos.md)
4.  [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) può restituire un token che il server invia al client per una seconda chiamata a **InitializeSecurityContext (Kerberos)** se la prima chiamata ha restituito SEC \_ I CONTINUE \_ \_ NEEDED.

Per i contesti [*di sicurezza a più*](../secgloss/s-gly.md)livelli, ad esempio l'autenticazione reciproca, la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione come descritto in precedenza, ma il pacchetto restituisce il codice di esito positivo SEC \_ I \_ CONTINUE \_ NEEDED.
2.  Il client invia il token di output al server e attende la risposta del server.
3.  Al momento della ricezione della risposta del server, il client chiama nuovamente **InitializeSecurityContext (Kerberos),** con *phContext* impostato sull'handle restituito dall'ultima chiamata. Il token ricevuto dal server viene fornito nel *parametro pInput.*

Se il server ha risposto correttamente, il pacchetto [*di sicurezza*](../secgloss/s-gly.md) restituisce SEC E OK e viene stabilita una \_ sessione \_ protetta.

Se la funzione restituisce una delle risposte di errore, la risposta del server non viene accettata e la sessione non viene stabilita.

Se la funzione restituisce SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED o SEC I COMPLETE AND CONTINUE, i passaggi \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2 e 3 vengono ripetuti.

Per [*inizializzare*](../secgloss/s-gly.md)un contesto di sicurezza, possono essere necessarie più chiamate a questa funzione, a seconda del meccanismo di autenticazione sottostante e delle scelte specificate nel *parametro fContextReq.*

I *parametri fContextReq* e *pfContextAttributes* sono maschera di bit che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [Requisiti di contesto](context-requirements.md). Il *parametro pfContextAttributes* è valido in caso di esito positivo, ma solo in caso di esito positivo finale è necessario esaminare i flag relativi agli aspetti di sicurezza del contesto. I valori restituiti intermedi possono impostare, ad esempio, il flag ISC \_ RET \_ ALLOCATED \_ MEMORY.

Se il flag ISC REQ USE SUPPLIED CREDS è impostato, il pacchetto di sicurezza deve cercare un tipo \_ \_ di buffer \_ \_ [](../secgloss/s-gly.md) \_ SECBUFFER PKG PARAMS nel buffer di \_ input *pInput.* Non si tratta di una soluzione generica, ma consente un accoppiamento sicuro di pacchetto di [*sicurezza*](../secgloss/s-gly.md) e applicazione quando appropriato.

Se è stato specificato \_ ISC REQ \_ ALLOCATE \_ MEMORY, il chiamante deve liberare la memoria chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Ad esempio, il token di input potrebbe essere la richiesta di un LAN Manager. In questo caso, il token di output sarà la risposta crittografata NTLM alla richiesta.

L'azione eseguita dal client dipende dal codice restituito da questa funzione. Se il codice restituito è SEC E OK, non sarà presente alcuna seconda chiamata \_ \_ a **InitializeSecurityContext (Kerberos)** e non è prevista alcuna risposta dal server. Se il codice restituito è SEC I CONTINUE NEEDED, il client prevede un token in risposta dal server e lo passa in una seconda chiamata \_ \_ a \_ **InitializeSecurityContext (Kerberos).** Il codice restituito SEC I COMPLETE NEEDED indica che il client deve completare la compilazione del \_ messaggio e chiamare la funzione \_ \_ [**CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) Il codice SEC \_ I COMPLETE AND CONTINUE incorpora \_ \_ \_ entrambe queste azioni.

Se **InitializeSecurityContext (Kerberos)** restituisce l'esito positivo alla prima (o solo) chiamata, il chiamante deve chiamare la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sull'handle restituito, anche se la chiamata ha esito negativo in una fase successiva dello scambio di autenticazione.

Il client può chiamare **nuovamente InitializeSecurityContext (Kerberos)** dopo che è stato completato correttamente. Ciò indica al pacchetto [*di sicurezza che*](../secgloss/s-gly.md) è necessario eseguire una riautenticazione.

I chiamanti in modalità kernel hanno le differenze seguenti: il nome di destinazione è una stringa [*Unicode*](../secgloss/u-gly.md) che deve essere allocata nella memoria virtuale tramite [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc). non deve essere allocato dal pool. I buffer passati e forniti in *pInput* *e pOutput* devono essere nella memoria virtuale, non nel pool.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
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

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)
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

 

 
