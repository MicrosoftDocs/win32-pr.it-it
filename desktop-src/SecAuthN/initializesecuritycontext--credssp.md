---
description: Avvia il lato client, il contesto di sicurezza in uscita da un handle di credenziale.
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: Funzione InitializeSecurityContext (CredSSP) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: aa359fc0cedf96f43d93cfb7d962035453328759
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305863"
---
# <a name="initializesecuritycontext-credssp-function"></a>Funzione InitializeSecurityContext (CredSSP)

La funzione **InitializeSecurityContext (CredSSP)** avvia il lato client, il contesto di sicurezza in uscita da un handle di credenziale. La funzione compila un contesto di sicurezza tra l'applicazione client e un peer remoto. **InitializeSecurityContext (CredSSP)** restituisce un token che il client deve passare al peer remoto; il peer a sua volta invia il token all'implementazione della sicurezza locale tramite la chiamata a [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . Il token generato deve essere considerato opaco da tutti i chiamanti.

In genere, la funzione **InitializeSecurityContext (CredSSP)** viene chiamata in un ciclo fino a quando non viene stabilito un contesto di sicurezza sufficiente.

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

Handle per le credenziali restituite da [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md). Questo handle viene utilizzato per compilare il contesto di sicurezza. La funzione **InitializeSecurityContext (CredSSP)** richiede almeno credenziali in uscita.

</dd> <dt>

*phContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **InitializeSecurityContext (CredSSP)**, questo puntatore è **null**. Alla seconda chiamata, questo parametro è un puntatore all'handle per il contesto parzialmente formato restituito nel parametro *phNewContext* dalla prima chiamata.

Alla prima chiamata a **InitializeSecurityContext (CredSSP)** specificare **null**. Nelle chiamate future specificare il token ricevuto nel parametro *phNewContext* dopo la prima chiamata a questa funzione.

</dd> <dt>

*pTargetName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica in modo univoco il server di destinazione. SChannel utilizza questo valore per verificare il certificato del server. Schannel usa anche questo valore per individuare la sessione nella cache della sessione quando si ristabilisce una connessione. La sessione memorizzata nella cache viene utilizzata solo se vengono soddisfatte tutte le condizioni seguenti:

-   Il nome di destinazione è lo stesso.
-   La voce della cache non è scaduta.
-   Il processo dell'applicazione che chiama la funzione è lo stesso.
-   La sessione di accesso è la stessa.
-   L'handle delle credenziali è lo stesso.

</dd> <dt>

*fContextReq* \[ in\]
</dt> <dd>

Flag di bit che indicano le richieste per il contesto. Non tutti i pacchetti possono supportare tutti i requisiti. I flag usati per questo parametro sono preceduti da ISC \_ req \_ , ad esempio ISC \_ req \_ delegate.

Questo parametro può essere costituito da uno o più dei flag di attributi seguenti.



| Valore                                                                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_ Richieste di \_ allocazione \_ memoria**</dt> <dt>0x100</dt> </dl>                         | Il pacchetto di sicurezza alloca i buffer di output per il chiamante. Al termine dell'utilizzo dei buffer di output, è possibile liberarli chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_ 0x800 \_ connessione req**</dt> <dt></dt> </dl>                                         | Il contesto di sicurezza non gestirà i messaggi di formattazione.<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_ \_ \_ Errore esteso di req**</dt> <dt>0x4000</dt> </dl>                           | Quando si verificano errori, viene inviata una notifica all'entità remota.<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_ \_Convalida del \_ cred \_ Manuale di req**</dt> <dt>0x80000</dt> </dl> | Credential Security Support Provider (CredSSP) non deve autenticare il server automaticamente. Questo flag viene sempre impostato quando si utilizza CredSSP.<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_ \_ \_ Rilevamento sequenza req**</dt> <dt>0x8</dt> </dl>                           | Rilevare i messaggi ricevuti fuori sequenza.<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_ 0x8000 \_ flusso req**</dt> <dt></dt> </dl>                                                    | Supportare una connessione orientata al flusso.<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_ Uso di REQ \_ \_ fornito \_ credenziali**</dt> <dt>0x80</dt> </dl>                | CredSSP non deve tentare di fornire automaticamente le credenziali per il client.<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_ 0x1 \_ delegato req**</dt> <dt></dt> </dl>                                                 | Indica che le credenziali dell'utente devono essere delegate al server.<br/> Se questo flag non è specificato, al server viene delegato un set vuoto di credenziali.<br/> **Windows Server 2008 e Windows Vista:** Questo flag è obbligatorio.<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_ 0x2 \_ di \_ autenticazione reciproca di req**</dt> <dt></dt> </dl>                                       | Indica che l'autenticazione del server non è obbligatoria. Se questo flag non è specificato, i criteri di delega vengono ancora applicati.<br/> **Windows Server 2008 e Windows Vista:** Questo flag viene ignorato.<br/>                                                 |



 

Gli attributi richiesti potrebbero non essere supportati dal client. Per ulteriori informazioni, vedere il parametro *pfContextAttr* .

Per altre descrizioni dei diversi attributi, vedere [requisiti di contesto](context-requirements.md).

</dd> <dt>

*Reserved1* \[ in\]
</dt> <dd>

Riservato. Questo parametro deve essere impostato su zero.

</dd> <dt>

*TargetDataRep* \[ in\]
</dt> <dd>

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, sulla destinazione. Questo parametro può essere una **sicurezza \_ nativa \_ DREP** o **\_ \_ DREP della rete di sicurezza**.

</dd> <dt>

*Pinput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori ai buffer forniti come input per il pacchetto. A meno che il contesto client non sia stato avviato dal server, il valore di questo parametro deve essere **null** nella prima chiamata alla funzione. Nelle chiamate successive alla funzione o quando il contesto client è stato avviato dal server, il valore di questo parametro è un puntatore a un buffer allocato con memoria sufficiente per memorizzare il token restituito dal computer remoto.

Quando si effettuano chiamate a questa funzione dopo la chiamata iniziale, è necessario che siano presenti due buffer. Il primo ha il **tipo \_ token SECBUFFER** e contiene il token ricevuto dal server. Il secondo buffer è di tipo **SECBUFFER \_ vuoto**; impostare i membri **pvBuffer** e **cbBuffer** su zero.

</dd> <dt>

*Reserved2* \[ in\]
</dt> <dd>

Riservato. Questo parametro deve essere impostato su zero.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **InitializeSecurityContext (CredSSP)**, questo puntatore riceve il nuovo handle di contesto. Alla seconda chiamata, *phNewContext* può corrispondere all'handle specificato nel parametro *phContext* .

Nelle chiamate successive alla prima chiamata, passare l'handle restituito qui come parametro *phContext* e specificare **null** per *phNewContext*.

</dd> <dt>

*pOutput* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Questa struttura contiene a sua volta i puntatori alla struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che riceve i dati di output. Se un buffer è stato tipizzato come **sec \_ ReadWrite** nell'input, sarà presente nell'output. Il sistema alloca un buffer per il token di sicurezza, se richiesto (tramite **ISC \_ req \_ allocare \_ memoria**) e immettere l'indirizzo nel descrittore del buffer per il token di sicurezza.

Se viene specificato il flag di **\_ \_ allocazione della \_ memoria di ISC req** , CredSSP alloca memoria per il buffer e inserisce le informazioni appropriate in [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc).

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Puntatore a un set di flag di bit che indicano gli [*attributi*](../secgloss/a-gly.md#_security_attribute_gly) del contesto stabilito. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md).

I flag usati per questo parametro sono preceduti da ISC RET \_ , ad esempio **ISC \_ ret \_ delegate**. Per un elenco di valori validi, vedere il parametro *fContextReq* .

Non controllare gli attributi correlati alla sicurezza finché la chiamata di funzione finale non viene completata correttamente. I flag di attributo non correlati alla sicurezza, ad esempio il flag **ASC \_ ret \_ allocazioned \_ Memory** , possono essere controllati prima del ritorno finale.

> [!Note]  
> Attributi di contesto specifici possono essere modificati durante la negoziazione con un peer remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il pacchetto di sicurezza restituisca sempre questo valore nell'ora locale. Questo parametro è facoltativo e deve essere passato **null** per i client di breve durata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce uno dei seguenti codici di riuscita.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ messaggio incompleto \_**</dt> </dl>     | I dati per l'intero messaggio non sono stati letti dalla rete.<br/> Quando viene restituito questo valore, il buffer *Pinput* contiene una struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un membro **BufferType** di **SecBuffer \_ mancante**. Il membro **cbBuffer** di **SecBuffer** specifica il numero di byte aggiuntivi che la funzione deve leggere dal client prima che questa funzione abbia esito positivo. Anche se questo numero non è sempre accurato, l'uso di questo numero può contribuire a migliorare le prestazioni evitando più chiamate a questa funzione.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Il contesto di sicurezza è stato inizializzato correttamente. Non è necessario eseguire un'altra chiamata a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) . Se la funzione restituisce un token di output, ovvero se il **\_ token SECBUFFER** in *pOutput* è di lunghezza diversa da zero, il token deve essere inviato al server.<br/>                                                                                                   |
| <dl> <dt>**SEC \_ \_ completamento \_ e \_ continuazione**</dt> </dl> | Il client deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e quindi passare l'output al server. Il client attende quindi un token restituito e lo passa, in un'altra chiamata, a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md).<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ I \_ completamenti \_ necessari**</dt> </dl>        | Il client deve completare la compilazione del messaggio e quindi chiamare la funzione [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ \_ continuazione \_ necessaria**</dt> </dl>        | Il client deve inviare il token di output al server e attendere un token restituito. Il client passa il token restituito in un'altra chiamata a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). Il token di output può essere vuoto.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**SECONDI \_ di \_ credenziali incomplete \_**</dt> </dl> | Il server ha richiesto l'autenticazione client, ma le credenziali fornite non includono un certificato o il certificato non è stato emesso da un'autorità di certificazione considerata attendibile dal server. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                              |



 

Se la funzione ha esito negativo, la funzione restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                          | Descrizione                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ memoria insufficiente \_**</dt> </dl>          | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                                                                                                                                                     |
| <dl> <dt>**\_ \_ errore interno sec \_ E**</dt> </dl>               | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**\_handle sec E \_ non valido \_**</dt> </dl>               | L'handle passato alla funzione non è valido.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ token non valido \_**</dt> </dl>                | Il formato del token di input non è corretto. Le possibili cause includono un token danneggiato in transito, un token di dimensioni non corrette e un token passato al pacchetto di sicurezza errato. Questa ultima condizione può verificarsi se il client e il server non hanno negoziato il pacchetto di sicurezza appropriato.<br/> |
| <dl> <dt>**SEC \_ E \_ accesso \_ negato**</dt> </dl>                 | Accesso non riuscito.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ Nessuna \_ autorità di autenticazione \_**</dt> </dl> | Non è stato possibile contattare un'autorità per l'autenticazione. Il nome di dominio dell'entità di autenticazione potrebbe essere errato, il dominio potrebbe non essere raggiungibile o potrebbe essersi verificato un errore di relazione di trust.<br/>                                                                    |
| <dl> <dt>**SEC \_ E \_ Nessuna \_ credenziale**</dt> </dl>               | Nessuna credenziale disponibile nel pacchetto di sicurezza.<br/>                                                                                                                                    |
| <dl> <dt>**SEC \_ E \_ destinazione \_ sconosciuta**</dt> </dl>               | La destinazione non è stata riconosciuta.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ funzione non supportata \_**</dt> </dl>         | Il valore del parametro *fContextReq* non è valido. Non è stato specificato un flag obbligatorio oppure è stato specificato un flag non supportato da CredSSP.<br/>                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ entità errata \_**</dt> </dl>              | L'entità che ha ricevuto la richiesta di autenticazione non corrisponde a quella passata nel parametro *pszTargetName* . Questo errore indica un errore durante l'autenticazione reciproca.<br/>                                                                                      |
| <dl> <dt>**\_criteri di \_ delega sec E \_**</dt> </dl>            | Il criterio non supporta la delega delle credenziali al server di destinazione.<br/>                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ criteri \_ \_ solo NLTM**</dt> </dl>            | La delega delle credenziali al server di destinazione non è consentita quando non viene eseguita l'autenticazione reciproca.<br/>                                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ autenticazione reciproca \_ \_ non riuscita**</dt> </dl>          | L'autenticazione del server non è riuscita quando il \_ \_ flag di autenticazione reciproca req \_ di ISC viene specificato nel parametro *fContextReq* .<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza, ma non è stato possibile stabilirlo, alcune applicazioni potrebbero scegliere di arrestare immediatamente la connessione.

Se gli attributi del contesto di sicurezza non sono sufficienti, il client deve liberare il contesto parzialmente creato chiamando la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

Il client chiama la funzione **InitializeSecurityContext (CredSSP)** per inizializzare un contesto in uscita.

Per un contesto di sicurezza a due gambe, la sequenza chiamante è la seguente:

1.  Il client chiama la funzione con *phContext* impostato su **null** e compila il descrittore del buffer con il messaggio di input.
2.  Il pacchetto di sicurezza esamina i parametri e costruisce un token opaco, inserendolo nell'elemento TOKEN nella matrice di buffer. Se il parametro *fContextReq* include il flag **ISC di \_ \_ allocazione della \_ memoria** , il pacchetto di sicurezza alloca la memoria e restituisce il puntatore nell'elemento token.
3.  Il client invia il token restituito nel buffer *pOutput* al server di destinazione. Il server passa quindi il token come argomento di input in una chiamata alla funzione [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) .
4.  [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) può restituire un token. Il server invia il token al client tramite una seconda chiamata a **InitializeSecurityContext (CredSSP)** se la prima chiamata ha restituito il secondo, se è **\_ \_ \_ necessario continuare**.

Se il server ha risposto correttamente, il pacchetto di sicurezza restituisce **sec \_ e \_ OK** e viene stabilita una sessione protetta.

Se la funzione restituisce una delle risposte di errore, la risposta del server non viene accettata e la sessione non viene stabilita.

Se la funzione restituisce il secondo, è necessario **\_ \_ continuare \_**, il **secondo è \_ \_ \_ necessario**, o **sec \_ i \_ completati \_ e \_ continuano**, i passaggi 2 e 3 vengono ripetuti.

L'inizializzazione del contesto di sicurezza può richiedere più di una chiamata a questa funzione, a seconda del meccanismo di autenticazione sottostante, nonché delle opzioni specificate nel parametro *fContextReq* .

I parametri *fContextReq* e *pfContextAttributes* sono maschere di maschera che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md). Anche se il parametro *pfContextAttributes* è valido in caso di esito positivo, è necessario esaminare i flag che riguardano gli aspetti di sicurezza del contesto solo per la restituzione finale riuscita. I ritorni intermedi possono impostare, ad esempio, il flag di **\_ \_ \_ memoria allocata RET di ISC** .

