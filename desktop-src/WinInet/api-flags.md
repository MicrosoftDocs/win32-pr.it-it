---
title: Flag API (WinInet. h)
description: Molte delle funzioni WinINet accettano una matrice di flag come parametro. Di seguito è riportata una breve descrizione dei flag definiti.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301958"
---
# <a name="api-flags"></a>Flag API

Molte delle funzioni WinINet accettano una matrice di flag come parametro. Di seguito è riportata una breve descrizione dei flag definiti.

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**Il \_ cookie Internet \_ valuta \_ P3P**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Indica che un'intestazione della piattaforma per la protezione della privacy (P3P) deve essere associata a un cookie.


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET \_ cookie di \_ terze \_ parti**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Indica che è in corso l'impostazione o il recupero di un cookie di terze parti.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**\_flag Internet \_ asincrono**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Esegue solo richieste asincrone sugli handle derivate dall'handle restituito da questa funzione. Solo la funzione [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**\_ \_ Async della cache del flag Internet \_**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Consente la scrittura di cache lazy.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**\_cache del flag Internet se la rete ha \_ \_ \_ \_ esito negativo**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Restituisce la risorsa dalla cache se la richiesta di rete per la risorsa ha esito negativo a causa di un [errore di \_ \_ \_ reimpostazione della connessione Internet](wininet-errors.md) o di [errore \_ Internet \_ non è in grado di \_ connettersi](wininet-errors.md) . Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**\_flag Internet \_ dont \_ cache**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Non aggiunge l'entità restituita alla cache. Si tratta di un valore identico a quello preferito, ovvero [ \_ \_ Nessuna \_ \_ scrittura nella cache](/windows).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**\_flag Internet \_ esistente \_ Connetti**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Tenta di utilizzare un oggetto [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) esistente se ne esiste uno con gli stessi attributi necessari per effettuare la richiesta. Questa operazione è utile solo con le operazioni FTP, poiché FTP è l'unico protocollo che in genere esegue più operazioni durante la stessa sessione. WinINet memorizza nella cache un singolo handle di connessione per ogni handle [**HINTERNET**](appendix-a-hinternet-handles.md) generato da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Le funzioni [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e **InternetConnect** utilizzano questo flag per le connessioni HTTP e FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_ \_ Invia form di flag Internet \_**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Indica che si tratta di un invio di form.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_flag Internet \_ dalla \_ cache**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Non esegue richieste di rete. Tutte le entità vengono restituite dalla cache. Se l'elemento richiesto non è presente nella cache, viene restituito un errore appropriato, ad esempio file di errore \_ \_ non \_ trovato. Solo la funzione [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**\_nuovo flag Internet \_ FWD \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica che la funzione deve utilizzare la copia della risorsa attualmente nella cache Internet. La data di scadenza e altre informazioni sulla risorsa non sono controllate. Se l'elemento richiesto non viene trovato nella cache Internet, il sistema tenta di individuare la risorsa nella rete. Questo valore è stato introdotto in Microsoft Internet Explorer 5 ed è associato alle operazioni dei pulsanti **Avanti** e **indietro** di Internet Explorer.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_ \_ collegamento ipertestuale flag Internet**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Impone un ricaricamento se non è presente alcuna scadenza e non viene restituito alcun tempo LastModified dal server per determinare se ricaricare l'elemento dalla rete. Questo flag può essere usato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**\_flag Internet \_ Ignora \_ certificato \_ CN \_ non valido**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Disabilita il controllo dei certificati basati su SSL/PCT restituiti dal server rispetto al nome host specificato nella richiesta. WinINet utilizza un semplice controllo per i certificati confrontando i nomi host corrispondenti e le semplici regole con caratteri jolly. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**il \_ flag Internet \_ Ignora la data del \_ certificato non è \_ \_ valida**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Disabilita il controllo dei certificati basati su SSL/PCT per le date di validità corrette. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_flag Internet \_ ignorare \_ Reindirizzamento \_ a \_ http**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Disabilita il rilevamento di questo tipo speciale di reindirizzamento. Quando si usa questo flag, WinINet consente i reindirizzamenti da HTTPS a URL HTTP in modo trasparente. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_flag Internet \_ ignorare \_ Reindirizzamento \_ a \_ https**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Disabilita il rilevamento di questo tipo speciale di reindirizzamento. Quando si usa questo flag, WinINet consente in modo trasparente i reindirizzamenti da HTTP a URL HTTPS. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**\_flag Internet \_ Mantieni \_ connessione**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Usa la semantica Keep-Alive, se disponibile, per la connessione. Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http). Questo flag è obbligatorio per Microsoft Network (MSN), NTLM e altri tipi di autenticazione.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**FLAG INTERNET che \_ \_ rende \_ persistente**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Non più supportata.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**il \_ flag Internet \_ deve \_ memorizzare nella cache la \_ richiesta**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Identico al valore preferito, **il \_ \_ \_ file di richiesta del flag Internet**. Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache. Questo flag può essere usato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**\_file con flag Internet \_ necessario \_**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache. Questo flag può essere usato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**\_flag Internet \_ Nessuna \_ autenticazione**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Non tenta automaticamente l'autenticazione. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**\_flag Internet \_ senza \_ \_ Reindirizzamento automatico**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Non gestisce automaticamente il reindirizzamento in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Questo flag può essere usato anche da [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) per le richieste HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**\_flag Internet \_ senza \_ \_ scrittura cache**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Non aggiunge l'entità restituita alla cache. Questo flag viene utilizzato da, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**\_flag Internet \_ senza \_ cookie**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Non aggiunge automaticamente le intestazioni dei cookie alle richieste e non aggiunge automaticamente i cookie restituiti al database dei cookie. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (per le richieste http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_flag Internet \_ Nessuna \_ interfaccia utente**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Disabilita la finestra di dialogo dei cookie. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo richieste http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**\_flag Internet \_ offline**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Identico **al \_ flag Internet \_ dalla \_ cache**. Non esegue richieste di rete. Tutte le entità vengono restituite dalla cache. Se l'elemento richiesto non è presente nella cache, viene restituito un errore appropriato, ad esempio file di errore \_ \_ non \_ trovato. Solo la funzione [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**\_flag Internet \_ passivo**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Usa la semantica FTP passiva. Solo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usano questo flag. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilizza questo flag per le richieste FTP e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilizza questo flag per i file e le directory FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**\_flag Internet \_ pragma \_ NoCache**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Impone la risoluzione della richiesta da parte del server di origine, anche se nel proxy esiste una copia memorizzata nella cache. La funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo per le richieste HTTP e HTTPS) e la funzione [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usano questo flag.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_flag Internet \_ dati non elaborati \_**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Restituisce i dati come struttura [**di \_ \_ dati Find Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) durante il recupero delle informazioni sulla directory FTP. Se questo flag non viene specificato o se la chiamata viene eseguita tramite un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) restituisce la versione HTML della directory. Solo la funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa questo flag.

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Restituisce inoltre una struttura di [**\_ \_ dati Find di Gopher**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) durante il recupero delle informazioni sulla directory gopher.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**prelettura flag INTERNET- \_ \_ lettura \_**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Questo flag è attualmente disabilitato.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**\_ricarica del flag Internet \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Impone un download del file, dell'oggetto o dell'elenco di directory richiesto dal server di origine e non dalla cache. Le funzioni [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usano questo flag.

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_area con \_ restrizioni del flag Internet \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica che il cookie da impostare è associato a un sito non attendibile.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**risincronizzazione del \_ flag Internet \_**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Ricarica le risorse HTTP se la risorsa è stata modificata dall'ultima volta in cui è stata scaricata. Tutte le risorse FTP vengono ricaricate. Questo flag può essere usato da [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e versioni precedenti:** Utilizzato anche da [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)e le risorse Gopher vengono ricaricate.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**\_flag Internet \_ sicuro**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



Utilizza semantica sicura delle transazioni. Questo si traduce nell'utilizzo di Secure Sockets Layer/Private Communications Technology (SSL/PCT) ed è significativo solo nelle richieste HTTP. Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), ma è ridondante se https://viene visualizzato nell'URL. La funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa questo flag per le connessioni HTTP. il flag verrà ereditato da tutti gli handle di richiesta creati in questa connessione.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**\_flag Internet \_ Transfer \_ ASCII**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Trasferisce il file come ASCII (solo FTP). Questo flag può essere usato da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)e [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_binario di \_ trasferimento del flag Internet \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Trasferisce il file come binario (solo FTP). Questo flag può essere usato da [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)e [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET \_ senza \_ callback**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica che non deve essere eseguito alcun callback per l'API. Viene usato per il parametro *dxContext* delle funzioni che consentono operazioni asincrone.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_opzione Internet \_ Disattiva \_ \_ autenticazione server**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Imposta un oggetto richiesta HTTP in modo che non effettuerà l'accesso ai server di origine, ma eseguirà l'accesso automatico ai server proxy HTTP. Questa opzione è diversa dal flag di richiesta INTERNET \_ flag \_ No \_ AUTH, che impedisce l'autenticazione sia per i server proxy che per i server di origine. L'impostazione di questa modalità eliminerà l'utilizzo di qualsiasi materiale delle credenziali (in precedenza fornito nome utente/password o certificato SSL client) durante la comunicazione con un server di origine. Tuttavia, se la richiesta deve transitare tramite un proxy di autenticazione, WinINet eseguirà comunque l'autenticazione automatica al proxy HTTP in base alle impostazioni dell'area Intranet per l'utente. L'impostazione predefinita dell'area Intranet è consentire l'accesso automatico utilizzando le credenziali predefinite dell'utente. Per garantire l'eliminazione di tutte le informazioni di identificazione, il chiamante deve combinare l' \_ opzione Internet \_ Elimina \_ \_ autenticazione server con il flag Internet \_ \_ nessun \_ cookie richiesta flag. Questa opzione può essere impostata solo su oggetti richiesta prima dell'invio. Se si tenta di impostare questa opzione dopo l'invio della richiesta, verrà \_ restituito \_ \_ lo stato dell'handle errato Internet \_ . Per questa opzione non è necessario alcun buffer. Viene usato da InternetSetOption per gli handle restituiti solo da HttpOpenRequest. Versione: richiede Internet Explorer 8,0 o versione successiva.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**\_flag API \_ WinInet \_ asincrono**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Forza le operazioni asincrone.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_ \_ sincronizzazione flag API \_ WinInet**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Forza le operazioni sincrone.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**\_contesto di \_ utilizzo del flag API \_ WinInet \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Impone all'API di usare il valore di contesto, anche se è impostato su zero.


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



 

