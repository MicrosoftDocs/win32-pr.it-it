---
title: Flag di opzione (WinInet. h)
description: I flag di opzione seguenti vengono utilizzati con le funzioni InternetQueryOption e InternetSetOption. Tutti i flag di opzione validi hanno un valore maggiore o uguale a INTERNET \_ prima opzione \_ e minore o uguale a Internet \_ Ultima \_ opzione.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302736"
---
# <a name="option-flags-winineth"></a>Flag di opzione (WinInet. h)

I flag di opzione seguenti vengono utilizzati con le funzioni [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) . Tutti i flag di opzione validi hanno un valore maggiore o uguale **a \_ Internet \_ prima** opzione e minore o uguale a **Internet \_ Ultima \_ opzione**.

<dl> <dt>

<span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**\_opzione Internet \_ ALTER \_ Identity**
</dt> <dd> <dl> <dt>

80
</dt> <dt>



Non implementato


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**\_opzione Internet \_ Async**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**\_ \_ ID async opzione \_ Internet**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**\_opzione Internet \_ - \_ priorità asincrona**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**\_opzione Internet \_ ignorare \_ \_ voce modificata**
</dt> <dd> <dl> <dt>

64
</dt> <dt>



Imposta o Recupera il valore booleano che determina se il sistema deve controllare la rete per il contenuto più recente e sovrascrivere le voci della cache modificate se viene rilevata una versione più recente. Se impostato su **true**, il sistema controlla la rete per il contenuto più recente e sovrascrive la voce della cache modificata con la versione più recente. Il valore predefinito è **false**, che indica che la voce della cache modificata deve essere utilizzata senza controllare la rete. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). È valido solo in Microsoft Internet Explorer 5 e versioni successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**\_handle del \_ flusso della cache delle opzioni \_ Internet \_**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Non più supportata.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**\_ \_ timestamp della cache delle opzioni Internet \_**
</dt> <dd> <dl> <dt>

69
</dt> <dt>



Recupera una struttura di [**\_ \_ timestamp della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) che contiene l'ora LastModified e scade l'ora dalla risorsa archiviata nella cache Internet. Questo valore viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**\_callback opzione \_ Internet**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Imposta o recupera l'indirizzo della funzione di callback definita per questo handle. Questa opzione può essere usata in tutti gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) . Usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_filtro di \_ callback delle opzioni Internet \_**
</dt> <dd> <dl> <dt>

54
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**\_contesto del \_ \_ certificato client dell'opzione \_ Internet**
</dt> <dd> <dl> <dt>

84
</dt> <dt>



