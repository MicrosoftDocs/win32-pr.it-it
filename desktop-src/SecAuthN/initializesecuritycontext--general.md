---
description: Avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle di credenziale.
ms.assetid: 21d965d4-3c03-4e29-a70d-4538c5c366b0
title: Funzione InitializeSecurityContext (General) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: bc96fe74202f1380d2d85946a373f176e14dfd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348076"
---
# <a name="initializesecuritycontext-general-function"></a>Funzione InitializeSecurityContext (General)

La funzione **InitializeSecurityContext (General)** avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle di credenziale. La funzione viene utilizzata per creare un [*contesto di sicurezza*](../secgloss/s-gly.md) tra l'applicazione client e un peer remoto. **InitializeSecurityContext (generale)** restituisce un token che il client deve passare al peer remoto, che a sua volta viene inviato all'implementazione della sicurezza locale tramite la chiamata [**AcceptSecurityContext (generale)**](acceptsecuritycontext--general.md) . Il token generato deve essere considerato opaco da tutti i chiamanti.

In genere, la funzione **InitializeSecurityContext (generale)** viene chiamata in un ciclo fino a quando non viene stabilito un [*contesto di sicurezza*](../secgloss/s-gly.md) sufficiente.

Per informazioni sull'utilizzo di questa funzione con un [*Security Support Provider*](../secgloss/s-gly.md) specifico (SSP), vedere gli argomenti seguenti.



| Argomento                                                                                  | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)     | Avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle delle credenziali utilizzando il [*pacchetto di sicurezza*](../secgloss/s-gly.md)Credential Security Support Provider (CredSSP).  
| [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md)       | Avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle delle credenziali utilizzando il [*pacchetto di sicurezza*](../secgloss/s-gly.md)digest.                        |
| [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)   | Avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle delle credenziali utilizzando il [*pacchetto di sicurezza*](../secgloss/s-gly.md)Kerberos.                      |
| [**InitializeSecurityContext (negoziazione)**](initializesecuritycontext--negotiate.md) | Avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle delle credenziali utilizzando il [*pacchetto di sicurezza*](../secgloss/s-gly.md)Negotiate.                     |
| [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)           | Avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle delle credenziali utilizzando il [*pacchetto di sicurezza*](../secgloss/s-gly.md)NTLM.                          |
| [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)   | Avvia il lato client, il contesto di [*sicurezza*](../secgloss/s-gly.md) in uscita da un handle delle credenziali usando il [*pacchetto di sicurezza*](../secgloss/s-gly.md)Schannel.                      |



 

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

Handle per le credenziali restituite da [**AcquireCredentialsHandle (generale)**](acquirecredentialshandle--general.md). Questo handle viene utilizzato per compilare il [*contesto di sicurezza*](../secgloss/s-gly.md). La funzione **InitializeSecurityContext (generale)** richiede almeno credenziali in uscita.

</dd> <dt>

*phContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **InitializeSecurityContext (generale)**, questo puntatore è **null**. Alla seconda chiamata, questo parametro è un puntatore all'handle per il contesto parzialmente formato restituito nel parametro *phNewContext* dalla prima chiamata.

Questo parametro è facoltativo con il SSP Microsoft Digest e può essere impostato su **null**.

Quando si usa SSP Schannel, alla prima chiamata a **InitializeSecurityContext (generale)** specificare **null**. Nelle chiamate future specificare il token ricevuto nel parametro *phNewContext* dopo la prima chiamata a questa funzione.

</dd> <dt>

