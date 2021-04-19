---
description: Questi attributi e modificatori vengono usati da WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Flag di informazioni query (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ba15c258a37627cdbdd79f13859761fd671385
ms.sourcegitcommit: df0933ad2b42f07031f4340330712c11cf712ff0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107385889"
---
# <a name="query-info-flags-winhttph"></a>Flag di informazioni query (Winhttp.h)

Questi attributi e modificatori vengono usati [**da WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders).

I flag di attributo vengono usati [**da WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) per indicare le informazioni da recuperare. La maggior parte dei flag di attributo viene mappata direttamente a un'intestazione HTTP specifica. Esistono anche alcuni flag speciali, ad esempio WINHTTP QUERY RAW HEADERS, che non \_ \_ sono correlati a \_ un'intestazione specifica.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**ACCETTA QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera i tipi di supporti accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**WINHTTP \_ QUERY \_ ACCEPT \_ CHARSET**
</dt> <dd> <dl> <dt>



Recupera i set di caratteri accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**CODIFICA WINHTTP \_ QUERY \_ ACCEPT \_**
</dt> <dd> <dl> <dt>



Recupera i valori accettabili di codifica del contenuto per la risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**LINGUAGGIO DI \_ ACCETTAZIONE \_ QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera i linguaggi naturali accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**INTERVALLI DI \_ ACCETTAZIONE \_ QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera i tipi di richieste di intervallo accettate per una risorsa.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**PERIODO DI \_ VALIDITÀ DELLE QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera il campo Age response-header , che contiene la stima del mittente del periodo di tempo dopo la generazione della risposta nel server di origine.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**CONSENTI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Riceve i [**verbi HTTP**](glossary.md) supportati dal server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**INFORMAZIONI DI AUTENTICAZIONE QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera l'Authentication-Info personalizzata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**AUTORIZZAZIONE \_ DELLE QUERY \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera le credenziali di autorizzazione utilizzate per una richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**CONTROLLO \_ \_ DELLA CACHE DELLE QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera le direttive di controllo della cache.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**CONNESSIONE DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera tutte le opzioni specificate per una determinata connessione e che non devono essere comunicate da proxy su ulteriori connessioni.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**BASE DEL CONTENUTO DELLA QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera l'URI Uniform Resource Identifier base per risolvere gli URL relativi all'interno dell'entità.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**DESCRIZIONE DEL CONTENUTO DELLA QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Obsoleta. Mantenuta per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**DISPOSIZIONE DEL CONTENUTO DELLE QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Obsoleta. Mantenuta per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**CODIFICA DEL CONTENUTO DELLE QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera il codice del contenuto aggiuntivo applicato all'intera risorsa.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**ID CONTENUTO QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera l'identificazione del contenuto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**LINGUAGGIO DEL CONTENUTO DELLE QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera la lingua in cui è scritto il contenuto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**LUNGHEZZA CONTENUTO QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera le dimensioni della risorsa, in byte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**PERCORSO DEL CONTENUTO DELLE QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera il percorso della risorsa per l'entità racchiusa nel messaggio.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**WINHTTP \_ QUERY \_ CONTENT \_ MD5**
</dt> <dd> <dl> <dt>



Recupera un digest MD5 del corpo dell'entità allo scopo di fornire un controllo di integrità del messaggio end-to-end per il corpo dell'entità. Per altre informazioni, vedere [RFC 1864.](https://www.ietf.org/rfc/rfc1864.txt)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**INTERVALLO DI CONTENUTO DI QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera la posizione nel corpo completo dell'entità in cui deve essere inserito il corpo dell'entità parziale e le dimensioni totali del corpo completo dell'entità.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**CODIFICA DI TRASFERIMENTO \_ \_ DEL CONTENUTO \_ DI QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera una trasformazione di codifica applicabile a un corpo dell'entità. Potrebbe essere già stato applicato, potrebbe essere necessario applicarlo o essere facoltativamente applicabile.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**TIPO DI CONTENUTO DI QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Riceve il tipo di contenuto della risorsa, ad esempio testo o html.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**COOKIE \_ DI QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera tutti i cookie associati alla richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**COSTO QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Non supportata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**WINHTTP \_ QUERY \_ CUSTOM**
</dt> <dd> <dl> <dt>



Consente [**a WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) di cercare il nome dell'intestazione specificato nel *parametro pwszName* e di archiviare le informazioni sull'intestazione in *lpBuffer*. Un'applicazione può **usare WINHTTP \_ OPTION RECEIVE \_ RESPONSE \_ \_ TIMEOUT** per limitare il tempo massimo di attesa della query per la ricezione di tutte le intestazioni.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**DATA QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Riceve la data e l'ora di origine del messaggio.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**QUERY WINHTTP \_ \_ DERIVATA \_ DA**
</dt> <dd> <dl> <dt>



Non supportata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETAG DELLA QUERY \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera il tag di entità per l'entità associata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**WINHTTP \_ QUERY \_ EXPECT**
</dt> <dd> <dl> <dt>



Recupera l'intestazione Expect, che indica se l'applicazione client deve prevedere risposte serie 100.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**SCADENZA QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Riceve la data e l'ora dopo le quali la risorsa deve essere considerata obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**QUERY WINHTTP \_ \_ INOLTRATA**
</dt> <dd> <dl> <dt>



Obsoleta. Mantenuta per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**QUERY WINHTTP \_ \_ DA**
</dt> <dd> <dl> <dt>



Recupera l'indirizzo di posta elettronica dell'utente che controlla l'agente utente richiedente [*se*](glossary.md) viene specificata l'intestazione From.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**HOST \_ DI QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'host Internet e il numero di porta della risorsa richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**WINHTTP \_ QUERY \_ IF \_ MATCH**
</dt> <dd> <dl> <dt>



Recupera il contenuto del campo If-Match di intestazione della richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**QUERY WINHTTP \_ \_ SE MODIFICATA \_ \_ DA**
</dt> <dd> <dl> <dt>



Recupera il contenuto dell'intestazione If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**QUERY WINHTTP \_ \_ SE NESSUNA \_ \_ CORRISPONDENZA**
</dt> <dd> <dl> <dt>



Recupera il contenuto del campo di intestazione della richiesta If-None-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**INTERVALLO DI \_ QUERY \_ WINHTTP \_ IF**
</dt> <dd> <dl> <dt>



Recupera il contenuto del campo If-Range di intestazione della richiesta. Questa intestazione consente all'applicazione client di verificare se l'entità correlata a una copia parziale dell'entità nella cache dell'applicazione client non è stata aggiornata. Se l'entità non è stata aggiornata, inviare le parti mancanti nell'applicazione client. Se l'entità è stata aggiornata, inviare l'intera entità aggiornata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**QUERY WINHTTP \_ \_ SE NON MODIFICATA \_ \_ DA**
</dt> <dd> <dl> <dt>



Recupera il contenuto del campo di intestazione della richiesta If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**COLLEGAMENTO A QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Obsoleta. Mantenuta per garantire la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**ULTIMA MODIFICA DELLA QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Riceve la data e l'ora dell'ultima modifica della risorsa. La data e l'ora sono determinate dal server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**PERCORSO QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera l'URI assoluto utilizzato in un'intestazione di risposta Location.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**NUMERO MASSIMO DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Indica il valore massimo di un valore WINHTTP \_ \_ \* QUERY. Non è un flag di query.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**NUMERO MASSIMO \_ \_ DI FORWARD DI QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera il numero di proxy o gateway che possono inoltrare la richiesta al server in ingresso successivo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**ID DEL MESSAGGIO DI QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Non supportata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**VERSIONE MIME DELLA QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Riceve la versione del Multipurpose Internet Mail Extensions (MIME) utilizzato per costruire il messaggio.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**URI \_ \_ ORIG DELLA QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleta. Mantenuta per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**PRAGMA \_ DI QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Riceve le direttive specifiche dell'implementazione che possono essere applicate a qualsiasi destinatario lungo la catena di richiesta/risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**AUTENTICAZIONE \_ DEL \_ PROXY DI QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**AUTORIZZAZIONE \_ DEL PROXY DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera l'intestazione utilizzata per identificare l'utente in un proxy che richiede l'autenticazione. Questa intestazione può essere recuperata solo prima che la richiesta venga inviata al server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**CONNESSIONE PROXY DI QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera l'Proxy-Connection personalizzata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**SUPPORTO DEL \_ PROXY DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera l'Proxy-Support personalizzata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**WINHTTP \_ QUERY \_ PUBLIC**
</dt> <dd> <dl> <dt>



Riceve i verbi HTTP disponibili in questo server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**INTERVALLO DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera l'intervallo di byte di un'entità.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**INTESTAZIONI NON \_ ELABORATE DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Riceve tutte le intestazioni restituite dal server. Ogni intestazione viene terminata da \\ "0". Un altro \\ "0" termina l'elenco di intestazioni.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**WINHTTP \_ QUERY \_ RAW \_ HEADERS \_ CRLF**
</dt> <dd> <dl> <dt>



Riceve tutte le intestazioni restituite dal server. Ogni intestazione è separata da una sequenza di ritorno a capo/avanzamento riga (CR/LF).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**REFERER DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Riceve l'URI della risorsa in cui è stato ottenuto l'URI richiesto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**AGGIORNAMENTO DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Obsoleta. Mantenuta per garantire la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**METODO DI \_ RICHIESTA DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Riceve il verbo HTTP utilizzato nella richiesta, in genere GET o POST.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**NUOVO TENTATIVO DI QUERY WINHTTP \_ \_ \_ DOPO**
</dt> <dd> <dl> <dt>



Recupera l'intervallo di tempo previsto che il servizio non sarà disponibile.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**SERVER DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera informazioni sul software usato dal server di origine per gestire la richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**COOKIE DEL \_ \_ SET DI QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Riceve il valore del set di cookie per la richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**CODICE DI STATO DELLA QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Riceve il codice di stato restituito dal server. Per un elenco dei valori possibili, vedere [**Codici di stato HTTP.**](http-status-codes.md)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**TESTO DELLO STATO DELLA QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Riceve testo aggiuntivo restituito dal server nella riga di risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**TITOLO \_ DELLA QUERY \_ WINHTTP**
</dt> <dd> <dl> <dt>



Obsoleta. Mantenuta per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**CODIFICA DI TRASFERIMENTO DI QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera il tipo di trasformazione applicato al corpo del messaggio in modo che possa essere trasferito in modo sicuro tra il mittente e il destinatario.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**QUERY WINHTTP \_ A MENO CHE NON VENGA MODIFICATA \_ \_ \_ DA**
</dt> <dd> <dl> <dt>



Recupera l'intestazione Unless-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**AGGIORNAMENTO DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera i protocolli di comunicazione aggiuntivi supportati dal server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**URI DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Riceve parte o tutto l'URI in base al quale è possibile identificare la risorsa REQUEST-URI.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**AGENTE UTENTE DI QUERY WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera informazioni sull'agente utente che ha effettuato la richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**WINHTTP \_ QUERY \_ VARY**
</dt> <dd> <dl> <dt>



Recupera l'intestazione che indica che l'entità è stata selezionata da una serie di rappresentazioni disponibili della risposta usando la negoziazione basata su server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**VERSIONE \_ DELLA QUERY \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera la versione HTTP presente nella riga di stato.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**QUERY WINHTTP \_ \_ TRAMITE**
</dt> <dd> <dl> <dt>



Recupera i protocolli intermedi e i destinatari tra l'agente utente e il server nelle richieste e tra il server di origine e il client nelle risposte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**AVVISO DI QUERY WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera informazioni aggiuntive sullo stato di una risposta che potrebbero non essere riflesse dal codice di stato della risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**WINHTTP \_ QUERY \_ WWW \_ AUTHENTICATE**
</dt> <dd> <dl> <dt>



Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal server.


</dt> </dl> </dd> </dl>

I flag di modifica vengono usati insieme a un flag di attributo per modificare la richiesta. I flag di modifica modificano il formato dei dati restituiti o indicano dove la [**funzione WinHttpQueryHeaders**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryheaders) deve cercare le informazioni.

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**NUMERO DI \_ \_ FLAG DI QUERY WINHTTP \_**
</dt> <dd> <dl> <dt>



Restituisce i dati come numero a 32 bit per le intestazioni il cui valore è un numero, ad esempio il codice di stato.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**INTESTAZIONI DI \_ RICHIESTA \_ FLAG DI QUERY \_ WINHTTP \_**
</dt> <dd> <dl> <dt>



Esegue query solo sulle intestazioni delle richieste.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**WINHTTP \_ QUERY \_ FLAG \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>



Restituisce il valore dell'intestazione come [**struttura SYSTEMTIME,**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) che non richiede all'applicazione di analizzare i dati. Usare per le intestazioni il cui valore è una stringa di data/ora, ad esempio "Last-Modified-Time".


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato | Windows XP, Windows 2000 Professional con solo app desktop SP3 \[\]      |
| Server minimo supportato | Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]   |
| Intestazione                   | <dl> <dt>Winhttp.h</dt> </dl> |

## <a name="see-also"></a>Vedere anche

* [Versioni di WinHTTP](winhttp-versions.md)
