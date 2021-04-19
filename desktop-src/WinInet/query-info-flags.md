---
title: Flag informazioni query (WinInet. h)
description: Gli elenchi seguenti contengono gli attributi e i modificatori usati da HttpQueryInfo e QueryInfo.
ms.assetid: b1613193-ae03-411e-bf05-de42f471cd8c
topic_type:
- apiref
api_name:
- HTTP_QUERY_ACCEPT
- HTTP_QUERY_ACCEPT_CHARSET
- HTTP_QUERY_ACCEPT_ENCODING
- HTTP_QUERY_ACCEPT_LANGUAGE
- HTTP_QUERY_ACCEPT_RANGES
- HTTP_QUERY_AGE
- HTTP_QUERY_ALLOW
- HTTP_QUERY_AUTHORIZATION
- HTTP_QUERY_CACHE_CONTROL
- HTTP_QUERY_CONNECTION
- HTTP_QUERY_CONTENT_BASE
- HTTP_QUERY_CONTENT_DESCRIPTION
- HTTP_QUERY_CONTENT_DISPOSITION
- HTTP_QUERY_CONTENT_ENCODING
- HTTP_QUERY_CONTENT_ID
- HTTP_QUERY_CONTENT_LANGUAGE
- HTTP_QUERY_CONTENT_LENGTH
- HTTP_QUERY_CONTENT_LOCATION
- HTTP_QUERY_CONTENT_MD5
- HTTP_QUERY_CONTENT_RANGE
- HTTP_QUERY_CONTENT_TRANSFER_ENCODING
- HTTP_QUERY_CONTENT_TYPE
- HTTP_QUERY_COOKIE
- HTTP_QUERY_COST
- HTTP_QUERY_CUSTOM
- HTTP_QUERY_DATE
- HTTP_QUERY_DERIVED_FROM
- HTTP_QUERY_ECHO_HEADERS
- HTTP_QUERY_ECHO_HEADERS_CRLF
- HTTP_QUERY_ECHO_REPLY
- HTTP_QUERY_ECHO_REQUEST
- HTTP_QUERY_ETAG
- HTTP_QUERY_EXPECT
- HTTP_QUERY_EXPIRES
- HTTP_QUERY_FORWARDED
- HTTP_QUERY_FROM
- HTTP_QUERY_HOST
- HTTP_QUERY_IF_MATCH
- HTTP_QUERY_IF_MODIFIED_SINCE
- HTTP_QUERY_IF_NONE_MATCH
- HTTP_QUERY_IF_RANGE
- HTTP_QUERY_IF_UNMODIFIED_SINCE
- HTTP_QUERY_LAST_MODIFIED
- HTTP_QUERY_LINK
- HTTP_QUERY_LOCATION
- HTTP_QUERY_MAX
- HTTP_QUERY_MAX_FORWARDS
- HTTP_QUERY_MESSAGE_ID
- HTTP_QUERY_MIME_VERSION
- HTTP_QUERY_ORIG_URI
- HTTP_QUERY_PRAGMA
- HTTP_QUERY_PROXY_AUTHENTICATE
- HTTP_QUERY_PROXY_AUTHORIZATION
- HTTP_QUERY_PROXY_CONNECTION
- HTTP_QUERY_PUBLIC
- HTTP_QUERY_RANGE
- HTTP_QUERY_RAW_HEADERS
- HTTP_QUERY_RAW_HEADERS_CRLF
- HTTP_QUERY_REFERER
- HTTP_QUERY_REFRESH
- HTTP_QUERY_REQUEST_METHOD
- HTTP_QUERY_RETRY_AFTER
- HTTP_QUERY_SERVER
- HTTP_QUERY_SET_COOKIE
- HTTP_QUERY_STATUS_CODE
- HTTP_QUERY_STATUS_TEXT
- HTTP_QUERY_TITLE
- HTTP_QUERY_TRANSFER_ENCODING
- HTTP_QUERY_UNLESS_MODIFIED_SINCE
- HTTP_QUERY_UPGRADE
- HTTP_QUERY_URI
- HTTP_QUERY_USER_AGENT
- HTTP_QUERY_VARY
- HTTP_QUERY_VERSION
- HTTP_QUERY_VIA
- HTTP_QUERY_WARNING
- HTTP_QUERY_WWW_AUTHENTICATE
- HTTP_QUERY_X_CONTENT_TYPE_OPTIONS
- HTTP_QUERY_P3P
- HTTP_QUERY_X_P2P_PEERDIST
- HTTP_QUERY_TRANSLATE
- HTTP_QUERY_X_UA_COMPATIBLE
- HTTP_QUERY_DEFAULT_STYLE
- HTTP_QUERY_X_FRAME_OPTIONS
- HTTP_QUERY_X_XSS_PROTECTION
- HTTP_QUERY_FLAG_COALESCE
- HTTP_QUERY_FLAG_NUMBER
- HTTP_QUERY_FLAG_REQUEST_HEADERS
- HTTP_QUERY_FLAG_SYSTEMTIME
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3a6166c59e158d041e730d2198f6e1b066a8b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302735"
---
# <a name="query-info-flags-winineth"></a>Flag informazioni query (WinInet. h)

