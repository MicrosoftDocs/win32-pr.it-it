---
title: HTTP_LOG_FIELD_ costanti (Http.h)
description: Definire i campi nel log W3C e nei log degli errori.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 616caaed9829c7f926f95f8982033457e1835a6beccfcad8313f6624d68195db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950830"
---
# <a name="http_log_field_-constants"></a>Costanti \_ HTTP LOG \_ FIELD \_

Le **costanti HTTP LOG \_ \_ FIELD \_** definiscono i campi nel log W3C e nei log degli errori.

Queste costanti vengono usate nella struttura [**HTTP \_ LOGGING \_ INFO.**](/windows/desktop/api/Http/ns-http-http_logging_info)

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**DATA \_ DEL CAMPO DEL LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Data in cui si è verificata l'attività.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**ORA \_ CAMPO \_ LOG \_ HTTP**
</dt> <dd> <dl> <dt>



Ora, in formato UTC (Coordinated Universal Time), in cui si è verificata l'attività.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**IP \_ CLIENT DEL CAMPO DEL LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Indirizzo IP del client che ha eseguito la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**NOME \_ UTENTE DEL CAMPO DEL LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Nome dell'utente autenticato che ha eseguito l'accesso al server. Gli utenti anonimi sono indicati da un trattino.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**NOME \_ DEL SITO DEL CAMPO DEL LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Nome del sito in cui è stata generata la voce del file di log.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**HTTP \_ NOME \_ COMPUTER CAMPO \_ \_ LOG**
</dt> <dd> <dl> <dt>



Nome del computer in cui è stata generata la voce del file di log.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**IP \_ DEL SERVER DEI CAMPI DEL LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Indirizzo IP del server in cui è stata generata la voce del file di log.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**METODO \_ DEL CAMPO DI LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Azione richiesta, ad esempio un metodo get.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**HTTP \_ LOG \_ FIELD \_ URI \_ STEM**
</dt> <dd> <dl> <dt>



Destinazione dell'azione, ad esempio Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_QUERY URI CAMPO LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Query, se presente, che il client stava tentando di eseguire. Una query URI è necessaria solo per le pagine dinamiche.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**STATO \_ DEL CAMPO DEL LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Codice di stato HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**STATO \_ \_ WIN32 DEL CAMPO DI LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Codice Windows stato.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**BYTE DEL CAMPO DEL LOG HTTP \_ \_ \_ \_ INVIATI**
</dt> <dd> <dl> <dt>



Numero, in byte, inviato dal server.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**BYTE DEL CAMPO DEL LOG HTTP \_ \_ \_ \_ RECV**
</dt> <dd> <dl> <dt>



Numero, in byte, ricevuto dal server.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**TEMPO DI CAMPO DEL LOG HTTP \_ \_ \_ \_ IMPIEGATO**
</dt> <dd> <dl> <dt>



Tempo, in millisecondi, dell'azione.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**PORTA \_ DEL SERVER HTTP LOG \_ FIELD \_ \_**
</dt> <dd> <dl> <dt>



Numero di porta del server configurato per il servizio.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**HTTP \_ LOG \_ FIELD \_ USER \_ AGENT**
</dt> <dd> <dl> <dt>



Applicazione usata dal client.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**COOKIE \_ DEL CAMPO DEL LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Contenuto del cookie inviato o ricevuto, se presente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**REFERER \_ \_ DEI CAMPI DI \_ LOG HTTP**
</dt> <dd> <dl> <dt>



Sito visitato per l'ultima volta dall'utente. Questo sito fornisce un collegamento al sito corrente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**VERSIONE \_ DEL CAMPO DEL LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Versione del protocollo HTTP usata dal client.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_HOST DEL CAMPO DEL \_ \_ LOG HTTP**
</dt> <dd> <dl> <dt>



Nome dell'intestazione host, se presente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**STATO \_ \_ SECONDARIO DEL CAMPO \_ DEL LOG \_ HTTP**
</dt> <dd> <dl> <dt>



Codice di errore di stato secondario.


</dt> </dl> </dd> </dl>

Per la registrazione degli errori HTTP vengono utilizzate le costanti seguenti.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP \_ LOG FIELD CLIENT PORT \_ (PORTA CLIENT DEL CAMPO DI REGISTRAZIONE \_ \_ HTTP)**
</dt> <dd> <dl> <dt>



Numero di porta client da cui viene ricevuta la richiesta. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_URI DEL CAMPO DEL LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



URI ricevuto nella richiesta, inclusa la parte di query. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**ID \_ SITO DEL CAMPO DEL \_ \_ \_ LOG HTTP**
</dt> <dd> <dl> <dt>



ID numerico specifico dell'applicazione del gruppo di URL in cui viene instradata la richiesta. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**MOTIVO \_ DEL CAMPO DEL LOG \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Frase del motivo dell'errore. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**NOME \_ CODA CAMPO LOG \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Nome della coda di richieste a cui viene inviata la richiesta. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**STREAMID \_ \_ DEL CAMPO DI \_ LOG HTTP**
</dt> <dd> <dl> <dt>



ID flusso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'API server HTTP versione 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**INFORMAZIONI \_ DI REGISTRAZIONE \_ HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**Proprietà HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





