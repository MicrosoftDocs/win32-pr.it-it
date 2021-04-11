---
description: Queste costanti e i valori corrispondenti indicano i codici di stato HTTP restituiti dai server su Internet.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: Codici di stato HTTP (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232214"
---
# <a name="http-status-codes-winhttph"></a>Codici di stato HTTP (WinHTTP. h)

Queste costanti e i valori corrispondenti indicano i codici di stato HTTP restituiti dai server su Internet.

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

<span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**stato HTTP WebDAV stato più \_ \_ \_ \_ stato**
</dt> <dd> <dl> <dt>

207
</dt> <dt>



Durante un'operazione di World Wide Web Distributed Authoring and Versioning (WebDAV), questo indica più codici di stato per una singola risposta. Il corpo della risposta contiene Extensible Markup Language (XML) che descrive i codici di stato. Per ulteriori informazioni, vedere [estensioni HTTP per la creazione distribuita](../webdav/webdav-portal.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_stato http \_ ambiguo**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



La risorsa richiesta è disponibile in una o più posizioni.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_stato http \_ spostato**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



La risorsa richiesta è stata assegnata a un nuovo Uniform Resource Identifier permanente (URI) e tutti i riferimenti futuri a questa risorsa devono essere eseguiti usando uno degli URI restituiti.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_Reindirizzamento stato \_ http**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



La risorsa richiesta risiede temporaneamente in un URI diverso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_metodo di \_ Reindirizzamento \_ stato http**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



La risposta alla richiesta si trova in un URI diverso e deve essere recuperata usando un [*verbo http*](glossary.md) Get su tale risorsa.


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



La richiesta reindirizzata mantiene lo stesso [*verbo http*](glossary.md). Comportamento HTTP/1.1.


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



Non implementato nel protocollo HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**stato HTTP non \_ \_ consentito**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Il server ha compreso la richiesta, ma non è in grado di soddisfarla.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_stato http \_ non \_ trovato**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Il server non ha trovato alcun elemento corrispondente all'URI richiesto.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**Metodo di stato HTTP non \_ \_ valido \_**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Il [*verbo http*](glossary.md) utilizzato non è consentito.


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



Il server non è in grado di accettare la richiesta senza una lunghezza del contenuto definita.


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



Il server non è in grado di elaborare la richiesta perché l'entità della richiesta è più grande del server che è in grado di elaborare.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_URI stato \_ http \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Il server non è in grado di eseguire la richiesta perché l'URI della richiesta è più lungo di quello che il server può interpretare.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**supporto di stato HTTP non \_ \_ supportato \_**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



Il server non è in grado di servire la richiesta perché l'entità della richiesta è in un formato non supportato dalla risorsa richiesta per il metodo richiesto.


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



Il server non supporta la versione del protocollo HTTP utilizzata nel messaggio di richiesta.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>      |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>   |
| Intestazione<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