*pTargetName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa con terminazione null che indica la destinazione del contesto. Il contenuto della stringa è specifico del [*pacchetto di sicurezza*](../secgloss/s-gly.md) , come descritto nella tabella seguente. L'elenco non è completo. È possibile aggiungere altri SSP di sistema e SSP di terze parti a un sistema.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>SSP in uso</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="Digest"></span><span id="digest"></span><span id="DIGEST"></span><dl> <dt><strong>Digest</strong></dt><dt></dt> </dl></td><td>Stringa con terminazione null che identifica in modo univoco l'URI della risorsa richiesta. La stringa deve essere composta da caratteri consentiti in un URI e deve essere rappresentabile dal set di codici ASCII US. È possibile usare la codifica percent per rappresentare i caratteri al di fuori del set di codici ASCII US.<br/></td></tr><tr class="even"><td><span id="Kerberos_or_Negotiate"></span><span id="kerberos_or_negotiate"></span><span id="KERBEROS_OR_NEGOTIATE"></span><dl> <dt><strong>Kerberos o negoziazione</strong></dt><dt></dt> </dl></td><td>Nome dell'entità servizio (SPN) o il [*contesto di sicurezza*](../secgloss/s-gly.md) del server di destinazione.<br/></td></tr><tr class="odd"><td><span id="NTLM"></span><span id="ntlm"></span><dl> <dt><strong>NTLM</strong></dt><dt></dt> </dl></td><td>Nome dell'entità servizio (SPN) o il [*contesto di sicurezza*](../secgloss/s-gly.md) del server di destinazione.<br/></td></tr><tr class="even"><td><span id="Schannel_SSL"></span><span id="schannel_ssl"></span><span id="SCHANNEL_SSL"></span><dl> <dt><strong>Schannel/SSL</strong></dt><dt></dt> </dl></td><td>Stringa con terminazione null che identifica in modo univoco il server di destinazione. SChannel utilizza questo valore per verificare il certificato del server. Schannel usa anche questo valore per individuare la sessione nella cache della sessione quando si ristabilisce una connessione. La sessione memorizzata nella cache viene utilizzata solo se vengono soddisfatte tutte le condizioni seguenti:<ul><li>Il nome di destinazione è lo stesso.</li><li>La voce della cache non è scaduta.</li><li>Il processo dell'applicazione che chiama la funzione è lo stesso.</li><li>La sessione di accesso è la stessa.</li><li>L'handle delle credenziali è lo stesso.</li></ul><br/></td></tr></tbody></table>



 

</dd> <dt>

*fContextReq* \[ in\]
</dt> <dd>

