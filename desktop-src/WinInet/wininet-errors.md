---
title: Messaggi di errore (WinInet. h)
description: Le funzioni WinINet restituiscono i codici di errore laddove appropriato. Gli errori seguenti sono specifici delle funzioni WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121623"
---
# <a name="error-messages-winineth"></a>Messaggi di errore (WinInet. h)

Le funzioni WinINet restituiscono i codici di errore laddove appropriato. Gli errori seguenti sono specifici delle funzioni WinINet.

<dl> <dt>

<span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERRORE \_ FTP \_ eliminato**
</dt> <dd> <dl> <dt>

12111
</dt> <dt>



Operazione FTP non completata perché la sessione è stata interrotta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERRORE \_ FTP \_ Nessuna \_ \_ modalità passiva**
</dt> <dd> <dl> <dt>

12112
</dt> <dt>



La modalità passiva non è disponibile nel server.


</dt> </dl> </dd> <dt>

<span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERRORE \_ \_ trasferimento FTP \_ in \_ corso**
</dt> <dd> <dl> <dt>

12110
</dt> <dt>



Impossibile eseguire l'operazione richiesta sull'handle della sessione FTP perché è già in corso un'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERRORE \_ Gopher \_ attributo \_ non \_ trovato**
</dt> <dd> <dl> <dt>

12137
</dt> <dt>



Impossibile trovare l'attributo richiesto.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**errore \_ dati Gopher errore \_ \_**
</dt> <dd> <dl> <dt>

12132
</dt> <dt>



È stato rilevato un errore durante la ricezione di dati dal server gopher.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERRORE \_ \_ di fine \_ dei \_ dati in Gopher**
</dt> <dd> <dl> <dt>

12133
</dt> <dt>



È stata raggiunta la fine dei dati.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**\_tipo di \_ \_ localizzatore errato Gopher \_ errore**
</dt> <dd> <dl> <dt>

12135
</dt> <dt>



Il tipo di localizzatore non è corretto per questa operazione.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERRORE \_ Gopher \_ non valido del \_ localizzatore**
</dt> <dd> <dl> <dt>

12134
</dt> <dt>



Il localizzatore specificato non è valido.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERRORE \_ Gopher \_ non \_ file**
</dt> <dd> <dl> <dt>

12131
</dt> <dt>



La richiesta deve essere eseguita per un localizzatore di file.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERRORE \_ Gopher \_ non \_ Gopher \_ Plus**
</dt> <dd> <dl> <dt>

12136
</dt> <dt>



L'operazione richiesta può essere eseguita solo su un gopher + server o con un localizzatore che specifica un'operazione di gopher +.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**errore \_ del \_ protocollo Gopher errore \_**
</dt> <dd> <dl> <dt>

12130
</dt> <dt>



È stato rilevato un errore durante l'analisi dei dati restituiti dal server gopher.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERRORE \_ Gopher \_ Unknown \_ Locator**
</dt> <dd> <dl> <dt>

12138
</dt> <dt>



Il tipo di localizzatore è sconosciuto.

> [!Note]  
> Windows XP e Windows Server 2003 R2 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERRORE \_ \_ cookie HTTP \_ rifiutato**
</dt> <dd> <dl> <dt>

12162
</dt> <dt>



Il cookie HTTP è stato rifiutato dal server.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERRORE \_ del \_ cookie HTTP necessario per la \_ \_ conferma**
</dt> <dd> <dl> <dt>

12161
</dt> <dt>



Il cookie HTTP richiede la conferma.

> [!Note]  
> Windows Vista e Windows Server 2008 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERRORE \_ http \_ server di livello inferiore \_**
</dt> <dd> <dl> <dt>

12151
</dt> <dt>



Il server non ha restituito intestazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**l' \_ \_ intestazione HTTP \_ Error \_ esiste già**
</dt> <dd> <dl> <dt>

12155
</dt> <dt>



Non è stato possibile aggiungere l'intestazione perché esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_ \_ \_ Impossibile trovare l'intestazione HTTP dell'errore \_**
</dt> <dd> <dl> <dt>

12150
</dt> <dt>



Non è stato possibile trovare l'intestazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERRORE \_ http \_ intestazione non valida \_**
</dt> <dd> <dl> <dt>

