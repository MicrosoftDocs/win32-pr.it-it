---
description: Consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza tra il server e un client remoto che usa digest.
ms.assetid: 017683e3-b21a-4e97-9232-582ac7dbd5b2
title: Funzione AcceptSecurityContext (Digest) (Sspi.h)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: ec6ad11e754124f56f5852b4e0b0a0347f1bb099
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628713"
---
# <a name="acceptsecuritycontext-digest-function"></a>Funzione AcceptSecurityContext (Digest)

La **funzione AcceptSecurityContext (Digest)** consente al componente server di un'applicazione di trasporto di stabilire un contesto di sicurezza [*tra*](../secgloss/s-gly.md) il server e un client remoto. Il client remoto usa la [**funzione InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) per avviare il processo di definizione di un contesto di sicurezza. Il server può richiedere uno o più token di risposta dal client remoto per completare la definizione del contesto di sicurezza.

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

Handle per le credenziali del server. Il server chiama la [**funzione AcquireCredentialsHandle (Digest)**](acquirecredentialshandle--digest.md) con il \_ flag SECPKG CRED INBOUND o \_ SECPKG CRED BOTH impostato per \_ recuperare questo \_ handle.

</dd> <dt>

*phContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Nella prima chiamata ad **AcceptSecurityContext (Digest)** questo puntatore è **NULL.** Nelle chiamate successive, *phContext* è l'handle per il contesto parzialmente formato restituito nel *parametro phNewContext* dalla prima chiamata.

</dd> <dt>

*pInput* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generata da una chiamata client a [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) che contiene il descrittore del buffer di input.

Nella tabella seguente viene illustrata la configurazione del buffer per DIGEST HTTP. Il primo buffer deve essere di tipo **SECBUFFER \_ TOKEN** e il resto deve essere di tipo **SECBUFFER \_ PKG \_ PARAMS**. SASL richiede solo il buffer zero.



| Tipo \# di buffer/buffer                                                                                                                                                                                                 | Significato                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> <dt> **TOKEN \_ SECBUFFER**</dt> </dl>                                        | Vuoto per la prima chiamata e la risposta di richiesta ricevuta dal client per la seconda chiamata.<br/>                                                             |
| <span id="1"></span><dl> <dt>**1**</dt> <dt> **SECBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Metodo. I caratteri sono in formato wireline dalla riga della richiesta. Caratteri ASCII a byte singolo.<br/>                                                                |
| <span id="2"></span><dl> <dt>**2**</dt> <dt> **SECBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Riservato.<br/>                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**PARAMS**</dt> <dt> **\_ PKG \_ DA** 3 SECBUFFER</dt> </dl>                                  | HEntity. Rappresentazione esadecimale di H(entity-body). Caratteri ASCII a byte singolo.<br/>                                                                       |
| <span id="4"></span><dl> <dt>**4**</dt> <dt> **SECBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Regno. Stringa dell'area di autenticazione per la richiesta. Stringa Unicode che deve essere rappresentabile in US ASCII.<br/>                                                                 |
| <span id="5"></span><dl> <dt>**5**</dt> <dt> **SECBUFFER \_ CHANNEL \_ BINDINGS** \| **SECBUFFER \_ READONLY**</dt> </dl> | Contiene il valore del token di associazione del canale.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> |



 

</dd> <dt>

*fContextReq* \[ Pollici\]
</dt> <dd>

