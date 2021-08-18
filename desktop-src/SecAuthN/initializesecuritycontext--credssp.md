---
description: Avvia il contesto di sicurezza in uscita sul lato client da un handle di credenziali.
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: Funzione InitializeSecurityContext (CredSSP) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5ba38dd10552f90ecfcc5045b96edc5e62aff1f8a2beec0f2a728fc1f0be8c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015991"
---
# <a name="initializesecuritycontext-credssp-function"></a>Funzione InitializeSecurityContext (CredSSP)

La **funzione InitializeSecurityContext (CredSSP)** avvia il contesto di sicurezza in uscita sul lato client da un handle di credenziali. La funzione crea un contesto di sicurezza tra l'applicazione client e un peer remoto. **InitializeSecurityContext (CredSSP)** restituisce un token che il client deve passare al peer remoto. il peer invia a sua volta il token all'implementazione della sicurezza locale tramite la chiamata [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md) Il token generato deve essere considerato opaco da tutti i chiamanti.

In genere, la **funzione InitializeSecurityContext (CredSSP)** viene chiamata in un ciclo fino a quando non viene stabilito un contesto di sicurezza sufficiente.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS SEC_ENTRY InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        unsigned long  fContextReq,
  _Reserved_  unsigned long  Reserved1,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PSecBufferDesc pInput,
  _In_        unsigned long  Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Out_opt_   PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phCredential* \[ in, facoltativo\]
</dt> <dd>

Handle per le credenziali restituite da [**AcquireCredentialsHandle (CredSSP).**](acquirecredentialshandle--credssp.md) Questo handle viene usato per compilare il contesto di sicurezza. La **funzione InitializeSecurityContext (CredSSP)** richiede almeno credenziali OUTBOUND.

</dd> <dt>

*phContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Nella prima chiamata a **InitializeSecurityContext (CredSSP)** questo puntatore è **NULL.** Nella seconda chiamata, questo parametro è un puntatore all'handle al contesto parzialmente formato restituito nel *parametro phNewContext* dalla prima chiamata.

Nella prima chiamata a **InitializeSecurityContext (CredSSP)** specificare **NULL.** Nelle chiamate future specificare il token ricevuto nel *parametro phNewContext* dopo la prima chiamata a questa funzione.

</dd> <dt>

*pTargetName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica in modo univoco il server di destinazione. Schannel usa questo valore per verificare il certificato del server. Schannel usa anche questo valore per individuare la sessione nella cache di sessione quando si ristabilirà una connessione. La sessione memorizzata nella cache viene usata solo se vengono soddisfatte tutte le condizioni seguenti:

-   Il nome di destinazione è lo stesso.
-   La voce della cache non è scaduta.
-   Il processo dell'applicazione che chiama la funzione è lo stesso.
-   La sessione di accesso è la stessa.
-   L'handle delle credenziali è lo stesso.

</dd> <dt>

*fContextReq* \[ Pollici\]
</dt> <dd>

Flag di bit che indicano le richieste per il contesto. Non tutti i pacchetti possono supportare tutti i requisiti. I flag usati per questo parametro sono preceduti da ISC \_ \_ REQ, ad esempio ISC \_ REQ \_ DELEGATE.

Questo parametro può essere uno o più dei flag di attributi seguenti.



| Valore                                                                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_ REQ \_ \_ ALLOCARE MEMORIA**</dt> <dt>0x100</dt> </dl>                         | Il pacchetto di sicurezza alloca buffer di output per il chiamante. Al termine dell'uso dei buffer di output, liberarli chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_ REQ \_ CONNECTION**</dt> <dt>0x800</dt> </dl>                                         | Il contesto di sicurezza non gestirà i messaggi di formattazione.<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_ REQ \_ EXTENDED \_ ERROR**</dt> <dt>0x4000</dt> </dl>                           | Quando si verificano errori, l'entità remota riceverà una notifica.<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_ REQ \_ MANUAL \_ CRED \_ VALIDATION**</dt> <dt>0x80000</dt> </dl> | Il provider di supporto per la sicurezza delle credenziali (CredSSP) non deve autenticare automaticamente il server. Questo flag viene sempre impostato quando si usa CredSSP.<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_ REQ \_ SEQUENCE \_ DETECT**</dt> <dt>0x8</dt> </dl>                           | Rilevare i messaggi ricevuti fuori sequenza.<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_ FLUSSO \_ REQ**</dt> <dt>0x8000</dt> </dl>                                                    | Supportare una connessione orientata al flusso.<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_ REQ \_ USE \_ SUPPLIED \_ CREDS**</dt> <dt>0x80</dt> </dl>                | CredSSP non deve tentare di fornire automaticamente le credenziali per il client.<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_ DELEGA \_ REQ**</dt> <dt>0x1</dt> </dl>                                                 | Indica che le credenziali dell'utente devono essere delegate al server.<br/> Se questo flag non viene specificato, al server viene delegato un set vuoto di credenziali.<br/> **Windows Server 2008 e Windows Vista:** Questo flag è obbligatorio.<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_ REQ \_ MUTUAL \_ AUTH**</dt> <dt>0x2</dt> </dl>                                       | Indica che l'autenticazione del server non è necessaria. I criteri di delega vengono comunque applicati se questo flag non è specificato.<br/> **Windows Server 2008 e Windows Vista:** Questo flag viene ignorato.<br/>                                                 |



 

