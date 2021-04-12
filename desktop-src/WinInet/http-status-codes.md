---
title: Codici di stato HTTP (WinInet. h)
description: La tabella seguente contiene le costanti e i valori corrispondenti per i codici di stato HTTP restituiti dai server su Internet.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6933617b0488e059c029dd783af238a3ddbb3ecb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400907"
---
# <a name="http-status-codes-winineth"></a>Codici di stato HTTP (WinInet. h)

La tabella seguente contiene le costanti e i valori corrispondenti per i codici di stato HTTP restituiti dai server su Internet.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_stato http \_ continua**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



La richiesta può essere continuata.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_protocolli del \_ cambio di stato http \_**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Il server ha cambiato i protocolli in un'intestazione di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**\_stato http \_ OK**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



La richiesta è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_stato http \_ creato**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



La richiesta è stata soddisfatta e ha causato la creazione di una nuova risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_stato http \_ accettato**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



La richiesta è stata accettata per l'elaborazione, ma l'elaborazione non è stata completata.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_stato http \_ parziale**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



Le metainformazioni restituite nell'intestazione dell'entità non sono il set definitivo disponibile dal server di origine.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_stato http \_ nessun \_ contenuto**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



Il server ha completato la richiesta, ma non sono presenti nuove informazioni da restituire.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_contenuto della \_ reimpostazione dello stato http \_**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



La richiesta è stata completata e il programma client deve reimpostare la visualizzazione del documento che ha causato l'invio della richiesta per consentire all'utente di avviare facilmente un'altra azione di input.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_contenuto parziale dello stato http \_ \_**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



Il server ha completato la richiesta di GET parziale per la risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_stato http \_ ambiguo**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



Il server non è riuscito a decidere cosa restituire.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_stato http \_ spostato**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



La risorsa richiesta è stata assegnata a un nuovo URI permanente (Uniform Resource Identifier) e tutti i riferimenti futuri a questa risorsa devono essere eseguiti usando uno degli URI restituiti.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_Reindirizzamento stato \_ http**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



La risorsa richiesta risiede temporaneamente in un URI diverso (Uniform Resource Identifier).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_metodo di \_ Reindirizzamento \_ stato http**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



La risposta alla richiesta si trova in un URI diverso (Uniform Resource Identifier) e deve essere recuperata usando un verbo HTTP GET su tale risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_stato http \_ non \_ modificato**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



La risorsa richiesta non è stata modificata.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_ \_ Usa proxy per lo stato http \_**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



È necessario accedere alla risorsa richiesta tramite il proxy fornito dal campo location.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_ \_ verbo Keep del reindirizzamento dello stato \_ http \_**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



La richiesta reindirizzata mantiene lo stesso verbo HTTP. Comportamento HTTP/1.1.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_richiesta non \_ valida di stato http \_**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



La richiesta non è stata elaborata dal server a causa di una sintassi non valida.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**\_stato http \_ negato**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



La risorsa richiesta prevede l'autenticazione degli utenti.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_ \_ req pagamento stato \_ http**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



Attualmente non implementato nel protocollo HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**stato HTTP non \_ \_ consentito**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Il server ha compreso la richiesta, ma sta rifiutando di soddisfarla.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_stato http \_ non \_ trovato**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Il server non ha trovato alcun elemento corrispondente all'URI richiesto (Uniform Resource Identifier).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**Metodo di stato HTTP non \_ \_ valido \_**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Il verbo HTTP utilizzato non è consentito.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**\_stato http \_ nessuno \_ accettabile**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



Non sono state trovate risposte accettabili per il client.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**richiesta \_ di \_ autenticazione proxy di stato \_ http \_**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Richiesta autenticazione proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ timeout richiesta stato \_ http**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



Timeout del server durante l'attesa della richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_conflitto stato \_ http**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



Non è stato possibile completare la richiesta a causa di un conflitto con lo stato corrente della risorsa. L'utente deve inviare nuovamente con ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_stato http \_ andato**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



La risorsa richiesta non è più disponibile nel server e non è noto alcun indirizzo di spedizione.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_lunghezza stato \_ http \_ obbligatoria**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



Il server rifiuta di accettare la richiesta senza una lunghezza del contenuto definita.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_Precond stato http \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



La precondizione specificata in uno o più campi di intestazione della richiesta ha restituito false quando è stato testato nel server.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_richiesta di stato http \_ \_ troppo \_ grande**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



Il server rifiuta di elaborare una richiesta perché l'entità della richiesta è più grande di quanto il server sia disposto o in grado di elaborare.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI stato \_ http \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Il server rifiuta di servire la richiesta perché l'URI della richiesta (Uniform Resource Identifier) è più lungo di quello che il server è disposto a interpretare.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**supporto di stato HTTP non \_ \_ supportato \_**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



Il server rifiuta di servire la richiesta perché l'entità della richiesta è in un formato non supportato dalla risorsa richiesta per il metodo richiesto.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_ \_ tentativo di stato http \_ con**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



La richiesta deve essere ritentata dopo aver eseguito l'azione appropriata.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_errore del \_ server di stato http \_**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



Si è verificata una condizione imprevista che ha impedito al server di completare la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_stato http \_ non \_ supportato**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



Il server non supporta la funzionalità necessaria per soddisfare la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**GATEWAY di stato HTTP non \_ \_ valido \_**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



Il server, che funge da gateway o proxy, ha ricevuto una risposta non valida dal server padre a cui ha effettuato l'accesso nel tentativo di completare la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**servizio di stato HTTP non \_ \_ \_ disponibile**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



Il servizio è momentaneamente sovraccarico.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_timeout del \_ gateway di stato http \_**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



Richiesta scaduta in attesa di un gateway.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_versione stato \_ http \_ non \_ sup**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



Il server non supporta o rifiuta di supportare la versione del protocollo HTTP utilizzata nel messaggio di richiesta.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

