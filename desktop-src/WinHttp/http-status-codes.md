---
description: Queste costanti e i valori corrispondenti indicano i codici di stato HTTP restituiti dai server su Internet.
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: Codici di stato HTTP (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f145a2a7b5f7e807d1b393d9c4fd9b4f71c81052f0f023a04f72e139842637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744572"
---
# <a name="http-status-codes-winhttph"></a>Codici di stato HTTP (Winhttp.h)

Queste costanti e i valori corrispondenti indicano i codici di stato HTTP restituiti dai server su Internet.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**STATO HTTP \_ \_ CONTINUA**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



La richiesta può essere continuata.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**PROTOCOLLI \_ DI CAMBIO DI STATO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Il server ha protocolli commutati in un'intestazione di aggiornamento.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**STATO \_ HTTP \_ OK**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



La richiesta è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**STATO \_ HTTP \_ CREATO**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



La richiesta è stata soddisfatta e ha comportato la creazione di una nuova risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**STATO HTTP \_ \_ ACCETTATO**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



La richiesta è stata accettata per l'elaborazione, ma l'elaborazione non è stata completata.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP \_ STATUS \_ PARTIAL**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



Le meta informazioni restituite nell'intestazione dell'entità non sono il set definitivo disponibile dal server di origine.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**STATO HTTP \_ \_ SENZA \_ CONTENUTO**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



Il server ha soddisfatto la richiesta, ma non sono disponibili nuove informazioni da inviare.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP \_ STATUS \_ RESET \_ CONTENT**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



La richiesta è stata completata e il programma client deve reimpostare la visualizzazione del documento che ha causato l'invio della richiesta per consentire all'utente di avviare facilmente un'altra azione di input.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**CONTENUTO \_ PARZIALE DELLO STATO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



Il server ha soddisfatto la richiesta GET parziale per la risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**STATO HTTP \_ \_ WEBDAV \_ MULTI \_ STATUS**
</dt> <dd> <dl> <dt>

207
</dt> <dt>



Durante un World Wide Web webDAV (Distributed Authoring and Versioning), ciò indica più codici di stato per una singola risposta. Il corpo della risposta contiene Extensible Markup Language (XML) che descrive i codici di stato. Per altre informazioni, vedere [Estensioni HTTP per la creazione distribuita.](../webdav/webdav-portal.md)


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**STATO \_ \_ HTTP AMBIGUO**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



La risorsa richiesta è disponibile in una o più posizioni.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**STATO HTTP \_ \_ SPOSTATO**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



La risorsa richiesta è stata assegnata a un nuovo UNIFORM RESOURCE IDENTIFIER permanente (URI) ed eventuali riferimenti futuri a questa risorsa devono essere eseuti usando uno degli URI restituiti.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**REINDIRIZZAMENTO \_ DELLO STATO \_ HTTP**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



La risorsa richiesta risiede temporaneamente in un URI diverso.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**METODO DI \_ \_ REINDIRIZZAMENTO DELLO STATO \_ HTTP**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



La risposta alla richiesta si trova in un URI diverso e deve essere recuperata usando un [*verbo HTTP*](glossary.md) GET su tale risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**STATO \_ HTTP \_ NON \_ MODIFICATO**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



La risorsa richiesta non è stata modificata.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP \_ STATUS \_ USE \_ PROXY**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



È necessario accedere alla risorsa richiesta tramite il proxy specificato dal campo location.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**VERBO \_ KEEP \_ DEL \_ REINDIRIZZAMENTO DELLO STATO \_ HTTP**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



La richiesta reindirizzata mantiene lo stesso [*verbo HTTP*](glossary.md). Comportamento HTTP/1.1.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**RICHIESTA DI STATO HTTP \_ \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



Impossibile elaborare la richiesta dal server a causa di una sintassi non valida.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**STATO HTTP \_ \_ NEGATO**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



La risorsa richiesta prevede l'autenticazione degli utenti.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**RICHIESTA \_ DI PAGAMENTO DELLO STATO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



Non implementato nel protocollo HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**STATO \_ HTTP \_ NON CONSENTITO**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Il server ha compreso la richiesta, ma non può soddisfarla.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**STATO \_ HTTP \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Il server non ha trovato nulla che corrisponda all'URI richiesto.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**METODO \_ HTTP STATUS \_ BAD \_**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Il [*verbo HTTP*](glossary.md) usato non è consentito.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**STATO HTTP \_ \_ NON ACCETTABILE \_**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



Non sono state trovate risposte accettabili per il client.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP \_ STATUS \_ PROXY \_ AUTH \_ REQ**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Autenticazione proxy richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**TIMEOUT \_ DELLA RICHIESTA DI STATO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



Timeout del server durante l'attesa della richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**CONFLITTO \_ DI STATO \_ HTTP**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



Impossibile completare la richiesta a causa di un conflitto con lo stato corrente della risorsa. L'utente deve inviare di nuovo con altre informazioni.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**STATO \_ HTTP NON PIÙ \_ VISUALIZZATO**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



La risorsa richiesta non è più disponibile nel server e non è noto alcun indirizzo di inoltro.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**LUNGHEZZA \_ DELLO STATO HTTP \_ \_ OBBLIGATORIA**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



Il server non può accettare la richiesta senza una lunghezza del contenuto definita.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**PRECOND STATO HTTP \_ \_ NON \_ RIUSCITO**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



La precondizione specificata in uno o più campi di intestazione della richiesta ha restituito false quando è stata testata nel server.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**RICHIESTA \_ DI STATO HTTP TROPPO \_ \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



Il server non è in grado di elaborare la richiesta perché l'entità richiesta è più grande di quella che il server è in grado di elaborare.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**URI \_ DI STATO HTTP TROPPO \_ \_ \_ LUNGO**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Il server non è in grado di eseguire la richiesta perché l'URI della richiesta è più lungo di quello che il server è in grado di interpretare.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**STATO HTTP \_ \_ SUPPORTO NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



Il server non è in grado di eseguire la richiesta perché l'entità della richiesta è in un formato non supportato dalla risorsa richiesta per il metodo richiesto.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**STATO HTTP \_ \_ \_ RIPROVARE CON**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



La richiesta deve essere ritentata dopo l'azione appropriata.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**ERRORE \_ DEL SERVER DI STATO \_ \_ HTTP**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



Il server ha rilevato una condizione imprevista che ha impedito di soddisfare la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**STATO \_ HTTP \_ NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



Il server non supporta la funzionalità necessaria per soddisfare la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**STATO HTTP \_ \_ GATEWAY NON \_ VALIDO**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



Il server, che funge da gateway o proxy, ha ricevuto una risposta non valida dal server upstream a cui ha effettuato l'accesso nel tentativo di soddisfare la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**SERVIZIO DI STATO HTTP \_ \_ \_ UNAVAIL**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



Il servizio è momentaneamente sovraccarico.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**TIMEOUT \_ \_ GATEWAY STATO \_ HTTP**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



Richiesta scaduta in attesa di un gateway.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**VERSIONE STATO HTTP \_ \_ NON \_ \_ SUP**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



Il server non supporta la versione del protocollo HTTP utilizzata nel messaggio di richiesta.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>      |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server solo con app desktop SP3 \[\]<br/>   |
| Intestazione<br/>                   | <dl> <dt>Winhttp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

