---
description: I valori di errore identificati in questo argomento vengono restituiti da GetLastError quando una delle funzioni di Microsoft Windows HTTP Services (WinHTTP) ha esito negativo.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Messaggi di errore (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d83fa1859f071b0fc0e651235deea51626f55b8a45cdb2a3ea8736a57317741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744717"
---
# <a name="error-messages-winhttph"></a>Messaggi di errore (Winhttp.h)

I valori di errore elencati di seguito vengono restituiti da [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando una delle funzioni di Microsoft Windows HTTP Services (WinHTTP) ha esito negativo e vengono restituiti anche nei 16 bit inferiori di errori [**HRESULT**](../com/structure-of-com-error-codes.md) restituiti dall'oggetto [**WinHttpRequest.**](winhttprequest.md)

I valori di errore i cui nomi iniziano con "ERROR \_ \_ WINHTTP" sono specifici delle funzioni WinHTTP. Le funzioni WinHTTP restituiscono anche Windows di errore, se appropriato.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERRORE \_ DEL SERVIZIO \_ \_ PROXY \_ AUTOMATICO WINHTTP \_**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Restituito [**da WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) quando non è possibile trovare un proxy per l'URL specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERRORE \_ WINHTTP \_ AUTODETECTION \_ FAILED**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Restituito [**da WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) se WinHTTP non è stato in grado di individuare l'URL del file di configurazione automatica del proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERRORE \_ WINHTTP \_ BAD AUTO PROXY \_ \_ \_ SCRIPT**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Si è verificato un errore durante l'esecuzione del codice di script nel file pac (Proxy Auto-Configuration).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERRORE \_ WINHTTP \_ NON PUÒ CHIAMARE \_ DOPO \_ \_ L'APERTURA**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Restituito [**dall'oggetto HttpRequest**](winhttprequest.md) se un'opzione specificata non può essere richiesta dopo la [**chiamata**](iwinhttprequest-open.md) al metodo Open.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERRORE \_ WINHTTP \_ NON PUÒ CHIAMARE \_ DOPO \_ \_ L'INVIO**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Restituito [**dall'oggetto HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta dopo la chiamata [**al metodo Send.**](iwinhttprequest-send.md)


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERRORE \_ WINHTTP \_ NON PUÒ CHIAMARE \_ PRIMA \_ \_ DELL'APERTURA**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Restituito [**dall'oggetto HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta prima di chiamare il [**metodo Open.**](iwinhttprequest-open.md)


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERRORE \_ WINHTTP \_ NON PUÒ CHIAMARE \_ PRIMA \_ \_ DELL'INVIO**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Restituito [**dall'oggetto HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta prima di chiamare il [**metodo Send.**](iwinhttprequest-send.md)


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERRORE \_ WINHTTP \_ NON È IN GRADO DI \_ CONNETTERSI**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Restituito se la connessione al server non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRORE \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED**
</dt> <dd> <dl> <dt>



Il server richiede l'autenticazione client SSL. L'applicazione recupera l'elenco di autorità di certificazione chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con **l'opzione WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ ISSUER \_ LIST.** Per altre informazioni, vedere **l'opzione WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ ISSUER \_ LIST.**

Se il server richiede il certificato client, ma non lo richiede, l'applicazione può chiamare in alternativa [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.** In questo caso, l'applicazione specifica la macro WINHTTP NO CLIENT CERT CONTEXT nel \_ \_ parametro \_ \_ *lpBuffer* **di WinHttpSetOption**. Per altre informazioni, vedere **l'opzione \_ WINHTTP OPTION \_ CLIENT \_ CERT \_ CONTEXT.**

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERRORE \_ WINHTTP \_ CLIENT \_ CERT NO ACCESS PRIVATE \_ \_ \_ \_ KEY**
</dt> <dd> <dl> <dt>



L'applicazione non dispone dei privilegi necessari per accedere alla chiave privata associata al certificato client.

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERRORE \_ WINHTTP \_ CLIENT \_ CERT NO PRIVATE \_ \_ \_ KEY**
</dt> <dd> <dl> <dt>



Al contesto per il certificato client SSL non è associata una chiave privata. Il certificato client potrebbe essere stato importato nel computer senza la chiave privata.

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERRORE \_ WINHTTP \_ CHUNKED \_ ENCODING HEADER \_ \_ SIZE \_ OVERFLOW**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Restituito [**da WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando viene rilevata una condizione di overflow durante l'analisi della codifica in blocchi.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRORE \_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando il server richiede l'autenticazione client.

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERRORE \_ DI CONNESSIONE WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La connessione con il server è stata reimpostata o terminata oppure è stato rilevato un protocollo SSL incompatibile. Ad esempio, WinHTTP versione 5.1 non supporta SSL2 a meno che il client non lo a abilita in modo specifico.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**\_L'INTESTAZIONE WINHTTP \_ DI ERRORE \_ ESISTE \_ GIÀ**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Obsoleto; non più usato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**È STATO \_ SUPERATO IL NUMERO DI INTESTAZIONI WINHTTP DI \_ \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Restituito [**da WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando in una risposta era presente un numero di intestazioni maggiore di quello che WinHTTP poteva ricevere.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**IMPOSSIBILE \_ TROVARE L'INTESTAZIONE WINHTTP \_ DI \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Impossibile trovare l'intestazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERRORE \_ WINHTTP \_ HEADER SIZE \_ \_ OVERFLOW**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Restituito [**da WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando le dimensioni delle intestazioni ricevute superano il limite per l'handle della richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERRORE \_ WINHTTP \_ STATO HANDLE NON \_ \_ CORRETTO**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Impossibile eseguire l'operazione richiesta perché l'handle fornito non è nello stato corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERRORE \_ WINHTTP \_ TIPO DI HANDLE \_ NON \_ CORRETTO**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Il tipo di handle fornito non è corretto per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERRORE \_ WINHTTP \_ ERRORE \_ INTERNO**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Si è verificato un errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**OPZIONE \_ WINHTTP \_ NON VALIDA PER \_ L'ERRORE**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Una richiesta a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ha specificato un valore di opzione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERRORE \_ WINHTTP \_ RICHIESTA DI QUERY \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Obsoleto; non più usato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERRORE \_ WINHTTP \_ RISPOSTA SERVER NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Impossibile analizzare la risposta del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERRORE \_ WINHTTP \_ URL NON \_ VALIDO**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



URL non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERRORE \_ WINHTTP \_ LOGIN FAILURE (ERRORE DI ACCESSO WINHTTP) \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Tentativo di accesso non riuscito. Quando viene rilevato questo errore, l'handle della richiesta deve essere chiuso [**con WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle). È necessario creare un nuovo handle di richiesta prima di ritentare la funzione che ha originariamente generato l'errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERRORE \_ WINHTTP \_ NAME NOT \_ \_ RESOLVED**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Impossibile risolvere il nome del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERRORE \_ WINHTTP \_ NON \_ INIZIALIZZATO**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Obsoleto; non più usato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERRORE \_ OPERAZIONE WINHTTP \_ \_ ANNULLATA**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



L'operazione è stata annullata, in genere perché l'handle su cui era in esecuzione la richiesta è stato chiuso prima del completamento dell'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERRORE \_ DELL'OPZIONE WINHTTP \_ \_ NON \_ IMPOSTABILE**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



L'opzione richiesta non può essere impostata, ma solo su cui viene eseguita una query.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERRORE \_ WINHTTP \_ OUT OF \_ \_ HANDLES**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Obsoleto; non viene più usato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERRORE \_ DI REINDIRIZZAMENTO WINHTTP \_ \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Il reindirizzamento non è riuscito perché lo schema è stato modificato o tutti i tentativi di reindirizzamento non sono riusciti (il valore predefinito è cinque tentativi).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERRORE \_ RICHIESTA DI INVIO DI NUOVO WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



La funzione WinHTTP non è riuscita. È possibile ritentare la funzione desiderata nello stesso handle di richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERRORE \_ OVERFLOW \_ SVUOTAMENTO RISPOSTA WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Restituito quando una risposta in ingresso supera un limite di dimensioni WinHTTP interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERRORE DI \_ ESECUZIONE DELLO SCRIPT WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Si è verificato un errore durante l'esecuzione di uno script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERRORE \_ WINHTTP \_ SECURE \_ CERT CN \_ \_ INVALID**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Restituito quando un nome CN del certificato non corrisponde al valore passato (equivalente a un **errore CERT \_ E CN \_ NO \_ \_ MATCH).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERRORE \_ WINHTTP \_ SECURE \_ CERT DATE \_ \_ INVALID**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Indica che un certificato richiesto non rientra nel periodo di validità durante la verifica rispetto all'orologio di sistema corrente o al timestamp nel file firmato oppure che i periodi di validità della catena di certificazione non vengono annidati correttamente (equivalente a un errore **CERT \_ E \_ EXPIRED** o **CERT \_ E \_ VALIDITYPERIODNESTING).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERRORE \_ WINHTTP \_ SECURE \_ CERT \_ REV \_ FAILED**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Indica che non è possibile controllare la revoca perché il server di revoca era offline (equivalente a **CRYPT \_ E \_ REVOCATION \_ OFFLINE).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERRORE \_ WINHTTP \_ SECURE \_ CERT \_ REVOKED**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Indica che un certificato è stato revocato (equivalente a **CRYPT \_ E \_ REVOKED).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERRORE DI \_ UTILIZZO \_ ERRATO DEL \_ CERTIFICATO SICURO \_ WINHTTP \_**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Indica che un certificato non è valido per l'utilizzo richiesto (equivalente a **CERT \_ E WRONG \_ \_ USAGE).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERRORE \_ ERRORE CANALE SICURO WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Indica che si è verificato un errore che ha a che fare con un canale sicuro (equivalente ai codici di errore che iniziano con "SEC E" e "SEC I" elencati nel file di \_ \_ intestazione \_ \_ "winerror.h").


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERRORE \_ WINHTTP \_ SECURE \_ FAILURE**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Il certificato Secure Sockets Layer (SSL) inviato dal server sono stati rilevati uno o più errori. Per determinare il tipo di errore rilevato, cercare una notifica [**WINHTTP \_ CALLBACK STATUS SECURE \_ \_ \_ FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) in una funzione di callback di stato. Per altre informazioni, vedere [**WINHTTP \_ STATUS \_ CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERRORE \_ WINHTTP \_ SECURE NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Indica che una catena di certificati è stata elaborata, ma terminata in un certificato radice non considerato attendibile dal provider di attendibilità (equivalente a **CERT \_ E \_ UNTRUSTEDROOT).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERRORE \_ WINHTTP \_ SECURE INVALID \_ \_ CERT**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Indica che un certificato non è valido (equivalente a errori come **CERT \_ E \_ ROLE,** **CERT \_ E \_ PATHLENCONST,** **CERT E \_ \_ CRITICAL,** **CERT E \_ \_ PURPOSE,** **CERT E \_ \_ ISSUERCHAINING,** **CERT E \_ \_ MALFORMED** e **CERT E \_ \_ CHAINING).**


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERRORE \_ DI ARRESTO DI WINHTTP \_**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



Il supporto della funzione WinHTTP è in fase di arresto o scaricamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERRORE \_ DI TIMEOUT WINHTTP \_**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Timeout della richiesta.

Questo errore può essere restituito come risultato del comportamento di timeout TCP/IP, indipendentemente dal valore di timeout impostato in Windows HTTP.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERRORE \_ \_ WINHTTP: IMPOSSIBILE SCARICARE LO \_ \_ \_ SCRIPT**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Non è possibile scaricare il file PAC. Ad esempio, il server a cui fa riferimento l'URL PAC potrebbe non essere raggiungibile o il server ha restituito una risposta 404 NON TROVATO.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERRORE \_ TIPO DI SCRIPT WINHTTP NON \_ \_ \_ GESTITO**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



Il tipo di script non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERRORE \_ WINHTTP \_ - SCHEMA NON \_ RICONOSCIUTO**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



L'URL ha specificato uno schema diverso da "http:" o "https:".


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRORE \_ MEMORIA \_ \_ INSUFFICIENTE**
</dt> <dd> <dl> <dt>



Memoria insufficiente per completare l'operazione richiesta.

**Intestazione:** Dichiarato in Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRORE \_ BUFFER \_ INSUFFICIENTE**
</dt> <dd> <dl> <dt>



Le dimensioni, in byte, del buffer fornito a una funzione non sono sufficienti per contenere i dati restituiti. Per altre informazioni, vedere la funzione specifica.

**Intestazione:** Dichiarato in Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERRORE \_ HANDLE NON \_ VALIDO**
</dt> <dd> <dl> <dt>



L'handle passato all'API (Application Programming Interface) è stato invalidato o chiuso.

**Intestazione:** Dichiarato in Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRORE \_ NESSUN \_ ALTRO \_ FILE**
</dt> <dd> <dl> <dt>



Non sono stati trovati altri file.

**Intestazione:** Dichiarato in Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRORE \_ NESSUN \_ ALTRO \_ ELEMENTO**
</dt> <dd> <dl> <dt>



Non sono stati trovati altri elementi.

**Intestazione:** Dichiarato in Winerror.h


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRORE \_ NON \_ SUPPORTATO**
</dt> <dd> <dl> <dt>



Lo stack di protocolli richiesto non viene caricato e l'applicazione non può avviare WinSock.

**Intestazione:** Dichiarato in Winerror.h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHttp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server solo con app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Intestazione<br/>                   | <dl> <dt>Winhttp.h</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