Flag di bit che specificano gli attributi richiesti dal server per stabilire il contesto. I flag di bit possono essere combinati usando operazioni **OR** bit per bit. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ REQ \_ ALLOCARE \_ MEMORIA**</dt> </dl>                                                  | Il digest alloca automaticamente i buffer di output. Al termine dell'uso dei buffer di output, liberarli chiamando la [**funzione FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br/>                                                                                                                                                                                                                                      |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**ASC \_ REQ ALLOW MISSING BINDINGS (ASC REQ \_ ALLOW MISSING \_ \_ BINDINGS)**</dt> </dl>                            | Indica che Digest non richiede associazioni di canale sia per i canali interni che per i canali esterni. Questo valore viene usato per la compatibilità con le versioni precedenti quando il supporto per l'associazione del canale dell'endpoint non è noto.<br/> Questo valore si escludono a vicenda con **ASC \_ REQ \_ PROXY \_ BINDINGS**.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**RISERVATEZZA DI ASC \_ REQ \_**</dt> </dl>                                                   | Crittografare e decrittografare i messaggi. <br/> Il provider di servizi condivisi digest supporta questo flag solo per SASL.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**ASSOCIAZIONI PROXY ASC \_ REQ \_ \_**</dt> </dl>                                                     | Indica che Digest richiede l'associazione di canali.<br/> Questo valore si escludono a vicenda con **ASC \_ REQ \_ ALLOW MISSING \_ \_ BINDINGS**.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore non è supportato.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**CONNESSIONE ASC \_ \_ REQ**</dt> </dl>                                                                  | Il [*contesto di sicurezza*](../secgloss/s-gly.md) non gestirà i messaggi di formattazione.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ERRORE ESTESO DI ASC \_ REQ \_ \_**</dt> </dl>                                                     | Quando si verificano errori, l'entità remota riceverà una notifica.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**ASC \_ REQ \_ HTTP (0x10000000)**</dt> </dl> | Usare Digest per HTTP. Omettere questo flag per usare Digest come meccanismo SASL.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**INTEGRITÀ DI ASC \_ \_ REQ**</dt> </dl>                                                                     | Firmare i messaggi e verificare le firme.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>                                                        | Rilevare i pacchetti riprodotti.<br/>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl>                                                  | Rilevare i messaggi ricevuti fuori sequenza.<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

Per i possibili flag di attributo e i relativi significati, vedere [Requisiti di contesto](context-requirements.md). I flag usati per questo parametro sono preceduti da ASC \_ REQ, ad esempio ASC \_ REQ \_ DELEGATE.

Gli attributi richiesti potrebbero non essere supportati dal client. Per altre informazioni, vedere il *parametro pfContextAttr.*

</dd> <dt>

*TargetDataRep* \[ Pollici\]
</dt> <dd>

Rappresentazione dei dati, ad esempio l'ordinamento dei byte, nella destinazione. Questo parametro può essere SECURITY \_ NATIVE \_ DREP o SECURITY \_ NETWORK \_ DREP.

Questo parametro non viene usato con digest SSP. Quando si usa Digest SSP, specificare zero per questo parametro.

</dd> <dt>

*phNewContext* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [struttura CtxtHandle.](sspi-handles.md) Nella prima chiamata ad **AcceptSecurityContext (Digest)** questo puntatore riceve il nuovo handle di contesto. Nelle chiamate successive, *phNewContext* può essere uguale all'handle specificato nel *parametro phContext.*

</dd> <dt>

*pOutput* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) che contiene il descrittore del buffer di output. Questo buffer viene inviato al client per l'input in chiamate aggiuntive a [**InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Un buffer di output può essere generato anche se la funzione restituisce SEC \_ E \_ OK. Qualsiasi buffer generato deve essere inviato all'applicazione client.

</dd> <dt>

*pfContextAttr* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un set di flag di bit che indicano gli attributi del contesto stabilito. Per una descrizione dei vari attributi, vedere [Requisiti di contesto](context-requirements.md). I flag usati per questo parametro sono preceduti da ASC \_ RET, ad esempio ASC \_ RET \_ DELEGATE.

Non verificare la presenza di attributi correlati alla sicurezza finché la chiamata di funzione finale non viene restituita correttamente. I flag di attributo non correlati alla sicurezza, ad esempio il flag ASC RET ALLOCATED MEMORY, possono essere controllati \_ \_ prima della restituzione \_ finale.

</dd> <dt>

*ptsTimeStamp* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura TimeStamp**](timestamp.md) che riceve l'ora di scadenza del contesto. È consigliabile che [*il pacchetto di sicurezza*](../secgloss/s-gly.md) restituirà sempre questo valore nell'ora locale.

Questo parametro è impostato su un tempo massimo costante. Non esiste alcuna scadenza per le credenziali o i contesti di sicurezza [*digest*](../secgloss/s-gly.md)o quando si usa il provider di servizi condivisi digest.