Gli elenchi seguenti contengono gli attributi e i modificatori usati da [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) e [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85)).

I flag di attributo vengono utilizzati da [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) per indicare quali dati recuperare. La maggior parte dei flag di attributo è mappata direttamente a un'intestazione HTTP specifica. Esistono anche alcuni flag speciali, ad esempio le [ \_ \_ \_ intestazioni RAW della query http](/windows), che non sono correlati a un'intestazione specifica.

<dl> <dt>

<span id="HTTP_QUERY_ACCEPT"></span><span id="http_query_accept"></span>**\_accettazione query \_ http**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Recupera i tipi di supporto accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_CHARSET"></span><span id="http_query_accept_charset"></span>**\_set di \_ caratteri Accept della query http \_**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Recupera i set di caratteri accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_ENCODING"></span><span id="http_query_accept_encoding"></span>**\_ \_ codifica Accept della query http \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Recupera i valori di codifica del contenuto accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_LANGUAGE"></span><span id="http_query_accept_language"></span>**\_lingua di \_ accettazione \_ query http**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Recupera i linguaggi naturali accettabili per la risposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ACCEPT_RANGES"></span><span id="http_query_accept_ranges"></span>**\_intervalli di \_ accettazione \_ query http**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Recupera i tipi di richieste di intervallo accettate per una risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AGE"></span><span id="http_query_age"></span>**\_tempo di query http \_**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Recupera il campo Age Response-header, che contiene la stima del mittente relativa alla quantità di tempo trascorsa dalla generazione della risposta nel server di origine.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ALLOW"></span><span id="http_query_allow"></span>**\_Consenti query \_ http**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Riceve i verbi HTTP supportati dal server.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_AUTHORIZATION"></span><span id="http_query_authorization"></span>**\_autorizzazione query \_ http**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Recupera le credenziali di autorizzazione utilizzate per una richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CACHE_CONTROL"></span><span id="http_query_cache_control"></span>**\_ \_ controllo cache query \_ http**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Recupera le direttive di controllo della cache.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONNECTION"></span><span id="http_query_connection"></span>**\_connessione query \_ http**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Recupera tutte le opzioni specificate per una particolare connessione e non devono essere comunicate tramite proxy tramite ulteriori connessioni.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_BASE"></span><span id="http_query_content_base"></span>**\_ \_ base contenuto query \_ http**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Recupera l'URI di base (Uniform Resource Identifier) per la risoluzione degli URL relativi nell'entità.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DESCRIPTION"></span><span id="http_query_content_description"></span>**\_ \_ Descrizione contenuto query \_ http**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Obsoleta. Gestito solo per compatibilità con le applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_DISPOSITION"></span><span id="http_query_content_disposition"></span>**\_disposizione del \_ contenuto della query http \_**
</dt> <dd> <dl> <dt>

47
</dt> <dt>



