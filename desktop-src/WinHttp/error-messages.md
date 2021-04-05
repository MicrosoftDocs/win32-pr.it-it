---
description: I valori di errore identificati in questo argomento vengono restituiti da GetLastError quando una delle funzioni di servizi HTTP di Microsoft Windows (WinHTTP) ha esito negativo.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Messaggi di errore (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882877"
---
# <a name="error-messages-winhttph"></a>Messaggi di errore (WinHTTP. h)

I valori di errore elencati di seguito vengono restituiti da [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando una delle funzioni di servizi HTTP di Microsoft Windows (WinHTTP) ha esito negativo e vengono restituite anche nei 16 bit inferiori di [**HRESULT**](../com/structure-of-com-error-codes.md) restituiti dall'oggetto [**WinHttpRequest**](winhttprequest.md) .

I valori di errore i cui nomi iniziano con "ERROR \_ WinHTTP \_ " sono specifici delle funzioni WinHTTP. Le funzioni WinHTTP restituiscono anche messaggi di errore di Windows laddove appropriato.

<dl> <dt>

<span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**errore \_ del \_ \_ servizio proxy \_ automatico \_ WinHTTP**
</dt> <dd> <dl> <dt>

12178
</dt> <dt>



Restituito da [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) quando non è possibile trovare un proxy per l'URL specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERRORE \_ di \_ rilevamento automatico WinHTTP \_ non riuscito**
</dt> <dd> <dl> <dt>

12180
</dt> <dt>



Restituito da [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) se WinHTTP non è stato in grado di individuare l'URL del file di configurazione automatica del proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERRORE \_ WinHTTP \_ \_ \_ script proxy auto \_ errato**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Si è verificato un errore durante l'esecuzione del codice di script nel file di configurazione automatica del proxy (PAC).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ chiamare \_ dopo l' \_ apertura**
</dt> <dd> <dl> <dt>

12103
</dt> <dt>



Restituito dall'oggetto [**HttpRequest**](winhttprequest.md) se non è possibile richiedere un'opzione specificata dopo che è stato chiamato il metodo [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ chiamare \_ dopo l' \_ INVIO**
</dt> <dd> <dl> <dt>

12102
</dt> <dt>



Restituito dall'oggetto [**HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta dopo la chiamata al metodo [**Send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ chiamare \_ prima dell' \_ apertura**
</dt> <dd> <dl> <dt>

12100
</dt> <dt>



Restituito dall'oggetto [**HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta prima di chiamare il metodo [**Open**](iwinhttprequest-open.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ chiamare \_ prima dell' \_ INVIO**
</dt> <dd> <dl> <dt>

12101
</dt> <dt>



Restituito dall'oggetto [**HttpRequest**](winhttprequest.md) se non è possibile eseguire un'operazione richiesta prima di chiamare il metodo [**Send**](iwinhttprequest-send.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERRORE \_ WinHTTP \_ non è in grado di \_ connettersi**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Restituito se la connessione al server non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRORE \_ \_ \_ certificato autenticazione client \_ WinHTTP \_ necessario**
</dt> <dd> <dl> <dt>



Il server richiede l'autenticazione client SSL. L'applicazione recupera l'elenco di autorità di certificazione chiamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione **WinHTTP \_ opzione \_ client \_ CERT \_ Issuer \_ List** . Per ulteriori informazioni, vedere l'opzione **WinHTTP opzione \_ \_ client \_ CERT \_ Issuer \_ List** .

Se il server richiede il certificato client, ma non lo richiede, l'applicazione può chiamare alternativamente [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione del contesto del certificato **client dell' \_ opzione \_ \_ \_ WinHTTP** . In questo caso, l'applicazione specifica la \_ macro del \_ contesto del certificato client WinHTTP nessuna \_ \_ nel parametro *lpBuffer* di **WinHttpSetOption**. Per ulteriori informazioni, vedere l'opzione di **\_ \_ \_ \_ contesto certificato client opzione WinHTTP** .

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERRORE \_ del \_ certificato client WinHTTP \_ \_ senza \_ accesso \_ \_ chiave privata**
</dt> <dd> <dl> <dt>



L'applicazione non dispone dei privilegi necessari per accedere alla chiave privata associata al certificato client.

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERRORE \_ del \_ certificato client WinHTTP \_ \_ senza \_ \_ chiave privata**
</dt> <dd> <dl> <dt>



Al contesto del certificato client SSL non è associata alcuna chiave privata. Il certificato client potrebbe essere stato importato nel computer senza la chiave privata.

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERRORE \_ di \_ dimensioni dell' \_ intestazione di codifica in blocchi WinHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>

12183
</dt> <dt>



Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando viene rilevata una condizione di overflow nel corso dell'analisi della codifica Chunked.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRORE \_ \_ \_ certificato autenticazione client \_ WinHTTP \_ necessario**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando il server richiede l'autenticazione client.

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo errore non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**errore \_ di \_ connessione WinHTTP errore \_**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La connessione al server è stata reimpostata o terminata oppure è stato rilevato un protocollo SSL incompatibile. Ad esempio, WinHTTP versione 5,1 non supporta SSL2, a meno che il client non lo consenta in modo specifico.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**l' \_ intestazione WinHTTP dell'errore \_ \_ \_ esiste già**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Obsoleto non più utilizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERRORE \_ \_ numero intestazioni \_ WinHTTP \_ superate**
</dt> <dd> <dl> <dt>

12181
</dt> <dt>



Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando un numero maggiore di intestazioni era presente in una risposta che WinHTTP poteva ricevere.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERRORE \_ di \_ intestazione WinHTTP \_ non \_ trovata**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Impossibile trovare l'intestazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**\_ \_ \_ overflow dimensioni intestazione WinHTTP \_ errore**
</dt> <dd> <dl> <dt>

12182
</dt> <dt>



Restituito da [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando le dimensioni delle intestazioni ricevute superano il limite per l'handle della richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERRORE \_ WinHTTP \_ \_ stato di handle errato \_**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Non è possibile eseguire l'operazione richiesta perché l'handle specificato non è nello stato corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERRORE \_ WinHTTP \_ \_ tipo di handle errato \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Il tipo di handle fornito non è corretto per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**errore \_ interno WinHTTP errore \_ \_**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Si è verificato un errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERRORE \_ WinHTTP \_ opzione non valida \_**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Una richiesta a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ha specificato un valore di opzione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERRORE \_ WinHTTP \_ \_ richiesta di query non valida \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



Obsoleto non più utilizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERRORE \_ WinHTTP \_ \_ risposta server non valida \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Impossibile analizzare la risposta del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERRORE \_ WinHTTP \_ non valido \_**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



URL non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**errore \_ di \_ accesso WinHTTP errore \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



Tentativo di accesso non riuscito. Quando si verifica questo errore, l'handle della richiesta deve essere chiuso con [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle). Prima di ritentare la funzione che ha generato questo errore, è necessario creare un nuovo handle di richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERRORE \_ \_ nome WinHTTP \_ non \_ risolto**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Il nome del server non può essere risolto.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERRORE \_ WinHTTP \_ non \_ inizializzato**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Obsoleto non più utilizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERRORE \_ WinHTTP \_ operazione \_ annullata**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



L'operazione è stata annullata, in genere perché l'handle su cui era in funzione la richiesta è stato chiuso prima del completamento dell'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**\_opzione WinHTTP di errore \_ \_ non \_ impostabile**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



Impossibile impostare l'opzione richiesta, solo query.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERRORE \_ WinHTTP \_ \_ di \_ handle**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Obsoleto non più utilizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERRORE \_ di \_ Reindirizzamento WinHTTP \_ non riuscito**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Il reindirizzamento non è riuscito perché lo schema è stato modificato o tutti i tentativi di reindirizzamento non sono riusciti (il valore predefinito è cinque tentativi).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERRORE WinHTTP-invia di nuovo la \_ \_ \_ richiesta**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



Funzione WinHTTP non riuscita. È possibile ritentare la funzione desiderata nello stesso handle di richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**\_ \_ \_ overflow svuotamento risposta WinHTTP \_ errore**
</dt> <dd> <dl> <dt>

12184
</dt> <dt>



Restituito quando una risposta in ingresso supera un limite di dimensioni WinHTTP interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**errore \_ di \_ esecuzione dello script WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12177
</dt> <dt>



Si è verificato un errore durante l'esecuzione di uno script.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERRORE \_ WinHTTP \_ Secure \_ Certificate \_ NC \_ non valido**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Restituito quando il nome CN di un certificato non corrisponde al valore passato (equivalente a un errore di **\_ \_ \_ non \_ corrispondenza di CERT E CN** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERRORE \_ WinHTTP \_ \_ certificato sicuro \_ data \_ non valido**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



Indica che un certificato richiesto non rientra nel periodo di validità durante la verifica in base al clock di sistema corrente o al timestamp nel file firmato oppure che i periodi di validità della catena di certificazione non vengono annidati correttamente (equivalente a un certificato **\_ e \_ scaduto** o a un errore **\_ \_ VALIDITYPERIODNESTING del certificato** ).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERRORE \_ WinHTTP \_ Secure \_ CERT \_ rev \_ non riuscito**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Indica che non è possibile controllare la revoca perché il server di revoca è offline (equivalente **alla \_ revoca E alla \_ revoca \_ offline**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERRORE \_ WinHTTP \_ Secure \_ CERT \_ revocato**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Indica che un certificato è stato revocato (equivalente alla **crittografia \_ E \_ revocata**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**errore durante l'utilizzo del \_ \_ \_ certificato sicuro WinHTTP \_ \_**
</dt> <dd> <dl> <dt>

12179
</dt> <dt>



Indica che un certificato non è valido per l'utilizzo richiesto (equivalente a **certificato \_ E \_ \_ utilizzo errato**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**errore \_ del \_ canale sicuro WinHTTP \_ di errore \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Indica che si è verificato un errore durante l'esecuzione di un canale sicuro (equivalente ai codici di errore che iniziano con "SEC e \_ \_ " e "sec \_ i \_ " elencati nel file di intestazione "Winerror. h").


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**errore errore \_ WinHTTP \_ sicuro \_**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



Il certificato Secure Sockets Layer (SSL) inviato dal server sono stati rilevati uno o più errori. Per determinare il tipo di errore rilevato, verificare la presenza di una notifica di [**\_ \_ \_ \_ errore di stato di callback WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) in una funzione di callback dello stato. Per ulteriori informazioni, vedere [**\_ \_ callback di stato WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERRORE \_ WinHTTP \_ Secure \_ CA non valida \_**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



Indica che una catena di certificati è stata elaborata, ma terminata in un certificato radice non attendibile dal provider di attendibilità (equivalente a **CERT \_ E \_ UNTRUSTEDROOT**).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERRORE \_ WinHTTP \_ Secure \_ certificato non valido \_**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Indica che un certificato non è valido (equivalente a errori quali **CERT \_ e \_ Role**, **CERT \_ e \_ PATHLENCONST**, **CERT \_ e \_ Critical**, **certificate e \_ \_ purpose**, **CERT \_ e \_ ISSUERCHAINING**, CERT e non **\_ \_ valido** e il **\_ \_ concatenamento di CERT** e).


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERRORE \_ di \_ arresto WinHTTP**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



Il supporto della funzione WinHTTP viene arrestato o scaricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**\_Timeout WinHTTP \_ errore**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Timeout della richiesta.

Questo errore può essere restituito come risultato del comportamento del timeout TCP/IP, indipendentemente dai valori di timeout impostati nei servizi HTTP di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERRORE \_ WinHTTP \_ Impossibile \_ \_ scaricare \_ lo script**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Non è possibile scaricare il file PAC. Ad esempio, il server a cui fa riferimento l'URL PAC potrebbe non essere raggiungibile o il server ha restituito una risposta 404 non trovata.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERRORE \_ WinHTTP \_ tipo di script non gestito \_ \_**
</dt> <dd> <dl> <dt>

12176
</dt> <dt>



Il tipo di script non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**\_schema errore WinHTTP non \_ riconosciuto \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



L'URL ha specificato uno schema diverso da "http:" o "https:".


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRORE \_ di \_ memoria insufficiente \_**
</dt> <dd> <dl> <dt>



Memoria insufficiente per completare l'operazione richiesta.

**Intestazione:** Dichiarata in Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRORE \_ buffer insufficiente \_**
</dt> <dd> <dl> <dt>



La dimensione, in byte, del buffer fornito a una funzione non è sufficiente per contenere i dati restituiti. Per ulteriori informazioni, vedere la funzione specifica.

**Intestazione:** Dichiarata in Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERRORE \_ handle non valido \_**
</dt> <dd> <dl> <dt>



L'handle passato al Application Programming Interface (API) è stato invalidato o chiuso.

**Intestazione:** Dichiarata in Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRORE \_ nessun \_ altro \_ file**
</dt> <dd> <dl> <dt>



Non sono stati trovati altri file.

**Intestazione:** Dichiarata in Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRORE \_ nessun \_ altro \_ elemento**
</dt> <dd> <dl> <dt>



Non sono stati trovati altri elementi.

**Intestazione:** Dichiarata in Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRORE \_ non \_ supportato**
</dt> <dd> <dl> <dt>



Lo stack di protocolli richiesto non è caricato e l'applicazione non può avviare WinSock.

**Intestazione:** Dichiarata in Winerror. h


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Intestazione<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