Gli attributi richiesti potrebbero non essere supportati dal client. Per altre informazioni, vedere il *parametro pfContextAttr.*

Per altre descrizioni dei vari attributi, vedere [Requisiti di contesto](context-requirements.md).

</dd> <dt>

*Riservato1* \[ Pollici\]
</dt> <dd>

Riservato. Questo parametro deve essere impostato su zero.

</dd> <dt>

*TargetDataRep* \[ Pollici\]
</dt> <dd>

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, nella destinazione. Questo parametro può essere **SECURITY \_ NATIVE \_ DREP** o **SECURITY NETWORK \_ \_ DREP.**

</dd> <dt>

*pInput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori ai buffer forniti come input per il pacchetto. A meno che il contesto client non sia stato avviato dal server, il valore di questo parametro deve essere **NULL** alla prima chiamata alla funzione. Nelle chiamate successive alla funzione o quando il contesto client è stato avviato dal server, il valore di questo parametro è un puntatore a un buffer allocato con memoria sufficiente per contenere il token restituito dal computer remoto.

Nelle chiamate a questa funzione dopo la chiamata iniziale, devono essere presenti due buffer. Il primo è di **tipo SECBUFFER \_ TOKEN** e contiene il token ricevuto dal server. Il secondo buffer è di **tipo SECBUFFER \_ EMPTY.** Impostare entrambi i membri **pvBuffer** **e cbBuffer** su zero.

</dd> <dt>

*Riservato2* \[ Pollici\]
</dt> <dd>

Riservato. Questo parametro deve essere impostato su zero.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata a **InitializeSecurityContext (CredSSP)** questo puntatore riceve il nuovo handle di contesto. Nella seconda chiamata, *phNewContext* può essere uguale all'handle specificato nel *parametro phContext.*

Nelle chiamate successive alla prima chiamata, passare l'handle restituito qui come parametro *phContext* e specificare **NULL** per *phNewContext*.

</dd> <dt>

