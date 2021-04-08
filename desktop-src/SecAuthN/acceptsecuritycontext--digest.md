---
description: Consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza tra il server e un client remoto che utilizza il digest.
ms.assetid: 017683e3-b21a-4e97-9232-582ac7dbd5b2
title: Funzione AcceptSecurityContext (digest) (SSPI. h)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 11ffa801612f14f5b9aaf61e7d48b61377bc9e56
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058486"
---
# <a name="acceptsecuritycontext-digest-function"></a>Funzione AcceptSecurityContext (digest)

La funzione **AcceptSecurityContext (digest)** consente al componente server di un'applicazione di trasporto di stabilire un [*contesto di sicurezza*](../secgloss/s-gly.md) tra il server e un client remoto. Il client remoto utilizza la funzione [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) per avviare il processo di creazione di un contesto di sicurezza. Il server può richiedere uno o più token di risposta dal client remoto per completare la creazione del contesto di sicurezza.

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
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phCredential* \[ in, facoltativo\]
</dt> <dd>

Handle per le credenziali del server. Il server chiama la funzione [**AcquireCredentialsHandle (digest)**](acquirecredentialshandle--digest.md) con il flag SECPKG \_ cred \_ in ingresso o SECPKG \_ cred \_ entrambi impostati per recuperare questo handle.

</dd> <dt>

*phContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **AcceptSecurityContext (digest)**, questo puntatore è **null**. Nelle chiamate successive, *phContext* è l'handle per il contesto parzialmente formattato che è stato restituito nel parametro *phNewContext* dalla prima chiamata.

</dd> <dt>

*Pinput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generata da una chiamata client a [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) che contiene il descrittore del buffer di input.

La tabella seguente illustra la configurazione del buffer per il digest HTTP. Il primo buffer deve essere di tipo **\_ token SECBUFFER** e il resto deve essere di tipo **SECBUFFER \_ pkg \_ params**. SASL richiede solo il buffer zero.



| \#Tipo di/buffer buffer                                                                                                                                                                                                 | Significato                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> <dt> **\_ token SECBUFFER**</dt> </dl>                                        | Empty per la prima chiamata e la risposta alla richiesta di verifica ricevuta dal client per la seconda chiamata.<br/>                                                             |
| <span id="1"></span><dl> <dt>**1**</dt> <dt> **SECBUFFER \_ pkg \_ params**</dt> </dl>                                  | Metodo. Il formato dei caratteri è wireline dalla riga della richiesta. Caratteri US ASCII a byte singolo.<br/>                                                                |
| <span id="2"></span><dl> <dt>**2**</dt> <dt> **\_ \_ parametri pkg SECBUFFER**</dt> </dl>                                  | Riservato.<br/>                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> <dt> **\_ \_ params SECBUFFER pkg**</dt> </dl>                                  | HEntity. Rappresentazione esadecimale di H (entità-Body). Caratteri US ASCII a byte singolo.<br/>                                                                       |
| <span id="4"></span><dl> <dt>**4**</dt> <dt> **\_ \_ parametri pkg SECBUFFER**</dt> </dl>                                  | Autenticazione. Stringa dell'area di autenticazione per la richiesta. Stringa Unicode che deve essere rappresentabile nel formato ASCII US.<br/>                                                                 |
| <span id="5"></span><dl> <dt>**5**</dt> <dt> **\_ \_ binding di canale SECBUFFER** \| **SECBUFFER \_ ReadOnly**</dt> </dl> | Contiene il valore del token di associazione del canale.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.<br/> |



 

</dd> <dt>

*fContextReq* \[ in\]
</dt> <dd>