Questo flag non è supportato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Il parametro *lpBuffer* deve essere un puntatore a una struttura del [**\_ contesto del certificato**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) e non un puntatore a un puntatore di **\_ contesto del certificato** . Se un'applicazione riceve l'errore certificato di **\_ \_ autenticazione client Internet \_ \_ \_ necessario**, deve chiamare [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o usare [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per fornire un certificato prima di ritentare la richiesta. [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) viene quindi chiamato in modo che il contesto del certificato passato possa essere rilasciato in modo indipendente dall'applicazione.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**opzione INTERNET (tabella \_ \_ codici)**
</dt> <dd> <dl> <dt>

68
</dt> <dt>



Per impostazione predefinita, la parte relativa all'host o all'autorità dell'URL Unicode viene codificata in base alla specifica IDN. Impostando questa opzione sulla richiesta o sull'handle di connessione, quando IDN è disabilitato, viene specificato uno schema di codifica della tabella codici per la parte host dell'URL. Il parametro *lpBuffer* nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la tabella codici DBCS desiderata. Se in *lpBuffer* non è specificata alcuna tabella codici, WinInet usa la tabella codici di sistema predefinita (CP \_ ACP). Nota: questa opzione viene ignorata se IDN non è disabilitato. Per ulteriori informazioni su come disabilitare IDN, vedere l'opzione **Internet \_ option \_ IDN** .

**Windows XP con SP2 e Windows Server 2003 con SP1:** Questo flag non è supportato.

**Versione:** Richiede Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**\_opzione Internet \_ percorso tabella codici \_**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Per impostazione predefinita, la parte del percorso dell'URL è con codifica UTF8. L'API WinINet esegue il carattere di escape (%) codifica dei caratteri a bit significativo. Impostando questa opzione sulla richiesta o sull'handle di connessione, viene disabilitata la codifica UTF8 e viene impostata una tabella codici specifica. Il parametro *lpBuffer* nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la tabella codici DBCS desiderata per il percorso. Se non viene specificata alcuna tabella codici in *lpBuffer*, WinInet usa il CP \_ UTF8 predefinito.

**Windows XP con SP2 e Windows Server 2003 con SP1:** Questo flag non è supportato.

**Versione:** Richiede Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**opzione INTERNET-tabella \_ \_ codici \_ aggiuntivi**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Per impostazione predefinita, la parte del percorso dell'URL è la tabella codici di sistema predefinita (CP \_ ACP). Carattere di escape (%) le conversioni non vengono eseguite sulla parte aggiuntiva. L'impostazione di questa opzione sulla richiesta o sull'handle di connessione Disabilita la \_ codifica CP ACP. Il parametro *lpBuffer* nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contiene la tabella codici DBCS desiderata per la parte aggiuntiva dell'URL. Se in *lpBuffer* non è specificata alcuna tabella codici, WinInet usa la tabella codici di sistema predefinita (CP \_ ACP).

**Windows XP con SP2 e Windows Server 2003 con SP1:** Questo flag non è supportato.

**Versione:** Richiede Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**\_opzione Internet \_ - \_ lunghezza contenuto compresso \_** 
</dt> <dd> <dl> <dt>

147
</dt> <dt>



Per una richiesta in cui WinInet decompressi la codifica del contenuto fornita dal server, recupera la lunghezza del contenuto segnalata dal server del corpo della risposta come ULONGLONG. Supportato in Windows 10, versione 1507 e successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**\_opzione Internet \_ Connect \_ BACKOFF**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**opzioni INTERNET- \_ \_ tentativi di connessione \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero di tentativi di WinINet per la risoluzione e la connessione a un host. Tenta solo una volta per ogni indirizzo IP. Se ad esempio si tenta di connettersi a un host multihome con dieci indirizzi IP e l'opzione INTERNET \_ \_ tentativi di connessione \_ è impostata su sette, WinInet tenterà solo di risolvere e connettersi ai primi sette indirizzi IP. Viceversa, dato lo stesso set di dieci indirizzi IP, se l'opzione INTERNET \_ \_ tentativi di connessione \_ è impostata su 20, WinInet tenta ognuno dei dieci una sola volta. Se un host dispone di un solo indirizzo IP e il primo tentativo di connessione ha esito negativo, non vengono eseguiti altri tentativi. Se un tentativo di connessione non riesce ancora dopo il numero di tentativi specificato, la richiesta viene annullata. Il valore predefinito per i \_ tentativi di connessione all'opzione Internet \_ \_ è cinque tentativi. Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**\_tempo di \_ connessione \_ opzione Internet**
</dt> <dd> <dl> <dt>

55
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**\_opzione Internet \_ \_ timeout connessione**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, da utilizzare per le richieste di connessione Internet. Se si imposta questa opzione su infinito (0xFFFFFFFF), questo timer verrà disabilitato.

Se una richiesta di connessione richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata. Quando si tenta di connettersi a più indirizzi IP per un singolo host (host multihomed), il limite di timeout è cumulativo per tutti gli indirizzi IP. Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**\_opzione Internet \_ - \_ stato connesso**
</dt> <dd> <dl> <dt>

50
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene lo stato connesso. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**\_valore del \_ contesto dell'opzione Internet \_**
</dt> <dd> <dl> <dt>

45
</dt> <dt>



Imposta o recupera un \_ ptr DWORD che contiene l'indirizzo del valore di contesto associato a questo handle [**HINTERNET**](appendix-a-hinternet-handles.md) . Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). In precedenza, il valore del contesto veniva impostato sull'indirizzo archiviato nel puntatore **lpBuffer** . Questo problema è stato corretto in modo da usare il valore archiviato nel buffer e al flag del [ \_ valore del \_ contesto \_ dell'opzione Internet](/windows) viene assegnato un nuovo valore. Il valore precedente, 10, è stato mantenuto in modo che le applicazioni scritte per il comportamento precedente siano ancora supportate.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**\_timeout di \_ \_ ricezione controllo opzione Internet \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Il [ \_ \_ \_ timeout di ricezione](/windows)è identico a Internet. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**\_timeout di \_ invio del controllo opzioni \_ Internet \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Il [ \_ \_ \_ timeout di invio](/windows)è identico a Internet. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_ \_ \_ timeout ricezione dati opzione \_ Internet**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta a una richiesta per il canale dati di una transazione FTP. Se la risposta richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata. Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Questo flag non ha alcun effetto sulla funzionalità HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**\_ \_ \_ timeout invio dati opzione \_ Internet**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Imposta o recupera un valore long integer senza segno, in millisecondi, che contiene il valore di timeout per inviare una richiesta per il canale dati di una transazione FTP. Se l'invio richiede più tempo rispetto a questo valore di timeout, l'invio viene annullato. Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Questo flag non ha alcun effetto sulla funzionalità HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**\_nome dell'opzione Internet \_ DataFile \_**
</dt> <dd> <dl> <dt>

33
</dt> <dt>



Recupera un valore stringa che contiene il nome del file che esegue il backup di un'entità scaricata. Questo flag è valido dopo il completamento di [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) . È possibile eseguire query su questa opzione solo con [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**\_opzione Internet \_ filedatafile \_ ext**
</dt> <dd> <dl> <dt>

96
</dt> <dt>



Imposta un valore stringa che contiene l'estensione del file che esegue il backup di un'entità scaricata. Questo flag deve essere impostato prima di chiamare [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). Questa opzione può essere impostata solo da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**\_informazioni sul \_ socket di diagnostica dell'opzione Internet \_ \_**
</dt> <dd> <dl> <dt>

67
</dt> <dt>



Recupera una struttura di [**\_ informazioni del \_ socket \_ di diagnostica Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) che contiene i dati relativi a una richiesta HTTP specificata. Questo flag viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

**Windows 7:** Questa opzione non è più supportata.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**\_ \_ Scarica autenticazione del digest dell'opzione Internet \_ \_**
</dt> <dd> <dl> <dt>

76
</dt> <dt>



Causa la disconnessione del pacchetto SSPI di autenticazione del digest da parte del sistema, con l'eliminazione di tutte le credenziali create per il processo. Per questa opzione non è necessario alcun buffer. Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**\_opzione Internet \_ Disabilita \_ Autodial**
</dt> <dd> <dl> <dt>

70
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**opzione INTERNET- \_ \_ timeout disconnesso \_**
</dt> <dd> <dl> <dt>

49
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**\_opzione Internet \_ Abilita \_ \_ protocollo http**
</dt> <dd> <dl> <dt>

148
</dt> <dt>



Imposta una maschera di bit DWORD di versioni HTTP avanzate accettabili. Può essere impostato su qualsiasi tipo di handle. I valori possibili sono:

-   \_Flag di protocollo http \_ \_ HTTP2 (0x2). Supportato in Windows 10, versione 1507 e versioni successive.

Non è possibile disabilitare le versioni legacy di HTTP (1,1 e precedenti) con questa opzione. Il valore predefinito è 0x0. Supportato in Windows 10, versione 1507 e successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**\_opzione Internet \_ Abilita \_ la \_ lettura della cache di Reindirizzamento \_**
</dt> <dd> <dl> <dt>

122
</dt> <dt>



In un handle di richiesta, imposta un valore booleano che controlla se i reindirizzamenti verranno restituiti dalla cache WinInet per una determinata richiesta. Il valore predefinito è FALSE. Supportato in Windows 8 e versioni successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**\_opzione Internet \_ Encode \_ extra**
</dt> <dd> <dl> <dt>

155
</dt> <dt>



Ottiene o imposta un valore BOOL che indica se i caratteri non ASCII nella stringa di query devono essere codificati in percentuale. Il valore predefinito è FALSE. Supportato in Windows 8.1 e versioni successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**\_opzione Internet \_ End \_ browser \_ Session**
</dt> <dd> <dl> <dt>

42
</dt> <dt>



Scarica le voci non utilizzate dalla cache delle password sull'unità disco rigido. Reimposta inoltre il tempo di memorizzazione nella cache utilizzato quando la modalità di sincronizzazione è una volta per sessione. Per questa opzione non è necessario alcun buffer. Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**\_maschera di \_ errore \_ opzione Internet**
</dt> <dd> <dl> <dt>

62
</dt> <dt>



Imposta un valore long integer senza segno che contiene le maschere di errore che possono essere gestite dall'applicazione client. Può trattarsi di una combinazione dei valori seguenti:

<dl> <dt>

<span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>\_maschera di errore Internet \_ \_ combinazione \_ sec \_ certificato
</dt> <dd>

0x2

Indica che tutti gli errori del certificato devono essere segnalati utilizzando la stessa restituzione dell'errore, ovvero errori del certificato di **\_ Internet \_ sec \_ \_**. Se questo flag è impostato, chiamare **InternetErrorDlg** al momento della ricezione dell'errore **errore \_ \_ \_ certificato \_ Internet sec** , in modo che l'utente possa rispondere a una finestra di dialogo familiare che descrive il problema.

> [!Caution]  
> La mancata notifica all'utente di questo errore espone l'utente a potenziali attacchi di spoofing.

 

</dd> <dt>

<span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>maschera di errore INTERNET- \_ \_ \_ Inserisci \_ CDROM
</dt> <dd>

0x1

Indica che l'applicazione client è in grado di gestire l' **errore \_ Internet \_ inserire \_** codice errore cdrom.

</dd> <dt>

<span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>errore di accesso della maschera di errore di INTERNET \_ visualizzazione del \_ corpo dell' \_ \_ \_ \_ entità \_
</dt> <dd>

0x8

Indica che l'applicazione client è in grado di gestire l' **errore di \_ accesso Internet errore Visualizza codice errore \_ \_ \_ \_ \_ corpo entità** .

</dd> <dt>

<span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>la \_ maschera di errore Internet \_ necessita di \_ \_ MSN \_ SSPI \_ pkg
</dt> <dd>

0x4

Non implementato.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**\_opzione Internet \_ \_ contesto aziendale**
</dt> <dd> <dl> <dt>

159
</dt> <dt>



Imposta un PWSTR contenente l'ID Enterprise (vedere https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) che si applica alla richiesta. Supportato in Windows 10, versione 1507 e successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_opzione Internet \_ - \_ errore esteso**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Recupera un valore long integer senza segno che contiene un codice di errore Winsock mappato ai messaggi di errore **\_ Internet \_** restituiti per ultimi in questo contesto di thread. Questa opzione viene usata in un handle [**HINTERNET**](appendix-a-hinternet-handles.md) **null** da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**\_opzione Internet \_ da \_ \_ timeout cache**
</dt> <dd> <dl> <dt>

63
</dt> <dt>



Imposta o Recupera il valore long integer senza segno A1n che contiene la quantità di tempo durante la quale il sistema deve attendere una risposta a una richiesta di rete prima di controllare la cache per una copia della risorsa. Se una richiesta di rete richiede più tempo del tempo specificato e la risorsa richiesta è disponibile nella cache, la risorsa viene recuperata dalla cache. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**\_tipo di \_ handle di opzione Internet \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Recupera un valore long integer senza segno che contiene il tipo di handle [**HINTERNET**](appendix-a-hinternet-handles.md) passati. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) per qualsiasi handle [HINTERNET](appendix-a-hinternet-handles.md) . Tra i possibili valori restituiti sono inclusi i seguenti.

<dl> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>\_tipo di handle Internet \_ \_ connessione \_ FTP
</dt> <dd>

2

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>\_tipo di handle Internet \_ \_ Connetti \_ Gopher
</dt> <dd>

3

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>\_tipo di handle Internet \_ \_ Connect \_ http
</dt> <dd>

4

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_richiesta di \_ file di tipo handle \_ Internet \_
</dt> <dd>

14

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>\_tipo di handle Internet \_ \_ \_ file FTP
</dt> <dd>

7

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>\_tipo di handle Internet \_ \_ \_ HTML file FTP \_
</dt> <dd>

8

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>tipo di handle INTERNET- \_ \_ \_ \_ ricerca FTP
</dt> <dd>

5

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>\_tipo di handle Internet \_ \_ FTP \_ trova \_ HTML
</dt> <dd>

6

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>\_ \_ file Gopher del tipo di handle Internet \_ \_
</dt> <dd>

11

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>\_tipo di handle Internet \_ \_ \_ HTML file Gopher \_
</dt> <dd>

12

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>tipo di handle INTERNET- \_ \_ \_ \_ trova Gopher
</dt> <dd>

9

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>\_tipo di handle Internet \_ \_ Gopher \_ Find \_ HTML
</dt> <dd>

10

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>\_ \_ richiesta HTTP di tipo handle \_ Internet \_
</dt> <dd>

13

</dd> <dt>

<span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>\_tipo di handle Internet \_ \_ Internet
</dt> <dd>

1

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**\_opzione Internet \_ HSTS**
</dt> <dd> <dl> <dt>

157
</dt> <dt>



Ottiene o imposta un valore BOOL che indica se WinInet deve seguire le direttive HTTP Strict Transport Security (HSTS) dai server. Se abilitate, le richieste con schema https://a domini che hanno un criterio HSTS memorizzato nella cache da WinInet verranno reindirizzate agli URL https://corrispondenti. Il valore predefinito è FALSE. Supportato in Windows 8.1 e versioni successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**\_opzione Internet \_ \_ decodifica http**
</dt> <dd> <dl> <dt>

65
</dt> <dt>



Consente a WinINet di eseguire la decodifica per gli schemi di codifica gzip e Deflate. Per ulteriori informazioni, vedere [**codifica del contenuto**](content-encoding.md).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**\_ \_ protocollo http opzione \_ Internet \_ usato**
</dt> <dd> <dl> <dt>

149
</dt> <dt>



Ottiene un valore DWORD che indica quale versione HTTP avanzata è stata utilizzata per una determinata richiesta. I valori possibili sono:

-   \_Flag di protocollo http \_ \_ HTTP2 (0x2). Supportato in Windows 10, versione 1507 e versioni successive.

0x0 indica HTTP/1.1 o versione precedente; vedere l' \_ opzione \_ Internet \_ versione http se è necessaria una maggiore precisione su quale versione legacy è stata usata. Supportato in Windows 10, versione 1507 e versioni successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**\_opzione Internet \_ \_ versione http**
</dt> <dd> <dl> <dt>

59
</dt> <dt>



Imposta o Recupera una struttura di [**\_ \_ informazioni sulla versione http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) che contiene la versione http supportata. Questa operazione deve essere utilizzata su un handle **null** . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

In Windows 7, Windows Server 2008 R2 e versioni successive, il valore del membro **dwMinorVersion** nella struttura delle [**\_ \_ informazioni sulla versione http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) viene sostituito dalle impostazioni di Internet Explorer. **EnableHttp1 \_ 1** è un valore del registro di sistema in **HKLM \\ software \\ Microsoft \\ InternetExplorer \\ AdvacnedOptions \\ http \\ GENABLE** controllato dalle opzioni Internet impostate in Internet Explorer per il sistema. Il valore predefinito di **EnableHttp1 \_ 1** è 1. La struttura delle **\_ \_ informazioni sulla versione http** viene ignorata per qualsiasi versione http inferiore a 1,1 se **EnableHttp1 \_ 1** è impostato su 1.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**\_identità opzione \_ Internet**
</dt> <dd> <dl> <dt>

78
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**opzione INTERNET- \_ \_ stato di inattività \_**
</dt> <dd> <dl> <dt>

51
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**\_opzione Internet \_ IDN**
</dt> <dd> <dl> <dt>

102
</dt> <dt>



Per impostazione predefinita, la parte relativa all'host o all'autorità dell'URL è codificata in base alla specifica IDN per le connessioni dirette e proxy. Questa opzione può essere utilizzata nella richiesta o nell'handle di connessione per abilitare o disabilitare IDN. Quando IDN è disabilitato, WinINet usa la tabella codici di sistema per codificare la porzione host o Authority dell'URL. Per disabilitare la conversione dell'host IDN, impostare il parametro *lpBuffer* nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) su zero. Per abilitare la conversione IDN solo sulla connessione diretta, specificare **il \_ flag Internet \_ IDN \_ Direct** nel parametro *lpBuffer* nella chiamata a **InternetSetOption**. Per abilitare la conversione IDN solo sulla connessione proxy, specificare **il \_ \_ \_ proxy IDN del flag Internet** nel parametro *lpBuffer* nella chiamata a **InternetSetOption**.

**Windows XP con SP2 e Windows Server 2003 con SP1:** Questo flag non è supportato.

**Versione:** Richiede Internet Explorer 7,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**\_opzione Internet \_ Ignore \_ offline**
</dt> <dd> <dl> <dt>

77
</dt> <dt>



Imposta o recupera un valore che indica se il flag globale offline deve essere ignorato per l'handle di richiesta specificato. Per questa opzione non è necessario alcun buffer. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con un handle di richiesta. Questa opzione è valida solo in Internet Explorer 5 e versioni successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**\_opzione Internet \_ Mantieni \_ connessione**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**\_ \_ timeout ascolto opzione \_ Internet**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**\_Opzione Internet \_ Max \_ Conns \_ per \_ 1 \_ 0 \_ Server**
</dt> <dd> <dl> <dt>

74
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server HTTP/1.0. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Questa opzione è valida solo in Internet Explorer 5 e versioni successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**\_opzione Internet \_ Max \_ connes \_ per \_ proxy**
</dt> <dd> <dl> <dt>

103
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni proxy CERN. Quando questa opzione è impostata o recuperata, il parametro *HINTERNET* deve essere impostato su un valore di handle **null** . Un valore di handle **null** indica che l'opzione deve essere impostata o sottoposta a query per il processo corrente. Quando si chiama [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con questa opzione, tutti gli oggetti proxy esistenti riceveranno il nuovo valore. Questo valore è limitato a un intervallo compreso tra 2 e 128, inclusi.

**Versione:** Richiede Internet Explorer 8,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**\_opzione Internet \_ Max \_ connes \_ per \_ Server**
</dt> <dd> <dl> <dt>

73
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per server. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Questa opzione è valida solo in Internet Explorer 5 e versioni successive.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**\_opzione Internet \_ \_ modalità offline**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_ \_ semantica offline opzione Internet \_**
</dt> <dd> <dl> <dt>

52
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_opzione Internet \_ scegliere \_ la \_ \_ firma debole**
</dt> <dd> <dl> <dt>

176
</dt> <dt>



Acconsentire esplicitamente alle firme deboli (ad esempio, SHA-1) per essere considerate non sicure. In questo modo, WinInet chiamerà [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) utilizzando il **parametro \_ \_ \_ di \_ \_ firma esplicito della catena di certificati** .


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**\_ \_ handle padre opzione \_ Internet**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Recupera l'handle padre per questo handle. Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**\_password opzione \_ Internet**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Imposta o recupera un valore stringa che contiene la password associata a un handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**opzione \_ Internet \_ per \_ ogni \_ opzione di connessione**
</dt> <dd> <dl> <dt>

75
</dt> <dt>



Imposta o Recupera una struttura [**Internet \_ per ogni \_ \_ \_ elenco**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) di opzioni conn che specifica un elenco di opzioni per una determinata connessione. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Questa opzione è valida solo in Internet Explorer 5 e versioni successive.

> [!Note]  
> **Internet \_ L' \_ opzione \_ per \_ connessione** consente di modificare le impostazioni a livello di sistema quando si utilizza un handle **null** nella chiamata a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Per aggiornare le impostazioni del proxy globale, è necessario chiamare **InternetSetOption** con il flag dell'opzione di **\_ \_ aggiornamento Internet Option** .

 

> [!Note]  
> Per modificare le informazioni sul proxy per l'intero processo senza influire sulle impostazioni globali in Internet Explorer 5 e versioni successive, usare questa opzione nell'handle restituito da [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Nell'esempio di codice seguente viene modificato il proxy per l'intero processo anche se l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) è chiuso e non viene utilizzato da alcuna richiesta.

 

Per ulteriori informazioni ed esempi di codice, vedere l' [articolo della Knowledge base 226473](https://support.microsoft.com/kb/226473).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**\_criteri opzione \_ Internet**
</dt> <dd> <dl> <dt>

48
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**\_proxy opzione \_ Internet**
</dt> <dd> <dl> <dt>

38
</dt> <dt>



Imposta o Recupera una struttura di [**\_ \_ informazioni sul proxy Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) che contiene i dati del proxy per un handle [**internetopt**](/windows/desktop/api/Wininet/nf-wininet-internetopena) esistente quando l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) non è **null**. Se l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) è **null**, la funzione imposta o esegue una query sui dati proxy globali. Questa opzione può essere usata sull'handle restituito da **InternetOpen**. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