*pOutput* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Questa struttura contiene a sua volta puntatori alla [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che riceve i dati di output. Se un buffer è stato digitato come **SEC \_ READWRITE** nell'input, sarà presente nell'output. Il sistema alloca un buffer per il token di sicurezza se richiesto (tramite **ISC \_ REQ \_ ALLOCATE \_ MEMORY)** e inserisce l'indirizzo nel descrittore del buffer per il token di sicurezza.

Se viene specificato il flag **ISC \_ REQ \_ ALLOCATE \_ MEMORY,** CredSSP alloca memoria per il buffer e inserirà le informazioni appropriate in [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc).

</dd> <dt>

*pfContextAttr* \[ Cambio\]
</dt> <dd>

Puntatore a un set di flag di bit che indicano [*gli attributi*](../secgloss/a-gly.md#_security_attribute_gly) del contesto stabilito. Per una descrizione dei vari attributi, vedere [Requisiti di contesto](context-requirements.md).

I flag usati per questo parametro sono preceduti da ISC \_ RET, ad esempio **ISC \_ RET \_ DELEGATE**. Per un elenco di valori validi, vedere il *parametro fContextReq.*

Non verificare la presenza di attributi correlati alla sicurezza fino a quando la chiamata di funzione finale non viene restituita correttamente. I flag di attributo non correlati alla sicurezza, ad esempio il flag **ASC \_ RET \_ ALLOCATED \_ MEMORY,** possono essere controllati prima della restituzione finale.

> [!Note]  
> Particolari attributi di contesto possono cambiare durante la negoziazione con un peer remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il pacchetto di sicurezza restituirà sempre questo valore nell'ora locale. Questo parametro è facoltativo **ed è** necessario passare NULL per i client di breve durata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce uno dei codici di esito positivo seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MESSAGGIO \_ \_ INCOMPLETO \_ SEC E**</dt> </dl>     | I dati per l'intero messaggio non sono stati letti dalla rete.<br/> Quando viene restituito questo valore, il buffer *pInput* contiene una [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un **membro BufferType** **di SECBUFFER \_ MISSING.** Il **membro cbBuffer** di **SecBuffer** specifica il numero di byte aggiuntivi che la funzione deve leggere dal client prima che questa funzione riesca. Anche se questo numero non è sempre accurato, l'uso di questo valore può contribuire a migliorare le prestazioni evitando più chiamate a questa funzione.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Il contesto di sicurezza è stato inizializzato correttamente. Non è necessaria [**un'altra chiamata a InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) Se la funzione restituisce un token di output, ad esempio se **il \_ TOKEN SECBUFFER** in *pOutput* è di lunghezza diversa da zero, tale token deve essere inviato al server.<br/>                                                                                                   |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Il client deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e quindi passare l'output al server. Il client attende quindi un token restituito e lo passa, in un'altra chiamata, a [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md)<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | Il client deve completare la compilazione del messaggio e quindi chiamare [**la funzione CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Il client deve inviare il token di output al server e attendere un token restituito. Il client passa il token restituito in un'altra chiamata [**a InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) Il token di output può essere vuoto.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**SEC \_ I \_ INCOMPLETE \_ CREDENTIALS**</dt> </dl> | Il server ha richiesto l'autenticazione client, ma le credenziali fornite non includono un certificato o il certificato non è stato emesso da un'autorità di certificazione che il server considera attendibile. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                              |



 

Se la funzione ha esito negativo, la funzione restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                          | Descrizione                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl>          | Memoria insufficiente per completare l'azione richiesta.<br/>                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ ERRORE \_ INTERNO**</dt> </dl>               | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**HANDLE SEC \_ E \_ NON \_ VALIDO**</dt> </dl>               | L'handle passato alla funzione non è valido.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ E TOKEN NON \_ \_ VALIDO**</dt> </dl>                | Il formato del token di input non è valido. Le possibili cause includono un token danneggiato in transito, un token di dimensioni non corrette e un token passato nel pacchetto di sicurezza errato. Questa ultima condizione può verificarsi se il client e il server non negoziano il pacchetto di sicurezza appropriato.<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                 | Accesso non riuscito.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY**</dt> </dl> | Non è stato possibile contattare alcuna autorità per l'autenticazione. È possibile che il nome di dominio dell'entità di autenticazione non sia corretto, che il dominio non sia raggiungibile o che si sia verificato un errore di relazione di trust.<br/>                                                                    |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>               | Nel pacchetto di sicurezza non sono disponibili credenziali.<br/>                                                                                                                                    |
| <dl> <dt>**SEC \_ E \_ DESTINAZIONE \_ SCONOSCIUTA**</dt> </dl>               | La destinazione non è stata riconosciuta.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E FUNZIONE NON \_ \_ SUPPORTATA**</dt> </dl>         | Il valore del *parametro fContextReq* non è valido. Non è stato specificato un flag obbligatorio oppure è stato specificato un flag non supportato da CredSSP.<br/>                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ WRONG \_ PRINCIPAL**</dt> </dl>              | L'entità che ha ricevuto la richiesta di autenticazione non corrisponde a quella passata nel *parametro pszTargetName.* Questo errore indica un errore nell'autenticazione reciproca.<br/>                                                                                      |
| <dl> <dt>**SEC \_ E \_ DELEGATION \_ POLICY**</dt> </dl>            | I criteri non supportano la delega delle credenziali al server di destinazione.<br/>                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ POLICY \_ NLTM \_ ONLY**</dt> </dl>            | La delega delle credenziali al server di destinazione non è consentita quando non viene ottenuta l'autenticazione reciproca.<br/>                                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ MUTUAL \_ AUTH \_ FAILED**</dt> </dl>          | L'autenticazione del server non è riuscita quando il flag ISC \_ REQ MUTUAL AUTH è specificato nel \_ parametro \_ *fContextReq.*<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza, ma non è stato possibile stabilirlo, alcune applicazioni possono scegliere di arrestare immediatamente la connessione.

Se gli attributi del contesto di sicurezza non sono sufficienti, il client deve liberare il contesto creato parzialmente chiamando la [**funzione DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

Il client chiama la **funzione InitializeSecurityContext (CredSSP)** per inizializzare un contesto in uscita.

Per un contesto di sicurezza a due elementi, la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione con *phContext impostato* su **NULL** e inserisce nel descrittore del buffer il messaggio di input.
2.  Il pacchetto di sicurezza esamina i parametri e costruisce un token opaco, inserendolo nell'elemento TOKEN nella matrice di buffer. Se il *parametro fContextReq* include il flag **ISC \_ REQ \_ ALLOCATE \_ MEMORY,** il pacchetto di sicurezza alloca la memoria e restituisce il puntatore nell'elemento TOKEN.
3.  Il client invia il token restituito nel buffer *pOutput* al server di destinazione. Il server passa quindi il token come argomento di input in una chiamata alla funzione [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md)
4.  [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) può restituire un token. Il server invia questo token al client tramite una seconda chiamata **a InitializeSecurityContext (CredSSP)** se la prima chiamata ha restituito **SEC I CONTINUE \_ \_ \_ NEEDED**.

Se il server ha risposto correttamente, il pacchetto di sicurezza restituisce **SEC \_ E \_ OK** e viene stabilita una sessione protetta.

Se la funzione restituisce una delle risposte di errore, la risposta del server non viene accettata e la sessione non viene stabilita.

Se la funzione restituisce **SEC \_ I CONTINUE \_ \_ NEEDED,** **SEC I COMPLETE \_ \_ \_ NEEDED** o **SEC I COMPLETE AND \_ \_ \_ \_ CONTINUE,** i passaggi 2 e 3 vengono ripetuti.

L'inizializzazione del contesto di sicurezza può richiedere più di una chiamata a questa funzione, a seconda del meccanismo di autenticazione sottostante e delle scelte specificate nel *parametro fContextReq.*

I *parametri fContextReq* e *pfContextAttributes* sono maschera di bit che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [Requisiti di contesto.](context-requirements.md) Anche se *il parametro pfContextAttributes* è valido in caso di esito positivo, è necessario esaminare i flag che riguardano gli aspetti di sicurezza del contesto solo sul risultato finale con esito positivo. I valori restituiti intermedi possono impostare, ad esempio, il flag **ISC \_ RET \_ ALLOCATED \_ MEMORY.**

Se il flag **ISC \_ REQ \_ USE \_ SUPPLIED \_ CREDS** è impostato, il pacchetto di sicurezza deve cercare un tipo di buffer **SECBUFFER \_ PKG \_ PARAMS** nel buffer di input *pInput.* Anche se non si tratta di una soluzione generica, consente un'associazione forte di pacchetto di sicurezza e applicazione quando appropriato.

Se **è stato specificato ISC \_ REQ ALLOCATE \_ \_ MEMORY,** il chiamante deve liberare la memoria chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Ad esempio, il token di input potrebbe essere la richiesta di un GESTORE LAN. In questo caso, il token di output sarà la risposta crittografata con NTLM alla richiesta.

L'azione eseguita dal client dipende dal codice restituito da questa funzione. Se il codice restituito è **SEC \_ E \_ OK,** non sarà presente alcuna seconda chiamata **a InitializeSecurityContext (CredSSP)** e non è prevista alcuna risposta dal server. Se il codice restituito è **SEC \_ I CONTINUE \_ \_ NEEDED,** il client si aspetta un token in risposta dal server e lo passa in una seconda chiamata a **InitializeSecurityContext (CredSSP).** Il **codice restituito SEC \_ I COMPLETE \_ \_ NEEDED** indica che il client deve completare la compilazione del messaggio e chiamare la [**funzione CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) Il **codice SEC I COMPLETE AND \_ \_ \_ \_ CONTINUE** incorpora entrambe queste azioni.

Se **InitializeSecurityContext (CredSSP)** restituisce l'esito positivo alla prima (o unica) chiamata, il chiamante deve infine chiamare la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sull'handle restituito, anche se la chiamata non riesce in una fase successiva dello scambio di autenticazione.

Il client può chiamare **di nuovo InitializeSecurityContext (CredSSP)** dopo che è stato completato correttamente. Indica al pacchetto di sicurezza che è necessario eseguire una riautenticazione.

I chiamanti in modalità kernel hanno le [**differenze seguenti:**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)il nome di destinazione è una stringa [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) che deve essere allocata nella memoria virtuale tramite VirtualAlloc . non deve essere allocato dal pool. I buffer passati e forniti in *pInput* e *pOutput* devono essere nella memoria virtuale, non nel pool.

Se la funzione restituisce **SEC \_ I \_ INCOMPLETE \_ CREDENTIALS,** verificare che le credenziali r passate alla funzione [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) specificano un certificato valido e attendibile Il certificato deve essere un certificato di autenticazione client emesso da un'autorità di certificazione attendibile dal server. Per ottenere un elenco delle CA attendibili dal server, chiamare la funzione [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) con l'attributo **SECPKG \_ ATTR \_ ISSUER \_ LIST \_ EX.**

Dopo aver ricevuto un certificato di autenticazione da un'autorità di certificazione che il server considera attendibile, l'applicazione client crea una nuova credenziale. A tale scopo, chiama la funzione [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) e quindi chiama di nuovo **InitializeSecurityContext (CredSSP),** specificando le nuove credenziali nel *parametro phCredential.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (include Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
</dt> <dt>

[**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)
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

 

 