12153
</dt> <dt>



L'intestazione specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERRORE \_ http \_ \_ richiesta di query non valida \_**
</dt> <dd> <dl> <dt>

12154
</dt> <dt>



La richiesta effettuata a [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERRORE \_ http \_ \_ risposta server non valida \_**
</dt> <dd> <dl> <dt>

12152
</dt> <dt>



Non è stato possibile analizzare la risposta del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERRORE \_ http \_ non \_ reindirizzato**
</dt> <dd> <dl> <dt>

12160
</dt> <dt>



La richiesta HTTP non è stata reindirizzata.


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERRORE \_ di \_ Reindirizzamento HTTP \_ non riuscito**
</dt> <dd> <dl> <dt>

12156
</dt> <dt>



Il reindirizzamento non è riuscito perché lo schema è stato modificato (ad esempio, da HTTP a FTP) o tutti i tentativi di reindirizzamento non sono riusciti (il valore predefinito è cinque tentativi).


</dt> </dl> </dd> <dt>

<span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERRORE \_ di \_ Reindirizzamento HTTP \_ necessario \_ conferma**
</dt> <dd> <dl> <dt>

12168
</dt> <dt>



Il reindirizzamento richiede la conferma dell'utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERRORE \_ \_ thread asincrono \_ Internet \_ non riuscito**
</dt> <dd> <dl> <dt>

12047
</dt> <dt>



L'applicazione non è in grado di avviare un thread asincrono.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERRORE \_ Internet \_ \_ \_ script proxy auto \_ errato**
</dt> <dd> <dl> <dt>

12166
</dt> <dt>



Si è verificato un errore nello script di configurazione automatica del proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERRORE \_ di \_ \_ lunghezza dell'opzione Internet errato \_**
</dt> <dd> <dl> <dt>

12010
</dt> <dt>



La lunghezza di un'opzione fornita a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) non è corretta per il tipo di opzione specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERRORE \_ Internet \_ \_ parametro registro di sistema non valido \_**
</dt> <dd> <dl> <dt>

12022
</dt> <dt>



È stato individuato un valore del registro di sistema obbligatorio, ma è un tipo errato o ha un valore non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERRORE \_ Internet \_ non in grado di \_ connettersi**
</dt> <dd> <dl> <dt>

12029
</dt> <dt>



Tentativo di connessione al server non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERRORE \_ Internet \_ CHG \_ Post \_ \_ non è \_ sicuro**
</dt> <dd> <dl> <dt>

12042
</dt> <dt>



L'applicazione sta inviando e tentando di modificare più righe di testo in un server non protetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERRORE \_ \_ \_ certificato autenticazione client \_ Internet \_ necessario**
</dt> <dd> <dl> <dt>

12044
</dt> <dt>



Il server richiede l'autenticazione client.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERRORE \_ di \_ autenticazione client Internet \_ \_ non \_ impostata**
</dt> <dd> <dl> <dt>

12046
</dt> <dt>



L'autorizzazione client non è configurata nel computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERRORE \_ di \_ connessione Internet \_ interrotta**
</dt> <dd> <dl> <dt>

12030
</dt> <dt>



La connessione al server è stata terminata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERRORE \_ di \_ reimpostazione della connessione Internet \_**
</dt> <dd> <dl> <dt>

12031
</dt> <dt>



La connessione al server è stata reimpostata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERRORE \_ di \_ decodifica Internet \_ non riuscita**
</dt> <dd> <dl> <dt>

12175
</dt> <dt>



WinINet non è riuscito a eseguire la decodifica del contenuto nella risposta. Per ulteriori informazioni, vedere l'argomento relativo alla [**codifica del contenuto**](content-encoding.md) .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**\_finestra di dialogo errore Internet \_ \_ in sospeso**
</dt> <dd> <dl> <dt>

12049
</dt> <dt>



Un altro thread ha una finestra di dialogo password in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERRORE \_ Internet \_ disconnesso**
</dt> <dd> <dl> <dt>

12163
</dt> <dt>



La connessione Internet è stata persa.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**errore \_ Internet \_ esteso \_ errore**
</dt> <dd> <dl> <dt>

12003
</dt> <dt>



Il server ha restituito un errore esteso. Si tratta in genere di una stringa o di un buffer contenente un messaggio di errore dettagliato. Chiamare [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) per recuperare il testo dell'errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERRORE \_ Internet \_ DUETOSECURITYCHECK non riuscito \_**
</dt> <dd> <dl> <dt>

12171
</dt> <dt>



La funzione non è riuscita a causa di un controllo di sicurezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERRORE \_ Internet \_ Force \_ retry**
</dt> <dd> <dl> <dt>

12032
</dt> <dt>



La funzione deve ripetere la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERRORE \_ Internet \_ fortezza \_ login \_ necessario**
</dt> <dd> <dl> <dt>

12054
</dt> <dt>



La risorsa richiesta richiede l'autenticazione della fortezza.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERRORE \_ \_ handle Internet \_ esistente**
</dt> <dd> <dl> <dt>

12036
</dt> <dt>



La richiesta non è riuscita perché l'handle esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERRORE \_ \_ da http \_ a HTTPS da Internet a \_ \_ \_ redir**
</dt> <dd> <dl> <dt>

12039
</dt> <dt>



L'applicazione sta migrando da un non SSL a una connessione SSL a causa di un reindirizzamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERRORE \_ Internet \_ https \_ http \_ Submit \_**
</dt> <dd> <dl> <dt>

12052
</dt> <dt>



I dati inviati a una connessione SSL vengono reindirizzati a una connessione non SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERRORE \_ \_ da Internet https \_ a \_ http \_ in \_ redir**
</dt> <dd> <dl> <dt>

12040
</dt> <dt>



L'applicazione sta migrando da un SSL a una connessione non SSL a causa di un reindirizzamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERRORE \_ nel \_ formato Internet errato \_**
</dt> <dd> <dl> <dt>

12027
</dt> <dt>



Il formato della richiesta non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERRORE \_ Internet \_ \_ handle errato \_ stato**
</dt> <dd> <dl> <dt>

12019
</dt> <dt>



Non è possibile eseguire l'operazione richiesta perché l'handle specificato non è nello stato corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERRORE \_ di \_ \_ tipo handle Internet errato \_**
</dt> <dd> <dl> <dt>

12018
</dt> <dt>



Il tipo di handle fornito non è corretto per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERRORE \_ di \_ Internet \_ password errata**
</dt> <dd> <dl> <dt>

12014
</dt> <dt>



Non è stato possibile completare la richiesta di connessione e accesso a un server FTP perché la password specificata non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERRORE \_ \_ \_ nome utente Internet errato \_**
</dt> <dd> <dl> <dt>

12013
</dt> <dt>



Non è stato possibile completare la richiesta di connessione e accesso a un server FTP perché il nome utente specificato non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERRORE in \_ Internet \_ Insert \_ CDROM**
</dt> <dd> <dl> <dt>

12053
</dt> <dt>



La richiesta richiede l'inserimento di un CD-ROM nell'unità CD-ROM per individuare la risorsa richiesta.

> [!Note]  
> Windows Vista e Windows Server 2008 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**errore \_ \_ interno Internet \_ errore**
</dt> <dd> <dl> <dt>

12004
</dt> <dt>



Si è verificato un errore interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERRORE \_ Internet \_ CA non valida \_**
</dt> <dd> <dl> <dt>

12045
</dt> <dt>



La funzione non ha familiarità con l'autorità di certificazione che ha generato il certificato del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERRORE \_ Internet \_ operazione non valida \_**
</dt> <dd> <dl> <dt>

12016
</dt> <dt>



L'operazione richiesta non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERRORE \_ Internet \_ opzione non valida \_**
</dt> <dd> <dl> <dt>

12009
</dt> <dt>



Una richiesta a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) ha specificato un valore di opzione non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERRORE \_ di \_ \_ richiesta proxy Internet non valida \_**
</dt> <dd> <dl> <dt>

