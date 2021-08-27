---
description: Avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali usando la delega [*vincolata*](../secgloss/s-gly.md)Schannel.
ms.assetid: c451089a-d10d-469c-99dd-43d75a6b0b2a
title: Funzione InitializeSecurityContext (Schannel) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 29bbaeac3ef307e3ef846f526d96a98a22395742
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472907"
---
# <a name="initializesecuritycontext-schannel-function"></a>Funzione InitializeSecurityContext (Schannel)

La **funzione InitializeSecurityContext (Schannel)** avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali. La funzione viene usata per compilare un [*contesto di sicurezza*](../secgloss/s-gly.md) tra l'applicazione client e un peer remoto. **InitializeSecurityContext (Schannel)** restituisce un token che il client deve passare al peer remoto, che il peer a sua volta invia all'implementazione della sicurezza locale tramite la chiamata [**AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md) Il token generato deve essere considerato opaco da tutti i chiamanti.

In genere, la **funzione InitializeSecurityContext (Schannel)** viene chiamata in un ciclo fino a quando non viene stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) sufficiente.

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

Handle per le credenziali restituite da [**AcquireCredentialsHandle (Schannel).**](acquirecredentialshandle--schannel.md) Questo handle viene utilizzato per compilare il [*contesto di sicurezza*](../secgloss/s-gly.md). La **funzione InitializeSecurityContext (Schannel)** richiede almeno credenziali OUTBOUND.

</dd> <dt>

*phContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata a **InitializeSecurityContext (Schannel)** questo puntatore è **NULL.** Nella seconda chiamata questo parametro è un puntatore all'handle al contesto parzialmente formato restituito nel parametro *phNewContext* dalla prima chiamata.

Nella prima chiamata a **InitializeSecurityContext (Schannel)** specificare **NULL.** Nelle chiamate future specificare il token ricevuto nel *parametro phNewContext* dopo la prima chiamata a questa funzione.

</dd> <dt>

*pszTargetName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica in modo univoco il server di destinazione. Schannel usa questo valore per verificare il certificato del server. Schannel usa anche questo valore per individuare la sessione nella cache della sessione durante la ristabilizione di una connessione. La sessione memorizzata nella cache viene usata solo se vengono soddisfatte tutte le condizioni seguenti:

-   Il nome di destinazione è lo stesso.
-   La voce della cache non è scaduta.
-   Il processo dell'applicazione che chiama la funzione è lo stesso.
-   La sessione di accesso è la stessa.
-   L'handle delle credenziali è lo stesso.

</dd> <dt>

*fContextReq* \[ Pollici\]
</dt> <dd>

Flag di bit che indicano le richieste per il contesto. Non tutti i pacchetti possono supportare tutti i requisiti. I flag usati per questo parametro sono preceduti dal prefisso ISC \_ \_ REQ, ad esempio ISC \_ REQ \_ DELEGATE. Questo parametro può essere uno o più dei flag di attributi seguenti.




