---
Description: I flag di opzione seguenti sono supportati da WinHttpQueryOption e WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Flag di opzione (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: ecc3d27bd8d168c276ccac2544dbc648fbdfee5732e87892624903285b3a2fcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744062"
---
# <a name="option-flags"></a>Flag di opzione

I flag di opzione seguenti sono supportati [**da WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) e [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPZIONE WINHTTP \_ \_ GARANTITA \_ CALLBACK NON \_ \_ BLOCCANTI**
</dt> <dd> <dl> <dt>



Il valore predefinito è FALSE. Se impostato su TRUE, WinHTTP non garantisce lo stato di avanzamento se i callback di stato sono bloccati dall'applicazione client.

L'applicazione client deve fare particolare attenzione a eseguire operazioni minime all'interno del callback senza bloccarsi, per restituire il più rapidamente possibile e, in particolare, non deve attendere le chiamate WinHTTP successive. Se non segue queste linee guida, è probabile che si sia verificata un'impatto negativo sulle prestazioni o un potenziale blocco dell'applicazione. Se usata nel modo prescritto, questa opzione può migliorare le prestazioni.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**CRITERIO DI \_ ACCESSO \_ AUTOMATICO DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica i criteri [di accesso automatico](authentication-in-winhttp.md) con uno dei valori seguenti.

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>LIVELLO DI SICUREZZA ACCESSO AUTOMATICO WINHTTP \_ \_ \_ \_ ELEVATO | Le credenziali predefinite non vengono usate. Si noti che questo flag ha effetto solo se si specifica il server in base al nome effettivo del computer. Non avrà effetto se si specifica il server in base a "localhost" o all'indirizzo IP. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>LIVELLO DI SICUREZZA ACCESSO AUTOMATICO WINHTTP \_ \_ \_ \_ BASSO | Per tutte le richieste viene eseguito un accesso autenticato con le credenziali predefinite. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>LIVELLO DI SICUREZZA ACCESSO AUTOMATICO WINHTTP \_ \_ \_ \_ MEDIO | Un accesso autenticato con le credenziali predefinite viene eseguito solo per le richieste nella Intranet locale. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**CONNESSIONI IN \_ BACKGROUND DELL'OPZIONE WINHTTP \_ \_**
</dt> <dd> <dl> <dt>

Quando si imposta questa opzione su un handle di sessione, è necessario passare il numero di connessioni da aprire. Quindi, al primo invio di una richiesta, invece di aprire una sola connessione, WinHttp apre una serie di connessioni in parallelo. In questo modo è possibile migliorare le prestazioni delle richieste successive alla stessa destinazione, senza il sovraccarico della creazione della connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**CALLBACK \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera il puntatore al set di funzioni di callback [**con WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**CONTESTO DEL CERTIFICATO \_ \_ CLIENT \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Imposta il contesto del certificato client. Se un'applicazione riceve [**l'errore \_ ERRORE WINHTTP CLIENT \_ \_ \_ AUTH CERT \_ NEEDED**](error-messages.md), deve chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per fornire un certificato prima di ritentare la richiesta. Come parte dell'elaborazione di questa opzione, WinHttp chiama [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) nel contesto del certificato fornito dal chiamante in modo che il contesto del certificato possa essere rilasciato in modo indipendente dal chiamante.

> [!Note]
> L'applicazione non deve tentare di chiudere l'archivio certificati con il flag CERT CLOSE STORE FORCE FLAG nella chiamata a \_ \_ \_ \_ [**CertCloseStore nell'archivio**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) certificati da cui è stato recuperato il contesto del certificato. Può verificarsi una violazione di accesso.

Quando il server richiede un certificato client, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) restituisce un [**errore \_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED.**](error-messages.md) Se il server richiede il certificato ma non lo richiede, l'applicazione può specificare questa opzione per indicare che non dispone di un certificato. Il server può scegliere un altro schema di autenticazione o consentire l'accesso anonimo al server. L'applicazione fornisce la macro **WINHTTP \_ NO CLIENT \_ \_ CERT \_ CONTEXT** nel parametro *lpBuffer* di [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) come illustrato nell'esempio di codice seguente.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Se il server richiede un certificato client, può inviare un codice di stato HTTP 403 in risposta. Per altre informazioni, vedere **l'opzione WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ ISSUER \_ LIST.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**ELENCO AUTORITÀ \_ DI CERTIFICAZIONE DEL CERTIFICATO CLIENT \_ \_ \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera una [**struttura SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) quando l'errore da [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) è **ERROR \_ WINHTTP CLIENT \_ \_ \_ AUTH CERT \_ NEEDED**. L'elenco di autorità di certificazione nella struttura contiene un elenco di autorità di certificazione (CA) accettabili dal server. L'applicazione client può filtrare l'elenco di autorità di certificazione per recuperare il certificato client per l'autenticazione SSL.

In alternativa, se il server richiede il certificato client, ma non lo richiede, l'applicazione può chiamare [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con l'opzione **WINHTTP \_ OPTION CLIENT \_ \_ CERT \_ CONTEXT.** Per altre informazioni, vedere **l'opzione \_ WINHTTP OPTION \_ CLIENT \_ CERT \_ CONTEXT.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**TABELLA CODICI \_ \_ DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Imposta la [*tabella codici*](glossary.md) usata per elaborare l'URL, ovvero la stringa di query. Il valore predefinito è UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**OPZIONE WINHTTP \_ \_ - CONFIGURARE \_ \_ L'AUTENTICAZIONE PASSPORT**
</dt> <dd> <dl> <dt>



Imposta un valore long integer non firmato che specifica se l'autenticazione [Passport nell'autenticazione WinHTTP](passport-authentication-in-winhttp.md) è abilitata. I possibili valori sono i seguenti:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ AUTH | Microsoft Passport'autenticazione è disabilitata. Questo è il valore predefinito. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ KEYRING | Il keyring Passport è disabilitato. Questo è il valore predefinito. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>ABILITARE \_ \_ L'AUTENTICAZIONE PASSPORT \_ WINHTTP | L'autenticazione Passport è abilitata. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING | Il keyring Passport è abilitato. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**TENTATIVI \_ DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero di tentativi di connessione a un host da parte diWinHTTP. Microsoft Windows http services (WinHTTP) tenta solo una volta per ogni indirizzo IP (Internet Protocol). Ad esempio, se si tenta di connettersi a un host multihomed con 10 indirizzi IP e **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è impostato su 7, WinHTTP prova a connettersi solo ai primi sette indirizzi IP. Dato lo stesso set di 10 indirizzi IP, se **l'opzione WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è impostata su 20, WinHTTP tenta ognuno dei 10 una sola volta. Se un tentativo di connessione ha ancora esito negativo dopo il numero specificato di tentativi o se il timeout di connessione è scaduto prima di allora, la richiesta viene annullata. Il valore predefinito per **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** è cinque tentativi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**TIMEOUT DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, espresso in millisecondi. L'impostazione di questa opzione su infinito (0xFFFFFFFF) disabiliterà questo timer.

Se una richiesta di connessione TCP richiede più tempo di questo valore di timeout, la richiesta viene annullata. Il timeout predefinito è 60 secondi. Quando si tenta di connettersi a più indirizzi IP per un singolo host (un host multihomed), il limite di timeout è per ogni singola connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**INFORMAZIONI DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'indirizzo IP di origine e di destinazione e la porta della richiesta che ha generato la risposta quando viene restituito [**WinHttpReceiveResponse.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) L'applicazione [**chiama WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con l'opzione **WINHTTP OPTION CONNECTION \_ \_ \_ INFO** e fornisce la struttura [**WINHTTP CONNECTION \_ \_ INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) nel *parametro lpBuffer.* Per altre informazioni, vedere **INFORMAZIONI SULLA \_ CONNESSIONE \_ WINHTTP.**

**Windows Server 2003 con SP1 e Windows XP con SP2:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V0**
</dt> <dd> <dl> <dt>



Ricostruisce lo struct [**TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) per la connessione sottostante usata dalla richiesta. Lo struct restituito può contenere statistiche provenienti da richieste precedenti inviate sulla stessa connessione.

> [!Note]
> Questa opzione è stata sostituita da **WINHTTP \_ OPTION CONNECTION \_ \_ STATS \_ V1.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V1**
</dt> <dd> <dl> <dt>



Ricostruisce lo struct [**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) per la connessione sottostante usata dalla richiesta. Lo struct restituito può contenere statistiche provenienti da richieste precedenti inviate sulla stessa connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**VALORE DI CONTESTO \_ \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un **\_ PTR DWORD** che contiene un puntatore al valore di contesto associato a questo handle [HINTERNET.](hinternet-handles-in-winhttp.md) Viene usato il valore archiviato nel buffer e al flag di **opzione WINHTTP \_ OPTION CONTEXT \_ \_ VALUE** viene assegnato un nuovo valore.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_ \_ DECOMPRESSIONE DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Imposta un valore DWORD di flag che determina se WinHTTP decomprime automaticamente i corpi di risposta con codifiche contenuto compresse. WinHTTP imposta anche un'intestazione Accept-Encoding appropriata, eseguendo l'override di qualsiasi elemento fornito dal chiamante. I valori supportati sono:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>FLAG \_ DI DECOMPRESSIONE \_ \_ WINHTTP GZIP | Decomprimere Content-Encoding: risposte gzip. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>FLAG DI \_ DECOMPRESSIONE WINHTTP \_ \_ DEFLATE | Decomprimere Content-Encoding: deflare le risposte. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>FLAG \_ DI DECOMPRESSIONE WINHTTP \_ \_ ALL | Decomprimere le risposte con qualsiasi codifica contenuto supportata. |

Per impostazione predefinita, WinHTTP recapita risposte compresse al chiamante senza modifiche.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**OPZIONE WINHTTP \_ PER \_ DISABILITARE \_ LA COMPILAZIONE DELLA CATENA \_ DI \_ CERTIFICATI**
</dt> <dd> <dl> <dt>


L'impostazione di questa opzione su un handle di sessione WinHttp consente di abilitare o disabilitare la creazione della catena di certificati del server.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**OPZIONE WINHTTP \_ \_ DISABILITA \_ FUNZIONALITÀ**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica quali funzionalità sono disabilitate con uno o più dei flag seguenti. Tenere presente che questa funzionalità deve essere passata a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) solo in handle di richiesta dopo che l'handle della richiesta è stato creato con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)e prima che la richiesta venga inviata [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>DISABILITARE \_ L'AUTENTICAZIONE WINHTTP \_ | L'autenticazione automatica è disabilitata. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>DISABILITARE \_ I COOKIE WINHTTP \_ | L'aggiunta automatica di intestazioni di cookie alle richieste è disabilitata. Inoltre, i cookie restituiti non vengono aggiunti automaticamente al database dei cookie. La disabilitazione dei cookie può comportare prestazioni scarse per l'autenticazione Passport. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE | Disabilita la semantica keep-alive per la connessione. La semantica keep-alive è necessaria per MSN, NTLM e altri tipi di autenticazione. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>DISABILITARE \_ I REINDIRIZZAMENTI WINHTTP \_ | Il reindirizzamento automatico è disabilitato quando si inviano richieste [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) Se il reindirizzamento automatico è disabilitato, un'applicazione deve registrare una funzione di callback perché l'autenticazione Passport riesca. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPZIONE WINHTTP \_ \_ DISABILITA IL \_ \_ FALLBACK DEL \_ PROTOCOLLO SICURO**
</dt> <dd> <dl> <dt>



Impedisce a WinHTTP di ritentare una connessione con una versione precedente del protocollo di sicurezza quando la negoziazione iniziale del protocollo non riesce.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPZIONE WINHTTP \_ DISABILITA \_ CODA DI \_ \_ FLUSSO**
</dt> <dd> <dl> <dt>



Consente alle nuove richieste di aprire una connessione HTTP/2 aggiuntiva quando viene raggiunto il limite massimo di flussi simultanei, anziché attendere il successivo flusso disponibile in una connessione esistente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**OPZIONE WINHTTP \_ \_ - ABILITARE LA \_ FUNZIONALITÀ**
</dt> <dd> <dl> <dt>



Imposta un valore di long integer senza segno che specifica le funzionalità attualmente abilitate. Può essere uno dei valori seguenti.

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION | Se abilitata, WinHTTP ripristina temporaneamente la rappresentazione del client per la durata delle operazioni di autenticazione del certificato SSL. Questo valore può essere impostato solo sull'handle di sessione. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>ABILITARE \_ LA \_ REVOCA SSL WINHTTP \_ | Se abilitata, WinHTTP consente la revoca SSL. Questo valore può essere impostato solo sull'handle della richiesta. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPZIONE WINHTTP \_ \_ ABILITA PROTOCOLLO \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Imposta una maschera di bit DWORD di versioni HTTP avanzate accettabili. I valori possibili sono:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>FLAG \_ DEL PROTOCOLLO \_ \_ WINHTTP HTTP2 (0x1) | Abilita HTTP/2 per la richiesta. |
| Nessuno (0x0) | Limita la richiesta a HTTP/1.1 e versioni precedenti. |

Le versioni legacy di HTTP (1.1 e precedenti) non possono essere disabilitate usando questa opzione. Il valore predefinito è 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**OPZIONE WINHTTP \_ \_ ABILITA \_ HTTP2 PLUS CLIENT \_ \_ \_ CERT**
</dt> <dd> <dl> <dt>


Questa opzione può essere impostata su un handle di sessione WinHttp per consentire a WinHttp di usare il contesto del certificato client fornito dal chiamante quando viene usato HTTP/2.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**OPZIONE WINHTTP \_ \_ ENABLETRACING**
</dt> <dd> <dl> <dt>



Imposta un **valore BOOL** che specifica se la traccia è attualmente abilitata. Per altre informazioni sulla funzionalità di traccia in WinHTTP, vedere [Funzionalità di traccia WinHTTP.](winhttptracecfg-exe--a-trace-configuration-tool.md) Questa opzione può essere impostata solo su un handle **HINTERNET** **NULL.**


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**OPZIONE WINHTTP \_ \_ ENCODE \_ EXTRA**
</dt> <dd> <dl> <dt>



Abilita la codifica della percentuale url per il percorso e la stringa di query.

In alternativa, è possibile eseguire la codifica percentuale prima di chiamare WinHttp.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**OPZIONE WINHTTP \_ \_ SCADENZA \_ CONNESSIONE**
</dt> <dd> <dl> <dt>



Questa opzione può essere impostata solo su un handle di richiesta ancora attivo (invio o ricezione). L'impostazione di questa opzione consente a WinHttp di interrompere la gestione delle richieste sulla connessione associata all'handle di richiesta passato. La connessione verrà chiusa dopo il completamento dell'handle della richiesta con cui viene chiamata questa opzione. Questa opzione non accetta parametri.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERRORE ESTESO \_ \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera un valore long integer senza segno che contiene un codice di errore di Microsoft Windows Sockets mappato ai messaggi di errore ERROR WINHTTP restituiti per l'ultima volta in questo \_ \_ \* contesto del thread. È possibile passare **NULL** come valore dell'handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**OPZIONE WINHTTP \_ \_ PRIMA CONNESSIONE \_ \_ DISPONIBILE**
</dt> <dd> <dl> <dt>


Per impostazione predefinita, quando WinHttp invia una richiesta, se non sono disponibili connessioni per gestire la richiesta, WinHttp tenterà di stabilire una nuova connessione e la richiesta verrà associata a questa nuova connessione. Quando si imposta questa opzione, tale richiesta verrà invece servita alla prima connessione che diventa disponibile e non necessariamente a quella stabilita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**CREDS \_ \_ PROXY GLOBALI \_ \_ DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Accetta un puntatore a [**una struttura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *hInternet* impostato su **NULL.** Questa opzione richiede la chiave del Registro **di sistema HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Impostazioni! ShareCredsWithWinHttp**. Se questa chiave del Registro di sistema non è impostata, WinHTTP restituirà **l'errore \_ ERROR WINHTTP \_ INVALID \_ OPTION**. Questa chiave del Registro di sistema non è presente per impostazione predefinita. Quando è impostata, WinINet invierà le credenziali a WinHTTP. Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet. Per condividere le credenziali del server oltre alle credenziali proxy, gli utenti devono impostare **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**CREDS \_ \_ GLOBALI DEL SERVER \_ \_ DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Accetta un puntatore a [**una struttura WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con il parametro della funzione *hInternet* impostato su **NULL.** Questa opzione richiede la chiave del Registro **di sistema HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Impostazioni! ShareCredsWithWinHttp**. Se questa chiave del Registro di sistema non è impostata, WinHTTP restituirà **l'errore \_ ERROR WINHTTP \_ INVALID \_ OPTION**. Questa chiave del Registro di sistema non è presente per impostazione predefinita. Quando è impostata, WinINet invierà le credenziali a WinHTTP. Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet. Per condividere le credenziali del server oltre alle credenziali proxy, gli utenti devono impostare **WINHTTP \_ OPTION USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DI \_ HANDLE DI \_ OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera un valore long integer senza segno che contiene il tipo dell'handle [HINTERNET](hinternet-handles-in-winhttp.md) passato. Il valore restituito può essere uno dei seguenti:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>CONNESSIONE DEL TIPO DI HANDLE WINHTTP \_ \_ \_ | L'handle è un handle di connessione. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>RICHIESTA DI TIPO HANDLE WINHTTP \_ \_ \_ | L'handle è un handle di richiesta. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESSIONE CON TIPO DI HANDLE WINHTTP \_ \_ \_ | L'handle è un handle di sessione. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**OPZIONE \_ \_ HTTP \_ PROTOCOL REQUIRED DI WINHTTP \_**
</dt> <dd> <dl> <dt>



Impedisce l'uso di versioni del protocollo diverse da quelle abilitate da **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** per la richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ USATO**
</dt> <dd> <dl> <dt>



Ottiene un valore DWORD che indica quale versione HTTP avanzata è stata utilizzata in una determinata richiesta. Per un elenco dei valori possibili, vedere **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**VERSIONE \_ \_ HTTP DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera una [**struttura HTTP \_ VERSION \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) che contiene la versione HTTP supportata. Si tratta di un'opzione a livello di processo. usare **NULL** per l'handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**OPZIONE \_ \_ WINHTTP \_ KEEPALIVE HTTP2**
</dt> <dd> <dl> <dt>


Questa opzione può essere impostata su un handle di sessione per fare in modo che WinHttp usi i frame PING HTTP/2 come meccanismo keep-live. I chiamanti specificano un timeout in millisecondi e, dopo che non è presente alcuna attività su una connessione per tale periodo di timeout, WinHttp inizierà a inviare frame PING HTTP/2. I chiamanti non possono impostare un valore di timeout inferiore a 5000 millisecondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**OPZIONE WINHTTP \_ \_ HTTP2 \_ PLUS TRANSFER \_ \_ ENCODING**
</dt> <dd> <dl> <dt>


Questa opzione può essere impostata su un handle di richiesta WinHttp per controllare il comportamento di WinHttp quando una risposta HTTP/2 contiene un'intestazione "Transfer-Encoding". In tal caso, WinHttp restituirà un errore se questa opzione è impostata su **FALSE.**


</dt> </dl> </dd> <dt>


<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**OPZIONE WINHTTP \_ \_ IGNORA REVOCA CERTIFICATO \_ \_ \_ OFFLINE**
</dt> <dd> <dl> <dt>



Consente alle connessioni protette di usare i certificati di sicurezza per i quali non è stato possibile scaricare l'elenco di revoche di certificati.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**FALLBACK \_ \_ DELL'OPZIONE IPV6 \_ FAST \_ WINHTTP**
</dt> <dd> <dl> <dt>



Abilita il fallback rapido IPv6 (Eyeballs)per la connessione. Questo comportamento è simile al comportamento di Happy Eyeballs descritto in [RFC 6555](https://tools.ietf.org/html/rfc6555) per migliorare i tempi di connessione nelle reti in cui IPv6 non è affidabile.
- Se entrambi gli indirizzi IPv6 e IPv4 vengono risolti per un determinato host, WinHttp inizierà connettendosi al primo indirizzo IPv6 risolto con un timeout breve (300 ms).
- Se la connessione non riesce, WinHttp tenterà di connettersi al primo indirizzo IPv4 risolto con il timeout standard.
- In caso di errore della seconda connessione, WinHttp ritenterà il primo indirizzo IPv6 risolto con il timeout standard.
- In caso di errore della terza connessione, WinHttp ripristina il comportamento predefinito per tutti gli indirizzi rimanenti, provando una connessione a ognuno con il timeout standard fino a quando non viene stabilita una connessione o non rimangono indirizzi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**L'OPZIONE WINHTTP \_ È LA RISPOSTA DI CONNESSIONE \_ \_ \_ \_ PROXY**
</dt> <dd> <dl> <dt>



Ottiene un valore che indica se è possibile recuperare un Connessione restituito da proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**OPZIONE \_ WINHTTP \_ MAX \_ CONNS \_ PER \_ 1 \_ 0 \_ SERVER**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server HTTP/1.0. Il valore predefinito è **INFINITE.**

**Windows Vista con SP1 e Windows Server 2008:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ SERVER**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il numero massimo di connessioni consentite per ogni server. Il valore predefinito è **INFINITE.**

Quando questa opzione è impostata su zero, WinHTTP imposta il limite per il numero di connessioni su 2.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**OPZIONE WINHTTP \_ \_ NUMERO MASSIMO DI \_ \_ \_ REINDIRIZZAMENTI HTTP AUTOMATICI**
</dt> <dd> <dl> <dt>



Imposta il numero massimo di reindirizzamenti che WinHTTP segue. il valore predefinito è 10. Questo limite impedisce ai siti non autorizzati di sospendere il client WinHTTP in seguito a un numero elevato di reindirizzamenti.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_L'OPZIONE \_ WINHTTP MAX HTTP STATUS \_ \_ \_ CONTINUE**
</dt> <dd> <dl> <dt>



Numero massimo di risposte con codice di stato informativo 100-199 ignorate prima di restituire il codice di stato finale al client WinHTTP. I codici di stato in formato informativo 100-199 possono essere inviati dal server prima del codice di stato finale e sono descritti nella specifica per HTTP/1.1 (per altre informazioni, vedere [RFC 2616).](https://www.ietf.org/rfc/rfc2616.txt) Il valore predefinito è 10.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**OPZIONE WINHTTP \_ \_ MAX RESPONSE DRAIN \_ \_ \_ SIZE**
</dt> <dd> <dl> <dt>



Limite alla quantità di dati svuotati dalle risposte per riutilizzare una connessione, specificata in byte. Il valore predefinito è 1 MB.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**DIMENSIONI MASSIME \_ INTESTAZIONE \_ RISPOSTA \_ \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Valore associato impostato sulla dimensione massima della parte di intestazione della risposta del server, specificata in byte. Questo limite protegge il client da un server non autorizzato che tenta di bloccare il client inviando una risposta con una quantità infinita di dati di intestazione. Il valore predefinito è 64 KB.

**Windows XP con SP1 e Windows 2000 con SP3:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**HANDLE PADRE \_ \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera l'handle padre per questo handle.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**TESTO \_ \_ \_ COBRANDING DELL'OPZIONE PASSPORT WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera una stringa che contiene il [*testo di cobranding*](glossary.md) fornito dal server di accesso Passport. Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401. Un'applicazione deve passare una dimensione del buffer, in byte, sufficientemente grande da contenere la stringa restituita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**URL \_ \_ \_ COBRANDING DELL'OPZIONE PASSPORT WINHTTP \_**
</dt> <dd> <dl> <dt>



Recupera una stringa che contiene un URL per un [*elemento grafico di cobranding*](glossary.md) fornito dal server di accesso Passport. Questa opzione deve essere recuperata immediatamente dopo che il server di accesso risponde con un codice di stato 401. Un'applicazione deve passare una dimensione del buffer, in byte, sufficientemente grande da contenere la stringa restituita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**URL \_ RESTITUITO \_ PASSPORT DELL'OPZIONE WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Imposta un'opzione di sola lettura su un handle di richiesta che recupera l'URL restituito di Passport.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**OPZIONE \_ \_ WINHTTP - \_ DISCONNESSIONE PASSPORT \_**
</dt> <dd> <dl> <dt>



Imposta l'opzione su un handle di sessione per disconnettersi da qualsiasi account di accesso Passport. Un'applicazione deve passare l'URL restituito di Passport recuperato con **l'URL \_ RESTITUITO \_ PASSPORT DELL'OPZIONE WINHTTP \_ \_**. Tutti i cookie correlati all'URL restituito vengono cancellati.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**PASSWORD \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore stringa contenente la password associata a un handle di richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**PROXY \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera una struttura [**WINHTTP \_ PROXY \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) che contiene i dati del proxy in un handle di sessione o in un handle di richiesta esistente. Quando si recuperano dati proxy, un'applicazione deve liberare le stringhe **lpszProxy** e **lpszProxyBypass** contenute in questa struttura (se non sono **NULL)** usando la funzione [**GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree) Un'applicazione può eseguire una query per i dati proxy globali (proxy predefinito) passando un handle **NULL.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**PASSWORD PROXY \_ \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore stringa contenente la password utilizzata per accedere al proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**NOME \_ \_ SPN PROXY \_ DELL'OPZIONE WINHTTP \_ USATO**
</dt> <dd> <dl> <dt>



Ottiene il nome dell'entità server proxy fornito da WinHTTP a SSPI durante l'autenticazione. Questo valore stringa viene utilizzato per passare a [**SspiPromptForCredentials dopo**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) un errore di autenticazione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**NOME UTENTE \_ \_ PROXY DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore stringa contenente il nome utente utilizzato per accedere al proxy.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**DIMENSIONI DEL \_ \_ BUFFER DI LETTURA \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Questa opzione è stata deprecata. non ha alcun effetto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**RISPOSTA DI CONNESSIONE \_ PROXY \_ DI RICEZIONE \_ \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Imposta un valore che indica se l'entità di risposta proxy può essere recuperata o meno. Questa opzione è disabilitata per impostazione predefinita.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**TIMEOUT DI \_ RICEZIONE \_ RISPOSTA PER \_ L'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per attendere la ricezione di tutte le intestazioni di risposta a una richiesta. Se WinHTTP non riesce a ricevere tutte le intestazioni entro questo periodo di timeout, la richiesta viene annullata. Il valore di timeout predefinito è 90 secondi.

Questo timeout viene controllato solo quando i dati vengono ricevuti dal socket. Di conseguenza, alla scadenza del timeout, l'applicazione client non viene notificata finché non arrivano altri dati dal server. Se non arrivano dati dal server, il ritardo tra la scadenza del timeout e la notifica dell'applicazione client potrebbe essere grande quanto il valore di timeout impostato usando il *parametro dwReceiveTimeout* della funzione [**WinHttpSetTimeouts.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**TIMEOUT RICEZIONE OPZIONE WINHTTP \_ \_ \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per ricevere una risposta parziale a una richiesta o leggere alcuni dati. Se la risposta richiede più tempo rispetto a questo valore di timeout, la richiesta viene annullata. Il valore di timeout predefinito è di 30 secondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta il comportamento di WinHTTP relativo alla gestione di un codice di stato di reindirizzamento HTTP 30x. Questa opzione può essere impostata su un handle di sessione o di richiesta su uno dei valori seguenti:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>CRITERIO DI \_ \_ REINDIRIZZAMENTO DELL'OPZIONE WINHTTP \_ \_ SEMPRE | Tutti i reindirizzamenti vengono seguiti automaticamente. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_L'OPZIONE WINHTTP \_ \_ REINDIRIZZA \_ I CRITERI NON CONSENTONO HTTPS A \_ \_ \_ HTTP | Vengono seguiti tutti i reindirizzamenti, ad eccezione di quelli originati da un URL sicuro (https) a un URL non sicuro (http). Si tratta dell'impostazione predefinita. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_ \_ MAI | I reindirizzamenti non vengono mai seguiti. Lo stato 30x viene restituito all'applicazione. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**OPZIONE WINHTTP \_ \_ REJECT \_ USERPWD \_ IN \_ URL**
</dt> <dd> <dl> <dt>



Rifiuta gli URL che contengono un nome utente e una password. Questa opzione rifiuta anche gli URL che contengono la semantica *username:password,* anche se non viene specificato alcun nome utente o password. Ad esempio, " u:p@hostname ", " ", " " e " " verrebbero contrassegnati :@hostname u:@hostname come non :p@hostname validi. Se alla funzione viene passato un URL non valido, restituisce [ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md). Per impostazione predefinita, questa opzione è disabilitata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**PRIORITÀ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Questa opzione è stata deprecata. non ha alcun effetto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**STATISTICHE DELLE \_ RICHIESTE \_ DI OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Rieduca le statistiche per la richiesta.  Per un elenco delle statistiche disponibili, vedere [**WINHTTP \_ REQUEST \_ STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**TEMPI DI RICHIESTA \_ \_ \_ DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Retreives timing information for the request (Retreives timing information for the request). Per un elenco degli intervalli disponibili, vedere [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**OPZIONE WINHTTP \_ \_ REQUIRE STREAM \_ \_ END**
</dt> <dd> <dl> <dt>


Questa opzione indica a WinHttp di ignorare le intestazioni di risposta "Content-Length" e di continuare a ricevere in un flusso fino a quando non viene ricevuto END_STREAM flag di risposta.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**NOME HOST \_ DELLA \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>


Questa opzione può essere impostata su un handle di richiesta WinHttp prima dell'invio. Se impostato, WinHttp userà la stringa fornita dal chiamante come nome host per la risoluzione DNS.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**TIMEOUT DI \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, espresso in millisecondi, per risolvere un nome host. Il valore di timeout predefinito è **INFINITE.** Se viene specificato un valore non predefinito, si verifica un sovraccarico della creazione di un thread per ogni risoluzione dei nomi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**PROTOCOLLI SICURI \_ DELL'OPZIONE WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Imposta un valore di long integer senza segno che specifica quali protocolli sicuri sono accettabili. Per impostazione predefinita, solo SSL3 e TLS1 sono abilitati in Windows 7 e Windows 8. Per impostazione predefinita, solo SSL3, TLS1.0, TLS1.1 e TLS1.2 sono abilitati in Windows 8.1 e Windows 10. Il valore può essere una combinazione di uno o più dei valori seguenti.

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ ALL | È possibile usare i protocolli Secure Sockets Layer (SSL) 2.0, SSL 3.0 e Transport Layer Security (TLS) 1.0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ SSL2 | È possibile usare il protocollo SSL 2.0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ SSL3 | È possibile usare il protocollo SSL 3.0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP \_ FLAG \_ SECURE \_ PROTOCOL \_ TLS1 | È possibile usare il protocollo TLS 1.0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP \_ FLAG SECURE PROTOCOL \_ \_ \_ TLS1 \_ 1 | È possibile usare il protocollo TLS 1.1. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP \_ FLAG SECURE PROTOCOL \_ \_ \_ TLS1 \_ 2 | È possibile usare il protocollo TLS 1.2. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**STRUCT DEL CERTIFICATO \_ \_ DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Recupera il certificato per un server SSL/TLS nella struttura [**WINHTTP \_ CERTIFICATE \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) L'applicazione deve liberare **i membri lpszSubjectInfo** **e lpszIssuerInfo** con [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**FLAG DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene i flag di sicurezza per un handle. Può essere una combinazione di questi valori:

| Termine | Descrizione |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>FLAG \_ DI SICUREZZA IGNORE \_ \_ CERT CN \_ \_ INVALID |Consente un nome comune non valido in un certificato. in altri, il nome del server specificato dall'applicazione non corrisponde al nome comune nel certificato. Se questo flag è impostato, l'applicazione non riceve un **callback WINHTTP \_ CALLBACK STATUS \_ FLAG \_ \_ CERT CN \_ \_ INVALID** callback. |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>FLAG \_ DI SICUREZZA IGNORA DATA CERTIFICATO NON \_ \_ \_ \_ VALIDA |Consente una data di certificato non valida, ad esempio un certificato scaduto o non ancora valido. Se questo flag è impostato, l'applicazione non riceve un **callback WINHTTP \_ CALLBACK STATUS \_ FLAG \_ \_ CERT DATE \_ \_ INVALID.** |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>FLAG \_ DI SICUREZZA IGNORA CA \_ \_ \_ SCONOSCIUTA | Consente un'autorità di certificazione non valida. Se questo flag è impostato, l'applicazione non riceve un callback DI CALLBACK **DI WINHTTP \_ STATUS FLAG INVALID \_ \_ \_ \_ CA.** |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>FLAG DI \_ SICUREZZA \_ IGNORA \_ L'UTILIZZO ERRATO \_ DEL \_ CERTIFICATO | Consente di stabilire l'identità di un server con un certificato non server, ad esempio un certificato client. |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>FLAG \_ DI SICUREZZA IGNORA FIRMA \_ \_ \_ DEBOLE | Consente di ignorare una firma debole.<br/>Questo flag è disponibile nell'aggiornamento cumulativo per ogni sistema operativo a partire da Windows 7 e Windows Server 2008 R2. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>FLAG \_ DI \_ SICUREZZA SICURO | Usa trasferimenti sicuri. Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>LIVELLO \_ DI ATTENDIBILITÀ DEL FLAG \_ DI SICUREZZA \_ MEDIO | Usa la crittografia media (56 bit). Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>LIVELLO \_ DI SICUREZZA DEL FLAG DI SICUREZZA \_ \_ SICURO | Usa una crittografia avanzata (a 128 bit). Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>LIVELLO \_ DI PROTEZIONE DEL FLAG DI SICUREZZA \_ \_ DEBOLE | Usa la crittografia debole (a 40 bit). Viene restituito solo in una chiamata a [**WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**INFORMAZIONI DI SICUREZZA \_ \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Rieduca la connessione SChannel e le informazioni di crittografia per una richiesta.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**BITNESS \_ CHIAVE DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Recupera un valore long integer senza segno che contiene il livello di crittografia della chiave di crittografia. Un numero maggiore indica una crittografia più avanzata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**TIMEOUT DI \_ INVIO \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore long integer senza segno che contiene il valore di timeout, in millisecondi, per inviare una richiesta o scrivere alcuni dati. Se l'invio della richiesta richiede più tempo del timeout, l'operazione di invio viene annullata. Il timeout predefinito è 30 secondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**
</dt> <dd> <dl> <dt>



Ottiene un puntatore [**alla struttura SecPkgContext \_ Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) che specifica un token di associazione del canale (CBT).

Un token di associazione del canale è una proprietà di un canale di trasporto sicuro e viene usato per associare un canale di autenticazione al canale di trasporto sicuro. Questo token può essere ottenuto da questa opzione solo dopo che è stata stabilita una connessione SSL.

> [!Note]
> Il passaggio di questa opzione e di un valore **Null** per *lpBuffer* [**a WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) restituirà ERROR INSUFFICIENT BUFFER e le dimensioni in byte necessarie per il buffer nel \_ parametro \_ *lpdwBufferLength.* Questo valore delle dimensioni del buffer restituito può essere passato in una chiamata successiva per eseguire una query per il token di associazione del canale. Questi passaggi sono necessari quando si gestisce WINHTTP CALLBACK STATUS REQUEST se si vogliono modificare le intestazioni della richiesta \_ in base al token di associazione del \_ \_ canale. Si noti Windows XP e Vista non supportano la modifica delle intestazioni delle richieste durante questo callback.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**CONTESTO CATENA \_ DI CERTIFICATI DEL SERVER \_ \_ \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera il contesto della catena di certificazione del server. **WINHTTP \_ OPTION \_ SERVER \_ CERT CHAIN \_ \_ CONTEXT** può essere passato per ottenere un puntatore duplicato a **CERT CHAIN \_ \_ CONTEXT** per una catena di certificati server ricevuta durante una connessione SSL negoziata. Il client deve chiamare [**CertFreeCertificateContext sul**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) puntatore PCCERT CONTEXT restituito che \_ viene inserito nel buffer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**CONTESTO DEL CERTIFICATO \_ \_ DEL SERVER \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Recupera il contesto di certificazione del server. **WINHTTP \_ È possibile passare OPTION \_ SERVER \_ CERT \_ CONTEXT** per ottenere un puntatore duplicato a [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) per un certificato del server ricevuto durante una connessione SSL negoziata. Il client deve chiamare [**CertFreeCertificateContext sul**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) puntatore PCCERT CONTEXT restituito che \_ viene inserito nel buffer.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**NOME \_ \_ SPN DEL SERVER \_ DELL'OPZIONE WINHTTP \_ USATO**
</dt> <dd> <dl> <dt>



Ottiene il nome dell'entità server del server fornito da WinHTTP a SSPI durante l'autenticazione. Questo valore stringa può essere passato a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) dopo un errore di autenticazione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**NOME \_ \_ SPN DELL'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Include o rimuove il numero di porta del server quando il nome SPN (nome dell'entità servizio) viene compilato per l'autenticazione Kerberos o Negotiate Kerberos. Questo flag è uno dei valori seguenti:

| Termine | Descrizione |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ DISABLE \_ SPN \_ SERVER \_ PORT | Rimuove il numero di porta del server. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>PORTA DEL \_ \_ SERVER SPN ABILITATA \_ WINHTTP \_ | Include il numero di porta del server. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**CODICE DI ERRORE \_ DEL \_ FLUSSO \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>


Questa opzione può essere eseguita su un handle di richiesta WinHttp e restituirà il codice di errore indicato da un frame RST_STREAM ricevuto in un flusso HTTP.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**OPZIONE WINHTTP \_ \_ TCP FAST \_ \_ OPEN**
</dt> <dd> <dl> <dt>



Abilita TCP Fast Open per la connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**OPZIONE \_ \_ WINHTTP TCP \_ KEEPALIVE**
</dt> <dd> <dl> <dt>



Questa opzione può essere impostata su un handle di sessione WinHttp per abilitare il comportamento keep-alive TCP nel socket sottostante. Accetta uno [**struct \_ tcp keepalive.**](/windows/win32/winsock/sio-keepalive-vals)


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPZIONE WINHTTP \_ \_ TLS FALSE \_ \_ START**
</dt> <dd> <dl> <dt>



Abilita TLS False Start per la connessione.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**OPZIONE WINHTTP \_ \_ \_ \_ FALLBACK NON SICURO DEL PROTOCOLLO TLS \_**
</dt> <dd> <dl> <dt>



Questa opzione può essere impostata su un handle di sessione WinHttp per controllare se è consentito il fallback a TLS 1.0 se si verifica un errore di handshake TLS con una versione del protocollo più recente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**EVENTO NOTIFICA \_ \_ DI SCARICAMENTO \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Accetta un evento che verrà impostato quando l'ultimo callback è stato completato per una sessione specifica. Questo flag deve essere usato in un handle di sessione. L'evento non può essere chiuso fino a quando non è stato impostato da WinHTTP.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**ANALISI \_ \_ DELL'INTESTAZIONE NON SICURA \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Questa opzione è riservata per uso interno e non deve essere chiamata.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**AGGIORNAMENTO \_ DELL'OPZIONE WINHTTP \_ AL WEB \_ \_ \_ SOCKET**
</dt> <dd> <dl> <dt>



Indica all'stack di avviare un processo di handshake WebSocket [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) Questa opzione non accetta parametri.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**URL DELL'OPZIONE WINHTTP \_ \_**
</dt> <dd> <dl> <dt>



Recupera un valore stringa che contiene l'URL completo di una risorsa scaricata. Se l'URL originale contiene dati aggiuntivi, ad esempio stringhe di ricerca o ancoraggi, o se la chiamata è stata reindirizzata, l'URL restituito è diverso da quello originale. L'applicazione deve passare un buffer, ridimensionato in byte, sufficientemente grande da contenere l'URL restituito in caratteri wide.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**L'OPZIONE WINHTTP \_ USA LE CREDENZIALI GLOBALI DEL \_ \_ \_ \_ SERVER**
</dt> <dd> <dl> <dt>



Accetta un **bool e** può essere impostato solo un handle di sessione. Verrà propagato solo agli handle creati dall'handle di sessione dopo l'impostazione dell'opzione . Se **TRUE,** questa opzione fa sì che come ultima risorsa l'uso di credenziali del server globali di cui è stato fatto il push da WinInet. Il valore predefinito per questa opzione è **FALSE.** Questa opzione richiede la chiave del Registro **di sistema HKLM \\ Software Microsoft Windows \\ \\ \\ CurrentVersion Internet \\ Impostazioni! ShareCredsWithWinHttp**. Questa chiave del Registro di sistema non è presente per impostazione predefinita. Quando è impostata, WinINet invierà le credenziali a WinHTTP. Ogni volta che WinHttp riceve una richiesta di autenticazione e se non sono impostate credenziali nell'handle corrente, userà le credenziali fornite da WinINet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**OPZIONE WINHTTP \_ \_ AGENTE \_ UTENTE**
</dt> <dd> <dl> <dt>



Imposta o recupera [](glossary.md) la stringa dell'agente utente sugli handle forniti da [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) e usati nelle funzioni [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) successive, purché non venga sottoposto a override da un'intestazione aggiunta da [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) **o WinHttpSendRequest.** Quando si recupera un agente utente, l'applicazione deve passare un buffer, ridimensionato in byte, sufficientemente grande da contenere l'URL restituito in caratteri wide. Quando si imposta l'agente utente, la dimensione del buffer è la lunghezza della stringa, in caratteri, più il carattere **di terminazione NULL.**


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**NOME UTENTE \_ DELL'OPZIONE WINHTTP \_**
</dt> <dd> <dl> <dt>



Imposta o recupera una stringa contenente il nome utente.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**TIMEOUT CHIUSURA \_ \_ WEB SOCKET \_ DELL'OPZIONE \_ \_ WINHTTP**
</dt> <dd> <dl> <dt>



Imposta il tempo, in millisecondi, di attesa di [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) per completare l'handshake di chiusura. Il valore predefinito è 10 secondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**OPZIONE WINHTTP \_ \_ INTERVALLO \_ \_ KEEPALIVE DEL WEB \_ SOCKET**
</dt> <dd> <dl> <dt>



Imposta l'intervallo, in millisecondi, per l'invio di un pacchetto keep-alive sulla connessione. L'intervallo predefinito è 30000 (30 secondi). L'intervallo minimo è 15000 (15 secondi). [**L'uso di WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) per impostare un valore minore di 15000 restituirà con **ERROR INVALID \_ \_ PARAMETER**.

> [!Note]
> Il valore predefinito per **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** viene letto da **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval**. Se non è impostato un valore, verrà usato il valore predefinito 30000. Non è possibile avere un intervallo keep-live inferiore a 15000 millisecondi.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**DIMENSIONI BUFFER \_ DI RICEZIONE WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di ricezione da utilizzare nelle connessioni WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**DIMENSIONI BUFFER \_ DI INVIO WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP**
</dt> <dd> <dl> <dt>



Imposta o recupera un valore DWORD che specifica le dimensioni del buffer di invio da usare nelle connessioni WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**CONTEGGIO \_ THREAD DI LAVORO \_ \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Imposta un valore long integer senza segno che specifica il numero di thread di lavoro che il pool di thread deve usare per i completamenti asincroni. Il valore predefinito di questa opzione è zero, che specifica che il numero di thread di lavoro è uguale al numero di CPU nel sistema. Questa opzione può essere impostata solo su un handle **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) prima che si sia verificata un'operazione asincrona. Questa opzione può essere impostata una sola volta.

**Windows Server 2008 R2 e Windows 7:** Questo flag è obsoleto.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**DIMENSIONI DEL \_ BUFFER DI \_ SCRITTURA \_ DELL'OPZIONE \_ WINHTTP**
</dt> <dd> <dl> <dt>



Questa opzione è stata deprecata. non ha alcun effetto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nella tabella seguente sono elencati i flag di opzione specificando gli handle su cui possono agire, se possono essere sottoposti a query e impostati e il tipo di dati utilizzato. Una "X" indica che il flag di opzione è valido per l'uso con la funzione o l'handle, mentre "-" specifica che il flag di opzione non è valido.

Se si tenta di impostare o eseguire una query su un flag di opzione Windows versione in cui non è supportata, verrà restituito **l'errore \_ WINHTTP \_ INVALID \_ OPTION**.

| Flag di opzione e tipo di dati | Handle di sessione | Handle di richiesta | Opzione di query | Opzione SET | Versione Windows minima |
|-|-|-|-|-|-|
| OPZIONE WINHTTP \_ \_ GARANTITA \_ CALLBACK NON \_ \_ BLOCCANTI<br/>**Bool** | X | \- | \- | X | \- |
| CRITERIO DI \_ ACCESSO \_ AUTOMATICO DELL'OPZIONE WINHTTP \_<br/>**Dword** | \- | X | \- | X | \- |
| CONNESSIONI IN \_ BACKGROUND DELL'OPZIONE WINHTTP \_ \_<br/>**Dword** | X | \- | \- | X | Windows 10 Versione 21H1 |
| CALLBACK \_ DELL'OPZIONE WINHTTP \_<br/>**Lpvoid** | X | X | X | X | \- |
| CONTESTO DEL CERTIFICATO \_ \_ CLIENT \_ DELL'OPZIONE \_ WINHTTP<br/>[**CONTESTO DEL \_ CERTIFICATO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| ELENCO AUTORITÀ \_ DI CERTIFICAZIONE DEL CERTIFICATO CLIENT \_ \_ \_ DELL'OPZIONE WINHTTP \_<br/>[**SecPkgContext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| TABELLA CODICI \_ \_ DELL'OPZIONE WINHTTP<br/>**Dword** | X | \- | \- | X | \- |
| OPZIONE WINHTTP \_ \_ - CONFIGURARE \_ \_ L'AUTENTICAZIONE PASSPORT<br/>**Dword** | X | \- | \- | X | \- |
| TENTATIVI \_ DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP<br/>**Dword** | X | X | X | X | \- |
| TIMEOUT DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_<br/>**Dword** | X | X | X | X | \- |
| INFORMAZIONI DI CONNESSIONE \_ \_ DELL'OPZIONE WINHTTP \_<br/>[**INFORMAZIONI DI \_ CONNESSIONE \_ WINHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V0<br/>[**TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10 Versione 1903 |
| STATISTICHE DI \_ CONNESSIONE \_ DELL'OPZIONE WINHTTP \_ \_ V1<br/>[**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10 Versione 2004 |
| VALORE DI CONTESTO \_ \_ DELL'OPZIONE WINHTTP \_<br/>**DWORD \_ PTR** | X | X | X | X | \- |
| \_ \_ DECOMPRESSIONE DELL'OPZIONE WINHTTP<br/>**Dword** | X | X | \- | X | Windows 8.1 |
| OPZIONE WINHTTP \_ PER \_ DISABILITARE \_ LA COMPILAZIONE DELLA CATENA \_ DI \_ CERTIFICATI<br/>**Bool** | X | \- | \- | X | Windows 10 Versione 21H1 |
| OPZIONE WINHTTP \_ \_ DISABILITA \_ FUNZIONALITÀ<br/>**Dword** | \- | X | \- | X | \- |
| OPZIONE WINHTTP \_ \_ DISABILITA IL \_ \_ FALLBACK DEL \_ PROTOCOLLO SICURO<br/>**Bool** | X | \- | \- | X | Windows 10 Versione 1903 |
| OPZIONE WINHTTP \_ DISABILITA \_ CODA DI \_ \_ FLUSSO<br/>**Bool** | X | X | \- | X | Windows 10 Versione 1809 |
| OPZIONE WINHTTP \_ \_ - ABILITARE LA \_ FUNZIONALITÀ<br/>**Dword** | \* | \* | \- | X | \- |
| OPZIONE WINHTTP \_ \_ ABILITA PROTOCOLLO \_ \_ HTTP<br/>**Dword** | X | X | \- | X | Windows 10 versione 1607 |
| OPZIONE WINHTTP \_ \_ ENABLE \_ HTTP2 PLUS CLIENT \_ \_ \_ CERT \_ CONTEXT<br/>**Bool** | X | \- | \- | X | Windows 10 Versione 21H1 |
| OPZIONE WINHTTP \_ \_ ENABLETRACING<br/>**Dword** | \- | \- | X | X | \- |
| OPZIONE WINHTTP \_ \_ ENCODE \_ EXTRA<br/>**Bool** | X | X | \- | X | Windows 10 Versione 1803 |
| L'OPZIONE WINHTTP \_ \_ SCADE LA \_ CONNESSIONE<br/>N/A | \- | X | \- | X | Windows 10 Versione 1903 |
| ERRORE ESTESO \_ \_ DELL'OPZIONE \_ WINHTTP<br/>**Dword** | X | X | X | \- | \- |
| OPZIONE WINHTTP \_ \_ PRIMA CONNESSIONE \_ \_ DISPONIBILE<br/>**Bool** | X | \- | \- | X | Windows 10 Versione 21H1 |
| CRED \_ \_ PROXY GLOBALI \_ \_ DELL'OPZIONE WINHTTP<br/>[**WINHTTP \_ CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| CRED SERVER \_ \_ GLOBALI \_ DELL'OPZIONE \_ WINHTTP<br/>[**WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| TIPO DI \_ HANDLE DELL'OPZIONE WINHTTP \_ \_<br/>**Dword** | X | X | X | \- | \- |
| PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ OBBLIGATORIO<br/>**Bool** | X | X | \- | X | Windows 10 Versione 1903 |
| PROTOCOLLO \_ \_ HTTP DELL'OPZIONE WINHTTP \_ \_ USATO<br/>**Dword** | \- | X | X | \- | Windows 10 versione 1607 |
| VERSIONE \_ \_ HTTP DELL'OPZIONE \_ WINHTTP<br/>[**INFORMAZIONI \_ SULLA VERSIONE \_ HTTP**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| OPZIONE WINHTTP \_ \_ HTTP2 \_ KEEPALIVE<br/>**Dword** | X | \- | \- | X | Windows 10 Versione 21H1 |
| OPZIONE WINHTTP \_ \_ HTTP2 \_ PLUS TRANSFER \_ \_ ENCODING<br/>**Bool** | X | X | \- | X | Windows 10 Versione 21H1 |
| OPZIONE WINHTTP \_ \_ IGNORA REVOCA CERTIFICATO \_ \_ \_ OFFLINE<br/>**Bool** | \- | X | \- | X | Windows 10 Versione 2004 |
| OPZIONE \_ \_ WINHTTP IPV6 \_ FAST \_ FALLBACK<br/>**Bool** | X | \- | \- | X | Windows 10 Versione 1903 |
| L'OPZIONE WINHTTP \_ \_ È PROXY CONNECT \_ \_ \_ RESPONSE<br/>**Bool** | X | X | X | \- | \- |
| OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ 1 \_ 0 \_ SERVER<br/>**Dword** | X | \- | X | X | \- |
| OPZIONE WINHTTP \_ \_ MAX \_ CONNS PER \_ \_ SERVER<br/>**Dword** | X | \- | X | X | \- |
| OPZIONE WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS<br/>**Dword** | X | X | X | X | \- |
| OPZIONE WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE<br/>**Dword** | X | X | X | X | \- |
| OPZIONE WINHTTP \_ \_ DIMENSIONE MASSIMA \_ \_ SVUOTAMENTO \_ RISPOSTA<br/>**Dword** | X | X | X | X | \- |
| DIMENSIONI MASSIME \_ INTESTAZIONE RISPOSTA \_ \_ \_ DELL'OPZIONE WINHTTP \_<br/>**Dword** | X | X | X | X | \- |
| HANDLE PADRE \_ DELL'OPZIONE WINHTTP \_ \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| TESTO \_ \_ \_ COBRANDING DELL'OPZIONE WINHTTP PASSPORT \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| URL \_ \_ \_ COBRANDING DELL'OPZIONE WINHTTP PASSPORT \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| URL \_ RESTITUITO \_ PASSPORT DELL'OPZIONE WINHTTP \_ \_<br/>**Lpvoid** | \- | X | X | \- | \- |
| OPZIONE WINHTTP \_ \_ - \_ DISCONNESSIONE PASSPORT \_<br/>**Lpvoid** | X | \- | \- | X | \- |
| PASSWORD \_ DELL'OPZIONE WINHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| PROXY \_ DELL'OPZIONE WINHTTP \_<br/>[**INFORMAZIONI SUL PROXY WINHTTP \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| PASSWORD PROXY \_ DELL'OPZIONE WINHTTP \_ \_<br/>**LPWSTR** | \- | X | X | X | \- |
| NOME \_ \_ SPN PROXY \_ DELL'OPZIONE WINHTTP \_ USATO<br/>**LPWSTR** | \- | X | X | \- | \- |
| NOME UTENTE \_ PROXY DELL'OPZIONE WINHTTP \_ \_<br/>**LPWSTR** | \- | X | X | X | \- |
| DIMENSIONI DEL \_ \_ BUFFER DI LETTURA \_ DELL'OPZIONE \_ WINHTTP<br/>**Dword** | \- | X | X | X | \- |
| L'OPZIONE WINHTTP \_ RICEVE LA RISPOSTA DI CONNESSIONE \_ \_ \_ \_ PROXY<br/>**Bool** | X | X | \- | X | \- |
| L'OPZIONE WINHTTP \_ RICEVE IL TIMEOUT DI \_ \_ \_ RISPOSTA<br/>**Dword** | X | X | X | X | \- |
| TIMEOUT DI \_ RICEZIONE \_ DELL'OPZIONE WINHTTP \_<br/>**Dword** | X | X | X | X | \- |
| CRITERI DI \_ REINDIRIZZAMENTO \_ DELL'OPZIONE WINHTTP \_<br/>**Dword** | X | X | X | X | \- |
| OPZIONE WINHTTP \_ \_ REJECT \_ USERPWD \_ IN \_ URL<br/>**Bool** | \- | X | \- | X | \- |
| PRIORITÀ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP \_<br/>**Dword** | \- | X | X | X | \- |
| STATISTICHE DI \_ RICHIESTA \_ \_ DELL'OPZIONE WINHTTP<br/>[**STATISTICHE DELLE \_ RICHIESTE \_ WINHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10 Versione 1903 |
| TEMPI DI RICHIESTA \_ \_ DELL'OPZIONE \_ WINHTTP<br/>[**TEMPI DI RICHIESTA WINHTTP \_ \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10 Versione 1903 |
| OPZIONE WINHTTP \_ \_ REQUIRE STREAM \_ \_ END<br/>**Bool** | X | X | \- | X | Windows 10 Versione 21H1 |
| NOME HOST \_ DELLA \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP<br/>**LPWSTR** | \- | X | \- | X | Windows 10 Versione 21H1 |
| TIMEOUT DI \_ RISOLUZIONE \_ DELL'OPZIONE WINHTTP \_<br/>**Dword** | X | X | X | X | \- |
| PROTOCOLLI SICURI \_ DELL'OPZIONE WINHTTP \_ \_<br/>**Dword** | X | \- | \- | X | \- |
| STRUCT DEL CERTIFICATO \_ \_ DI SICUREZZA \_ \_ DELL'OPZIONE WINHTTP<br/>[**INFORMAZIONI SUL CERTIFICATO WINHTTP \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| FLAG DI \_ SICUREZZA \_ DELL'OPZIONE WINHTTP \_<br/>**Dword** | \- | X | X | X | \- |
| INFORMAZIONI DI SICUREZZA \_ \_ DELL'OPZIONE \_ WINHTTP<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10 Versione 2004 |
| BITNESS \_ CHIAVE DI SICUREZZA \_ \_ \_ DELL'OPZIONE WINHTTP<br/>**Dword** | \- | X | X | \- | \- |
| TIMEOUT DI \_ INVIO \_ DELL'OPZIONE WINHTTP \_<br/>**Dword** | X | X | X | X | \- |
| WINHTTP \_ OPTION \_ SERVER \_ CBT<br/>[**Associazioni SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| CONTESTO CATENA DI CERTIFICATI DI WINHTTP \_ OPTION \_ SERVER \_ \_ \_<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10 Versione 2004 |
| CONTESTO CERTIFICATO DI WINHTTP \_ OPTION \_ SERVER \_ \_<br/>[**CONTESTO CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| NOME SPN DI WINHTTP \_ OPTION \_ SERVER \_ \_ USATO<br/>**LPWSTR** | \- | X | X | \- | \- |
| NOME \_ \_ SPN DELL'OPZIONE WINHTTP<br/>**Dword** | \- | X | \- | X | \- |
| CODICE DI ERRORE \_ \_ DEL FLUSSO \_ DELL'OPZIONE \_ WINHTTP<br/>**Dword** | \- | X | X | \- | Windows 10 Versione 21H1 |
| OPZIONE WINHTTP \_ \_ TCP FAST \_ \_ APERTA<br/>**Bool** | X | \- | \- | X | Windows 10 Versione 2004 |
| OPZIONE WINHTTP \_ \_ TCP \_ KEEPALIVE<br/>[**tcp \_ keepalive**](/windows/win32/winsock/sio-keepalive-vals) | X | \- | \- | X | Windows 10 Versione 2004 |
| OPZIONE WINHTTP \_ \_ TLS FALSE \_ \_ START<br/>**Bool** | X | \- | \- | X | Windows 10 Versione 2004 |
| FALLBACK NON SICURO DEL PROTOCOLLO \_ \_ TLS \_ \_ DELL'OPZIONE WINHTTP \_<br/>**Bool** | X | \- | \- | X | Windows 10 Versione 21H1 |
| EVENTO NOTIFICA \_ \_ DI SCARICAMENTO \_ DELL'OPZIONE WINHTTP \_<br/>[HINTERNET](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| ANALISI \_ \_ DELL'INTESTAZIONE NON SICURA \_ DELL'OPZIONE \_ WINHTTP<br/>**Dword** | \- | X | \- | X | \- |
| AGGIORNAMENTO \_ DELL'OPZIONE WINHTTP \_ AL WEB \_ \_ \_ SOCKET<br/>N/A | \- | X | \- | X | \- |
| URL DELL'OPZIONE WINHTTP \_ \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| L'OPZIONE WINHTTP \_ USA LE CREDENZIALI GLOBALI DEL \_ \_ \_ \_ SERVER<br/>**Bool** | X | X | \- | X | \- |
| OPZIONE WINHTTP \_ \_ AGENTE \_ UTENTE<br/>**LPWSTR** | X | \- | X | X | \- |
| NOME UTENTE \_ DELL'OPZIONE WINHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| TIMEOUT CHIUSURA \_ \_ WEB SOCKET \_ DELL'OPZIONE \_ \_ WINHTTP<br/>**Dword** | \- | \- | X | X | \- |
| OPZIONE WINHTTP \_ \_ INTERVALLO \_ \_ KEEPALIVE DEL WEB \_ SOCKET<br/>**Dword** | \- | \- | X | X | \- |
| DIMENSIONI BUFFER \_ DI RICEZIONE WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP<br/>**Dword** | X | X | X | X | Windows 8.1 |
| DIMENSIONI BUFFER \_ DI INVIO WEB SOCKET \_ \_ \_ PER \_ \_ L'OPZIONE WINHTTP<br/>**Dword** | X | X | X | X | Windows 8.1 |
| CONTEGGIO \_ THREAD DI LAVORO \_ \_ DELL'OPZIONE \_ WINHTTP<br/>**Dword** | \- | \- | \- | X | \- |
| DIMENSIONI DEL \_ BUFFER DI \_ SCRITTURA \_ DELL'OPZIONE \_ WINHTTP<br/>**Dword** | \- | X | X | X | \- |

> [!Note]
> Per Windows XP e Windows 2000, vedere [Requisiti di run-time.](winhttp-start-page.md)

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]            |
| Server minimo supportato | Windows Server 2003, Windows 2000 Server solo con app desktop SP3 \[\]         |
| Componente ridistribuibile          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000. |
| Intestazione                   | Winhttp.h                                                                       |

## <a name="see-also"></a>Vedi anche

[Versioni di WinHTTP](winhttp-versions.md)