Obsoleta. Gestito solo per compatibilità con le applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ENCODING"></span><span id="http_query_content_encoding"></span>**\_codifica del \_ contenuto della query http \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Recupera tutte le codifiche di contenuto aggiuntive applicate all'intera risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_ID"></span><span id="http_query_content_id"></span>**\_ \_ ID contenuto query \_ http**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Recupera l'identificazione del contenuto.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LANGUAGE"></span><span id="http_query_content_language"></span>**\_lingua del \_ contenuto della query http \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Recupera la lingua in cui si trova il contenuto.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LENGTH"></span><span id="http_query_content_length"></span>**\_ \_ lunghezza contenuto query \_ http**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Recupera le dimensioni, in byte, della risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_LOCATION"></span><span id="http_query_content_location"></span>**\_percorso del \_ contenuto della query http \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Recupera il percorso della risorsa per l'entità racchiusa nel messaggio.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_MD5"></span><span id="http_query_content_md5"></span>**\_ \_ MD5 contenuto query \_ http**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Recupera un digest MD5 del corpo dell'entità allo scopo di fornire un controllo di integrità dei messaggi end-to-end per il corpo dell'entità. Per ulteriori informazioni, vedere RFC1864, il campo dell'intestazione Content-MD5, all'indirizzo [https://ftp.isi.edu/in-notes/rfc1864.txt](https://tools.ietf.org/html/rfc1864) .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_RANGE"></span><span id="http_query_content_range"></span>**\_ \_ intervallo contenuto query \_ http**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Recupera la posizione nel corpo entità completo in cui deve essere inserito il corpo dell'entità parziale e le dimensioni totali del corpo dell'entità completo.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TRANSFER_ENCODING"></span><span id="http_query_content_transfer_encoding"></span>**\_ \_ \_ codifica trasferimento contenuto query \_ http**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Riceve la codifica del contenuto aggiuntiva applicata alla risorsa.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CONTENT_TYPE"></span><span id="http_query_content_type"></span>**\_tipo di \_ contenuto \_ query http**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Riceve il tipo di contenuto della risorsa (ad esempio testo/HTML).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COOKIE"></span><span id="http_query_cookie"></span>**\_cookie di query http \_**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Recupera tutti i cookie associati alla richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_COST"></span><span id="http_query_cost"></span>**\_costo query \_ http**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Non più supportata.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_CUSTOM"></span><span id="http_query_custom"></span>**\_query http \_ personalizzata**
</dt> <dd> <dl> <dt>

65535
</dt> <dt>



Fa in modo che [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) cerchi il nome dell'intestazione specificato in *lpvBuffer* e memorizzi i dati dell'intestazione in *lpvBuffer*.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DATE"></span><span id="http_query_date"></span>**\_data query \_ http**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Riceve la data e l'ora in cui è stato originato il messaggio.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DERIVED_FROM"></span><span id="http_query_derived_from"></span>**\_query http \_ derivata \_ da**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Non più supportata.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS"></span><span id="http_query_echo_headers"></span>**\_ \_ intestazioni echo della query http \_**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Non implementato attualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_HEADERS_CRLF"></span><span id="http_query_echo_headers_crlf"></span>**\_intestazioni echo della query http \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Non implementato attualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REPLY"></span><span id="http_query_echo_reply"></span>**\_ \_ risposta echo query \_ http**
</dt> <dd> <dl> <dt>

72
</dt> <dt>



Non implementato attualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ECHO_REQUEST"></span><span id="http_query_echo_request"></span>**\_ \_ richiesta echo di query http \_**
</dt> <dd> <dl> <dt>

71
</dt> <dt>