| valore | Significato | 
|-------|---------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl><dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt></dl> | Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) alloca automaticamente i buffer di output. Dopo aver terminato di usare i buffer di output, liberarli chiamando la [<strong>funzione FreeContextBuffer.</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br /> | 
| <span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl><dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt></dl> | Crittografare i messaggi [<strong>usando la funzione EncryptMessage.</strong>](encryptmessage--general.md)<br /> | 
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl><dt><strong>ISC_REQ_CONNECTION</strong></dt></dl> | Il [*contesto di sicurezza non*](../secgloss/s-gly.md) gestirà i messaggi di formattazione.<br /> | 
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl><dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt></dl> | Quando si verificano errori, l'entità remota riceverà una notifica.<br /> | 
| <span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl><dt><strong>ISC_REQ_INTEGRITY</strong></dt></dl> | Firmare i messaggi e verificare le firme usando [<strong>le funzioni EncryptMessage</strong>](encryptmessage--general.md) [<strong>e MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl><dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt></dl> | Schannel non deve autenticare automaticamente il server.<br /> | 
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl><dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt></dl> | Verranno soddisfatti i criteri di autenticazione reciproca del servizio.<br /><blockquote>[!Caution]<br />Ciò non significa necessariamente che viene eseguita l'autenticazione reciproca, ma solo che vengono soddisfatti i criteri di autenticazione del servizio. Per assicurarsi che l'autenticazione reciproca sia eseguita, chiamare [<strong>la funzione QueryContextAttributes (Schannel).</strong>](querycontextattributes--schannel.md)</blockquote><br /> | 
| <span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl><dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt></dl> | Rilevare i messaggi riprodotti che sono stati codificati usando le [<strong>funzioni EncryptMessage</strong>](encryptmessage--general.md) [<strong>o MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl><dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt></dl> | Rilevare i messaggi ricevuti fuori sequenza.<br /> | 
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl><dt><strong>ISC_REQ_STREAM</strong></dt></dl> | Supportare una connessione orientata al flusso.<br /> | 
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl><dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt></dl> | Schannel non deve tentare di fornire automaticamente le credenziali per il client.<br /> | 




 

Gli attributi richiesti potrebbero non essere supportati dal client. Per altre informazioni, vedere il *parametro pfContextAttr.*

Per altre descrizioni dei vari attributi, vedere Requisiti [di contesto.](context-requirements.md)

</dd> <dt>

*Riservato1* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*TargetDataRep* \[ Pollici\]
</dt> <dd>

Questo parametro non viene usato con Schannel. Impostarlo su zero.

</dd> <dt>

*pInput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a [**una struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori ai buffer forniti come input per il pacchetto. A meno che il contesto client non sia stato avviato dal server, il valore di questo parametro deve essere **NULL** alla prima chiamata alla funzione. Nelle chiamate successive alla funzione o quando il contesto client è stato avviato dal server, il valore di questo parametro è un puntatore a un buffer allocato con memoria sufficiente per contenere il token restituito dal computer remoto.

Nelle chiamate a questa funzione dopo la chiamata iniziale devono essere presenti due buffer. Il primo è di **tipo SECBUFFER \_ TOKEN** e contiene il token ricevuto dal server. Il secondo buffer è di **tipo SECBUFFER \_ EMPTY.** Impostare entrambi i membri **pvBuffer** **e cbBuffer** su zero.

</dd> <dt>

*Riservato2* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata a **InitializeSecurityContext (Schannel),** questo puntatore riceve il nuovo handle di contesto. Nella seconda chiamata, *phNewContext* può essere uguale all'handle specificato nel *parametro phContext.*

Nelle chiamate successive alla prima chiamata, passare l'handle restituito qui come *parametro phContext* e specificare **NULL** per *phNewContext.*

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori alla [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che riceve i dati di output. Se un buffer è stato digitato come SEC \_ READWRITE nell'input, sarà presente nell'output. Il sistema alloca un buffer per il token di sicurezza, se richiesto (tramite ISC REQ ALLOCATE MEMORY) e inserisce l'indirizzo nel descrittore del buffer per \_ \_ il token di \_ sicurezza.

Se viene specificato il flag ISC REQ ALLOCATE MEMORY, SSP Schannel alloca memoria per il buffer e inserrà le informazioni appropriate \_ \_ in \_ [**SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Inoltre, il chiamante deve passare un buffer di tipo **SECBUFFER \_ ALERT**. Nell'output, se viene generato un avviso, questo buffer contiene informazioni sull'avviso e la funzione ha esito negativo.

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

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il [*pacchetto di sicurezza restituirà*](../secgloss/s-gly.md) sempre questo valore nell'ora locale. Questo parametro è facoltativo **ed è** necessario passare NULL per i client di breve durata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce uno dei codici di esito positivo seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Il client deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e quindi passare l'output al server. Il client attende quindi un token restituito e lo passa, in un'altra chiamata, a [**InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md)<br/>                                                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | Il client deve completare la compilazione del messaggio e quindi chiamare [**la funzione CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Il client deve inviare il token di output al server e attendere un token restituito. Il token restituito viene quindi passato in un'altra chiamata [**a InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md) Il token di output può essere vuoto.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ I \_ INCOMPLETE \_ CREDENTIALS**</dt> </dl> | Il server ha richiesto l'autenticazione client e le credenziali fornite non includono un certificato o il certificato non è stato emesso da un'autorità di certificazione (CA) attendibile dal server. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                         |
| <dl> <dt>**MESSAGGIO \_ \_ INCOMPLETO \_ SEC E**</dt> </dl>     | I dati per l'intero messaggio non sono stati letti dalla rete.<br/> Quando viene restituito questo valore, il buffer *pInput* contiene una [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un **membro BufferType** **di SECBUFFER \_ MISSING.** Il **membro cbBuffer** di **SecBuffer** contiene un valore che indica il numero di byte aggiuntivi che la funzione deve leggere dal client prima che questa funzione riesca. Anche se questo numero non è sempre accurato, l'uso di questo valore può contribuire a migliorare le prestazioni evitando più chiamate a questa funzione.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Il [*contesto di sicurezza*](../secgloss/s-gly.md) è stato inizializzato correttamente. Non è necessaria [**un'altra chiamata a InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md) Se la funzione restituisce un token di output, ad esempio se IL TOKEN SECBUFFER \_ in *pOutput* è di lunghezza diversa da zero, tale token deve essere inviato al server.<br/>                                                                                                                               |



 

Se la funzione ha esito negativo, la funzione restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl>            | Memoria insufficiente per completare l'azione richiesta.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ E \_ ERRORE \_ INTERNO**</dt> </dl>                 | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**HANDLE SEC \_ E \_ NON \_ VALIDO**</dt> </dl>                 | L'handle passato alla funzione non è valido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E TOKEN NON \_ \_ VALIDO**</dt> </dl>                  | L'errore è dovuto a un token di input in formato non valido, ad esempio un token danneggiato in transito, un token di dimensioni non corrette o un token passato nella delega [*vincolata errata.*](../secgloss/s-gly.md) Il passaggio di un token al pacchetto errato può verificarsi se il client e il server non negoziano la delega [*vincolata appropriata.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                   | Accesso non riuscito.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY**</dt> </dl>   | Non è stato possibile contattare alcuna autorità per l'autenticazione. È possibile che il nome di dominio dell'entità di autenticazione non sia corretto, che il dominio non sia raggiungibile o che si sia verificato un errore di relazione di trust.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>                 | Nessuna credenziale disponibile nella delega [*vincolata*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ DESTINAZIONE \_ SCONOSCIUTA**</dt> </dl>                 | La destinazione non è stata riconosciuta.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E FUNZIONE NON \_ \_ SUPPORTATA**</dt> </dl>           | Nel parametro fContextReq è stato specificato un flag di attributo di contesto non \_ valido (ISC REQ DELEGATE o \_ ISC \_ REQ \_ PROMPT FOR \_ \_ CREDS). <br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ WRONG \_ PRINCIPAL**</dt> </dl>                | L'entità che ha ricevuto la richiesta di autenticazione non corrisponde a quella passata nel *parametro pszTargetName.* Ciò indica un errore nell'autenticazione reciproca.<br/>                                                                                                          |
| <dl> <dt>**MANCATA \_ \_ CORRISPONDENZA DEL PROTOCOLLO \_ \_ DELL'APPLICAZIONE SEC E**</dt> </dl> | Non esiste alcun protocollo applicativo comune tra il client e il server.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza, ma non è stato possibile stabilirlo, alcune applicazioni possono scegliere di arrestare immediatamente la connessione.

Se gli attributi del [*contesto di sicurezza*](../secgloss/s-gly.md) non sono sufficienti, il client deve liberare il contesto creato parzialmente chiamando la funzione [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

La **funzione InitializeSecurityContext (Schannel)** viene usata da un client per inizializzare un contesto in uscita.

Per un contesto di [*sicurezza a due elementi,*](../secgloss/s-gly.md)la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione con *phContext impostato* su **NULL** e inserisce nel descrittore del buffer il messaggio di input.
2.  Il [*pacchetto di*](../secgloss/s-gly.md) sicurezza esamina i parametri e costruisce un token opaco, inserendolo nell'elemento TOKEN nella matrice di buffer. Se il *parametro fContextReq* include il flag ISC REQ ALLOCATE MEMORY, il pacchetto di sicurezza alloca la memoria e restituisce il \_ \_ \_ puntatore nell'elemento TOKEN. [](../secgloss/s-gly.md)
3.  Il client invia il token restituito nel buffer *pOutput* al server di destinazione. Il server passa quindi il token come argomento di input in una chiamata alla [**funzione AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md)
4.  [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) può restituire un token, che il server invia al client per una seconda chiamata a **InitializeSecurityContext (Schannel)** se la prima chiamata ha restituito SEC \_ I CONTINUE \_ \_ NEEDED.

Per i contesti di sicurezza a [*più*](../secgloss/s-gly.md)livelli, ad esempio l'autenticazione reciproca, la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione come descritto in precedenza, ma il pacchetto restituisce il codice di esito positivo SEC \_ I \_ CONTINUE \_ NEEDED.
2.  Il client invia il token di output al server e attende la risposta del server.
3.  Alla ricezione della risposta del server, il client chiama di nuovo **InitializeSecurityContext (Schannel),** con *phContext impostato* sull'handle restituito dall'ultima chiamata. Il token ricevuto dal server viene fornito nel *parametro pInput.*

Se il server ha risposto correttamente, il pacchetto [*di sicurezza*](../secgloss/s-gly.md) restituisce SEC E OK e viene stabilita una \_ sessione \_ protetta.

Se la funzione restituisce una delle risposte di errore, la risposta del server non viene accettata e la sessione non viene stabilita.

Se la funzione restituisce SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED o SEC I COMPLETE AND CONTINUE, i passaggi \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2 e 3 vengono ripetuti.

Per inizializzare [*un*](../secgloss/s-gly.md)contesto di sicurezza, può essere necessaria più di una chiamata a questa funzione, a seconda del meccanismo di autenticazione sottostante e delle scelte specificate nel *fContextReq parametro.*

I *parametri fContextReq* e *pfContextAttributes* sono maschera di bit che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [Requisiti di contesto.](context-requirements.md) Il *parametro pfContextAttributes* è valido in caso di esito positivo, ma solo al completamento dell'operazione di restituzione è necessario esaminare i flag che riguardano gli aspetti di sicurezza del contesto. I valori restituiti intermedi possono impostare, ad esempio, il flag ISC \_ RET \_ ALLOCATED \_ MEMORY.

Se il flag ISC REQ USE SUPPLIED CREDS è impostato, il pacchetto di sicurezza deve cercare un tipo di \_ \_ buffer \_ \_ SECBUFFER PKG PARAMS [](../secgloss/s-gly.md) nel buffer di input \_ \_ *pInput.* Non si tratta di una soluzione generica, ma consente un'associazione forte di pacchetto [*di*](../secgloss/s-gly.md) sicurezza e applicazione quando appropriato.

Se è stato specificato ISC REQ ALLOCATE MEMORY, il chiamante deve liberare la \_ memoria chiamando la funzione \_ \_ [**FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Ad esempio, il token di input potrebbe essere la richiesta di un GESTORE LAN. In questo caso, il token di output sarà la risposta crittografata con NTLM alla richiesta.

L'azione eseguita dal client dipende dal codice restituito da questa funzione. Se il codice restituito è SEC E OK, non sarà presente alcuna seconda chiamata \_ \_ a **InitializeSecurityContext (Schannel)** e non è prevista alcuna risposta dal server. Se il codice restituito è SEC I CONTINUE NEEDED, il client prevede un token in risposta dal server e lo passa in una seconda chiamata \_ \_ a \_ **InitializeSecurityContext (Schannel).** Il codice restituito SEC I COMPLETE NEEDED indica che il client deve completare la compilazione del messaggio \_ e chiamare la funzione \_ \_ [**CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) Il codice SEC \_ I COMPLETE AND CONTINUE incorpora \_ \_ \_ entrambe queste azioni.

Se **InitializeSecurityContext (Schannel)** restituisce l'esito positivo alla prima (o unica) chiamata, il chiamante deve infine chiamare la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sull'handle restituito, anche se la chiamata non riesce in una fase successiva dello scambio di autenticazione.

Il client può chiamare **di nuovo InitializeSecurityContext (Schannel)** dopo che è stato completato correttamente. Indica al pacchetto di sicurezza [*che è necessario*](../secgloss/s-gly.md) eseguire una riautenticazione.

I chiamanti in modalità kernel hanno le differenze seguenti: il nome di destinazione è una stringa [*Unicode*](../secgloss/u-gly.md) che deve essere allocata nella memoria virtuale tramite [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); non deve essere allocato dal pool. I buffer passati e forniti in *pInput* e *pOutput* devono essere nella memoria virtuale, non nel pool.

Se la funzione restituisce SEC I INCOMPLETE CREDENTIALS, verificare di aver specificato un certificato valido e \_ \_ \_ attendibile nelle credenziali. Il certificato viene specificato quando si chiama [**la funzione AcquireCredentialsHandle (Schannel).**](acquirecredentialshandle--schannel.md) Il certificato deve essere un certificato di autenticazione client emesso da un'autorità di certificazione (CA) attendibile dal server. Per ottenere un elenco delle CA attendibili dal server, chiamare la funzione [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) e specificare l'attributo SECPKG \_ ATTR \_ ISSUER \_ LIST \_ EX.

Dopo che un'applicazione client riceve un certificato di autenticazione da una CA attendibile dal server, l'applicazione crea una nuova credenziale chiamando la funzione [**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md) e quindi chiamando di nuovo **InitializeSecurityContext (Schannel),** specificando la nuova credenziale nel *parametro phCredential.*

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
</dt> <dt>

[**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md)
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

 

 