Flag di bit che indicano le richieste per il contesto. Non tutti i pacchetti possono supportare tutti i requisiti. I flag usati per questo parametro sono preceduti da ISC \_ req \_ , ad esempio ISC \_ req \_ delegate. Questo parametro può essere costituito da uno o più dei flag di attributi seguenti.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valore</th><th>Significato</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) alloca automaticamente i buffer di output. Al termine dell'utilizzo dei buffer di output, è possibile liberarli chiamando la funzione [<strong>FreeContextBuffer</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-freecontextbuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Crittografare i messaggi utilizzando la funzione [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Il [*contesto di sicurezza*](../secgloss/s-gly.md) non gestirà i messaggi di formattazione. Questo valore è l'impostazione predefinita per le istanze della [*delega vincolata*](../secgloss/s-gly.md)Kerberos, Negotiate e NTLM.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>Il server può utilizzare il contesto per l'autenticazione ad altri server come client. Per il corretto funzionamento di questo flag è necessario impostare il flag ISC_REQ_MUTUAL_AUTH. Valido per Kerberos. Ignorare questo flag per la [*delega vincolata*](../secgloss/c-gly.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Quando si verificano errori, viene inviata una notifica all'entità remota.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl> <dt><strong>ISC_REQ_HTTP</strong></dt> </dl></td><td>Usare digest per HTTP. Omettere questo flag per utilizzare il digest come meccanismo SASL.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Firmare i messaggi e verificare le firme usando le funzioni [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) e [<strong>MakeSignature</strong>] (makesignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt> </dl></td><td>Schannel non deve autenticare il server automaticamente.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Verranno soddisfatti i criteri di autenticazione reciproca del servizio.<br/><blockquote>[!Caution]<br />
Ciò non significa necessariamente che venga eseguita l'autenticazione reciproca, solo che i criteri di autenticazione del servizio siano soddisfatti. Per assicurarsi che venga eseguita l'autenticazione reciproca, chiamare la funzione [<strong>QueryContextAttributes (generale)</strong>] (QueryContextAttributes--General.MD).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Se questo flag è impostato, il flag di <strong>ISC_REQ_INTEGRITY</strong> viene ignorato.<br/> Questo valore è supportato solo dalla [*delega vincolata*](../secgloss/s-gly.md)Negotiate e Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Rilevare i messaggi riprodotti che sono stati codificati tramite le funzioni [<strong>EncryptMessage</strong>] (EncryptMessage--General.MD) o [<strong>MakeSignature</strong>] (makesignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Rilevare i messaggi ricevuti fuori sequenza.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Supportare una connessione orientata al flusso.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>È necessario negoziare una nuova [*chiave di sessione*](../secgloss/s-gly.md) .<br/> Questo valore è supportato solo dalla [*delega vincolata*](../secgloss/s-gly.md)Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt> </dl></td><td>Schannel non deve tentare di fornire automaticamente le credenziali per il client.<br/></td></tr></tbody></table>



 

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

Questo parametro non viene usato con digest o Schannel. Impostarlo su zero.

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

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **InitializeSecurityContext (generale)**, questo puntatore riceve il nuovo handle di contesto. Alla seconda chiamata, *phNewContext* può corrispondere all'handle specificato nel parametro *phContext* .

Quando si usa SSP Schannel, quando si effettuano chiamate dopo la prima chiamata, passare l'handle restituito qui come parametro *phContext* e specificare **null** per *phNewContext*.

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene i puntatori alla struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che riceve i dati di output. Se un buffer è stato tipizzato come SEC \_ ReadWrite nell'input, sarà presente nell'output. Il sistema alloca un buffer per il token di sicurezza, se richiesto (tramite ISC \_ req \_ allocare \_ memoria) e immettere l'indirizzo nel descrittore del buffer per il token di sicurezza.

Quando si utilizza il provider di servizi condivisi Microsoft Digest, questo parametro riceve la risposta alla richiesta di verifica da inviare al server.

Quando si usa SSP Schannel, se \_ \_ si specifica il flag ISC di allocazione della \_ memoria, SSP Schannel alloca memoria per il buffer e inserisce le informazioni appropriate in [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc). Inoltre, il chiamante deve passare un buffer di tipo **SECBUFFER \_ Alert**. Nell'output, se viene generato un avviso, questo buffer contiene informazioni sull'avviso e la funzione ha esito negativo.

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

Non esiste alcuna ora di scadenza per il [*contesto di sicurezza*](../secgloss/s-gly.md)o le credenziali di Microsoft Digest SSP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce uno dei seguenti codici di esito positivo.



| Codice restituito                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ \_ completamento \_ e \_ continuazione**</dt> </dl> | Il client deve chiamare [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e quindi passare l'output al server. Il client attende quindi un token restituito e lo passa, in un'altra chiamata, a [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md).<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ I \_ completamenti \_ necessari**</dt> </dl>        | Il client deve completare la compilazione del messaggio e quindi chiamare la funzione [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ \_ continuazione \_ necessaria**</dt> </dl>        | Il client deve inviare il token di output al server e attendere un token restituito. Il token restituito viene quindi passato in un'altra chiamata a [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md). Il token di output può essere vuoto.<br/>                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**SECONDI \_ di \_ credenziali incomplete \_**</dt> </dl> | Usare con Schannel. Il server ha richiesto l'autenticazione client e le credenziali fornite non includono un certificato o il certificato non è stato emesso da un'autorità di certificazione considerata attendibile dal server. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                              |
| <dl> <dt>**SEC \_ E \_ messaggio incompleto \_**</dt> </dl>     | Usare con Schannel. I dati per l'intero messaggio non sono stati letti dalla rete.<br/> Quando viene restituito questo valore, il buffer *Pinput* contiene una struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un membro **BufferType** di **SecBuffer \_ mancante**. Il membro **cbBuffer** di **SecBuffer** contiene un valore che indica il numero di byte aggiuntivi che la funzione deve leggere dal client prima che questa funzione abbia esito positivo. Anche se questo numero non è sempre accurato, l'uso di questo numero può contribuire a migliorare le prestazioni evitando più chiamate a questa funzione.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | Il [*contesto di sicurezza*](../secgloss/s-gly.md) è stato inizializzato correttamente. Non è necessario eseguire un'altra chiamata a [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md) . Se la funzione restituisce un token di output, ovvero se il token SECBUFFER \_ in *pOutput* è di lunghezza diversa da zero, il token deve essere inviato al server.<br/>                                                                                                                                                    |



 

Se la funzione ha esito negativo, la funzione restituisce uno dei codici di errore seguenti.



| Codice restituito                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ E \_ memoria insufficiente \_**</dt> </dl>          | La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**\_ \_ errore interno sec \_ E**</dt> </dl>               | Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**\_handle sec E \_ non valido \_**</dt> </dl>               | L'handle passato alla funzione non è valido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ token non valido \_**</dt> </dl>                | L'errore è dovuto a un token di input in formato non valido, ad esempio un token danneggiato in transito, un token di dimensioni non corrette o un token passato al [*pacchetto di sicurezza*](../secgloss/s-gly.md)errato. Il passaggio di un token al pacchetto errato può verificarsi se il client e il server non hanno negoziato il [*pacchetto di sicurezza*](../secgloss/s-gly.md)appropriato.<br/> |
| <dl> <dt>**SEC \_ E \_ accesso \_ negato**</dt> </dl>                 | Accesso non riuscito.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ Nessuna \_ autorità di autenticazione \_**</dt> </dl> | Non è stato possibile contattare un'autorità per l'autenticazione. Il nome di dominio dell'entità di autenticazione potrebbe essere errato, il dominio potrebbe non essere raggiungibile o potrebbe essersi verificato un errore di relazione di trust.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ Nessuna \_ credenziale**</dt> </dl>               | Nessuna credenziale disponibile nel [*pacchetto di sicurezza*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**SEC \_ E \_ destinazione \_ sconosciuta**</dt> </dl>               | La destinazione non è stata riconosciuta.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E \_ funzione non supportata \_**</dt> </dl>         | Nel parametro FContextReq è stato specificato un flag di attributo di contesto non valido (ISC \_ req \_ delegate o ISC \_ req \_ prompt \_ per \_ credenziali). <br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E \_ entità errata \_**</dt> </dl>              | L'entità che ha ricevuto la richiesta di autenticazione non corrisponde a quella passata nel parametro *pszTargetName* . Ciò indica un errore durante l'autenticazione reciproca.<br/>                                                                                                          |



 

## <a name="remarks"></a>Commenti

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza, ma non è stato possibile stabilirlo, alcune applicazioni potrebbero scegliere di arrestare immediatamente la connessione.

Se gli attributi del [*contesto di sicurezza*](../secgloss/s-gly.md) non sono sufficienti, il client deve liberare il contesto parzialmente creato chiamando la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

La funzione **InitializeSecurityContext (generale)** viene utilizzata da un client per inizializzare un contesto in uscita.

Per un [*contesto di sicurezza*](../secgloss/s-gly.md)a due gambe, la sequenza chiamante è la seguente:

1.  Il client chiama la funzione con *phContext* impostato su **null** e compila il descrittore del buffer con il messaggio di input.
2.  Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) esamina i parametri e costruisce un token opaco, inserendolo nell'elemento token nella matrice di buffer. Se il parametro *fContextReq* include il \_ flag ISC \_ di allocazione della \_ memoria, il [*pacchetto di sicurezza*](../secgloss/s-gly.md) alloca la memoria e restituisce il puntatore nell'elemento token.
3.  Il client invia il token restituito nel buffer *pOutput* al server di destinazione. Il server passa quindi il token come argomento di input in una chiamata alla funzione [**AcceptSecurityContext (generale)**](acceptsecuritycontext--general.md) .
4.  [**AcceptSecurityContext (generale)**](acceptsecuritycontext--general.md) può restituire un token, che il server invia al client per una seconda chiamata a **InitializeSecurityContext (generale)** se la prima chiamata ha restituito un secondo di cui è \_ \_ \_ necessario continuare.

Per i [*contesti di sicurezza*](../secgloss/s-gly.md)a più gambe, ad esempio l'autenticazione reciproca, la sequenza chiamante è la seguente:

1.  Il client chiama la funzione come descritto in precedenza, ma il pacchetto restituisce il \_ \_ codice di \_ esito positivo continuo necessario.
2.  Il client invia il token di output al server e attende la risposta del server.
3.  Al momento della ricezione della risposta del server, il client chiama di nuovo **InitializeSecurityContext (General)** , con *phContext* impostato sull'handle restituito dall'ultima chiamata a. Il token ricevuto dal server viene fornito nel parametro *Pinput* .

Se il server ha risposto correttamente, il [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituisce sec \_ e \_ OK e viene stabilita una sessione protetta.

Se la funzione restituisce una delle risposte di errore, la risposta del server non viene accettata e la sessione non viene stabilita.

Se la funzione restituisce il secondo, è necessario continuare, il \_ \_ \_ secondo \_ \_ \_ è necessario, o sec \_ i \_ completati \_ e \_ continuano, i passaggi 2 e 3 vengono ripetuti.

Per inizializzare un [*contesto di sicurezza*](../secgloss/s-gly.md), potrebbe essere necessaria più di una chiamata a questa funzione, a seconda del meccanismo di autenticazione sottostante, nonché delle opzioni specificate nel parametro *fContextReq* .

I parametri *fContextReq* e *pfContextAttributes* sono maschere di maschera che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md). Il parametro *pfContextAttributes* è valido in caso di esito positivo, ma solo in caso di esito positivo finale è possibile esaminare i flag relativi agli aspetti di sicurezza del contesto. I ritorni intermedi possono impostare, ad esempio, \_ il \_ flag di memoria allocata RET di ISC \_ .

Se viene impostata la richiesta di \_ \_ utilizzo del \_ flag credenziali fornito da ISC \_ , il [*pacchetto di sicurezza*](../secgloss/s-gly.md) deve cercare un tipo di \_ buffer SECBUFFER pkg \_ params nel buffer di input *Pinput* . Non si tratta di una soluzione generica, ma consente un forte accoppiamento del [*pacchetto di sicurezza*](../secgloss/s-gly.md) e dell'applicazione quando appropriato.

Se \_ \_ \_ è stata specificata la memoria di ISC req allocata, il chiamante deve liberare la memoria chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Ad esempio, il token di input potrebbe essere la sfida di un gestore di LAN. In questo caso, il token di output sarà la risposta crittografata NTLM alla richiesta di verifica.

L'azione eseguita dal client dipende dal codice restituito da questa funzione. Se il codice restituito è SEC \_ e \_ OK, non sarà prevista alcuna seconda chiamata **InitializeSecurityContext (generale)** e non sarà prevista alcuna risposta dal server. Se il codice restituito è SEC \_ \_ , continuerà a essere \_ necessario, il client aspetta un token in risposta dal server e lo passa in una seconda chiamata a **InitializeSecurityContext (generale)**. Il \_ \_ \_ codice restituito necessario per il completamento del secondo indica che il client deve completare la compilazione del messaggio e chiamare la funzione [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . Il \_ \_ \_ codice per il completamento e la \_ continuazione del codice incorpora entrambe le azioni.

Se **InitializeSecurityContext (General)** restituisce Success sulla prima (o solo) chiamata, il chiamante deve chiamare la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) sull'handle restituito, anche se la chiamata ha esito negativo in una fase successiva dello scambio di autenticazione.

Il client può chiamare nuovamente **InitializeSecurityContext (General)** dopo che è stato completato correttamente. Indica al pacchetto di [*sicurezza*](../secgloss/s-gly.md) che si desidera una riautenticazione.

I chiamanti in modalità kernel presentano le differenze seguenti: il nome di destinazione è una stringa [*Unicode*](../secgloss/u-gly.md) che deve essere allocata nella memoria virtuale usando [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); non deve essere allocato dal pool. I buffer passati e specificati in *Pinput* e *pOutput* devono trovarsi nella memoria virtuale, non nel pool.

Quando si usa SSP Schannel, se la funzione restituisce le \_ \_ credenziali incomplete del secondo \_ , verificare di aver specificato un certificato valido e attendibile nelle credenziali. Il certificato viene specificato quando si chiama la funzione [**AcquireCredentialsHandle (generale)**](acquirecredentialshandle--general.md) . Il certificato deve essere un certificato di autenticazione client emesso da un'autorità di certificazione (CA) considerata attendibile dal server. Per ottenere un elenco delle CA considerate attendibili dal server, chiamare la funzione [**QueryContextAttributes (General)**](querycontextattributes--general.md) e specificare l' \_ attributo SECPKG attr \_ Issuer \_ List \_ ex.

Quando si usa SSP Schannel, dopo che un'applicazione client ha ricevuto un certificato di autenticazione da un'autorità di certificazione considerata attendibile dal server, l'applicazione crea una nuova credenziale chiamando la funzione [**AcquireCredentialsHandle (generale)**](acquirecredentialshandle--general.md) e chiamando di nuovo **InitializeSecurityContext (General)** , specificando la nuova credenziale nel parametro *phCredential* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomi Unicode e ANSI<br/>   | **InitializeSecurityContextW** (Unicode) e **InitializeSecurityContextA** (ANSI)<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (generale)**](acceptsecuritycontext--general.md)
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

 

 