> [!Note]  
> Fino all'ultima chiamata del processo di autenticazione, l'ora di scadenza per il contesto può non essere corretta perché verranno fornite altre informazioni durante le fasi successive della negoziazione. Pertanto, *ptsTimeStamp* deve essere **NULL** fino all'ultima chiamata alla funzione.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei valori seguenti.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Codice/valore restituito</th><th>Descrizione</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>La funzione non è riuscita. La memoria disponibile non è sufficiente per completare l'azione richiesta.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>La funzione non è riuscita. Si è verificato un errore che non è stato mappato a un codice di errore SSPI.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>La funzione non è riuscita. L'handle passato alla funzione non è valido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>La funzione non è riuscita. Il token passato alla funzione non è valido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>L'accesso non è riuscito.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>La funzione non è riuscita. Non è stato possibile contattare alcuna autorità per l'autenticazione. Ciò potrebbe essere dovuto alle condizioni seguenti:<br/><ul><li>Il nome di dominio dell'entità di autenticazione non è corretto.</li><li>Il dominio non è disponibile.</li><li>La relazione di trust non è riuscita.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>La funzione non è riuscita. L'handle delle credenziali specificato nel <em>parametro phCredential</em> non è valido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>Funzione completata. Il [*contesto di*](../secgloss/s-gly.md) sicurezza ricevuto dal client è stato accettato. Se un token di output è stato generato dalla funzione, deve essere inviato al processo client.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>La funzione non è riuscita. Nel parametro <em>fContextReq</em> è stato specificato un flag di attributo di contesto non valido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>Funzione completata. Il server deve chiamare [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) e passare il token di output al client. Il server attende quindi un token restituito dal client e quindi esegue un'altra chiamata a [<strong>AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>Funzione completata. Il server deve completare la compilazione del messaggio dal client e quindi chiamare la funzione [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>Funzione completata. Il server deve inviare il token di output al client e attendere un token restituito. Il token restituito deve essere passato in <em>pInput per</em> un'altra chiamata a [<strong>AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>La funzione non è riuscita. La funzione [<strong>AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md) è stata chiamata dopo che è stato stabilito il contesto specificato.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>La funzione non è riuscita. I criteri di associazione del canale non sono stati soddisfatti.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Commenti

La **funzione AcceptSecurityContext (Digest)** è la controparte del server alla [**funzione InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md)

Quando il server riceve una richiesta da un client, il server usa il *parametro fContextReq* per specificare ciò che richiede della sessione. In questo modo, un server può specificare che i [](../secgloss/i-gly.md)client devono essere in grado di usare una sessione riservata o controllata dall'integrità e può rifiutare i client che non soddisfano tale richiesta. In alternativa, un server non può richiedere nulla e tutto ciò che il client può fornire o richiede viene restituito nel *parametro pfContextAttr.*

Per un pacchetto che supporta l'autenticazione a più livelli, ad esempio l'autenticazione reciproca, la sequenza di chiamata è la seguente:

1.  Il client trasmette un token al server.
2.  Il server chiama **AcceptSecurityContext (Digest)** la prima volta, che genera un token di risposta che viene quindi inviato al client.
3.  Il client riceve il token e lo passa a [**InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Se **InitializeSecurityContext (Digest)** restituisce SEC E OK, l'autenticazione reciproca è stata completata e può iniziare \_ una sessione \_ protetta. Se **InitializeSecurityContext (Digest)** restituisce un codice di errore, la negoziazione dell'autenticazione reciproca termina. In caso contrario, il token di sicurezza restituito da **InitializeSecurityContext (Digest)** viene inviato al client e i passaggi 2 e 3 vengono ripetuti.

I *parametri fContextReq* e *pfContextAttr* sono maschera di bit che rappresentano vari attributi di contesto. Per una descrizione dei vari attributi, vedere [Requisiti di contesto](context-requirements.md).

> [!Note]  
> Il *parametro pfContextAttr* è valido in caso di esito positivo, ma solo in caso di esito positivo finale è necessario esaminare i flag relativi agli aspetti di sicurezza del contesto. I valori restituiti intermedi possono impostare, ad esempio, il flag ISC \_ RET \_ ALLOCATED \_ MEMORY.

 

Il chiamante è responsabile di determinare se gli attributi di contesto finali sono sufficienti. Se, ad esempio, la riservatezza (crittografia) è stata richiesta, ma non è stato possibile stabilirlo, alcune applicazioni possono scegliere di arrestare immediatamente la connessione. Se non [*è possibile stabilire*](../secgloss/s-gly.md) il contesto di sicurezza, il server deve liberare il contesto creato parzialmente chiamando la funzione [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) Per informazioni su quando chiamare la **funzione DeleteSecurityContext,** vedere **DeleteSecurityContext**.

Dopo aver [*stabilito il contesto*](../secgloss/s-gly.md) di sicurezza, l'applicazione server può usare la funzione [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) per recuperare un handle per l'account utente a cui è stato eseguito il mapping del certificato client. Inoltre, il server può usare la [**funzione ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) per rappresentare l'utente.

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

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (digest)**](initializesecuritycontext--digest.md)
</dt> </dl>

 

 