Non implementato attualmente.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ETAG"></span><span id="http_query_etag"></span>**\_ETag query \_ http**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Recupera il tag di entità per l'entità associata.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPECT"></span><span id="http_query_expect"></span>**\_ \_ si prevede che la query http**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Recupera l'intestazione Expect, che indica se l'applicazione client deve prevedere le risposte della serie 100.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_EXPIRES"></span><span id="http_query_expires"></span>**\_scadenza della query http \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Riceve la data e l'ora in cui la risorsa deve essere considerata obsoleta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FORWARDED"></span><span id="http_query_forwarded"></span>**\_query http \_ avanzata**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Obsoleta. Gestito solo per compatibilità con le applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FROM"></span><span id="http_query_from"></span>**\_query http \_ da**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Recupera l'indirizzo di posta elettronica dell'utente che controlla l'agente utente richiedente se l'intestazione From viene assegnata.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_HOST"></span><span id="http_query_host"></span>**\_host query \_ http**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Recupera l'host Internet e il numero di porta della risorsa richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MATCH"></span><span id="http_query_if_match"></span>**\_query http \_ se \_ corrisponde**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Recupera il contenuto del If-Match campo di intestazione della richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_MODIFIED_SINCE"></span><span id="http_query_if_modified_since"></span>**\_query http \_ se \_ modificata \_ dopo**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Recupera il contenuto dell'intestazione If-Modified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_NONE_MATCH"></span><span id="http_query_if_none_match"></span>**\_query http \_ se \_ Nessuna \_ corrispondenza**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Recupera il contenuto del campo dell'intestazione della richiesta If-None-Match.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_RANGE"></span><span id="http_query_if_range"></span>**\_query http \_ se l' \_ intervallo**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Recupera il contenuto del If-Range campo di intestazione della richiesta. Questa intestazione consente all'applicazione client di verificare che l'entità correlata a una copia parziale dell'entità nella cache dell'applicazione client non sia stata aggiornata. Se l'entità non è stata aggiornata, inviare le parti mancanti nell'applicazione client. Se l'entità è stata aggiornata, inviare l'intera entità aggiornata.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_IF_UNMODIFIED_SINCE"></span><span id="http_query_if_unmodified_since"></span>**\_query http \_ se non \_ modificata \_ da**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Recupera il contenuto del campo di intestazione della richiesta If-Unmodified-Since.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LAST_MODIFIED"></span><span id="http_query_last_modified"></span>**\_ \_ Ultima modifica della query http \_**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Riceve la data e l'ora in cui il server ritiene che la risorsa sia stata modificata per ultima.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LINK"></span><span id="http_query_link"></span>**\_collegamento query \_ http**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Obsoleta. Gestito solo per compatibilità con le applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_LOCATION"></span><span id="http_query_location"></span>**\_percorso query \_ http**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Recupera il Uniform Resource Identifier assoluto (URI) utilizzato in un'intestazione di risposta della posizione.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX"></span><span id="http_query_max"></span>**\_Max query \_ http**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Non è un flag di query. Indica il valore massimo di un \_ valore di query http \_ \* .


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MAX_FORWARDS"></span><span id="http_query_max_forwards"></span>**\_ \_ numero massimo di \_ INOLTRi query http**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Recupera il numero di proxy o gateway che è in grado di inoltrare la richiesta al server in ingresso successivo.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MESSAGE_ID"></span><span id="http_query_message_id"></span>**\_ \_ ID messaggio query \_ http**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Non più supportata.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_MIME_VERSION"></span><span id="http_query_mime_version"></span>**\_ \_ versione MIME della query http \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Riceve la versione del protocollo MIME utilizzato per costruire il messaggio.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_ORIG_URI"></span><span id="http_query_orig_uri"></span>**\_ \_ URI orig della query http \_**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Obsoleta. Gestito solo per compatibilità con le applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PRAGMA"></span><span id="http_query_pragma"></span>**\_pragma query \_ http**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Riceve le direttive specifiche dell'implementazione che potrebbero essere applicabili a qualsiasi destinatario lungo la catena di richiesta/risposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHENTICATE"></span><span id="http_query_proxy_authenticate"></span>**\_ \_ autenticazione proxy query \_ http**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal proxy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_AUTHORIZATION"></span><span id="http_query_proxy_authorization"></span>**\_ \_ autorizzazione proxy query \_ http**
</dt> <dd> <dl> <dt>

61
</dt> <dt>