> [!Note]  
> È consigliabile usare l'opzione \_ opzione Internet \_ per \_ connessione anziché il \_ \_ proxy di opzione Internet \_ . Per ulteriori informazioni, vedere l' [articolo KB 226473](https://support.microsoft.com/kb/226473).

 


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**\_ \_ password proxy opzione \_ Internet**
</dt> <dd> <dl> <dt>

44
</dt> <dt>



Imposta o recupera un valore stringa che contiene la password utilizzata per accedere al proxy. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Questa opzione può essere impostata sull'handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**\_ \_ impostazioni proxy opzioni \_ Internet \_ modificate**
</dt> <dd> <dl> <dt>

95 
</dt> <dt>



Avvisa l'istanza di WinInet corrente che le impostazioni proxy sono state modificate e che devono essere aggiornate con le nuove impostazioni. Per avvisare tutte le istanze di WinInet disponibili, impostare il parametro *buffer* di [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) su **null** e *bufferLength* su 0 quando si passa questa opzione. Questa opzione può essere impostata sull'handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**\_ \_ nome utente proxy opzione Internet \_**
</dt> <dd> <dl> <dt>

43
</dt> <dt>



Imposta o recupera un valore stringa che contiene il nome utente utilizzato per accedere al proxy. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Questa opzione può essere impostata sull'handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**\_dimensioni del \_ buffer di lettura opzione \_ Internet \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene la dimensione del buffer di lettura. Questa opzione può essere utilizzata per gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituiti da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)e [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (solo sessione FTP). Questa opzione viene usata da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**\_ \_ velocità effettiva ricezione opzione Internet \_**
</dt> <dd> <dl> <dt>

57
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_timeout di \_ ricezione \_ opzione Internet**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta a una richiesta. Se la risposta richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata. Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Questa opzione non è destinata a rappresentare un timeout immediato e con granularità fine. È possibile prevedere che il timeout venga eseguito fino a sei secondi dopo il valore di timeout set.

Se utilizzata in riferimento a una transazione FTP, questa opzione si riferisce al canale di controllo.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**\_aggiornamento opzioni \_ Internet**
</dt> <dd> <dl> <dt>

37
</dt> <dt>



Consente di rileggere i dati del proxy dal registro di sistema per un handle. Non è necessario alcun buffer. Questa opzione può essere usata nell'handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituito da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**\_opzione Internet \_ Rimuovi \_ identità**
</dt> <dd> <dl> <dt>

79
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**\_flag di \_ richiesta di opzione Internet \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Recupera un valore long integer senza segno che contiene i flag di stato speciali che indicano lo stato del download in corso. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). L' [opzione \_ Internet \_ Request \_ Flags](/windows) può essere uno dei valori seguenti:

<dl> <dt>

<span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET \_ REQFLAG \_ Async
</dt> <dd>

0x00000002

Non implementato.

</dd> <dt>

<span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>\_ \_ scrittura cache REQFLAG \_ Internet \_ disabilitata
</dt> <dd>

0x00000040

La richiesta Internet non può essere memorizzata nella cache (ad esempio, una richiesta HTTPS).

</dd> <dt>

<span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET \_ REQFLAG \_ dalla \_ cache
</dt> <dd>

0x00000001

La risposta proviene dalla cache.

</dd> <dt>

<span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>\_ \_ timeout rete REQFLAG \_ Internet
</dt> <dd>

0x00000080

Timeout della richiesta Internet.

</dd> <dt>

<span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET \_ REQFLAG \_ senza \_ intestazioni
</dt> <dd>

0x00000008

La risposta originale non conteneva intestazioni.

</dd> <dt>

<span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET \_ REQFLAG \_ passivo
</dt> <dd>

0x00000010

Non implementato.

</dd> <dt>

<span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET \_ REQFLAG \_ tramite \_ proxy
</dt> <dd>

0x00000004

La richiesta è stata effettuata tramite un proxy.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**\_ \_ priorità richiesta opzione \_ Internet**
</dt> <dd> <dl> <dt>