12033
</dt> <dt>



La richiesta al proxy non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERRORE \_ \_ URL Internet non valido \_**
</dt> <dd> <dl> <dt>

12005
</dt> <dt>



L'URL non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERRORE \_ \_ elemento Internet \_ non \_ trovato**
</dt> <dd> <dl> <dt>

12028
</dt> <dt>



Impossibile trovare l'elemento richiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**errore \_ di \_ accesso Internet errore \_**
</dt> <dd> <dl> <dt>

12015
</dt> <dt>



La richiesta di connessione e accesso a un server FTP non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**errore \_ di \_ accesso Internet errore \_ \_ visualizzazione \_ \_ corpo entità**
</dt> <dd> <dl> <dt>

12174
</dt> <dt>



Il MS-Logoff intestazione digest è stato restituito dal sito Web. Questa intestazione indica in modo specifico al pacchetto digest di ripulire le credenziali per l'area di autenticazione associata. Questo errore viene restituito solo se è stata impostata l'opzione del [ \_ \_ \_ \_ \_ \_ \_ corpo dell'entità Visualizza errore di accesso alla maschera di errore Internet](option-flags.md) ; in caso contrario, viene restituito un errore di **\_ \_ accesso \_ a Internet** .


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERRORE di \_ sicurezza di Internet \_ mista \_**
</dt> <dd> <dl> <dt>

12041
</dt> <dt>



Il contenuto non è interamente sicuro. Parte del contenuto visualizzato potrebbe provenire da server non protetti.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERRORE \_ \_ nome Internet \_ non \_ risolto**
</dt> <dd> <dl> <dt>

12007
</dt> <dt>



Non è stato possibile risolvere il nome del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERRORE \_ Internet \_ necessario \_ MSN \_ SSPI SSPI \_**
</dt> <dd> <dl> <dt>

12173
</dt> <dt>



Non implementato attualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERRORE \_ Internet \_ richiesta \_ interfaccia utente**
</dt> <dd> <dl> <dt>

12034
</dt> <dt>



È stata richiesta un'interfaccia utente o un'altra operazione di blocco.

> [!Note]  
> Windows Vista e Windows Server 2008 e versioni precedenti.

 


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERRORE \_ Internet \_ senza \_ callback**
</dt> <dd> <dl> <dt>

12025
</dt> <dt>



Impossibile effettuare una richiesta asincrona perché una funzione di callback non è stata impostata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERRORE \_ Internet \_ senza \_ contesto**
</dt> <dd> <dl> <dt>

12024
</dt> <dt>



Impossibile effettuare una richiesta asincrona perché è stato specificato un valore di contesto zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERRORE \_ Internet \_ senza \_ \_ accesso diretto**
</dt> <dd> <dl> <dt>

12023
</dt> <dt>



Non è possibile effettuare l'accesso diretto alla rete in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERRORE \_ Internet \_ non \_ inizializzato**
</dt> <dd> <dl> <dt>

12172
</dt> <dt>



Non è stata eseguita l'inizializzazione dell'API WinINet. Indica che una funzione di livello superiore, ad esempio [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena), non è ancora stata chiamata.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERRORE \_ Internet \_ non \_ \_ richiesta proxy**
</dt> <dd> <dl> <dt>

12020
</dt> <dt>



La richiesta non può essere effettuata tramite un proxy.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERRORE \_ \_ operazione Internet \_ annullata**
</dt> <dd> <dl> <dt>

12017
</dt> <dt>



L'operazione è stata annullata, in genere perché l'handle su cui era in funzione la richiesta è stato chiuso prima del completamento dell'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**\_opzione Internet di errore \_ \_ non \_ impostabile**
</dt> <dd> <dl> <dt>

12011
</dt> <dt>



Impossibile impostare l'opzione richiesta, solo query.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERRORE \_ \_ di Internet \_ degli \_ handle**
</dt> <dd> <dl> <dt>

12001
</dt> <dt>



Al momento non è stato possibile generare più handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERRORE \_ Internet \_ Post \_ \_ non \_ sicuro**
</dt> <dd> <dl> <dt>

12043
</dt> <dt>



L'applicazione sta inviando i dati a un server non protetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERRORE \_ \_ protocollo Internet \_ non \_ trovato**
</dt> <dd> <dl> <dt>

12008
</dt> <dt>



Il protocollo richiesto non è stato individuato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERRORE \_ \_ server proxy Internet non \_ \_ raggiungibile**
</dt> <dd> <dl> <dt>

12165
</dt> <dt>



Impossibile raggiungere il server proxy designato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERRORE \_ di \_ \_ modifica dello schema di reindirizzamento Internet \_**
</dt> <dd> <dl> <dt>

12048
</dt> <dt>



La funzione non è stata in grado di gestire il reindirizzamento perché lo schema è stato modificato (ad esempio, da HTTP ad FTP).


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERRORE \_ \_ valore registro di sistema Internet \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

12021
</dt> <dt>



Impossibile trovare un valore obbligatorio del registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**\_richiesta Internet di errore \_ \_ in sospeso**
</dt> <dd> <dl> <dt>

12026
</dt> <dt>



Non è stato possibile completare l'operazione richiesta perché una o più richieste sono in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**\_finestra di \_ dialogo Riprova Internet errore \_**
</dt> <dd> <dl> <dt>

12050
</dt> <dt>



È necessario ritentare la finestra di dialogo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERRORE per il \_ \_ certificato CN di Internet sec \_ \_ \_ non valido**
</dt> <dd> <dl> <dt>

12038
</dt> <dt>



Il nome comune del certificato SSL (campo nome host) non è corretto, ad esempio se è stato immesso www.server.com e il nome comune nel certificato è www.different.com.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERRORE in \_ Internet \_ sec \_ CERT \_ data \_ non valida**
</dt> <dd> <dl> <dt>

12037
</dt> <dt>



La data del certificato SSL ricevuta dal server non è valida. Il certificato è scaduto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**\_errori del certificato di Internet \_ sec errore \_ \_**
</dt> <dd> <dl> <dt>

12055
</dt> <dt>



Il certificato SSL contiene errori.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERRORE \_ Internet \_ sec \_ CERT \_ No \_ REV**
</dt> <dd> <dl> <dt>

12056
</dt> <dt>



Il certificato SSL non è stato revocato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERRORE di \_ Internet \_ sec \_ CERT \_ rev \_ non riuscito**
</dt> <dd> <dl> <dt>

12057
</dt> <dt>



Revoca del certificato SSL non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERRORE \_ \_ certificato Internet \_ sec \_ revocato**
</dt> <dd> <dl> <dt>

12170
</dt> <dt>



Il certificato SSL è stato revocato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERRORE \_ di \_ \_ certificato non valido per Internet sec \_**
</dt> <dd> <dl> <dt>

12169
</dt> <dt>



Il certificato SSL non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**errore \_ \_ canale di sicurezza Internet \_ errore \_**
</dt> <dd> <dl> <dt>

12157
</dt> <dt>



Si è verificato un errore interno durante il caricamento delle librerie SSL.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERRORE \_ server Internet non \_ \_ raggiungibile**
</dt> <dd> <dl> <dt>

12164
</dt> <dt>



Il sito Web o il server indicato non è raggiungibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERRORE \_ di \_ arresto Internet**
</dt> <dd> <dl> <dt>

12012
</dt> <dt>



È in corso l'arresto o lo scaricamento del supporto di WinINet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERRORE \_ Internet \_ TCPIP \_ non \_ installato**
</dt> <dd> <dl> <dt>

12159
</dt> <dt>



Lo stack di protocolli richiesto non è caricato e l'applicazione non può avviare WinSock.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**\_timeout Internet \_ errore**
</dt> <dd> <dl> <dt>

12002
</dt> <dt>



Timeout della richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERRORE \_ Internet \_ non è possibile \_ \_ memorizzare nella cache il \_ file**
</dt> <dd> <dl> <dt>

12158
</dt> <dt>



La funzione non è in grado di memorizzare il file nella cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERRORE \_ Internet \_ non è possibile \_ \_ scaricare \_ lo script**
</dt> <dd> <dl> <dt>

12167
</dt> <dt>



Non è stato possibile scaricare lo script di configurazione automatica del proxy. Il \_ flag Internet \_ deve \_ \_ essere impostato come flag della richiesta della cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**schema di errore \_ Internet non \_ riconosciuto \_**
</dt> <dd> <dl> <dt>

12006
</dt> <dt>



Non è stato possibile riconoscere lo schema URL oppure non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERRORE \_ handle non valido \_**
</dt> <dd> <dl> <dt>



L'handle passato all'API è stato invalidato o chiuso.

**Intestazione:** Dichiarata in Winerror. h


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRORE di \_ più \_ dati**
</dt> <dd> <dl> <dt>



sono disponibili più dati.

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



 

