---
description: Avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle delle credenziali utilizzando la [*delega vincolata*](../secgloss/s-gly.md)Negotiate.
ms.assetid: 031b0e82-f246-4291-aed3-f443ab152e00
title: Funzione InitializeSecurityContext (Negotiate) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f4fd8c68896f10627ff1d66c3f576ca06d67e029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880694"
---
# <a name="initializesecuritycontext-negotiate-function"></a>Funzione InitializeSecurityContext (Negotiate)

La funzione **InitializeSecurityContext (Negotiate)** avvia il lato client, il [*contesto di sicurezza*](../secgloss/s-gly.md) in uscita da un handle di credenziale. La funzione viene utilizzata per creare un [*contesto di sicurezza*](../secgloss/s-gly.md) tra l'applicazione client e un peer remoto. **InitializeSecurityContext (Negotiate)** restituisce un token che il client deve passare al peer remoto, a sua volta inviato dal peer all'implementazione della sicurezza locale tramite la chiamata [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) . Il token generato deve essere considerato opaco da tutti i chiamanti.

In genere, la funzione **InitializeSecurityContext (Negotiate)** viene chiamata in un ciclo fino a quando non viene stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) sufficiente.

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

Handle per le credenziali restituite da [**AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md). Questo handle viene utilizzato per compilare il [*contesto di sicurezza*](../secgloss/s-gly.md). La funzione **InitializeSecurityContext (Negotiate)** richiede almeno credenziali in uscita.

</dd> <dt>

*phContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **InitializeSecurityContext (Negotiate)**, questo puntatore è **null**. Alla seconda chiamata, questo parametro è un puntatore all'handle per il contesto parzialmente formato restituito nel parametro *phNewContext* dalla prima chiamata.

</dd> <dt>

*pszTargetName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione null che indica il nome dell'entità servizio (SPN) o il [*contesto di sicurezza*](../secgloss/s-gly.md) del server di destinazione.

Le applicazioni devono fornire un nome SPN valido per attenuare gli attacchi di riproduzione.

</dd> <dt>

*fContextReq* \[ in\]
</dt> <dd>