58
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene la priorità delle richieste che competono per una connessione su un handle HTTP. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**\_opzione Internet \_ Reimposta \_ \_ sessione Urlcache**
</dt> <dd> <dl> <dt>

60
</dt> <dt>



Avvia una nuova sessione della cache per il processo. Non è necessario alcun buffer. Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Questa opzione è riservata solo per uso interno.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**\_opzione Internet \_ \_ chiave di cache secondaria \_**
</dt> <dd> <dl> <dt>

53
</dt> <dt>



Imposta o recupera un valore stringa che contiene la chiave di cache secondaria. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona). Questa opzione è riservata solo per uso interno.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**\_certificato di \_ sicurezza delle opzioni Internet \_**
</dt> <dd> <dl> <dt>

35
</dt> <dt>



Recupera il certificato per un server SSL/PCT (Secure Sockets Layer/tecnologia di comunicazione privata) in una stringa formattata. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_ \_ struct certificato di sicurezza opzione \_ Internet \_**
</dt> <dd> <dl> <dt>

32
</dt> <dt>



Recupera il certificato per un server SSL/PCT nella struttura delle \_ informazioni del certificato Internet \_ . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**\_flag di \_ sicurezza delle opzioni Internet \_**
</dt> <dd> <dl> <dt>

31
</dt> <dt>



