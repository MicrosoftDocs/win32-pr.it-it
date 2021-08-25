---
description: Avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali.
ms.assetid: 21d965d4-3c03-4e29-a70d-4538c5c366b0
title: Funzione InitializeSecurityContext (General) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: e0a4b1b9ff38faa840667f513aee25d61c23180d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627367"
---
# <a name="initializesecuritycontext-general-function"></a>Funzione InitializeSecurityContext (Generale)

La **funzione InitializeSecurityContext (Generale)** avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali. La funzione viene usata per compilare un [*contesto di sicurezza*](../secgloss/s-gly.md) tra l'applicazione client e un peer remoto. **InitializeSecurityContext (Generale)** restituisce un token che il client deve passare al peer remoto, che il peer invia a sua volta all'implementazione della sicurezza locale tramite la chiamata [**AcceptSecurityContext (Generale).**](acceptsecuritycontext--general.md) Il token generato deve essere considerato opaco da tutti i chiamanti.

In genere, la **funzione InitializeSecurityContext (General)** viene chiamata in un ciclo fino a quando non viene stabilito un contesto [*di sicurezza*](../secgloss/s-gly.md) sufficiente.

Per informazioni sull'uso di questa funzione con un [*provider di supporto*](../secgloss/s-gly.md) per la sicurezza (SSP) specifico, vedere gli argomenti seguenti.



| Argomento                                                                                  | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)     | Avvia il contesto di [](../secgloss/s-gly.md) sicurezza in uscita sul lato client da un handle di credenziali usando il pacchetto di sicurezza CredSSP (Credential Security Support [*Provider).*](../secgloss/s-gly.md)  
| [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md)       | Avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali usando il pacchetto di [*sicurezza Digest*](../secgloss/s-gly.md).                        |
| [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)   | Avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali usando il pacchetto [*di sicurezza*](../secgloss/s-gly.md)Kerberos.                      |
| [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) | Avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali usando il pacchetto di [*sicurezza*](../secgloss/s-gly.md)Negotiate .                     |
| [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)           | Avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali usando il pacchetto di [*sicurezza*](../secgloss/s-gly.md)NTLM .                          |
| [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)   | Avvia il contesto di sicurezza in uscita sul lato client [*da*](../secgloss/s-gly.md) un handle di credenziali usando il pacchetto di [*sicurezza*](../secgloss/s-gly.md)Schannel .                      |



 

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

Handle per le credenziali restituite da [**AcquireCredentialsHandle (Generale).**](acquirecredentialshandle--general.md) Questo handle viene usato per compilare il [*contesto di sicurezza*](../secgloss/s-gly.md). La **funzione InitializeSecurityContext (Generale)** richiede almeno credenziali OUTBOUND.

</dd> <dt>

*phContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Nella prima chiamata a **InitializeSecurityContext (Generale)** questo puntatore è **NULL.** Nella seconda chiamata, questo parametro è un puntatore all'handle al contesto parzialmente formato restituito nel *parametro phNewContext* dalla prima chiamata.

Questo parametro è facoltativo con Microsoft Digest SSP e può essere impostato su **NULL.**

Quando si usa SSP Schannel, nella prima chiamata a **InitializeSecurityContext (Generale)** specificare **NULL.** Nelle chiamate future specificare il token ricevuto nel *parametro phNewContext* dopo la prima chiamata a questa funzione.

</dd> <dt>