Recupera l'intestazione utilizzata per identificare l'utente a un proxy che richiede l'autenticazione. Questa intestazione può essere recuperata solo prima dell'invio della richiesta al server.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PROXY_CONNECTION"></span><span id="http_query_proxy_connection"></span>**\_ \_ connessione proxy query \_ http**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Recupera l'intestazione del Proxy-Connection.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_PUBLIC"></span><span id="http_query_public"></span>**\_query http \_ pubblica**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Riceve i metodi disponibili in questo server.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RANGE"></span><span id="http_query_range"></span>**\_intervallo query \_ http**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Recupera l'intervallo di byte di un'entità.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS"></span><span id="http_query_raw_headers"></span>**\_ \_ intestazioni RAW della query http \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Riceve tutte le intestazioni restituite dal server. Ogni intestazione viene terminata con " \\ 0". Un " \\ 0" aggiuntivo termina l'elenco di intestazioni.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RAW_HEADERS_CRLF"></span><span id="http_query_raw_headers_crlf"></span>**\_intestazioni RAW della query http \_ \_ \_ CRLF**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Riceve tutte le intestazioni restituite dal server. Ogni intestazione è separata da una sequenza di ritorno a capo/avanzamento riga (CR/LF).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFERER"></span><span id="http_query_referer"></span>**\_ \_ Referer query http**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Riceve il Uniform Resource Identifier (URI) della risorsa in cui è stato ottenuto l'URI richiesto.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REFRESH"></span><span id="http_query_refresh"></span>**\_aggiornamento query \_ http**
</dt> <dd> <dl> <dt>

46
</dt> <dt>



Obsoleta. Gestito solo per compatibilità con le applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_REQUEST_METHOD"></span><span id="http_query_request_method"></span>**\_metodo di \_ richiesta di query http \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Riceve il verbo HTTP usato nella richiesta, in genere GET o POST.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_RETRY_AFTER"></span><span id="http_query_retry_after"></span>**\_tentativo di query http \_ \_ dopo**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Recupera l'intervallo di tempo per cui il servizio non è disponibile.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SERVER"></span><span id="http_query_server"></span>**\_server di query http \_**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Recupera i dati sul software utilizzato dal server di origine per gestire la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_SET_COOKIE"></span><span id="http_query_set_cookie"></span>**\_cookie del \_ set di query http \_**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Riceve il valore del set di cookie per la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_CODE"></span><span id="http_query_status_code"></span>**\_codice di \_ stato della query http \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Riceve il codice di stato restituito dal server. Per ulteriori informazioni e un elenco di valori possibili, vedere [**codici di stato http**](http-status-codes.md).


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_STATUS_TEXT"></span><span id="http_query_status_text"></span>**\_ \_ testo stato query \_ http**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Riceve qualsiasi testo aggiuntivo restituito dal server nella riga di risposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TITLE"></span><span id="http_query_title"></span>**\_titolo della query http \_**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Obsoleta. Gestito solo per compatibilità con le applicazioni legacy.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSFER_ENCODING"></span><span id="http_query_transfer_encoding"></span>**\_ \_ codifica trasferimento query \_ http**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Recupera il tipo di trasformazione applicato al corpo del messaggio in modo che possa essere trasferito in modo sicuro tra il mittente e il destinatario.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UNLESS_MODIFIED_SINCE"></span><span id="http_query_unless_modified_since"></span>**\_query http \_ a meno che non venga \_ modificata \_ da**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Recupera l'intestazione a meno che non venga modificata.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_UPGRADE"></span><span id="http_query_upgrade"></span>**\_aggiornamento query \_ http**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Recupera i protocolli di comunicazione aggiuntivi supportati dal server.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_URI"></span><span id="http_query_uri"></span>**\_URI query \_ http**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Riceve alcuni o tutti gli URI (Uniform Resource Identifier) in base ai quali è possibile identificare la risorsa Request-URI.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_USER_AGENT"></span><span id="http_query_user_agent"></span>**\_ \_ agente utente query \_ http**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Recupera i dati relativi all'agente utente che ha effettuato la richiesta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VARY"></span><span id="http_query_vary"></span>**\_variazione query \_ http**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Recupera l'intestazione che indica che l'entità è stata selezionata da un numero di rappresentazioni disponibili della risposta mediante la negoziazione basata su server.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VERSION"></span><span id="http_query_version"></span>**\_versione query \_ http**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Riceve l'ultimo codice di risposta restituito dal server.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_VIA"></span><span id="http_query_via"></span>**\_query http \_ tramite**
</dt> <dd> <dl> <dt>