Se viene impostata la richiesta di utilizzo del flag **\_ \_ \_ \_ credenziali fornito da ISC** , il pacchetto di sicurezza deve cercare un tipo di buffer **SECBUFFER \_ pkg \_ params** nel buffer di input *Pinput* . Sebbene non si tratta di una soluzione generica, è possibile associare in modo sicuro le applicazioni e i pacchetti di sicurezza.

Se è stata specificata la **memoria di ISC \_ req \_ allocata \_** , il chiamante deve liberare la memoria chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Ad esempio, il token di input potrebbe essere la sfida di un gestore di LAN. In questo caso, il token di output sarà la risposta crittografata NTLM alla richiesta di verifica.

L'azione eseguita dal client dipende dal codice restituito da questa funzione. Se il codice restituito è **sec \_ E \_ OK**, non sarà prevista alcuna seconda chiamata a **InitializeSecurityContext (CredSSP)** e non sarà prevista alcuna risposta dal server. Se il codice restituito è **sec \_ , \_ continuerà \_** a essere necessario, il client aspetta un token in risposta dal server e lo passa in una seconda chiamata a **InitializeSecurityContext (CredSSP)**. Il codice restituito necessario per il **\_ \_ completamento \_ del secondo** indica che il client deve completare la compilazione del messaggio e chiamare la funzione [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . Il **codice \_ \_ per il completamento \_ e la \_ continuazione** del codice incorpora entrambe le azioni.

