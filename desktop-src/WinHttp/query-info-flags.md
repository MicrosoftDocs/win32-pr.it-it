---
description: Questi attributi e modificatori vengono usati da WinHttpQueryHeaders.
ms.assetid: c26dac1d-9a75-440a-a0ef-a2029f138f3b
title: Flag informazioni query (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9ffc8f4ba4a947fe6fb277617c99460c43ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050235"
---
# <a name="query-info-flags-winhttph"></a>Flag informazioni query (WinHTTP. h)

Questi attributi e modificatori vengono usati da [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

I flag di attributo vengono usati da [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) per indicare quali informazioni recuperare. La maggior parte dei flag di attributo è mappata direttamente a un'intestazione HTTP specifica. Esistono anche alcuni flag speciali, ad esempio le \_ intestazioni RAW della query WinHTTP \_ \_ , che non sono correlati a un'intestazione specifica.

<dl> <dt>

<span id="WINHTTP_QUERY_ACCEPT"></span><span id="winhttp_query_accept"></span>**\_accettazione query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera i tipi di supporto accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_CHARSET"></span><span id="winhttp_query_accept_charset"></span>**\_set di \_ caratteri Accept della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera i set di caratteri accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_ENCODING"></span><span id="winhttp_query_accept_encoding"></span>**\_codifica di \_ accettazione della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera i valori di codifica del contenuto accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="winhttp_query_accept_language"></span>**\_lingua di \_ accettazione \_ query WinHTTP**
</dt> <dd> <dl> <dt>



Recupera i linguaggi naturali accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ACCEPT_RANGES"></span><span id="winhttp_query_accept_ranges"></span>**\_intervalli di \_ accettazione della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera i tipi di richieste di intervallo accettate per una risorsa.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AGE"></span><span id="winhttp_query_age"></span>**\_tempo di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera il campo Age Response-header, che contiene la stima del mittente relativa alla quantità di tempo trascorsa dalla generazione della risposta nel server di origine.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ALLOW"></span><span id="winhttp_query_allow"></span>**\_Consenti query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Riceve il [*verbo http*](glossary.md)s supportato dal server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHENTICATION_INFO"></span><span id="winhttp_query_authentication_info"></span>**\_informazioni di \_ autenticazione della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'intestazione del Authentication-Info.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_AUTHORIZATION"></span><span id="winhttp_query_authorization"></span>**\_autorizzazione per query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera le credenziali di autorizzazione utilizzate per una richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CACHE_CONTROL"></span><span id="winhttp_query_cache_control"></span>**\_ \_ controllo cache query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera le direttive di controllo della cache.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONNECTION"></span><span id="winhttp_query_connection"></span>**\_connessione query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera tutte le opzioni specificate per una particolare connessione e non devono essere comunicate tramite proxy tramite ulteriori connessioni.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_BASE"></span><span id="winhttp_query_content_base"></span>**\_ \_ base contenuto query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera la Uniform Resource Identifier di base (URI) per risolvere gli URL relativi nell'entità.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="winhttp_query_content_description"></span>**\_ \_ Descrizione contenuto query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Obsoleta. Gestito per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_DISPOSITION"></span><span id="winhttp_query_content_disposition"></span>**\_disposizione del \_ contenuto della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleta. Gestito per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ENCODING"></span><span id="winhttp_query_content_encoding"></span>**\_codifica del \_ contenuto della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la codifica del contenuto aggiuntiva applicata all'intera risorsa.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_ID"></span><span id="winhttp_query_content_id"></span>**\_ \_ ID contenuto query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera l'identificazione del contenuto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LANGUAGE"></span><span id="winhttp_query_content_language"></span>**\_lingua del \_ contenuto della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la lingua in cui è scritto il contenuto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LENGTH"></span><span id="winhttp_query_content_length"></span>**\_ \_ lunghezza contenuto query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera le dimensioni, in byte, della risorsa.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_LOCATION"></span><span id="winhttp_query_content_location"></span>**\_percorso del \_ contenuto della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera il percorso della risorsa per l'entità racchiusa nel messaggio.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_MD5"></span><span id="winhttp_query_content_md5"></span>**\_ \_ MD5 contenuto query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera un digest MD5 del corpo dell'entità allo scopo di fornire un controllo di integrità dei messaggi end-to-end per il corpo dell'entità. Per ulteriori informazioni, vedere [RFC 1864](https://www.ietf.org/rfc/rfc1864.txt).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_RANGE"></span><span id="winhttp_query_content_range"></span>**\_ \_ intervallo contenuto query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera la posizione nel corpo dell'entità completo in cui deve essere inserito il corpo dell'entità parziale e le dimensioni totali del corpo dell'entità completo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="winhttp_query_content_transfer_encoding"></span>**\_codifica del \_ trasferimento del contenuto delle query WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera una trasformazione di codifica applicabile a un corpo di entità. Potrebbe essere già stato applicato, potrebbe essere necessario applicarlo o eventualmente applicabile.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CONTENT_TYPE"></span><span id="winhttp_query_content_type"></span>**\_tipo di \_ contenuto della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve il tipo di contenuto della risorsa, ad esempio testo o HTML.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COOKIE"></span><span id="winhttp_query_cookie"></span>**\_cookie di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera tutti i cookie associati alla richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_COST"></span><span id="winhttp_query_cost"></span>**\_costo query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Non supportata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_CUSTOM"></span><span id="winhttp_query_custom"></span>**\_personalizzata della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Fa in modo che [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) cerchi il nome di intestazione specificato nel parametro *pwszName* e archivia le informazioni di intestazione in *lpBuffer*. Un'applicazione può utilizzare **il \_ \_ timeout di \_ risposta \_ di ricezione dell'opzione WinHTTP** per limitare il tempo massimo di attesa della query per la ricezione di tutte le intestazioni.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DATE"></span><span id="winhttp_query_date"></span>**\_data query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Riceve la data e l'ora in cui è stato originato il messaggio.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_DERIVED_FROM"></span><span id="winhttp_query_derived_from"></span>**\_query WinHTTP \_ derivata \_ da**
</dt> <dd> <dl> <dt>



Non supportata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ETAG"></span><span id="winhttp_query_etag"></span>**\_ETag query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera il tag di entità per l'entità associata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPECT"></span><span id="winhttp_query_expect"></span>**\_ \_ si prevede che la query WinHTTP**
</dt> <dd> <dl> <dt>



Recupera l'intestazione Expect, che indica se l'applicazione client deve prevedere le risposte della serie 100.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_EXPIRES"></span><span id="winhttp_query_expires"></span>**\_scadenza della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve la data e l'ora in cui la risorsa deve essere considerata obsoleta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FORWARDED"></span><span id="winhttp_query_forwarded"></span>**\_query WinHTTP \_ avanzata**
</dt> <dd> <dl> <dt>



Obsoleta. Gestito per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FROM"></span><span id="winhttp_query_from"></span>**\_query WinHTTP \_ da**
</dt> <dd> <dl> <dt>



Recupera l'indirizzo di posta elettronica dell'utente che controlla l' [*agente utente*](glossary.md) richiedente se l'intestazione From viene assegnata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_HOST"></span><span id="winhttp_query_host"></span>**\_host query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera l'host Internet e il numero di porta della risorsa richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MATCH"></span><span id="winhttp_query_if_match"></span>**\_query WinHTTP \_ se \_ corrispondente**
</dt> <dd> <dl> <dt>



Recupera il contenuto del If-Match campo di intestazione della richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="winhttp_query_if_modified_since"></span>**\_query WinHTTP \_ se \_ modificata \_ dopo**
</dt> <dd> <dl> <dt>



Recupera il contenuto dell'intestazione If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_NONE_MATCH"></span><span id="winhttp_query_if_none_match"></span>**\_query WinHTTP \_ se \_ Nessuna \_ corrispondenza**
</dt> <dd> <dl> <dt>



Recupera il contenuto del campo dell'intestazione della richiesta If-None-Match.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_RANGE"></span><span id="winhttp_query_if_range"></span>**\_query WinHTTP \_ se \_ intervallo**
</dt> <dd> <dl> <dt>



Recupera il contenuto del If-Range campo di intestazione della richiesta. Questa intestazione consente all'applicazione client di verificare se l'entità correlata a una copia parziale dell'entità nella cache dell'applicazione client non è stata aggiornata. Se l'entità non è stata aggiornata, inviare le parti mancanti nell'applicazione client. Se l'entità è stata aggiornata, inviare l'intera entità aggiornata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="winhttp_query_if_unmodified_since"></span>**\_query WinHTTP \_ se non \_ modificata \_ dopo**
</dt> <dd> <dl> <dt>



Recupera il contenuto del campo di intestazione della richiesta If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LINK"></span><span id="winhttp_query_link"></span>**\_collegamento alla query WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleta. Gestito per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LAST_MODIFIED"></span><span id="winhttp_query_last_modified"></span>**\_ \_ Ultima modifica della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve la data e l'ora dell'Ultima modifica della risorsa. La data e l'ora sono determinate dal server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_LOCATION"></span><span id="winhttp_query_location"></span>**\_percorso della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'URI assoluto utilizzato in un'intestazione di risposta della posizione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX"></span><span id="winhttp_query_max"></span>**\_Max query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Indica il valore massimo di un \_ valore di query WinHTTP \_ \* . Non è un flag di query.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MAX_FORWARDS"></span><span id="winhttp_query_max_forwards"></span>**\_ \_ numero massimo di \_ inoltri della query WinHTTP**
</dt> <dd> <dl> <dt>



Recupera il numero di proxy o gateway che è in grado di inoltrare la richiesta al server in ingresso successivo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MESSAGE_ID"></span><span id="winhttp_query_message_id"></span>**\_ \_ ID messaggio di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Non supportata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_MIME_VERSION"></span><span id="winhttp_query_mime_version"></span>**\_ \_ versione MIME della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve la versione del protocollo MIME (Multipurpose Internet Mail Extensions) utilizzato per costruire il messaggio.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_ORIG_URI"></span><span id="winhttp_query_orig_uri"></span>**\_ \_ URI orig query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Obsoleta. Gestito per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PRAGMA"></span><span id="winhttp_query_pragma"></span>**\_pragma query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Riceve le direttive specifiche dell'implementazione che potrebbero essere applicabili a qualsiasi destinatario lungo la catena di richiesta/risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="winhttp_query_proxy_authenticate"></span>**\_ \_ autenticazione proxy query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="winhttp_query_proxy_authorization"></span>**\_ \_ autorizzazione proxy query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera l'intestazione utilizzata per identificare l'utente a un proxy che richiede l'autenticazione. Questa intestazione può essere recuperata solo prima dell'invio della richiesta al server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_CONNECTION"></span><span id="winhttp_query_proxy_connection"></span>**\_ \_ connessione proxy di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'intestazione del Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PROXY_SUPPORT"></span><span id="winhttp_query_proxy_support"></span>**\_supporto del \_ proxy di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'intestazione del Proxy-Support.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_PUBLIC"></span><span id="winhttp_query_public"></span>**\_query WinHTTP \_ pubblica**
</dt> <dd> <dl> <dt>



Riceve i verbi HTTP disponibili in questo server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RANGE"></span><span id="winhttp_query_range"></span>**\_intervallo di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'intervallo di byte di un'entità.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS"></span><span id="winhttp_query_raw_headers"></span>**\_ \_ intestazioni RAW della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve tutte le intestazioni restituite dal server. Ogni intestazione viene terminata con " \\ 0". Un " \\ 0" aggiuntivo termina l'elenco di intestazioni.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="winhttp_query_raw_headers_crlf"></span>**\_intestazioni RAW di query WinHTTP \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>



Riceve tutte le intestazioni restituite dal server. Ogni intestazione è separata da una sequenza di ritorno a capo/avanzamento riga (CR/LF).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFERER"></span><span id="winhttp_query_referer"></span>**\_Referer della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve l'URI della risorsa in cui è stato ottenuto l'URI richiesto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REFRESH"></span><span id="winhttp_query_refresh"></span>**\_aggiornamento query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Obsoleta. Gestito per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_REQUEST_METHOD"></span><span id="winhttp_query_request_method"></span>**\_metodo di \_ richiesta di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve il verbo HTTP usato nella richiesta, in genere GET o POST.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_RETRY_AFTER"></span><span id="winhttp_query_retry_after"></span>**\_tentativo di query WinHTTP \_ \_ dopo**
</dt> <dd> <dl> <dt>



Recupera l'intervallo di tempo per cui il servizio non è disponibile.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SERVER"></span><span id="winhttp_query_server"></span>**\_server di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera le informazioni sul software utilizzato dal server di origine per gestire la richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_SET_COOKIE"></span><span id="winhttp_query_set_cookie"></span>**\_ \_ cookie set di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve il valore del set di cookie per la richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_CODE"></span><span id="winhttp_query_status_code"></span>**\_codice di \_ stato della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve il codice di stato restituito dal server. Per un elenco di valori possibili, vedere [**codici di stato http**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_STATUS_TEXT"></span><span id="winhttp_query_status_text"></span>**\_ \_ testo stato query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Riceve il testo aggiuntivo restituito dal server nella riga di risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TITLE"></span><span id="winhttp_query_title"></span>**\_titolo della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Obsoleta. Gestito per la compatibilità delle applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_TRANSFER_ENCODING"></span><span id="winhttp_query_transfer_encoding"></span>**\_codifica di \_ trasferimento \_ query WinHTTP**
</dt> <dd> <dl> <dt>



Recupera il tipo di trasformazione applicato al corpo del messaggio in modo che possa essere trasferito in modo sicuro tra il mittente e il destinatario.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="winhttp_query_unless_modified_since"></span>**\_query WinHTTP \_ a meno che non venga \_ modificata \_ da**
</dt> <dd> <dl> <dt>



Recupera l'intestazione a meno che non venga modificata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_UPGRADE"></span><span id="winhttp_query_upgrade"></span>**\_aggiornamento di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera i protocolli di comunicazione aggiuntivi supportati dal server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_URI"></span><span id="winhttp_query_uri"></span>**\_URI di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Riceve parte o tutto l'URI mediante il quale è possibile identificare la risorsa Request-URI.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_USER_AGENT"></span><span id="winhttp_query_user_agent"></span>**\_ \_ agente utente query \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera le informazioni sull'agente utente che ha effettuato la richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VARY"></span><span id="winhttp_query_vary"></span>**\_query WinHTTP \_ Vary**
</dt> <dd> <dl> <dt>



Recupera l'intestazione che indica che l'entità è stata selezionata da un numero di rappresentazioni disponibili della risposta mediante la negoziazione basata su server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VERSION"></span><span id="winhttp_query_version"></span>**\_versione della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la versione HTTP presente nella riga di stato.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_VIA"></span><span id="winhttp_query_via"></span>**\_query WinHTTP \_ tramite**
</dt> <dd> <dl> <dt>



Recupera i protocolli intermedi e i destinatari tra l'agente utente e il server nelle richieste e tra il server di origine e il client sulle risposte.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WARNING"></span><span id="winhttp_query_warning"></span>**\_avviso di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera informazioni aggiuntive sullo stato di una risposta che potrebbero non essere riflesse dal codice di stato della risposta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_WWW_AUTHENTICATE"></span><span id="winhttp_query_www_authenticate"></span>**\_autenticazione del \_ sito Web di query WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal server.


</dt> </dl> </dd> </dl>

I flag di modifica vengono utilizzati in combinazione con un flag di attributo per modificare la richiesta. I flag di modifica possono modificare il formato dei dati restituiti o indicare il punto in cui la funzione [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) deve cercare le informazioni.

<dl> <dt>

<span id="WINHTTP_QUERY_FLAG_NUMBER"></span><span id="winhttp_query_flag_number"></span>**\_numero di \_ flag della query WinHTTP \_**
</dt> <dd> <dl> <dt>



Restituisce i dati come numero a 32 bit per le intestazioni il cui valore è un numero, ad esempio il codice di stato.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="winhttp_query_flag_request_headers"></span>**\_intestazioni di \_ richiesta del flag di query WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Solo intestazioni della richiesta di query.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="winhttp_query_flag_systemtime"></span>**\_flag di query WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Restituisce il valore dell'intestazione come struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , che non richiede l'analisi dei dati da parte dell'applicazione. Utilizzare per le intestazioni il cui valore è una stringa di data/ora, ad esempio "Last-Modified-Time".


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

 