*pTargetName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che indica la destinazione del contesto. Il contenuto della stringa [*è specifico del pacchetto*](../secgloss/s-gly.md) di sicurezza, come descritto nella tabella seguente. L'elenco non è completo. È possibile aggiungere altri provider di servizi di sistema e provider di servizi di terze parti a un sistema.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Provider di servizi condivisi in uso</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="Digest"></span><span id="digest"></span><span id="DIGEST"></span><dl> <dt><strong>Digest</strong></dt><dt></dt> </dl></td><td>Stringa con terminazione Null che identifica in modo univoco l'URI della risorsa richiesta. La stringa deve essere costituita da caratteri consentiti in un URI e deve essere rappresentabile dal set di codice ASCII degli Stati Uniti. La codifica percentuale può essere usata per rappresentare caratteri esterni al set di codice ASCII degli Stati Uniti.<br/></td></tr><tr class="even"><td><span id="Kerberos_or_Negotiate"></span><span id="kerberos_or_negotiate"></span><span id="KERBEROS_OR_NEGOTIATE"></span><dl> <dt><strong>Kerberos o Negotiate</strong></dt><dt></dt> </dl></td><td>Nome dell'entità servizio (SPN) o [*contesto di sicurezza*](../secgloss/s-gly.md) del server di destinazione.<br/></td></tr><tr class="odd"><td><span id="NTLM"></span><span id="ntlm"></span><dl> <dt><strong>NTLM</strong></dt><dt></dt> </dl></td><td>Nome dell'entità servizio (SPN) o [*contesto di sicurezza*](../secgloss/s-gly.md) del server di destinazione.<br/></td></tr><tr class="even"><td><span id="Schannel_SSL"></span><span id="schannel_ssl"></span><span id="SCHANNEL_SSL"></span><dl> <dt><strong>Schannel/SSL</strong></dt><dt></dt> </dl></td><td>Stringa con terminazione Null che identifica in modo univoco il server di destinazione. Schannel usa questo valore per verificare il certificato del server. Schannel usa anche questo valore per individuare la sessione nella cache di sessione quando si ristabilirà una connessione. La sessione memorizzata nella cache viene usata solo se vengono soddisfatte tutte le condizioni seguenti:<ul><li>Il nome di destinazione è lo stesso.</li><li>La voce della cache non è scaduta.</li><li>Il processo dell'applicazione che chiama la funzione è lo stesso.</li><li>La sessione di accesso è la stessa.</li><li>L'handle delle credenziali è lo stesso.</li></ul><br/></td></tr></tbody></table>



 

</dd> <dt>

*fContextReq* \[ Pollici\]
</dt> <dd>