Se **InitializeSecurityContext (CredSSP)** restituisce Success sulla prima o solo chiamata, il chiamante deve chiamare la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sull'handle restituito, anche se la chiamata ha esito negativo in una fase successiva dello scambio di autenticazione.

Il client può chiamare nuovamente **InitializeSecurityContext (CredSSP)** dopo che è stato completato correttamente. Indica al pacchetto di sicurezza che si desidera una riautenticazione.

I chiamanti in modalità kernel presentano le differenze seguenti: il nome di destinazione è una stringa [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) che deve essere allocata nella memoria virtuale usando [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); non deve essere allocato dal pool. I buffer passati e specificati in *Pinput* e *pOutput* devono trovarsi nella memoria virtuale, non nel pool.

Se la funzione restituisce **le \_ \_ \_ credenziali incomplete del secondo**, verificare che le credenziali r passate alla funzione [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) abbiano specificato un certificato valido e attendibile il certificato deve essere un certificato di autenticazione client emesso da un'autorità di certificazione considerata attendibile dal server. Per ottenere un elenco delle CA considerate attendibili dal server, chiamare la funzione [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) con l'attributo **SECPKG \_ attr \_ Issuer \_ List \_ ex** .

Dopo aver ricevuto un certificato di autenticazione da un'autorità di certificazione che il server considera attendibile, l'applicazione client crea una nuova credenziale. Questa operazione viene eseguita chiamando la funzione [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) e chiamando di nuovo **InitializeSecurityContext (CredSSP)** , specificando la nuova credenziale nel parametro *phCredential* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
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

 

 
