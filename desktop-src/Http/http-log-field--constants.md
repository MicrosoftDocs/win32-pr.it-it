---
title: Costanti HTTP_LOG_FIELD_ (http. h)
description: Definire i campi nel registro W3C e nei log degli errori.
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
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301379"
---
# <a name="http_log_field_-constants"></a>\_ \_ Costanti campi del log http \_

Le costanti dei campi di **\_ \_ \_ log http** definiscono i campi nel registro W3C e nei log degli errori.

Queste costanti vengono utilizzate nella struttura di [**\_ \_ informazioni di registrazione http**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_ \_ data campo registro \_ http**
</dt> <dd> <dl> <dt>



Data in cui si è verificata l'attività.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_ \_ ora campo registro \_ http**
</dt> <dd> <dl> <dt>



Ora, in formato UTC (Coordinated Universal Time), in cui si è verificata l'attività.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_ \_ \_ IP client campo registro \_ http**
</dt> <dd> <dl> <dt>



Indirizzo IP del client che ha eseguito la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_ \_ \_ nome utente campo registro \_ http**
</dt> <dd> <dl> <dt>



Nome dell'utente autenticato che ha eseguito l'accesso al server. Gli utenti anonimi sono indicati da un trattino.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_ \_ \_ nome sito campo registro \_ http**
</dt> <dd> <dl> <dt>



Nome del sito in cui è stata generata la voce del file di log.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Http \_ \_ \_ \_ nome computer campo Registro**
</dt> <dd> <dl> <dt>



Nome del computer in cui è stata generata la voce del file di log.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_IP del \_ server del campo di log http \_ \_**
</dt> <dd> <dl> <dt>



Indirizzo IP del server in cui è stata generata la voce del file di log.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_ \_ Metodo campo registro \_ http**
</dt> <dd> <dl> <dt>



Azione richiesta, ad esempio, un metodo Get.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Http \_ \_ \_ \_ radice URI campo Registro**
</dt> <dd> <dl> <dt>



Destinazione dell'azione, ad esempio Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_ \_ \_ query URI campo registro \_ http**
</dt> <dd> <dl> <dt>



Eventuale query che il client sta tentando di eseguire. Una query URI è necessaria solo per le pagine dinamiche.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_ \_ stato campo registro \_ http**
</dt> <dd> <dl> <dt>



Codice di stato HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_ \_ \_ Stato Win32 campo registro \_ http**
</dt> <dd> <dl> <dt>



Codice di stato di Windows.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_byte del campo di log http \_ \_ \_ inviati**
</dt> <dd> <dl> <dt>



Numero, in byte, inviato dal server.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_ \_ byte campo registro \_ http \_ ricezione**
</dt> <dd> <dl> <dt>



Numero, in byte, ricevuto dal server.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_ \_ tempo campo registro \_ http \_ impiegato**
</dt> <dd> <dl> <dt>



Tempo, in millisecondi, dell'azione.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_porta del \_ server del campo di log http \_ \_**
</dt> <dd> <dl> <dt>



Numero di porta del server configurato per il servizio.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Http \_ \_ \_ \_ agente utente campo di log**
</dt> <dd> <dl> <dt>



Applicazione utilizzata dal client.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_ \_ cookie campo registro \_ http**
</dt> <dd> <dl> <dt>



Contenuto del cookie inviato o ricevuto, se disponibile.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_ \_ riferimento campo registro \_ http**
</dt> <dd> <dl> <dt>



Sito che l'utente ha visitato per ultimo. Questo sito fornisce un collegamento al sito corrente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_ \_ versione campo registro \_ http**
</dt> <dd> <dl> <dt>



Versione del protocollo HTTP utilizzata dal client.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_ \_ host campo registro \_ http**
</dt> <dd> <dl> <dt>



Nome dell'intestazione host, se presente.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_ \_ \_ stato secondario campo registro \_ http**
</dt> <dd> <dl> <dt>



Codice di errore dello stato secondario.


</dt> </dl> </dd> </dl>

Per la registrazione degli errori HTTP vengono utilizzate le costanti seguenti.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_ \_ \_ porta client campo di log http \_**
</dt> <dd> <dl> <dt>



Numero di porta client da cui viene ricevuta la richiesta. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_ \_ URI campo registro \_ http**
</dt> <dd> <dl> <dt>



URI ricevuto nella richiesta, inclusa la parte della query. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ \_ \_ ID sito campo registro \_ http**
</dt> <dd> <dl> <dt>



ID numerico specifico dell'applicazione del gruppo di URL in cui viene indirizzata la richiesta. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_ \_ motivo campo registro \_ http**
</dt> <dd> <dl> <dt>



La frase del motivo dell'errore. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_ \_ \_ nome coda campo registro \_ http**
</dt> <dd> <dl> <dt>



Nome della coda di richieste a cui viene inviata la richiesta. Questo campo di log viene usato solo per la registrazione degli errori.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_campo registro \_ http \_ STREAMID**
</dt> <dd> <dl> <dt>



ID del flusso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti API server HTTP versione 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_informazioni di registrazione http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