Flag di bit che indicano le richieste per il contesto. Non tutti i pacchetti possono supportare tutti i requisiti. I flag usati per questo parametro sono preceduti da ISC \_ req \_ , ad esempio ISC \_ req \_ delegate. Questo parametro può essere costituito da uno o più dei flag di attributi seguenti.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) alloca automaticamente i buffer di output. Al termine dell'utilizzo dei buffer di output, è possibile liberarli chiamando la funzione [<strong>FreeContextBuffer</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-freecontextbuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Crittografare i messaggi utilizzando la funzione [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Il [*contesto di sicurezza*](../secgloss/s-gly.md) non gestirà i messaggi di formattazione. Questo è il valore predefinito.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>Il server può utilizzare il contesto per l'autenticazione ad altri server come client. Per il corretto funzionamento di questo flag è necessario impostare il flag ISC_REQ_MUTUAL_AUTH. Valido per Kerberos. Ignorare questo flag per la [*delega vincolata*](../secgloss/c-gly.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Quando si verificano errori, viene inviata una notifica all'entità remota.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Firmare i messaggi e verificare le firme usando le funzioni [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) e [<strong>MakeSignature</strong>] (makesignature.MD).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Verranno soddisfatti i criteri di autenticazione reciproca del servizio.<br/><blockquote>[!Caution]<br />
Ciò non significa necessariamente che venga eseguita l'autenticazione reciproca, solo che i criteri di autenticazione del servizio siano soddisfatti. Per assicurarsi che venga eseguita l'autenticazione reciproca, chiamare la funzione [<strong>QueryContextAttributes (Negotiate)</strong>] (QueryContextAttributes--Negotiate.MD).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Se questo flag è impostato, il flag di <strong>ISC_REQ_INTEGRITY</strong> viene ignorato.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Rilevare i messaggi riprodotti che sono stati codificati tramite le funzioni [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) o [<strong>MakeSignature</strong>] (makesignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Rilevare i messaggi ricevuti fuori sequenza.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Supportare una connessione orientata al flusso.<br/></td></tr></tbody></table>



 

Gli attributi richiesti potrebbero non essere supportati dal client. Per ulteriori informazioni, vedere il parametro *pfContextAttr* .

Per altre descrizioni dei diversi attributi, vedere [requisiti di contesto](context-requirements.md).

</dd> <dt>

*Reserved1* \[ in\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*TargetDataRep* \[ in\]
</dt> <dd>

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, sulla destinazione. Questo parametro può essere una sicurezza \_ nativa \_ DREP o DREP della rete di sicurezza \_ \_ .

</dd> <dt>

*Pinput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori ai buffer forniti come input per il pacchetto. A meno che il contesto client non sia stato avviato dal server, il valore di questo parametro deve essere **null** nella prima chiamata alla funzione. Nelle chiamate successive alla funzione o quando il contesto client è stato avviato dal server, il valore di questo parametro è un puntatore a un buffer allocato con memoria sufficiente per memorizzare il token restituito dal computer remoto.

</dd> <dt>

*Reserved2* \[ in\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **InitializeSecurityContext (Negotiate)**, questo puntatore riceve il nuovo handle di contesto. Alla seconda chiamata, *phNewContext* può corrispondere all'handle specificato nel parametro *phContext* .

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene i puntatori alla struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che riceve i dati di output. Se un buffer è stato tipizzato come SEC \_ ReadWrite nell'input, sarà presente nell'output. Il sistema alloca un buffer per il token di sicurezza, se richiesto (tramite ISC \_ req \_ allocare \_ memoria) e immettere l'indirizzo nel descrittore del buffer per il token di sicurezza.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Puntatore a una variabile per ricevere un set di flag di bit che indicano gli [*attributi*](../secgloss/a-gly.md#_security_attribute_gly) del contesto stabilito. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md).

I flag usati per questo parametro sono preceduti da ISC RET \_ , ad esempio ISC \_ ret \_ delegate. Per un elenco di valori validi, vedere il parametro *fContextReq* .

Non controllare gli attributi correlati alla sicurezza finché la chiamata di funzione finale non viene completata correttamente. I flag di attributo non correlati alla sicurezza, ad esempio il \_ flag ASC RET \_ allocazioned \_ Memory, possono essere controllati prima del ritorno finale.

> [!Note]  
> Attributi di contesto specifici possono essere modificati durante la negoziazione con un peer remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituisca sempre questo valore nell'ora locale. Questo parametro è facoltativo e deve essere passato **null** per i client di breve durata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce uno dei seguenti codici di esito positivo.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Il [*contesto di sicurezza*](../secgloss/s-gly.md) è stato inizializzato correttamente. Non è necessario eseguire un'altra chiamata a [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) . Se la funzione restituisce un token di output, ovvero se il token SECBUFFER \_ in *pOutput* è di lunghezza diversa da zero, il token deve essere inviato al server.<br/> |
| <dl> <dt>**SEC \_ \_ completamento \_ e \_ continuazione**</dt> </dl> | Il client deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e quindi passare l'output al server. Il client attende quindi un token restituito e lo passa, in un'altra chiamata, a [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md).<br/>                                                                                                                                  |
| <dl> <dt>**SEC \_ I \_ completamenti \_ necessari**</dt> </dl>        | Il client deve completare la compilazione del messaggio e quindi chiamare la funzione [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ \_ continuazione \_ necessaria**</dt> </dl>        | Il client deve inviare il token di output al server e attendere un token restituito. Il token restituito viene quindi passato in un'altra chiamata a [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md). Il token di output può essere vuoto.<br/>                                                                                                                                                       |



 

Se la funzione ha esito negativo, la funzione restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ memoria insufficiente \_**</dt> </dl>          | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**\_ \_ errore interno sec \_ E**</dt> </dl>               | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**\_handle sec E \_ non valido \_**</dt> </dl>               | L'handle passato alla funzione non è valido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ token non valido \_**</dt> </dl>                | L'errore è dovuto a un token di input in formato non valido, ad esempio un token danneggiato in transito, un token di dimensioni non corrette o un token passato alla [*delega vincolata*](../secgloss/s-gly.md)errata. Il passaggio di un token al pacchetto errato può verificarsi se il client e il server non hanno negoziato la [*delega vincolata*](../secgloss/s-gly.md)corretta.<br/> |
| <dl> <dt>**SEC \_ E \_ accesso \_ negato**</dt> </dl>                 | Accesso non riuscito.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ Nessuna \_ autorità di autenticazione \_**</dt> </dl> | Non è stato possibile contattare un'autorità per l'autenticazione. Il nome di dominio dell'entità di autenticazione potrebbe essere errato, il dominio potrebbe non essere raggiungibile o potrebbe essersi verificato un errore di relazione di trust.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ Nessuna \_ credenziale**</dt> </dl>               | Nessuna credenziale disponibile nella [*delega vincolata*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ destinazione \_ sconosciuta**</dt> </dl>               | La destinazione non è stata riconosciuta.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E \_ funzione non supportata \_**</dt> </dl>         | Nel parametro FContextReq è stato specificato un flag di attributo di contesto non valido (ISC \_ req \_ delegate o ISC \_ req \_ prompt \_ per \_ credenziali). <br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ entità errata \_**</dt> </dl>              | L'entità che ha ricevuto la richiesta di autenticazione non corrisponde a quella passata nel parametro *pszTargetName* . Ciò indica un errore durante l'autenticazione reciproca.<br/>                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza, ma non è stato possibile stabilirlo, alcune applicazioni potrebbero scegliere di arrestare immediatamente la connessione.

Se gli attributi del [*contesto di sicurezza*](../secgloss/s-gly.md) non sono sufficienti, il client deve liberare il contesto parzialmente creato chiamando la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

La funzione **InitializeSecurityContext (Negotiate)** viene utilizzata da un client per inizializzare un contesto in uscita.

Per un [*contesto di sicurezza*](../secgloss/s-gly.md)a due gambe, la sequenza chiamante è la seguente:

1.  Il client chiama la funzione con *phContext* impostato su **null** e compila il descrittore del buffer con il messaggio di input.
2.  Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) esamina i parametri e costruisce un token opaco, inserendolo nell'elemento token nella matrice di buffer. Se il parametro *fContextReq* include il \_ flag ISC \_ di allocazione della \_ memoria, il [*pacchetto di sicurezza*](../secgloss/s-gly.md) alloca la memoria e restituisce il puntatore nell'elemento token.
3.  Il client invia il token restituito nel buffer *pOutput* al server di destinazione. Il server passa quindi il token come argomento di input in una chiamata alla funzione [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .
4.  [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) può restituire un token, che il server invia al client per una seconda chiamata a **InitializeSecurityContext (Negotiate)** se la prima chiamata restituita al secondo per \_ \_ continuare \_ .

Per i [*contesti di sicurezza*](../secgloss/s-gly.md)a più gambe, ad esempio l'autenticazione reciproca, la sequenza chiamante è la seguente:

1.  Il client chiama la funzione come descritto in precedenza, ma il pacchetto restituisce il \_ \_ codice di \_ esito positivo continuo necessario.
2.  Il client invia il token di output al server e attende la risposta del server.
3.  Al momento della ricezione della risposta del server, il client chiama di nuovo **InitializeSecurityContext (Negotiate)** , con *phContext* impostato sull'handle restituito dall'ultima chiamata a. Il token ricevuto dal server viene fornito nel parametro *Pinput* .

Se il server ha risposto correttamente, il [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituisce sec \_ e \_ OK e viene stabilita una sessione protetta.

Se la funzione restituisce una delle risposte di errore, la risposta del server non viene accettata e la sessione non viene stabilita.

Se la funzione restituisce il secondo, è necessario continuare, il \_ \_ \_ secondo \_ \_ \_ è necessario, o sec \_ i \_ completati \_ e \_ continuano, i passaggi 2 e 3 vengono ripetuti.

Per inizializzare un [*contesto di sicurezza*](../secgloss/s-gly.md), potrebbe essere necessaria più di una chiamata a questa funzione, a seconda del meccanismo di autenticazione sottostante, nonché delle opzioni specificate nel parametro *fContextReq* .

I parametri *fContextReq* e *pfContextAttributes* sono maschere di maschera che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md). Il parametro *pfContextAttributes* è valido in caso di esito positivo, ma solo in caso di esito positivo finale è possibile esaminare i flag relativi agli aspetti di sicurezza del contesto. I ritorni intermedi possono impostare, ad esempio, \_ il \_ flag di memoria allocata RET di ISC \_ .

Se viene impostata la richiesta di \_ \_ utilizzo del \_ flag credenziali fornito da ISC \_ , il [*pacchetto di sicurezza*](../secgloss/s-gly.md) deve cercare un tipo di \_ buffer SECBUFFER pkg \_ params nel buffer di input *Pinput* . Non si tratta di una soluzione generica, ma consente un forte accoppiamento del [*pacchetto di sicurezza*](../secgloss/s-gly.md) e dell'applicazione quando appropriato.

Se \_ \_ \_ è stata specificata la memoria di ISC req allocata, il chiamante deve liberare la memoria chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Ad esempio, il token di input potrebbe essere la sfida di un gestore di LAN. In questo caso, il token di output sarà la risposta crittografata NTLM alla richiesta di verifica.

L'azione eseguita dal client dipende dal codice restituito da questa funzione. Se il codice restituito è SEC \_ E \_ OK, non sarà prevista alcuna seconda chiamata **InitializeSecurityContext (Negotiate)** e non sarà prevista alcuna risposta dal server. Se il codice restituito è SEC \_ \_ , continuerà a essere \_ necessario, il client aspetta un token in risposta dal server e lo passa in una seconda chiamata a **InitializeSecurityContext (Negotiate)**. Il \_ \_ \_ codice restituito necessario per il completamento del secondo indica che il client deve completare la compilazione del messaggio e chiamare la funzione [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . Il \_ \_ \_ codice per il completamento e la \_ continuazione del codice incorpora entrambe le azioni.

Se **InitializeSecurityContext (Negotiate)** restituisce Success sulla prima o solo chiamata, il chiamante deve chiamare la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sull'handle restituito, anche se la chiamata ha esito negativo in una fase successiva dello scambio di autenticazione.

Il client può chiamare nuovamente **InitializeSecurityContext (Negotiate)** dopo che è stato completato correttamente. Indica al pacchetto di [*sicurezza*](../secgloss/s-gly.md) che si desidera una riautenticazione.

I chiamanti in modalità kernel presentano le differenze seguenti: il nome di destinazione è una stringa [*Unicode*](../secgloss/u-gly.md) che deve essere allocata nella memoria virtuale usando [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); non deve essere allocato dal pool. I buffer passati e specificati in *Pinput* e *pOutput* devono trovarsi nella memoria virtuale, non nel pool.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (negoziazione)**](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[**AcquireCredentialsHandle (negoziazione)**](acquirecredentialshandle--negotiate.md)
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

 

 