Flag di bit che specificano gli attributi necessari al server per stabilire il contesto. I flag di bit possono essere combinati usando **operazioni OR bit per** bit. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ req \_ alloca \_ memoria**</dt> </dl>                                                  | Il digest alloca automaticamente i buffer di output. Al termine dell'utilizzo dei buffer di output, è possibile liberarli chiamando la funzione [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/>                                                                                                                                                                                                                                      |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**ASC \_ req \_ consente \_ le \_ associazioni mancanti**</dt> </dl>                            | Indica che il digest non richiede binding di canale per i canali interni ed esterni. Questo valore viene utilizzato per la compatibilità con le versioni precedenti quando il supporto per l'associazione di canale dell'endpoint non è noto.<br/> Questo valore si escludono a vicenda con le **\_ \_ \_ associazioni proxy ASC req**.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**\_ \_ riservatezza ASC req**</dt> </dl>                                                   | Crittografare e decrittografare i messaggi. <br/> Il provider SSP digest supporta questo flag solo per SASL.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**\_ \_ Binding proxy ASC \_ req**</dt> </dl>                                                     | Indica che il digest richiede l'associazione di canale.<br/> Questo valore si escludono a vicenda con **ASC \_ req consente le \_ \_ \_ associazioni mancanti**.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**\_connessione ASC req \_**</dt> </dl>                                                                  | Il [*contesto di sicurezza*](../secgloss/s-gly.md) non gestirà i messaggi di formattazione.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_ \_ errore esteso di ASC req \_**</dt> </dl>                                                     | Quando si verificano errori, viene inviata una notifica all'entità remota.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**ASC \_ req \_ http (0x10000000)**</dt> </dl> | Usare digest per HTTP. Omettere questo flag per utilizzare il digest come meccanismo SASL.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**integrità di ASC \_ req \_**</dt> </dl>                                                                     | Firmare i messaggi e verificare le firme.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**\_ \_ rilevamento riesecuzione di ASC req \_**</dt> </dl>                                                        | Rilevare i pacchetti riprodotti.<br/>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**\_ \_ rilevamento sequenza ASC \_ req**</dt> </dl>                                                  | Rilevare i messaggi ricevuti fuori sequenza.<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

Per i flag di attributo possibili e i relativi significati, vedere [requisiti di contesto](context-requirements.md). I flag usati per questo parametro sono preceduti dal prefisso ASC \_ req, ad esempio, ASC \_ req \_ delegate.

Gli attributi richiesti potrebbero non essere supportati dal client. Per ulteriori informazioni, vedere il parametro *pfContextAttr* .

</dd> <dt>

*TargetDataRep* \[ in\]
</dt> <dd>

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, sulla destinazione. Questo parametro può essere una sicurezza \_ nativa \_ DREP o DREP della rete di sicurezza \_ \_ .

Questo parametro non viene utilizzato con il provider SSP del digest. Quando si utilizza SSP digest, specificare zero per questo parametro.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [CtxtHandle](sspi-handles.md) . Alla prima chiamata a **AcceptSecurityContext (digest)**, questo puntatore riceve il nuovo handle di contesto. Nelle chiamate successive, *phNewContext* può corrispondere all'handle specificato nel parametro *phContext* .

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene il descrittore del buffer di output. Questo buffer viene inviato al client per l'input in chiamate aggiuntive a [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md). Un buffer di output può essere generato anche se la funzione restituisce SEC \_ E \_ OK. Qualsiasi buffer generato deve essere restituito all'applicazione client.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un set di flag di bit che indicano gli attributi del contesto stabilito. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md). I flag usati per questo parametro sono preceduti dal prefisso ASC \_ RET, ad esempio ASC \_ ret \_ delegate.

Non controllare gli attributi correlati alla sicurezza finché la chiamata di funzione finale non viene completata correttamente. I flag di attributo non correlati alla sicurezza, ad esempio \_ il \_ flag ASC RET allocazioned \_ Memory, possono essere controllati prima della restituzione finale.

</dd> <dt>