66
</dt> <dt>



Recupera i protocolli intermedi e i destinatari tra l'agente utente e il server nelle richieste e tra il server di origine e il client sulle risposte.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WARNING"></span><span id="http_query_warning"></span>**\_avviso query \_ http**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Recupera dati aggiuntivi sullo stato di una risposta che potrebbero non essere riflesse dal codice di stato della risposta.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_WWW_AUTHENTICATE"></span><span id="http_query_www_authenticate"></span>**\_ \_ autenticazione www della query http \_**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Recupera lo schema di autenticazione e l'area di autenticazione restituiti dal server.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_CONTENT_TYPE_OPTIONS"></span><span id="http_query_x_content_type_options"></span>**\_Opzioni del \_ \_ tipo di contenuto query HTTP X \_ \_**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Recupera il valore dell'intestazione X-Content-Type-Options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_P3P"></span><span id="http_query_p3p"></span>**\_P3P query \_ http**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Recupera il valore dell'intestazione P3P.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_P2P_PEERDIST"></span><span id="http_query_x_p2p_peerdist"></span>**\_Query http \_ X \_ \_ PEERDIST P2P**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Recupera il valore dell'intestazione X-P2P-PeerDist.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_TRANSLATE"></span><span id="http_query_translate"></span>**\_traduzione query \_ http**
</dt> <dd> <dl> <dt>

82
</dt> <dt>



Recupera il valore dell'intestazione translate.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_UA_COMPATIBLE"></span><span id="http_query_x_ua_compatible"></span>**\_compatibilità con query http \_ X \_ UA \_**
</dt> <dd> <dl> <dt>

83
</dt> <dt>



Recupera il valore dell'intestazione X-UA-Compatible.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_DEFAULT_STYLE"></span><span id="http_query_default_style"></span>**\_ \_ stile predefinito query \_ http**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Recupera il valore dell'intestazione Default-Style.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_FRAME_OPTIONS"></span><span id="http_query_x_frame_options"></span>**\_ \_ \_ Opzioni frame X query \_ http**
</dt> <dd> <dl> <dt>

85
</dt> <dt>



Recupera il valore dell'intestazione X-frame-options.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_X_XSS_PROTECTION"></span><span id="http_query_x_xss_protection"></span>**\_protezione XSS della query http \_ X \_ \_**
</dt> <dd> <dl> <dt>

86
</dt> <dt>



Recupera il valore dell'intestazione X-XSS-Protection.


</dt> </dl> </dd> </dl>

I flag di modifica vengono utilizzati in combinazione con un flag di attributo per modificare la richiesta. I flag di modifica possono modificare il formato dei dati restituiti o indicare dove [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) (o [**QueryInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774972(v=vs.85))) deve cercare i dati.

<dl> <dt>

<span id="HTTP_QUERY_FLAG_COALESCE"></span><span id="http_query_flag_coalesce"></span>**\_flag di query http \_ \_ COALESCE**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_NUMBER"></span><span id="http_query_flag_number"></span>**\_numero di \_ flag della query http \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Restituisce i dati come numero a 32 bit per le intestazioni il cui valore è un numero, ad esempio il codice di stato.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_REQUEST_HEADERS"></span><span id="http_query_flag_request_headers"></span>**\_intestazioni di \_ richiesta del flag di query http \_ \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Solo intestazioni della richiesta di query.


</dt> </dl> </dd> <dt>

<span id="HTTP_QUERY_FLAG_SYSTEMTIME"></span><span id="http_query_flag_systemtime"></span>**\_flag di query http \_ \_ SYSTEMTIME**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Restituisce il valore dell'intestazione come struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , che non richiede l'analisi dei dati da parte dell'applicazione. Utilizzare per le intestazioni il cui valore è una stringa di data/ora, ad esempio "Last-Modified-Time".


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



 