Flag di bit che indicano le richieste per il contesto. Non tutti i pacchetti possono supportare tutti i requisiti. I flag usati per questo parametro sono preceduti da ISC \_ \_ REQ, ad esempio ISC \_ REQ \_ DELEGATE. Questo parametro può essere uno o più dei flag di attributi seguenti.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) alloca automaticamente i buffer di output. Al termine dell'uso dei buffer di output, liberarli chiamando la funzione [<strong>FreeContextBuffer</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Crittografare i messaggi usando la funzione [<strong>EncryptMessage</strong>](encryptmessage--general.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Il [*contesto di sicurezza*](../secgloss/s-gly.md) non gestirà i messaggi di formattazione. Questo valore è l'impostazione predefinita per la delega vincolata Kerberos, Negotiate e [*NTLM.*](../secgloss/s-gly.md)<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>Il server può usare il contesto per l'autenticazione ad altri server come client. Il ISC_REQ_MUTUAL_AUTH deve essere impostato per il funzionamento di questo flag. Valido per Kerberos. Ignorare questo flag per la [*delega vincolata.*](../secgloss/c-gly.md)<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Quando si verificano errori, l'entità remota riceverà una notifica.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl> <dt><strong>ISC_REQ_HTTP</strong></dt> </dl></td><td>Usare Digest per HTTP. Omettere questo flag per usare Digest come meccanismo SASL.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Firmare i messaggi e verificare le firme usando le funzioni [<strong>EncryptMessage</strong>](encryptmessage--general.md) e [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt> </dl></td><td>Schannel non deve autenticare automaticamente il server.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Verranno soddisfatti i criteri di autenticazione reciproca del servizio.<br/><blockquote>[!Caution]<br />
Questo non significa necessariamente che viene eseguita l'autenticazione reciproca, ma solo che vengono soddisfatti i criteri di autenticazione del servizio. Per assicurarsi che l'autenticazione reciproca sia eseguita, chiamare la funzione [<strong>QueryContextAttributes (General)</strong>](querycontextattributes--general.md).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Se questo flag è impostato, <strong>il</strong> flag ISC_REQ_INTEGRITY viene ignorato.<br/> Questo valore è supportato solo dalle delega vincolate Negotiate [*e*](../secgloss/s-gly.md)Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Rilevare i messaggi riprodotti codificati usando le funzioni [<strong>EncryptMessage</strong>](encryptmessage--general.md) o [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Rilevare i messaggi ricevuti fuori sequenza.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Supportare una connessione orientata al flusso.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>È necessario [*negoziare una*](../secgloss/s-gly.md) nuova chiave di sessione.<br/> Questo valore è supportato solo dalla delega [*vincolata*](../secgloss/s-gly.md)Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt> </dl></td><td>Schannel non deve tentare di fornire automaticamente le credenziali per il client.<br/></td></tr></tbody></table>



 

Gli attributi richiesti potrebbero non essere supportati dal client. Per altre informazioni, vedere il *parametro pfContextAttr.*

Per altre descrizioni dei vari attributi, vedere Requisiti [di contesto](context-requirements.md).

</dd> <dt>

*Riservato1* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*TargetDataRep* \[ Pollici\]
</dt> <dd>

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, nella destinazione. Questo parametro può essere SECURITY \_ NATIVE \_ DREP o SECURITY \_ NETWORK \_ DREP.

Questo parametro non viene usato con Digest o Schannel. Impostarlo su zero.

</dd> <dt>

*pInput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori ai buffer forniti come input per il pacchetto. A meno che il contesto client non sia stato avviato dal server, il valore di questo parametro deve essere **NULL** alla prima chiamata alla funzione. Nelle chiamate successive alla funzione o quando il contesto client è stato avviato dal server, il valore di questo parametro è un puntatore a un buffer allocato con memoria sufficiente per contenere il token restituito dal computer remoto.

</dd> <dt>

*Riservato2* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Alla prima chiamata a **InitializeSecurityContext (Generale)** questo puntatore riceve il nuovo handle di contesto. Nella seconda chiamata, *phNewContext* può essere uguale all'handle specificato nel *parametro phContext.*

Quando si usa SSP Schannel, nelle chiamate successive alla prima chiamata passare l'handle restituito qui come parametro *phContext* e specificare **NULL** per *phNewContext*.

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene puntatori alla [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che riceve i dati di output. Se un buffer è stato digitato come SEC \_ READWRITE nell'input, sarà presente nell'output. Il sistema alloca un buffer per il token di sicurezza se richiesto (tramite ISC REQ ALLOCATE MEMORY) e inserisce l'indirizzo nel descrittore del \_ buffer per il token di \_ \_ sicurezza.

Quando si usa Microsoft Digest provider di servizi condivisi, questo parametro riceve la risposta di richiesta che deve essere inviata al server.

Quando si usa SSP Schannel, se viene specificato il flag ISC REQ ALLOCATE MEMORY, il provider SSP Schannel alloca memoria per il buffer e inserirà le informazioni appropriate \_ \_ in \_ [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc). Inoltre, il chiamante deve passare un buffer di tipo **SECBUFFER \_ ALERT**. Nell'output, se viene generato un avviso, questo buffer contiene informazioni sull'avviso e la funzione ha esito negativo.

</dd> <dt>

*pfContextAttr* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile per ricevere un set di flag di bit che indicano [*gli attributi*](../secgloss/a-gly.md#_security_attribute_gly) del contesto stabilito. Per una descrizione dei vari attributi, vedere [Requisiti di contesto](context-requirements.md).

I flag usati per questo parametro sono preceduti da ISC \_ RET, ad esempio ISC \_ RET \_ DELEGATE. Per un elenco di valori validi, vedere il *parametro fContextReq.*

Non verificare la presenza di attributi correlati alla sicurezza finché la chiamata di funzione finale non viene restituita correttamente. I flag di attributo non correlati alla sicurezza, ad esempio il flag ASC RET ALLOCATED MEMORY, possono essere controllati \_ \_ prima della restituzione \_ finale.

> [!Note]  
> Particolari attributi di contesto possono cambiare durante la negoziazione con un peer remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il [*pacchetto di sicurezza restituirà*](../secgloss/s-gly.md) sempre questo valore nell'ora locale. Questo parametro è facoltativo e deve essere passato **NULL** per i client di breve durata.

Non esiste alcuna scadenza per le credenziali Microsoft Digest [*contesto*](../secgloss/s-gly.md)di sicurezza SSP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce uno dei codici di esito positivo seguenti.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | Il client deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e quindi passare l'output al server. Il client attende quindi un token restituito e lo passa, in un'altra chiamata, a [**InitializeSecurityContext (Generale).**](initializesecuritycontext--general.md)<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ COMPLETATO \_ \_ NECESSARIO**</dt> </dl>        | Il client deve completare la compilazione del messaggio e quindi chiamare la [**funzione CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | Il client deve inviare il token di output al server e attendere un token restituito. Il token restituito viene quindi passato in un'altra chiamata [**a InitializeSecurityContext (Generale).**](initializesecuritycontext--general.md) Il token di output può essere vuoto.<br/>                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ I \_ CREDENZIALI INCOMPLETE \_**</dt> </dl> | Usare con Schannel. Il server ha richiesto l'autenticazione client e le credenziali fornite non includono un certificato o il certificato non è stato emesso da un'autorità di certificazione attendibile dal server. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                              |
| <dl> <dt>**MESSAGGIO \_ SEC E \_ \_ INCOMPLETO**</dt> </dl>     | Usare con Schannel. I dati per l'intero messaggio non sono stati letti dalla rete.<br/> Quando viene restituito questo valore, il buffer *pInput* contiene una [**struttura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un **membro BufferType** **di SECBUFFER \_ MISSING**. Il **membro cbBuffer** di **SecBuffer** contiene un valore che indica il numero di byte aggiuntivi che la funzione deve leggere dal client prima che questa funzione riesca. Anche se questo numero non è sempre accurato, l'uso di può contribuire a migliorare le prestazioni evitando più chiamate a questa funzione.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Il [*contesto di sicurezza*](../secgloss/s-gly.md) è stato inizializzato correttamente. Non è necessaria un'altra [**chiamata a InitializeSecurityContext (General).**](initializesecuritycontext--general.md) Se la funzione restituisce un token di output, ad esempio se il TOKEN SECBUFFER \_ in *pOutput* è di lunghezza diversa da zero, tale token deve essere inviato al server.<br/>                                                                                                                                                    |



 

Se la funzione ha esito negativo, la funzione restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ MEMORIA \_ INSUFFICIENTE**</dt> </dl>          | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERRORE \_ INTERNO SEC E \_ \_**</dt> </dl>               | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**HANDLE \_ SEC E NON \_ \_ VALIDO**</dt> </dl>               | L'handle passato alla funzione non è valido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**TOKEN \_ SEC E NON \_ \_ VALIDO**</dt> </dl>                | L'errore è dovuto a un token di input in formato non valido, ad esempio un token danneggiato in transito, un token di dimensioni non corrette o un token passato nel pacchetto di [*sicurezza errato.*](../secgloss/s-gly.md) Il passaggio di un token al pacchetto errato può verificarsi se il client e il server non negoziano il pacchetto [*di sicurezza appropriato.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SEC \_ E \_ LOGON \_ DENIED**</dt> </dl>                 | L'accesso non è riuscito.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E NESSUNA AUTORITÀ DI \_ \_ \_ AUTENTICAZIONE**</dt> </dl> | Non è stato possibile contattare alcuna autorità per l'autenticazione. Il nome di dominio dell'entità autenticante potrebbe non essere corretto, il dominio potrebbe non essere raggiungibile o potrebbe esserci stato un errore di relazione di trust.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NESSUNA \_ CREDENZIALE**</dt> </dl>               | Nel pacchetto di sicurezza non sono disponibili [*credenziali*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**DESTINAZIONE \_ SEC E \_ \_ SCONOSCIUTA**</dt> </dl>               | La destinazione non è stata riconosciuta.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E FUNZIONE NON \_ \_ SUPPORTATA**</dt> </dl>         | Nel parametro fContextReq è stato specificato un flag di attributo di contesto non \_ valido (ISC REQ DELEGATE o \_ ISC \_ REQ \_ PROMPT FOR \_ \_ CREDS). <br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ WRONG \_ PRINCIPAL**</dt> </dl>              | L'entità che ha ricevuto la richiesta di autenticazione non corrisponde a quella passata nel *parametro pszTargetName.* Ciò indica un errore nell'autenticazione reciproca.<br/>                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza, ma non è stato possibile stabilirlo, alcune applicazioni possono scegliere di arrestare immediatamente la connessione.

Se gli attributi del [*contesto di sicurezza*](../secgloss/s-gly.md) non sono sufficienti, il client deve liberare il contesto creato parzialmente chiamando la funzione [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

La **funzione InitializeSecurityContext (Generale)** viene usata da un client per inizializzare un contesto in uscita.

Per un contesto di [*sicurezza a due elementi,*](../secgloss/s-gly.md)la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione con *phContext impostato* su **NULL** e inserisce nel descrittore del buffer il messaggio di input.
2.  Il [*pacchetto di*](../secgloss/s-gly.md) sicurezza esamina i parametri e costruisce un token opaco, inserendolo nell'elemento TOKEN nella matrice di buffer. Se il *parametro fContextReq* include il flag ISC REQ ALLOCATE MEMORY, il pacchetto di sicurezza alloca la memoria e restituisce il \_ \_ \_ puntatore nell'elemento TOKEN. [](../secgloss/s-gly.md)
3.  Il client invia il token restituito nel buffer *pOutput* al server di destinazione. Il server passa quindi il token come argomento di input in una chiamata alla [**funzione AcceptSecurityContext (General).**](acceptsecuritycontext--general.md)
4.  [**AcceptSecurityContext (Generale)**](acceptsecuritycontext--general.md) può restituire un token, che il server invia al client per una seconda chiamata a **InitializeSecurityContext (Generale)** se la prima chiamata ha restituito SEC \_ I CONTINUE \_ \_ NEEDED.

Per i contesti di sicurezza a [*più*](../secgloss/s-gly.md)livelli, ad esempio l'autenticazione reciproca, la sequenza di chiamata è la seguente:

1.  Il client chiama la funzione come descritto in precedenza, ma il pacchetto restituisce il codice di esito positivo SEC \_ I \_ CONTINUE \_ NEEDED.
2.  Il client invia il token di output al server e attende la risposta del server.
3.  Alla ricezione della risposta del server, il client chiama di nuovo **InitializeSecurityContext (Generale)** con *phContext* impostato sull'handle restituito dall'ultima chiamata. Il token ricevuto dal server viene fornito nel *parametro pInput.*

Se il server ha risposto correttamente, il pacchetto [*di sicurezza*](../secgloss/s-gly.md) restituisce SEC E OK e viene stabilita una \_ sessione \_ protetta.

Se la funzione restituisce una delle risposte di errore, la risposta del server non viene accettata e la sessione non viene stabilita.

Se la funzione restituisce SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED o SEC I COMPLETE AND CONTINUE, i passaggi \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2 e 3 vengono ripetuti.

Per inizializzare [*un*](../secgloss/s-gly.md)contesto di sicurezza, può essere necessaria più di una chiamata a questa funzione, a seconda del meccanismo di autenticazione sottostante e delle scelte specificate nel *fContextReq parametro.*

I *parametri fContextReq* e *pfContextAttributes* sono maschera di bit che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [Requisiti di contesto.](context-requirements.md) Il *parametro pfContextAttributes* è valido in caso di esito positivo, ma solo al completamento dell'operazione di restituzione è necessario esaminare i flag che riguardano gli aspetti di sicurezza del contesto. I valori restituiti intermedi possono impostare, ad esempio, il flag ISC \_ RET \_ ALLOCATED \_ MEMORY.

Se il flag ISC REQ USE SUPPLIED CREDS è impostato, il pacchetto di sicurezza deve cercare un tipo di \_ \_ buffer \_ \_ SECBUFFER PKG PARAMS [](../secgloss/s-gly.md) nel buffer di input \_ \_ *pInput.* Non si tratta di una soluzione generica, ma consente un'associazione forte di pacchetto [*di*](../secgloss/s-gly.md) sicurezza e applicazione quando appropriato.

Se è stato specificato ISC REQ ALLOCATE MEMORY, il chiamante deve liberare la \_ memoria chiamando la funzione \_ \_ [**FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Ad esempio, il token di input potrebbe essere la richiesta di un GESTORE LAN. In questo caso, il token di output sarà la risposta crittografata con NTLM alla richiesta.

L'azione eseguita dal client dipende dal codice restituito da questa funzione. Se il codice restituito è SEC E OK, non sarà presente alcuna seconda chiamata \_ \_ a **InitializeSecurityContext (General)** e non è prevista alcuna risposta dal server. Se il codice restituito è SEC I CONTINUE NEEDED, il client prevede un token in risposta dal server e lo passa in una seconda chiamata \_ \_ a \_ **InitializeSecurityContext (Generale).** Il codice restituito SEC I COMPLETE NEEDED indica che il client deve completare la compilazione del messaggio \_ e chiamare la funzione \_ \_ [**CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) Il codice SEC \_ I COMPLETE AND CONTINUE incorpora \_ \_ \_ entrambe queste azioni.

Se **InitializeSecurityContext (Generale)** restituisce l'esito positivo alla prima (o solo) chiamata, il chiamante deve chiamare la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sull'handle restituito, anche se la chiamata ha esito negativo in una parte successiva dello scambio di autenticazione.

Il client può chiamare **nuovamente InitializeSecurityContext (General)** dopo che è stato completato correttamente. Indica al pacchetto di sicurezza [*che è necessario*](../secgloss/s-gly.md) eseguire una riautenticazione.

I chiamanti in modalità kernel hanno le differenze seguenti: il nome di destinazione è una stringa [*Unicode*](../secgloss/u-gly.md) che deve essere allocata nella memoria virtuale tramite [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); non deve essere allocato dal pool. I buffer passati e forniti in *pInput* e *pOutput* devono essere nella memoria virtuale, non nel pool.

Quando si usa SSP Schannel, se la funzione restituisce SEC \_ I \_ INCOMPLETE CREDENTIALS, verificare di aver specificato un certificato valido e attendibile \_ nelle credenziali. Il certificato viene specificato quando si chiama [**la funzione AcquireCredentialsHandle (Generale).**](acquirecredentialshandle--general.md) Il certificato deve essere un certificato di autenticazione client emesso da un'autorità di certificazione (CA) attendibile dal server. Per ottenere un elenco delle CA attendibili dal server, chiamare la funzione [**QueryContextAttributes (General)**](querycontextattributes--general.md) e specificare l'attributo SECPKG \_ ATTR \_ ISSUER \_ LIST \_ EX.

Quando si usa SSP Schannel, dopo che un'applicazione client riceve un certificato di autenticazione da una CA considerato attendibile dal server, l'applicazione crea una nuova credenziale chiamando la funzione [**AcquireCredentialsHandle (General)**](acquirecredentialshandle--general.md) e quindi chiamando di nuovo **InitializeSecurityContext (General),** specificando le nuove credenziali nel *parametro phCredential.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Sspi.h (includere Security.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomi Unicode e ANSI<br/>   | **InitializeSecurityContextW** (Unicode) e **InitializeSecurityContextA** (ANSI)<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Generale)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**AcquireCredentialsHandle (generale)**](acquirecredentialshandle--general.md)
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

 

 