*ptsTimeStamp* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che il [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituisca sempre questo valore nell'ora locale.

Questo parametro è impostato su un tempo massimo costante. Non esiste alcuna data di scadenza per il [*contesto di sicurezza*](../secgloss/s-gly.md)del digest o per le credenziali o quando si utilizza il provider SSP del digest.

> [!Note]  
> Fino all'ultima chiamata del processo di autenticazione, l'ora di scadenza per il contesto può non essere corretta perché verranno fornite ulteriori informazioni durante le fasi successive della negoziazione. Pertanto, *ptsTimeStamp* deve essere **null** fino all'ultima chiamata alla funzione.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei valori seguenti.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Codice/valore restituito</th><th>Descrizione</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>La funzione non è riuscita. La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>La funzione non è riuscita. Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>La funzione non è riuscita. L'handle passato alla funzione non è valido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>La funzione non è riuscita. Il token passato alla funzione non è valido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Accesso non riuscito.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>La funzione non è riuscita. Non è stato possibile contattare un'autorità per l'autenticazione. Questo problema può essere dovuto alle condizioni seguenti:<br/><ul><li>Il nome di dominio dell'entità di autenticazione non è corretto.</li><li>Il dominio non è disponibile.</li><li>Relazione di trust non riuscita.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>La funzione non è riuscita. L'handle delle credenziali specificato nel parametro <em>phCredential</em> non è valido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Funzione completata. Il [*contesto di sicurezza*](../secgloss/s-gly.md) ricevuto dal client è stato accettato. Se è stato generato un token di output dalla funzione, è necessario inviarlo al processo client.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>La funzione non è riuscita. Il flag di attributo di contesto non valido è stato specificato nel parametro <em>fContextReq</em> .<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Funzione completata. Il server deve chiamare [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) e passare il token di output al client. Il server attende quindi un token restituito dal client e quindi effettua un'altra chiamata a [<strong>AcceptSecurityContext (digest)</strong>] (AcceptSecurityContext--digest.MD).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Funzione completata. Il server deve terminare la compilazione del messaggio dal client, quindi chiamare la funzione [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Funzione completata. Il server deve inviare il token di output al client e attendere un token restituito. Il token restituito deve essere passato in <em>Pinput</em> per un'altra chiamata a [<strong>AcceptSecurityContext (digest)</strong>] (AcceptSecurityContext--digest.MD).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>La funzione non è riuscita. La funzione [<strong>AcceptSecurityContext (digest)</strong>] (AcceptSecurityContext--digest.MD) è stata chiamata dopo che è stato stabilito il contesto specificato.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>La funzione non è riuscita. Il criterio di associazione del canale non è stato soddisfatto.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Commenti

La funzione **AcceptSecurityContext (digest)** è la controparte del server della funzione [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md) .

Quando il server riceve una richiesta da un client, il server usa il parametro *fContextReq* per specificare cosa richiede la sessione. In questo modo, un server può specificare che i client devono essere in grado di usare una sessione riservata o controllata dall' [*integrità*](../secgloss/i-gly.md)e rifiutare i client che non sono in grado di soddisfare tale richiesta. In alternativa, un server può non richiedere alcun elemento e qualsiasi altro elemento che il client può fornire o richiede viene restituito nel parametro *pfContextAttr* .

Per un pacchetto che supporta l'autenticazione a più gambe, ad esempio l'autenticazione reciproca, la sequenza chiamante è la seguente:

1.  Il client trasmette un token al server.
2.  Il server chiama **AcceptSecurityContext (digest)** la prima volta, che genera un token di risposta che viene quindi inviato al client.
3.  Il client riceve il token e lo passa a [**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md). Se **InitializeSecurityContext (digest)** restituisce sec \_ e \_ OK, l'autenticazione reciproca è stata completata ed è possibile avviare una sessione protetta. Se **InitializeSecurityContext (digest)** restituisce un codice di errore, termina la negoziazione di autenticazione reciproca. In caso contrario, il token di sicurezza restituito da **InitializeSecurityContext (digest)** viene inviato al client e i passaggi 2 e 3 vengono ripetuti.

I parametri *fContextReq* e *pfContextAttr* sono maschere di maschera che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [requisiti di contesto](context-requirements.md).

> [!Note]  
> Il parametro *pfContextAttr* è valido in caso di esito positivo, ma solo in caso di esito positivo finale è possibile esaminare i flag relativi agli aspetti di sicurezza del contesto. I ritorni intermedi possono impostare, ad esempio, \_ il \_ flag di memoria allocata RET di ISC \_ .

 

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, è stata richiesta la riservatezza (crittografia) ma non è stato possibile stabilirla, è possibile che alcune applicazioni decidano immediatamente di arrestare la connessione. Se non è possibile stabilire il [*contesto di sicurezza*](../secgloss/s-gly.md) , il server deve liberare il contesto parzialmente creato chiamando la funzione [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Per informazioni sul momento in cui chiamare la funzione **DeleteSecurityContext** , vedere **DeleteSecurityContext**.

Una volta stabilito il [*contesto di sicurezza*](../secgloss/s-gly.md) , l'applicazione server può utilizzare la funzione [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) per recuperare un handle per l'account utente a cui è stato eseguito il mapping del certificato client. Inoltre, il server può utilizzare la funzione [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) per rappresentare l'utente.

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

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md)
</dt> </dl>

 

 