Recupera un valore long integer senza segno che contiene i flag di sicurezza per un handle. Questa opzione viene utilizzata da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Può essere una combinazione dei valori seguenti.

<dl> <dt>

<span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>FLAG di sicurezza \_ \_ 128bit
</dt> <dd>

0x20000000

Identico al flag di sicurezza del valore preferito [ \_ \_ \_ Strong](/windows). Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>FLAG di sicurezza \_ \_ 40BIT
</dt> <dd>

0x10000000

Identico al flag di sicurezza del valore preferito [ \_ \_ \_ debole](/windows). Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>FLAG di sicurezza \_ \_ 56BIT
</dt> <dd>

0x40000000

Identico al flag di sicurezza del valore preferito [ \_ \_ \_ medio](/windows). Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>FLAG di sicurezza \_ \_ fortezza
</dt> <dd>

0x08000000

Indica che la fortezza è stata utilizzata per fornire riservatezza, autenticazione e/o integrità per la connessione specificata.

</dd> <dt>

<span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>FLAG di sicurezza \_ \_ IETFSSL4
</dt> <dd>

0x00000020

Non implementato.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>FLAG di sicurezza \_ \_ Ignora \_ certificato \_ CN \_ non valido
</dt> <dd>

0x00001000

Ignora il messaggio di errore [ \_ \_ \_ \_ \_ non valido della CN del certificato di errore di Internet sec](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>FLAG di sicurezza \_ \_ Ignora \_ certificato \_ data \_ non valido
</dt> <dd>

0x00002000

Ignora il messaggio di errore [ \_ \_ \_ \_ \_ non valido relativo alla data del certificato di Internet sec](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_flag \_ di sicurezza ignora \_ Reindirizzamento \_ a \_ http
</dt> <dd>

0x00008000

Ignora il messaggio [ \_ di errore Internet \_ https \_ per \_ http \_ su \_ redir](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_flag \_ di sicurezza ignora \_ Reindirizzamento \_ a \_ https
</dt> <dd>

0x00004000

Ignora l' [errore \_ \_ \_ da http a HTTPS per il messaggio di errore di \_ \_ \_ redir](wininet-errors.md) .

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>il \_ flag di sicurezza \_ Ignora la \_ revoca
</dt> <dd>

0x00000080

Ignora i problemi di revoca dei certificati.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ CA sconosciuta
</dt> <dd>

0x00000100

Ignora i problemi di autorità di certificazione sconosciuti.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ firma debole
</dt> <dd>

0x00010000

Ignora i problemi di firma del certificato vulnerabili.

</dd> <dt>

<span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ utilizzo errato
</dt> <dd>

0x00000200

Ignora problemi di utilizzo non corretti.

</dd> <dt>

<span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>FLAG di sicurezza \_ \_ NORMALBITNESS
</dt> <dd>

0x10000000

Identico al flag di sicurezza del valore [ \_ \_ \_ debole](/windows). Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>FLAG di sicurezza \_ \_ PCT
</dt> <dd>

0x00000008

Non implementato.

</dd> <dt>

<span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>FLAG di sicurezza \_ \_ PCT4
</dt> <dd>

0x00000010

Non implementato.

</dd> <dt>

<span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>FLAG di sicurezza \_ \_ sicuro
</dt> <dd>

0x00000001

USA i trasferimenti sicuri. Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>\_SSL del flag di sicurezza \_
</dt> <dd>

0x00000002

Non implementato.

</dd> <dt>

<span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>FLAG di sicurezza \_ \_ SSL3
</dt> <dd>

0x00000004

Non implementato.

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>livello \_ medio del flag di sicurezza \_ \_
</dt> <dd>

0x40000000

Usa la crittografia media (a 56 bit). Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>sicurezza del flag di sicurezza \_ \_ \_ avanzata
</dt> <dd>

0x20000000

Usa la crittografia complessa (a 128 bit). Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>resistenza al flag di sicurezza \_ \_ \_ debole
</dt> <dd>

0x10000000

Usa la crittografia debole (a 40 bit). Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> <dt>

<span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>FLAG di sicurezza \_ \_ UNKNOWNBIT
</dt> <dd>

0x80000000

Le dimensioni del bit utilizzate nella crittografia sono sconosciute. Questa operazione viene restituita solo in una chiamata a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).

</dd> </dl>

Tenere presente che i dati recuperati in questo modo si riferiscono a una transazione che si è verificata, il cui livello di sicurezza non può più essere modificato.

</dl> </dd> <dt>

<span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**\_opzione Internet \_ chiave di sicurezza \_ \_ bit**
</dt> <dd> <dl> <dt>

36
</dt> <dt>



Recupera un valore long integer senza segno che contiene la dimensione in bit della chiave di crittografia. Maggiore è il numero, maggiore è il livello di crittografia utilizzato. Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). Tenere presente che i dati recuperati in questo modo si riferiscono a una transazione che si è già verificata, il cui livello di sicurezza non può più essere modificato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**\_ \_ velocità effettiva di invio dell'opzione Internet \_**
</dt> <dd> <dl> <dt>

56
</dt> <dt>



Non implementato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**\_timeout di \_ INVIO \_ opzione Internet**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Imposta o recupera un valore long integer senza segno, in millisecondi, che contiene il valore di timeout per l'invio di una richiesta. Se l'invio richiede più tempo rispetto a questo valore di timeout, l'invio viene annullato. Questa opzione può essere usata in qualsiasi handle [**HINTERNET**](appendix-a-hinternet-handles.md) , incluso un handle **null** . Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Se utilizzata in riferimento a una transazione FTP, questa opzione si riferisce al canale di controllo.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**\_contesto della \_ \_ catena di certificati del server opzioni \_ Internet \_**
</dt> <dd> <dl> <dt>

105
</dt> <dt>



Recupera il contesto della catena di certificati del server come [ \_ \_ contesto di catena PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)duplicato. Questo contesto duplicato può essere passato a qualsiasi funzione API di crittografia che accetta [un \_ \_ contesto della catena PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context). È necessario chiamare [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) nel [ \_ \_ contesto della catena PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) restituito al termine del contesto della catena di certificati.

**Versione:** Richiede Internet Explorer 8,0.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**\_Impostazioni opzioni \_ Internet \_ modificate**
</dt> <dd> <dl> <dt>

39
</dt> <dt>



Notifica al sistema che le impostazioni del registro di sistema sono state modificate in modo da verificare le impostazioni alla successiva chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_opzione Internet \_ Disattiva \_ \_ autenticazione server**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Imposta un oggetto richiesta HTTP in modo che non effettuerà l'accesso ai server di origine, ma eseguirà l'accesso automatico ai server proxy HTTP. Questa opzione è diversa dal flag di richiesta **Internet \_ flag \_ No \_ AUTH**, che impedisce l'autenticazione sia per i server proxy che per i server di origine.

L'impostazione di questa modalità eliminerà l'utilizzo di qualsiasi materiale delle credenziali (in precedenza fornito nome utente/password o certificato SSL client) durante la comunicazione con un server di origine. Tuttavia, se la richiesta deve transitare tramite un proxy di autenticazione, WinINet eseguirà comunque l'autenticazione automatica al proxy HTTP in base alle impostazioni dell'area Intranet per l'utente. L'impostazione predefinita dell'area Intranet è consentire l'accesso automatico utilizzando le credenziali predefinite dell'utente.

Per garantire l'eliminazione di tutte le informazioni di identificazione, il chiamante deve combinare l' **\_ opzione Internet \_ Elimina \_ \_ autenticazione server** con il flag **Internet \_ \_ nessun \_ cookie** richiesta flag.

Questa opzione può essere impostata solo su oggetti richiesta prima dell'invio. Se si tenta di impostare questa opzione dopo l'invio della richiesta, verrà restituito **\_ \_ \_ \_ lo stato dell'handle errato Internet**.

Per questa opzione non è necessario alcun buffer. Viene usato da [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per gli handle restituiti solo da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .

**Versione:** Richiede Internet Explorer 8,0 o versione successiva.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**\_opzione Internet \_ Disattiva \_ comportamento**
</dt> <dd> <dl> <dt>

81
</dt> <dt>



Opzione per utilizzo generico utilizzata per escludere i comportamenti a livello di processo. Il parametro *lpBuffer* della funzione deve essere un puntatore a un valore DWORD contenente il comportamento specifico da escludere. Non è possibile eseguire query su questa opzione con [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona). I valori consentiti sono:

<dl> <dt>

<span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET non \_ visualizzare \_ Reimposta \_ tutti
</dt> <dd>

0

Disabilita tutte le evitazioni, riattivando il comportamento predefinito e configurato. Questa opzione equivale a impostare Internet per la cancellazione dei **\_ \_ \_ criteri \_ di cookie** e per l'eliminazione dei cookie in modo **\_ \_ \_ permanente \_** .

**Versione:** Richiede Internet Explorer 6,0 o versione successiva.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET non \_ visualizzare i \_ criteri dei cookie \_ 
</dt> <dd>

1

Ignora tutti i criteri cookie configurati e consente l'impostazione dei cookie.

**Versione:** Richiede Internet Explorer 6,0 o versione successiva.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET per \_ disattivare la \_ \_ reimpostazione dei criteri cookie \_ 
</dt> <dd>

2

Disabilita la soppressione **dei \_ \_ \_ criteri dei cookie in Internet** , consentendo la valutazione dei cookie in base ai criteri cookie configurati.

**Versione:** Richiede Internet Explorer 6,0 o versione successiva.

</dd> <dt>

<span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET non \_ visualizzare \_ cookie \_ permanente
</dt> <dd>

3

Elimina la persistenza dei cookie, anche se il server li ha specificati come permanenti.

**Versione:** Richiede Internet Explorer 8,0 o versione successiva.

</dd> <dt>

<span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET non \_ visualizzare il \_ cookie \_ Mantieni \_ reimpostato
</dt> <dd>

4

Disabilita l'eliminazione di **\_ \_ \_ persistenza dei cookie in Internet** , riabilitando la persistenza dei cookie. Eventuali cookie eliminati in precedenza non diventeranno permanenti.

**Versione:** Richiede Internet Explorer 8,0 o versione successiva.

</dd> </dl>

</dl> </dd> <dt>

<span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**\_URL opzione \_ Internet**
</dt> <dd> <dl> <dt>

34
</dt> <dt>



Recupera un valore stringa che contiene l'URL completo di una risorsa scaricata. Se l'URL originale contiene dati aggiuntivi, ad esempio stringhe di ricerca o ancoraggi, oppure se la chiamata è stata reindirizzata, l'URL restituito è diverso dall'originale. Questa opzione è valida per gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituiti da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**\_ \_ agente utente opzione \_ Internet**
</dt> <dd> <dl> <dt>

41
</dt> <dt>



Imposta o recupera la stringa dell'agente utente negli handle forniti da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) e usata nelle funzioni [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) successive, purché non venga sottoposta a override da un'intestazione aggiunta da [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) o [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**\_ \_ nome utente opzione Internet**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Imposta o Recupera una stringa che contiene il nome utente associato a un handle restituito da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**\_versione opzione \_ Internet**
</dt> <dd> <dl> <dt>

40
</dt> <dt>



Recupera una struttura di **\_ \_ informazioni sulla versione di Internet** che contiene il numero di versione di Wininet.dll. Questa opzione può essere usata in un handle [**HINTERNET**](appendix-a-hinternet-handles.md) **null** da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_dimensioni del \_ buffer di scrittura delle opzioni Internet \_ \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Imposta o recupera un valore long integer senza segno che contiene la dimensione, in byte, del buffer di scrittura. Questa opzione può essere utilizzata per gli handle [**HINTERNET**](appendix-a-hinternet-handles.md) restituiti da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (solo sessione FTP). Viene usato da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                   |
| Intestazione<br/>                   | <dl> <dt>WinInet. h; </dt> <dt>Winineti. h</dt> </dl> |



 

