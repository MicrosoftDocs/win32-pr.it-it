---
Description: I flag di opzione seguenti sono supportati da WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Flag di opzione (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 56eea8e528c445c5ce6f852ff8841073dd74d6a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332888"
---
# <a name="option-flags"></a>Flag di opzione

I flag di opzione seguenti sono supportati da [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**l' \_ opzione WinHTTP ha \_ assicurato \_ \_ callback non bloccanti \_**
</dt> <dd> <dl> <dt>



Il valore predefinito è FALSE. Se impostato su TRUE, WinHTTP non garantisce lo stato di avanzamento se i callback di stato sono bloccati dall'applicazione client.

L'applicazione client deve prestare particolare attenzione a eseguire le operazioni minime all'interno del callback senza bloccarle, restituendo il più rapidamente possibile e in particolare non deve attendere le chiamate WinHTTP successive. Se non segue queste linee guida, è probabile che si verifichi un impatto negativo sulle prestazioni o un potenziale blocco dell'applicazione. Se utilizzata nel modo prestabilito, questa opzione può migliorare le prestazioni.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**criteri di accesso \_ automatico opzione WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica i [criteri di accesso automatici](authentication-in-winhttp.md) con uno dei valori seguenti.

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>\_livello di sicurezza automatico WinHTTP- \_ \_ \_ alto | Le credenziali predefinite non vengono utilizzate. Si noti che questo flag viene applicato solo se si specifica il server in base al nome del computer effettivo. Non avrà effetto, se si specifica il server in base a "localhost" o indirizzo IP. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>\_livello di sicurezza automatico WinHTTP- \_ \_ \_ basso | Per tutte le richieste viene eseguito un accesso autenticato con le credenziali predefinite. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>\_supporto del livello di \_ sicurezza automatico WinHTTP \_ \_ | Un accesso autenticato con le credenziali predefinite viene eseguito solo per le richieste nella Intranet locale. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_callback di opzioni WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera il puntatore al set di funzioni di callback con [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_contesto del \_ \_ certificato client dell'opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Imposta il contesto del certificato client. Se un'applicazione riceve un errore per il certificato di [**\_ \_ autenticazione client WinHTTP \_ \_ \_ necessario**](error-messages.md), deve chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per fornire un certificato prima di ritentare la richiesta. Nell'ambito dell'elaborazione di questa opzione, WinHttp chiama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) nel contesto del certificato fornito dal chiamante, in modo che il contesto del certificato possa essere rilasciato in modo indipendente dal chiamante.

> [!Note]
> L'applicazione non deve tentare di chiudere l'archivio certificati con il flag del flag di chiusura dell'archivio certificati per la \_ \_ \_ \_ chiamata a [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) nell'archivio certificati da cui è stato recuperato il contesto del certificato. Potrebbe verificarsi una violazione di accesso.

Quando il server richiede un certificato client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce un errore relativo al certificato di [**autenticazione del \_ \_ client WinHTTP \_ \_ \_ necessario**](error-messages.md) . Se il server richiede il certificato ma non lo richiede, l'applicazione può specificare questa opzione per indicare che non dispone di un certificato. Il server può scegliere un altro schema di autenticazione o consentire l'accesso anonimo al server. L'applicazione fornisce la macro del **contesto del certificato del \_ \_ client WinHTTP \_ \_ Nessuna** nel parametro *lpBuffer* di [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , come illustrato nell'esempio di codice seguente.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Se il server richiede un certificato client, può inviare un codice di stato HTTP 403 in risposta. Per ulteriori informazioni, vedere l'opzione **WinHTTP opzione \_ \_ client \_ CERT \_ Issuer \_ List** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_elenco di \_ \_ \_ autorità emittenti del certificato client dell'opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera una [**struttura \_ IssuerListInfoEx di SecPkgContext**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando l'errore [**di WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) è errore il certificato di **autenticazione del \_ client WinHTTP \_ \_ \_ \_ necessario**. L'elenco delle autorità emittenti nella struttura contiene un elenco di autorità di certificazione (CA) accettabili dal server. L'applicazione client può filtrare l'elenco di CA per recuperare il certificato client per l'autenticazione SSL.

In alternativa, se il server richiede il certificato client, ma non lo richiede, l'applicazione può chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione del contesto del certificato **client dell' \_ opzione \_ \_ \_ WinHTTP** . Per ulteriori informazioni, vedere l'opzione di **\_ \_ \_ \_ contesto certificato client opzione WinHTTP** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**opzione WINHTTP-tabella \_ \_ codici**
</dt> <dd> <dl> <dt>



Imposta la [*tabella codici*](glossary.md) utilizzata per elaborare l'URL (ovvero la stringa di query). Il valore predefinito è UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_opzione WinHTTP \_ Configure \_ Passport \_ AUTH**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica se [l'autenticazione Passport nell'autenticazione WinHTTP](passport-authentication-in-winhttp.md) è abilitata. I possibili valori sono i seguenti:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ disabilitare \_ l' \_ autenticazione Passport | L'autenticazione Microsoft Passport è disabilitata. Questo è il valore predefinito. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ disabilitare \_ il \_ portachiavi Passport | Il portachiavi Passport è disabilitato. Questo è il valore predefinito. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ Abilita \_ \_ autenticazione Passport | Autenticazione Passport abilitata. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ Abilita \_ il \_ portachiavi Passport | Il portachiavi Passport è abilitato. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_tentativi di \_ connessione dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero di tentativi di timesWinHTTP per la connessione a un host. I servizi HTTP di Microsoft Windows (WinHTTP) tentano una sola volta per ogni indirizzo IP (Internet Protocol). Se ad esempio si tenta di connettersi a un host multihomed con 10 indirizzi IP e i **tentativi di connessione dell' \_ opzione \_ \_ WinHTTP** sono impostati su 7, WinHTTP tenterà solo di connettersi ai primi sette indirizzi IP. Dato lo stesso set di 10 indirizzi IP, se il tentativo di **\_ connessione dell'opzione \_ \_ WinHTTP** è impostato su 20, WinHTTP tenterà ogni 10 una sola volta. Se un tentativo di connessione non riesce ancora dopo il numero di tentativi specificato o se il timeout di connessione è scaduto prima di, la richiesta viene annullata. Il valore predefinito per **i \_ \_ \_ tentativi di connessione dell'opzione WinHTTP** è cinque tentativi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ timeout connessione opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi. Se si imposta questa opzione su infinito (0xFFFFFFFF), questo timer verrà disabilitato.

Se una richiesta di connessione TCP impiega più tempo rispetto a questo valore di timeout, la richiesta viene annullata. Il timeout predefinito è di 60 secondi. Quando si tenta di connettersi a più indirizzi IP per un singolo host (host multihomed), il limite di timeout è per ogni singola connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_informazioni di \_ connessione dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'indirizzo IP di origine e di destinazione e la porta della richiesta che ha generato la risposta quando [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce. L'applicazione chiama [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione di **\_ informazioni di \_ connessione \_ dell'opzione WinHTTP** e fornisce la struttura delle [**informazioni di \_ connessione \_ WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) nel parametro *lpBuffer* . Per ulteriori informazioni, vedere **le \_ \_ informazioni di connessione WinHTTP**.

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_Opzioni WinHTTP \_ connessione \_ statistiche \_ V0**
</dt> <dd> <dl> <dt>



Recupera lo struct [**TCP \_ info \_ V0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) per la connessione sottostante utilizzata dalla richiesta. Lo struct restituito può contenere statistiche delle richieste precedenti inviate tramite la stessa connessione.

> [!Note]
> Questa opzione è stata sostituita dall' **\_ opzione WinHTTP \_ Connection \_ Statistics \_ V1**.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Opzioni WinHTTP \_ connessione \_ statistiche \_ V1**
</dt> <dd> <dl> <dt>



Recupera lo struct [**TCP \_ info \_ V1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) per la connessione sottostante utilizzata dalla richiesta. Lo struct restituito può contenere statistiche delle richieste precedenti inviate tramite la stessa connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_valore del \_ contesto dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un **\_ ptr DWORD** che contiene un puntatore al valore di contesto associato a questo handle [HINTERNET](hinternet-handles-in-winhttp.md) . Viene utilizzato il valore archiviato nel buffer e al flag di opzione del **\_ valore del \_ contesto \_ dell'opzione WinHTTP** viene assegnato un nuovo valore.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**decompressione dell' \_ opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta un valore DWORD dei flag che determinano se WinHTTP decomprimerà automaticamente i corpi della risposta con codifiche di contenuto compresse. In WinHTTP viene inoltre impostata un'intestazione Accept-Encoding appropriata, eseguendo l'override di qualsiasi oggetto fornito dal chiamante. I valori supportati sono:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_flag di decompressione WinHTTP ( \_ \_ gzip) | Decomprimi Content-Encoding: risposte gzip. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_flag di decompressione WinHTTP \_ \_ deflate | Decomprimi Content-Encoding: Deflate risposte. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_flag di decompressione WinHTTP \_ \_ tutti | Decomprimere le risposte con qualsiasi codifica di contenuto supportata. |

Per impostazione predefinita, WinHTTP fornirà risposte compresse al chiamante senza modifiche.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_funzionalità di \_ disabilitazione dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica quali funzionalità sono disabilitate con uno o più dei flag seguenti. Tenere presente che questa funzionalità deve essere passata solo a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) sugli handle di richiesta dopo la creazione dell'handle di richiesta con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e prima che la richiesta venga inviata con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ Disabilita \_ l'autenticazione | L'autenticazione automatica è disabilitata. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>\_disabilitare i \_ cookie in WinHTTP | L'aggiunta automatica delle intestazioni dei cookie alle richieste è disabilitata. Inoltre, i cookie restituiti non vengono aggiunti automaticamente al database dei cookie. La disabilitazione dei cookie può comportare una riduzione delle prestazioni per l'autenticazione Passport. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_disabilitazione WinHTTP \_ Keep- \_ Alive | Disabilita la semantica Keep-Alive per la connessione. La semantica Keep-Alive è necessaria per MSN, NTLM e altri tipi di autenticazione. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_REindirizzamenti disabilitati WinHTTP \_ | Il reindirizzamento automatico è disabilitato quando si inviano richieste con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Se il reindirizzamento automatico è disabilitato, un'applicazione deve registrare una funzione di callback affinché l'autenticazione Passport abbia esito positivo. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_opzione WinHTTP \_ disabilitare \_ il \_ fallback del protocollo sicuro \_**
</dt> <dd> <dl> <dt>



Impedisce a WinHTTP di ritentare una connessione con una versione precedente del protocollo di sicurezza quando la negoziazione del protocollo iniziale ha esito negativo.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_opzione WinHTTP \_ disabilitare \_ la \_ coda di flusso**
</dt> <dd> <dl> <dt>



Consente alle nuove richieste di aprire una connessione HTTP/2 aggiuntiva quando viene raggiunto il limite massimo di flussi simultanei, anziché attendere il successivo flusso disponibile su una connessione esistente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_funzionalità di \_ Abilitazione dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica le funzionalità attualmente abilitate. Può essere uno dei valori seguenti.

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ Abilita \_ la \_ rappresentazione del ripristino SSL \_ | Se abilitata, WinHTTP Annulla temporaneamente la rappresentazione client per la durata delle operazioni di autenticazione del certificato SSL. Questo valore può essere impostato solo nell'handle della sessione. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ Abilita \_ \_ revoca SSL | Se abilitata, WinHTTP consente la revoca SSL. Questo valore può essere impostato solo nell'handle della richiesta. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_opzione WinHTTP \_ Abilita \_ \_ protocollo http**
</dt> <dd> <dl> <dt>



Imposta una maschera di bit DWORD di versioni HTTP avanzate accettabili. I valori possibili sono:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_Flag di protocollo WinHTTP \_ \_ HTTP2 (0x1) | Abilita HTTP/2 per la richiesta. |
| Nessuno (0x0) | Limita la richiesta a HTTP/1.1 e versioni precedenti. |

Non è possibile disabilitare le versioni legacy di HTTP (1,1 e precedenti) con questa opzione. Il valore predefinito è 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_opzione WinHTTP \_ ENABLETRACING**
</dt> <dd> <dl> <dt>



Imposta un valore **bool** che specifica se la traccia è attualmente abilitata. Per ulteriori informazioni sulla funzionalità di traccia in WinHTTP, vedere la pagina relativa alla [funzionalità di traccia WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md). Questa opzione può essere impostata solo su un handle **HINTERNET** **null** .


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**\_opzione WinHTTP \_ Encode \_ extra**
</dt> <dd> <dl> <dt>



Abilita la codifica URL percentuale per percorso e stringa di query.

In alternativa, è possibile codificare la percentuale prima di chiamare WinHttp.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ errore esteso dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera un valore unsigned long integer che contiene un codice di errore di Microsoft Windows Sockets di cui è stato eseguito il mapping ai \_ messaggi di errore WinHTTP di errore \_ \* restituiti per ultimi in questo contesto del thread. È possibile passare **null** come valore dell'handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_opzione WinHTTP \_ \_ proxy globale \_ credenziali**
</dt> <dd> <dl> <dt>



Accetta un puntatore a una [**struttura \_ credenziali WinHTTP \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *HINTERNET* impostato su **null**. Questa opzione richiede la chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings. ShareCredsWithWinHttp**. Se questa chiave del registro di sistema non è impostata, WinHTTP restituirà l' **errore errore \_ WinHTTP \_ non valido \_**. Questa chiave del registro di sistema non è presente per impostazione predefinita. Quando è impostato, WinINet invierà le credenziali a WinHTTP. Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono state impostate credenziali sull'handle corrente, utilizzerà le credenziali fornite da WinINet. Per condividere le credenziali del server oltre alle credenziali proxy, gli utenti devono impostare l' **opzione WinHTTP per l' \_ \_ utilizzo delle \_ \_ \_ credenziali globali del server** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_opzione WinHTTP \_ \_ server globale \_ credenziali**
</dt> <dd> <dl> <dt>



Accetta un puntatore a una [**struttura \_ credenziali WinHTTP \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *HINTERNET* impostato su **null**. Questa opzione richiede la chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings. ShareCredsWithWinHttp**. Se questa chiave del registro di sistema non è impostata, WinHTTP restituirà l' **errore errore \_ WinHTTP \_ non valido \_**. Questa chiave del registro di sistema non è presente per impostazione predefinita. Quando è impostato, WinINet invierà le credenziali a WinHTTP. Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono state impostate credenziali sull'handle corrente, utilizzerà le credenziali fornite da WinINet. Per condividere le credenziali del server oltre alle credenziali proxy, gli utenti devono impostare l' **opzione WinHTTP per l' \_ \_ utilizzo delle \_ \_ \_ credenziali globali del server** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**\_tipo di \_ handle dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera un valore long integer senza segno che contiene il tipo dell'handle [HINTERNET](hinternet-handles-in-winhttp.md) passato. Il valore restituito può essere uno dei seguenti:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_connessione del \_ tipo di handle WinHTTP \_ | L'handle è un handle di connessione. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_richiesta del \_ tipo di handle WinHTTP \_ | L'handle è un handle di richiesta. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_sessione del \_ tipo di handle WinHTTP \_ | L'handle è un handle di sessione. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**il \_ protocollo HTTP dell'opzione WinHTTP è \_ \_ \_ obbligatorio**
</dt> <dd> <dl> <dt>



Impedisce che le versioni del protocollo diverse da quelle abilitate dall' **opzione WinHTTP abilitano l'uso del \_ \_ \_ \_ protocollo http** per la richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_opzione WinHTTP \_ \_ protocollo http \_ usato**
</dt> <dd> <dl> <dt>



Ottiene un valore DWORD che indica quale versione HTTP avanzata è stata utilizzata per una determinata richiesta. Per un elenco di valori possibili, vedere **\_ opzione WinHTTP \_ Abilita \_ \_ protocollo http**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_opzione WinHTTP \_ \_ versione http**
</dt> <dd> <dl> <dt>



Imposta o Recupera una struttura di [**\_ \_ informazioni sulla versione http**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) che contiene la versione http supportata. Si tratta di un'opzione a livello di processo. utilizzare **null** per l'handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_opzione WinHTTP \_ ignorare la revoca del \_ certificato \_ \_ offline**
</dt> <dd> <dl> <dt>



Consente alle connessioni sicure di usare i certificati di sicurezza per i quali non è stato possibile scaricare l'elenco di revoche di certificati.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_Opzione WinHTTP \_ - \_ fallback rapido IPv6 \_**
</dt> <dd> <dl> <dt>



Abilita il fallback rapido IPv6 (più a occhi più contenti) per la connessione. Questo comportamento è simile al comportamento degli occhi felici descritto in [RFC 6555](https://tools.ietf.org/html/rfc6555) per migliorare i tempi di connessione nelle reti in cui IPv6 non è affidabile.
- Se gli indirizzi IPv6 e IPv4 vengono risolti per un determinato host, WinHttp inizierà con la connessione al primo indirizzo IPv6 risolto con un timeout breve (300 ms).
- Se la connessione ha esito negativo, WinHttp tenterà di connettersi al primo indirizzo IPv4 risolto con il timeout standard.
- Se la seconda connessione ha esito negativo, WinHttp tenterà di ritentare il primo indirizzo IPv6 risolto con il timeout standard.
- Se la terza connessione ha esito negativo, WinHttp ripristinerà il comportamento predefinito per tutti gli indirizzi rimanenti, tentando di connettersi a ognuno con il timeout standard fino a quando non viene effettuata una connessione o non rimangono indirizzi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**l' \_ opzione WinHTTP \_ è la \_ risposta di \_ connessione proxy \_**
</dt> <dd> <dl> <dt>



Ottiene un valore che indica se è possibile recuperare una risposta di connessione del proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Opzione WinHTTP \_ numero massimo di \_ conn \_ per \_ \_ Server 1 0 \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server HTTP/1.0. Il valore predefinito è **infinito**.

**Windows Vista con SP1 e Windows Server 2008:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_opzione WinHTTP \_ numero massimo di \_ conn \_ per \_ Server**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per server. Il valore predefinito è **infinito**.

Quando questa opzione è impostata su zero, WinHTTP imposta il limite per il numero di connessioni a 2.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_opzione WinHTTP \_ numero massimo di \_ \_ \_ reindirizzamenti automatici http**
</dt> <dd> <dl> <dt>



Imposta il numero massimo di reindirizzamenti che WinHTTP segue; il valore predefinito è 10. Questo limite impedisce ai siti non autorizzati di far sospendere il client WinHTTP dopo un numero elevato di reindirizzamenti.

**Windows XP con SP1 e windows 2000 con SP3:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_opzione WinHTTP \_ numero \_ massimo \_ stato http \_ continua**
</dt> <dd> <dl> <dt>



Il numero massimo di risposte del codice di stato 100-199 informativo ignorate prima di restituire il codice di stato finale al client WinHTTP. I codici di stato informativi 100-199 possono essere inviati dal server prima del codice di stato finale e sono descritti nella specifica per HTTP/1.1 (per ulteriori informazioni, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). Il valore predefinito è 10.

**Windows XP con SP1 e windows 2000 con SP3:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**\_ \_ dimensioni massime \_ \_ svuotamento risposta \_ opzione WinHTTP**
</dt> <dd> <dl> <dt>



Oggetto associato alla quantità di dati svuotati dalle risposte per riutilizzare una connessione, specificata in byte. Il valore predefinito è 1 MB.

**Windows XP con SP1 e windows 2000 con SP3:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_ \_ dimensioni massime \_ \_ intestazione risposta \_ opzione WinHTTP**
</dt> <dd> <dl> <dt>



Set associato alla dimensione massima della parte di intestazione della risposta del server, specificato in byte. Questo limite protegge il client da un server non autorizzato che tenta di bloccare il client inviando una risposta con una quantità infinita di dati di intestazione. Il valore predefinito è 64KB.

**Windows XP con SP1 e windows 2000 con SP3:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ handle padre dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'handle padre per questo handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**testo per la personalizzazione dell' \_ opzione WinHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Recupera una stringa che contiene il testo di [*cobranding*](glossary.md) fornito dal server di accesso Passport. Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401. Un'applicazione deve passare una dimensione del buffer, in byte, sufficientemente grande da mantenere la stringa restituita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_URL di \_ \_ copersonalizzazione dell'opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera una stringa che contiene un URL per un'immagine di [*cobranding*](glossary.md) fornita dal server di accesso Passport. Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401. Un'applicazione deve passare una dimensione del buffer, in byte, sufficientemente grande da mantenere la stringa restituita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_opzione WinHTTP \_ - \_ URL restituito Passport \_**
</dt> <dd> <dl> <dt>



Imposta un'opzione di sola lettura su un handle di richiesta che recupera l'URL di ritorno Passport.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_opzione WinHTTP \_ - \_ disconnessione Passport \_**
</dt> <dd> <dl> <dt>



Imposta l'opzione in un handle di sessione per disconnettersi da qualsiasi account di accesso Passport. Un'applicazione deve passare l'URL di ritorno al passaporto recuperato con l' **\_ opzione WinHTTP \_ Passport \_ return \_ URL**. Tutti i cookie correlati all'URL restituito vengono cancellati.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_password opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore stringa che contiene la password associata a un handle di richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_proxy dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o Recupera una struttura di [**\_ \_ informazioni proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) che contiene i dati del proxy su un handle di sessione o un handle di richiesta esistente. Quando si recuperano i dati proxy, un'applicazione deve liberare le stringhe **lpszProxy** e **lpszProxyBypass** contenute in questa struttura (se sono non **null**) utilizzando la funzione [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Un'applicazione può eseguire una query per i dati globali del proxy (proxy predefinito) passando un handle **null** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_ \_ password proxy opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore stringa che contiene la password utilizzata per accedere al proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**\_SPN del proxy dell'opzione WinHTTP \_ \_ \_ usato**
</dt> <dd> <dl> <dt>



Ottiene il nome dell'entità del server proxy fornito da WinHTTP a SSPI durante l'autenticazione. Questo valore stringa è usefor passando a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) dopo un errore di autenticazione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_ \_ nome utente proxy opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore stringa che contiene il nome utente utilizzato per accedere al proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_dimensioni del \_ buffer di lettura dell'opzione WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Questa opzione è stata deprecata. non ha alcun effetto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**\_risposta di \_ \_ connessione proxy \_ di ricezione opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta un valore che indica se è possibile recuperare l'entità di risposta del proxy. Questa opzione è disabilitata per impostazione predefinita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_timeout di \_ \_ risposta ricezione opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, di attesa per la ricezione di tutte le intestazioni di risposta a una richiesta. Se WinHTTP non riesce a ricevere tutte le intestazioni entro questo periodo di timeout, la richiesta viene annullata. Il valore di timeout predefinito è 90 secondi.

Questo timeout viene controllato solo quando i dati vengono ricevuti dal socket. Di conseguenza, quando il timeout scade, l'applicazione client non riceve una notifica finché non arriva un numero maggiore di dati dal server. Se non arrivano dati dal server, il ritardo tra la scadenza del timeout e la notifica dell'applicazione client potrebbe essere pari a quello del valore di timeout impostato utilizzando il parametro *dwReceiveTimeout* della funzione [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_timeout di \_ ricezione dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta parziale a una richiesta o leggere alcuni dati. Se la risposta richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata. Il valore di timeout predefinito è di 30 secondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_criteri di \_ Reindirizzamento \_ Opzioni WinHTTP**
</dt> <dd> <dl> <dt>



Imposta il comportamento di WinHTTP sulla gestione di un codice di stato di reindirizzamento HTTP di 30x. Questa opzione può essere impostata su un handle di sessione o di richiesta su uno dei valori seguenti:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_criteri di \_ Reindirizzamento opzioni WinHTTP \_ \_ sempre | Tutti i reindirizzamenti vengono seguiti automaticamente. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ criteri di reindirizzamento opzioni WinHTTP non \_ \_ consentono \_ https \_ per \_ http | Vengono seguiti tutti i reindirizzamenti, ad eccezione di quelli che hanno origine da un URL protetto (HTTPS) a un URL non sicuro (http). Si tratta dell'impostazione predefinita. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_criteri di \_ Reindirizzamento opzioni WinHTTP \_ \_ mai | I reindirizzamenti non vengono mai seguiti. Lo stato 30x viene restituito all'applicazione. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_opzione WinHTTP \_ rifiutare \_ USERPWD \_ nell' \_ URL**
</dt> <dd> <dl> <dt>



Rifiuta gli URL contenenti un nome utente e una password. Questa opzione rifiuta anche gli URL che contengono la semantica *username: password* , anche se non è specificato alcun nome utente o password. Ad esempio, " u:p@hostname ", " :@hostname ", " u:@hostname " e " :p@hostname " verrebbero tutti contrassegnati come non validi. Se alla funzione viene passato un URL non valido, viene restituito [l' \_ errore \_ WinHTTP \_ non valido](error-messages.md). Per impostazione predefinita, questa opzione è disabilitata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_ \_ priorità richiesta opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Questa opzione è stata deprecata. non ha alcun effetto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_statistiche delle \_ richieste di opzioni WinHTTP \_**
</dt> <dd> <dl> <dt>



Statistiche recupera per la richiesta.  Per un elenco delle statistiche disponibili, vedere [**WinHTTP \_ Request \_ Statistics**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_tempi di \_ richiesta dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Informazioni sull'intervallo di recupera per la richiesta. Per un elenco degli intervalli disponibili, vedere [**\_ \_ tempi di richiesta WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**\_ \_ timeout risoluzione opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per la risoluzione di un nome host. Il valore di timeout predefinito è **infinito**. Se viene specificato un valore non predefinito, si verifica un sovraccarico di una creazione di thread per risoluzione dei nomi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**\_protocolli di \_ sicurezza delle opzioni WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica quali protocolli di sicurezza sono accettabili. Per impostazione predefinita, solo SSL3 e TLS1 sono abilitati in Windows 7 e Windows 8. Per impostazione predefinita, solo SSL3, TLS 1.0, TLS 1.1 e TLS 1.2 sono abilitati in Windows 8.1 e Windows 10. Il valore può essere una combinazione di uno o più dei valori seguenti.

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>FLAG WINHTTP- \_ \_ protocollo sicuro- \_ \_ tutto | È possibile usare i protocolli Secure Sockets Layer (SSL) 2,0, SSL 3,0 e Transport Layer Security (TLS) 1,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>FLAG WINHTTP- \_ \_ \_ protocollo protetto \_ SSL2 | Il protocollo SSL 2,0 può essere usato. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>FLAG WINHTTP- \_ \_ \_ protocollo protetto \_ SSL3 | Il protocollo SSL 3,0 può essere usato. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>FLAG WINHTTP- \_ \_ \_ protocollo protetto \_ TLS1 | Il protocollo TLS 1,0 può essere usato. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Protocollo WinHTTP \_ flag \_ Secure \_ TLS1 \_ 1 | Il protocollo TLS 1,1 può essere usato. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Protocollo WinHTTP \_ flag \_ Secure \_ TLS1 \_ 2 | Il protocollo TLS 1,2 può essere usato. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_ \_ struct certificato di sicurezza opzione \_ WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera il certificato per un server SSL/TLS nella struttura [**delle \_ \_ informazioni del certificato WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . L'applicazione deve liberare i membri **lpszSubjectInfo** e **lpszIssuerInfo** con [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_flag di \_ sicurezza delle opzioni WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene i flag di sicurezza per un handle. Può essere una combinazione di questi valori:

| Termine | Descrizione |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>FLAG di sicurezza \_ \_ Ignora \_ certificato \_ CN \_ non valido |Consente un nome comune non valido in un certificato; ovvero, il nome del server specificato dall'applicazione non corrisponde al nome comune nel certificato. Se questo flag è impostato, l'applicazione non riceve un callback **del \_ certificato di stato di callback WinHTTP non \_ \_ \_ \_ \_ valido** . |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>FLAG di sicurezza \_ \_ Ignora \_ certificato \_ data \_ non valido |Consente la data di un certificato non valido, ovvero un certificato scaduto o non ancora valido. Se questo flag è impostato, l'applicazione non riceve un callback **del \_ flag di stato del callback WinHTTP \_ data non \_ \_ \_ \_ valido** . |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ CA sconosciuta | Consente un'autorità di certificazione non valida. Se questo flag è impostato, l'applicazione non riceve un callback **della \_ \_ CA non \_ \_ valido del \_ flag di stato di callback WinHTTP** . |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>il \_ flag di sicurezza \_ Ignora l' \_ utilizzo del certificato \_ non corretto \_ | Consente di stabilire l'identità di un server con un certificato non server (ad esempio, un certificato client). |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>FLAG di sicurezza \_ \_ Ignora \_ \_ firma debole | Consente di ignorare una firma vulnerabile.<br/>Questo flag è disponibile nell'aggiornamento cumulativo per ogni sistema operativo a partire da Windows 7 e Windows Server 2008 R2. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>FLAG di sicurezza \_ \_ sicuro | USA i trasferimenti sicuri. Questa operazione viene restituita solo in una chiamata a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>livello \_ medio del flag di sicurezza \_ \_ | Usa la crittografia media (a 56 bit). Questa operazione viene restituita solo in una chiamata a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>sicurezza del flag di sicurezza \_ \_ \_ avanzata | Usa la crittografia complessa (a 128 bit). Questa operazione viene restituita solo in una chiamata a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>resistenza al flag di sicurezza \_ \_ \_ debole | Usa la crittografia debole (a 40 bit). Questa operazione viene restituita solo in una chiamata a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**\_informazioni di \_ sicurezza sull'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Recupera la connessione SChannel e le informazioni di crittografia per una richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_chiave di sicurezza dell'opzione WinHTTP \_ \_ \_ bit**
</dt> <dd> <dl> <dt>



Recupera un valore long integer senza segno che contiene il livello di codifica della chiave di crittografia. Un numero maggiore indica una crittografia più avanzata del livello di crittografia.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ timeout invio opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per inviare una richiesta o scrivere alcuni dati. Se l'invio della richiesta richiede più tempo del timeout, l'operazione di invio viene annullata. Il timeout predefinito è 30 secondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_Server opzioni \_ WinHTTP \_ CBT**
</dt> <dd> <dl> <dt>



Ottiene un puntatore alla struttura di [**\_ Binding SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) che specifica un token di associazione di canale (CBT).

Un token di associazione di canale è una proprietà di un canale di trasporto sicuro e viene utilizzato per associare un canale di autenticazione al canale di trasporto protetto. Questo token può essere ottenuto solo tramite questa opzione dopo che è stata stabilita una connessione SSL.

> [!Note]
> Se si passa questa opzione e un valore **null** per *lpBuffer* a [**WINHTTPQUERYOPTION**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) , viene restituito l'errore \_ buffer insufficiente \_ e le dimensioni di byte richieste per il buffer nel parametro *lpdwBufferLength* . Il valore della dimensione del buffer restituito può essere passato in una chiamata successiva a query per il token di associazione del canale. Questi passaggi sono necessari \_ \_ \_ per la gestione della richiesta di stato di callback WinHTTP se si desidera modificare le intestazioni della richiesta in base al token di associazione del canale. Si noti che Windows XP e vista non supportano la modifica delle intestazioni delle richieste durante questo callback.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_ \_ \_ contesto catena di certificati \_ server \_ Opzioni WinHTTP**
</dt> <dd> <dl> <dt>



Recupera il contesto della catena di certificazione server. **WinHTTP \_ È possibile passare il \_ \_ \_ \_ contesto della catena** di certificati del server di opzione per ottenere un puntatore duplicato al **\_ \_ contesto della catena** di certificati per una catena di certificati server ricevuta durante una connessione SSL negoziata. Il client deve chiamare [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sul puntatore di contesto PCCERT restituito \_ che viene inserito nel buffer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_ \_ \_ contesto certificato server opzioni \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera il contesto di certificazione del server. **WinHTTP \_ È possibile passare il \_ \_ \_ contesto** del certificato del server per ottenere un puntatore duplicato al [**contesto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) del certificato per un certificato del server ricevuto durante una connessione SSL negoziata. Il client deve chiamare [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) sul puntatore di contesto PCCERT restituito \_ che viene inserito nel buffer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**\_ \_ nome SPN Server opzioni WinHTTP \_ \_ usato**
</dt> <dd> <dl> <dt>



Ottiene il nome dell'entità server server fornito da WinHTTP a SSPI durante l'autenticazione. Questo valore stringa può essere passato a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) dopo un errore di autenticazione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_ \_ nome SPN opzione WinHTTP**
</dt> <dd> <dl> <dt>



Include o rimuove il numero di porta del server quando il nome SPN (nome dell'entità servizio) viene compilato per Kerberos o negozia l'autenticazione Kerberos. Questo flag è uno dei valori seguenti:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>\_disabilitare la \_ \_ porta del server SPN \_ | Rimuove il numero di porta del server. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_Abilita WinHTTP \_ \_ porta server \_ SPN | Include il numero di porta del server. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_opzione WinHTTP \_ - \_ apertura rapida TCP \_**
</dt> <dd> <dl> <dt>



Consente l'apertura rapida di TCP per la connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**opzione WINHTTP ( \_ \_ avvio) TLS \_ false \_**
</dt> <dd> <dl> <dt>



Abilita l'avvio di TLS false per la connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_evento di \_ scaricamento dell'opzione WinHTTP \_ Notify \_**
</dt> <dd> <dl> <dt>



Accetta un evento che verrà impostato al completamento dell'ultimo callback per una determinata sessione. Questo flag deve essere utilizzato in un handle di sessione. Non è possibile chiudere l'evento finché non è stato impostato da WinHTTP.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**opzione WINHTTP- \_ \_ analisi dell'intestazione non sicura \_ \_**
</dt> <dd> <dl> <dt>



Questa opzione è riservata per uso interno e non deve essere chiamata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_aggiornamento dell'opzione WinHTTP \_ \_ a \_ Web \_ socket**
</dt> <dd> <dl> <dt>



Indica allo stack di avviare un processo di handshake WebSocket con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Questa opzione non accetta parametri.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_URL opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Recupera un valore stringa che contiene l'URL completo di una risorsa scaricata. Se l'URL originale contiene dati aggiuntivi, ad esempio stringhe di ricerca o ancoraggi, oppure se la chiamata è stata reindirizzata, l'URL restituito è diverso dall'originale. L'applicazione deve passare un buffer, ridimensionato in byte, sufficientemente grande da mantenere l'URL restituito in caratteri wide.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_opzione WinHTTP \_ usare \_ le \_ credenziali del server globale \_**
</dt> <dd> <dl> <dt>



Accetta un **bool** e può essere impostato solo un handle di sessione. Si propagherà solo fino a handle creati dall'handle di sessione dopo che l'opzione è stata impostata. Se **true**, questa opzione determina come ultima risorsa l'uso delle credenziali del server globale da WinInet. Il valore predefinito per questa opzione è **false**. Questa opzione richiede la chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings. ShareCredsWithWinHttp**. Questa chiave del registro di sistema non è presente per impostazione predefinita. Quando è impostato, WinINet invierà le credenziali a WinHTTP. Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono state impostate credenziali sull'handle corrente, utilizzerà le credenziali fornite da WinINet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_ \_ agente utente opzione \_ WinHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera la stringa dell' [*agente utente*](glossary.md) negli handle forniti da [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usata nelle funzioni [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) successive, purché non venga sottoposta a override da un'intestazione aggiunta da [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) o **WinHttpSendRequest**. Quando si recupera un agente utente, l'applicazione deve passare un buffer, ridimensionato in byte, che è sufficientemente grande da mantenere l'URL restituito in caratteri wide. Quando si imposta l'agente utente, le dimensioni del buffer corrispondono alla lunghezza della stringa, in caratteri, e al carattere di terminazione **null** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_ \_ nome utente opzione WinHTTP**
</dt> <dd> <dl> <dt>



Imposta o Recupera una stringa che contiene il nome utente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_timeout di \_ chiusura di Web \_ socket \_ \_ per l'opzione WinHTTP**
</dt> <dd> <dl> <dt>



Imposta il tempo, in millisecondi, che [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) deve attendere per completare l'handshake di chiusura. Il valore predefinito è 10 secondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_ \_ \_ \_ intervallo KeepAlive di Web socket per l'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta l'intervallo, in millisecondi, per l'invio di un pacchetto Keep-Alive sulla connessione. L'intervallo predefinito è 30000 (30 secondi). L'intervallo minimo è 15000 (15 secondi). Se si utilizza [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare un valore inferiore a 15000, verrà restituito con **errore \_ \_ parametro non valido**.

> [!Note]
> Il valore predefinito per **l' \_ \_ intervallo di Web \_ socket \_ KeepAlive \_ dell'opzione WinHTTP** viene letto da **HKLM: \\ software \\ Microsoft \\ WebSocket \\ keepAliveInterval**. Se non è impostato alcun valore, verrà utilizzato il valore predefinito 30000. Non è possibile avere un intervallo di KeepAlive inferiore a 15000 millisecondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**\_dimensioni del \_ \_ buffer di \_ ricezione \_ dell' \_ opzione WinHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di ricezione da usare nelle connessioni WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**\_dimensioni del \_ \_ buffer di invio del socket Web \_ \_ dell'opzione WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di invio da usare nelle connessioni WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_ \_ conteggio thread di lavoro opzione \_ WinHTTP \_**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica il numero di thread di lavoro che il pool di thread deve usare per i completamenti asincroni. Il valore predefinito di questa opzione è zero, che specifica che il numero di thread di lavoro è uguale al numero di CPU nel sistema. Questa opzione può essere impostata solo su un handle [HINTERNET](hinternet-handles-in-winhttp.md) **null** prima che si verifichi un'operazione asincrona.   Questa opzione può essere impostata solo una volta.

**Windows Server 2008 R2 e Windows 7:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_dimensioni del \_ buffer di scrittura dell'opzione WinHTTP \_ \_**
</dt> <dd> <dl> <dt>



Questa opzione è stata deprecata. non ha alcun effetto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nella tabella seguente sono elencati i flag di opzione specificando gli handle su cui possono agire, se è possibile eseguire query e impostare e il tipo di dati utilizzato. Una "X" indica che il flag di opzione è valido per l'uso con la funzione o l'handle, mentre un "-" specifica che il flag di opzione non è valido.

Se si tenta di impostare o eseguire una query su un flag di opzione in una versione di Windows in cui non è supportata, l' **\_ \_ \_ opzione errore WinHTTP non sarà valida**.

| Flag di opzione e tipo di dati | Handle di sessione | Handle di richiesta | Opzione di query | Opzione SET | Versione minima di Windows |
|-|-|-|-|-|-|
| l' \_ opzione WinHTTP ha \_ assicurato \_ \_ callback non bloccanti \_<br/>**BOOL** | X | \- | \- | X | \- |
| criteri di accesso \_ automatico opzione WinHTTP \_ \_<br/>**DWORD** | \- | X | \- | X | \- |
| \_callback di opzioni WinHTTP \_<br/>**LPVOID** | X | X | X | X | \- |
| \_contesto del \_ \_ certificato client dell'opzione \_ WinHTTP<br/>[**contesto del certificato \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| \_elenco di \_ \_ \_ autorità emittenti del certificato client dell'opzione \_ WinHTTP<br/>[**\_IssuerListInfoEx SecPkgContext**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| opzione WINHTTP-tabella \_ \_ codici<br/>**DWORD** | X | \- | \- | X | \- |
| \_opzione WinHTTP \_ Configure \_ Passport \_ AUTH<br/>**DWORD** | X | \- | \- | X | \- |
| \_tentativi di \_ connessione dell'opzione WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ timeout connessione opzione \_ WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_informazioni di \_ connessione dell'opzione WinHTTP \_<br/>[**\_informazioni di connessione WinHTTP \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| \_Opzioni WinHTTP \_ connessione \_ statistiche \_ V0<br/>[**\_Informazioni TCP \_ V0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10 versione 1903 |
| \_Opzioni WinHTTP \_ connessione \_ statistiche \_ V1<br/>[**\_Informazioni TCP \_ V1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10 versione 2004 |
| \_valore del \_ contesto dell'opzione WinHTTP \_<br/>**\_ptr DWORD** | X | X | X | X | \- |
| decompressione dell' \_ opzione WinHTTP \_<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| \_funzionalità di \_ disabilitazione dell'opzione WinHTTP \_<br/>**DWORD** | \- | X | \- | X | \- |
| \_opzione WinHTTP \_ disabilitare \_ il \_ fallback del protocollo sicuro \_<br/>**BOOL** | X | \- | \- | X | Windows 10 versione 1903 |
| \_opzione WinHTTP \_ disabilitare \_ la \_ coda di flusso<br/>**BOOL** | X | X | \- | X | Windows 10 versione 1809 |
| \_funzionalità di \_ Abilitazione dell'opzione WinHTTP \_<br/>**DWORD** | \* | \* | \- | X | \- |
| \_opzione WinHTTP \_ Abilita \_ \_ protocollo http<br/>**DWORD** | X | X | \- | X | Windows 10 versione 1607 |
| \_opzione WinHTTP \_ ENABLETRACING<br/>**DWORD** | \- | \- | X | X | \- |
| \_opzione WinHTTP \_ Encode \_ extra<br/>**BOOL** | X | X | \- | X | Windows 10 versione 1803 |
| \_ \_ errore esteso dell'opzione WinHTTP \_<br/>**DWORD** | X | X | X | \- | \- |
| \_opzione WinHTTP \_ \_ proxy globale \_ credenziali<br/>[**\_credenziali WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| \_opzione WinHTTP \_ \_ server globale \_ credenziali<br/>[**WINHTTP \_ credenziali \_ ex**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| \_tipo di \_ handle dell'opzione WinHTTP \_<br/>**DWORD** | X | X | X | \- | \- |
| il \_ protocollo HTTP dell'opzione WinHTTP è \_ \_ \_ obbligatorio<br/>**BOOL** | X | X | \- | X | Windows 10 versione 1903 |
| \_opzione WinHTTP \_ \_ protocollo http \_ usato<br/>**DWORD** | \- | X | X | \- | Windows 10 versione 1607 |
| \_opzione WinHTTP \_ \_ versione http<br/>[**\_informazioni sulla versione http \_**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| \_opzione WinHTTP \_ ignorare la revoca del \_ certificato \_ \_ offline<br/>**BOOL** | \- | X | \- | X | Windows 10 versione 2004 |
| \_Opzione WinHTTP \_ - \_ fallback rapido IPv6 \_<br/>**BOOL** | X | \- | \- | X | Windows 10 versione 1903 |
| l' \_ opzione WinHTTP \_ è la \_ risposta di \_ connessione proxy \_<br/>**BOOL** | X | X | X | \- | \- |
| \_Opzione WinHTTP \_ numero massimo di \_ conn \_ per \_ \_ Server 1 0 \_<br/>**DWORD** | X | \- | X | X | \- |
| \_opzione WinHTTP \_ numero massimo di \_ conn \_ per \_ Server<br/>**DWORD** | X | \- | X | X | \- |
| \_opzione WinHTTP \_ numero massimo di \_ \_ \_ reindirizzamenti automatici http<br/>**DWORD** | X | X | X | X | \- |
| \_opzione WinHTTP \_ numero \_ massimo \_ stato http \_ continua<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ dimensioni massime \_ \_ svuotamento risposta \_ opzione WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ dimensioni massime \_ \_ intestazione risposta \_ opzione WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ handle padre dell'opzione WinHTTP \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| testo per la personalizzazione dell' \_ opzione WinHTTP \_ \_ \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_URL di \_ \_ copersonalizzazione dell'opzione \_ WinHTTP<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_opzione WinHTTP \_ - \_ URL restituito Passport \_<br/>**LPVOID** | \- | X | X | \- | \- |
| \_opzione WinHTTP \_ - \_ disconnessione Passport \_<br/>**LPVOID** | X | \- | \- | X | \- |
| \_password opzione \_ WinHTTP<br/>**LPWSTR** | \- | X | X | X | \- |
| \_proxy dell'opzione WinHTTP \_<br/>[**\_informazioni proxy \_ WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| \_ \_ password proxy opzione \_ WinHTTP<br/>**LPWSTR** | \- | X | X | X | \- |
| \_SPN del proxy dell'opzione WinHTTP \_ \_ \_ usato<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_ \_ nome utente proxy opzione WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_dimensioni del \_ buffer di lettura dell'opzione WinHTTP \_ \_<br/>**DWORD** | \- | X | X | X | \- |
| \_risposta di \_ \_ connessione proxy \_ di ricezione opzione WinHTTP \_<br/>**BOOL** | X | X | \- | X | \- |
| \_timeout di \_ \_ risposta ricezione opzione WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_timeout di \_ ricezione dell'opzione WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_criteri di \_ Reindirizzamento \_ Opzioni WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_opzione WinHTTP \_ rifiutare \_ USERPWD \_ nell' \_ URL<br/>**BOOL** | \- | X | \- | X | \- |
| \_ \_ priorità richiesta opzione \_ WinHTTP<br/>**DWORD** | \- | X | X | X | \- |
| \_statistiche delle \_ richieste di opzioni WinHTTP \_<br/>[**\_statistiche della richiesta WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10 versione 1903 |
| \_tempi di \_ richiesta dell'opzione WinHTTP \_<br/>[**\_tempi di richiesta WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10 versione 1903 |
| \_ \_ timeout risoluzione opzione \_ WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_protocolli di \_ sicurezza delle opzioni WinHTTP \_<br/>**DWORD** | X | \- | \- | X | \- |
| \_ \_ struct certificato di sicurezza opzione \_ WinHTTP \_<br/>[**\_informazioni sul certificato WinHTTP \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| \_flag di \_ sicurezza delle opzioni WinHTTP \_<br/>**DWORD** | \- | X | X | X | \- |
| \_informazioni di \_ sicurezza sull'opzione WinHTTP \_<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10 versione 2004 |
| \_chiave di sicurezza dell'opzione WinHTTP \_ \_ \_ bit<br/>**DWORD** | \- | X | X | \- | \- |
| \_ \_ timeout invio opzione \_ WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| \_Server opzioni \_ WinHTTP \_ CBT<br/>[**\_Binding SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| \_ \_ \_ contesto catena di certificati \_ server \_ Opzioni WinHTTP<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10 versione 2004 |
| \_ \_ \_ contesto certificato server opzioni \_ WinHTTP<br/>[**CONTESTO DEL CERTIFICATO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| \_ \_ nome SPN Server opzioni WinHTTP \_ \_ usato<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_ \_ nome SPN opzione WinHTTP<br/>**DWORD** | \- | X | \- | X | \- |
| \_opzione WinHTTP \_ - \_ apertura rapida TCP \_<br/>**BOOL** | X | \- | \- | X | Windows 10 versione 2004 |
| opzione WINHTTP ( \_ \_ avvio) TLS \_ false \_<br/>**BOOL** | X | \- | \- | X | Windows 10 versione 2004 |
| \_evento di \_ scaricamento dell'opzione WinHTTP \_ Notify \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| opzione WINHTTP- \_ \_ analisi dell'intestazione non sicura \_ \_<br/>**DWORD** | \- | X | \- | X | \- |
| \_aggiornamento dell'opzione WinHTTP \_ \_ a \_ Web \_ socket<br/>N/D | \- | X | \- | X | \- |
| \_URL opzione \_ WinHTTP<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_opzione WinHTTP \_ usare \_ le \_ credenziali del server globale \_<br/>**BOOL** | X | X | \- | X | \- |
| \_ \_ agente utente opzione \_ WinHTTP<br/>**LPWSTR** | X | \- | X | X | \- |
| \_ \_ nome utente opzione WinHTTP<br/>**LPWSTR** | \- | X | X | X | \- |
| \_timeout di \_ chiusura di Web \_ socket \_ \_ per l'opzione WinHTTP<br/>**DWORD** | \- | \- | X | X | \- |
| \_ \_ \_ \_ intervallo KeepAlive di Web socket per l'opzione WinHTTP \_<br/>**DWORD** | \- | \- | X | X | \- |
| \_dimensioni del \_ \_ buffer di \_ ricezione \_ dell' \_ opzione WinHTTP<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| \_dimensioni del \_ \_ buffer di invio del socket Web \_ \_ dell'opzione WinHTTP \_<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| \_ \_ conteggio thread di lavoro opzione \_ WinHTTP \_<br/>**DWORD** | \- | \- | \- | X | \- |
| \_dimensioni del \_ buffer di scrittura dell'opzione WinHTTP \_ \_<br/>**DWORD** | \- | X | X | X | \- |

> [!Note]
> Per Windows XP e Windows 2000, vedere [requisiti di run-time](winhttp-start-page.md).

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]            |
| Server minimo supportato | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]         |
| Componente ridistribuibile          | WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000. |
| Intestazione                   | WinHTTP. h                                                                       |

## <a name="see-also"></a>Vedi anche

[Versioni WinHTTP](winhttp-versions.md)
