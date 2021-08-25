---
title: Valori restituiti da BITS
description: Il file Bitsmsg.h contiene le costanti del valore restituito seguenti.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- errori BITS
- errori BITS, codici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c6795572a2f81324e287c385a78e22e0b195dbbc3af061585fc847c464a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173830"
---
# <a name="bits-return-values"></a>Valori restituiti da BITS

Il file Bitsmsg.h contiene le costanti del valore restituito seguenti. Le costanti rappresentano i valori restituiti generati da BITS e i valori restituiti HTTP che BITS acquisisce. Tutti gli altri valori restituiti che è possibile ricevere sono i valori restituiti COM, RPC o Windows convertiti (BITS usa la macro [HRESULT \_ FROM \_ WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) per convertire i valori restituiti Windows in valori HRESULT).

Si noti che il file Bitsmsg.h contiene valori restituiti aggiuntivi non elencati di seguito.

<dl> <dt>

<span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG \_ S PARTIAL COMPLETE \_ \_ (0x00200017)
</dt> <dd>

Subset dei file del processo trasferiti correttamente prima della chiamata al metodo [**IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Quelli non completati sono stati eliminati.

</dd> <dt>

<span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S NON È IN GRADO DI ELIMINARE FILE \_ \_ \_ \_ (0X0020001A)
</dt> <dd>

Impossibile eliminare tutti i file temporanei associati al processo.

</dd> <dt>

<span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S SOTTOPOSTO A OVERRIDE DA CRITERI \_ \_ \_ (0x00200055)
</dt> <dd>

La preferenza di configurazione è stata salvata correttamente, ma la preferenza non verrà usata perché un'impostazione Criteri di gruppo predefinita sostituisce la preferenza.

</dd> <dt>

<span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E NOT FOUND \_ \_ (0x80200001)
</dt> <dd>

Il processo richiesto non è stato trovato.

</dd> <dt>

<span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG \_ E INVALID STATE \_ \_ (0x80200002)
</dt> <dd>

L'azione richiesta non è consentita nello stato del processo corrente.

</dd> <dt>

<span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ EMPTY (0x80200003)
</dt> <dd>

Il processo deve contenere uno o più file prima di poter riprendere il processo.

</dd> <dt>

<span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>FILE \_ BG E \_ \_ NON DISPONIBILE \_ (0x80200004)
</dt> <dd>

Le informazioni sul file non sono disponibili perché l'errore non è associato a un file locale o remoto.

</dd> <dt>

<span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>PROTOCOLLO \_ BG E \_ \_ NON DISPONIBILE \_ (0x80200005)
</dt> <dd>

Le informazioni sul protocollo non sono disponibili perché l'errore non è associato al protocollo di trasferimento specificato.

</dd> <dt>

<span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG \_ E DESTINATION LOCKED \_ \_ (0x8020000D)
</dt> <dd>

Il volume file system di destinazione, specificato nel nome file locale, è bloccato.

</dd> <dt>

<span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>VOLUME \_ BG E \_ \_ MODIFICATO (0x8020000E)
</dt> <dd>

Il volume di destinazione, specificato nel nome file locale, è stato modificato. Ad esempio, il disco floppy originale è stato sostituito con un disco floppy diverso.

</dd> <dt>

<span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG \_ E ERROR INFORMATION UNAVAILABLE \_ \_ \_ (0X8020000F)
</dt> <dd>

Le informazioni sugli errori sono disponibili solo quando lo stato del processo è BG \_ JOB \_ STATE \_ ERROR. Le informazioni sull'errore non sono disponibili dopo che BITS ha avviato il trasferimento dei dati del processo o la chiusura del client.

</dd> <dt>

<span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ NETWORK \_ DISCONNECTED (0x80200010)
</dt> <dd>

La scheda di rete è inattiva o disconnessa. Tutti i processi vengono inseriti nello stato BG \_ JOB \_ STATE TRANSIENT \_ \_ ERROR.

</dd> <dt>

<span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>DIMENSIONI FILE MANCANTI BG \_ E \_ \_ \_ (0x80200011)
</dt> <dd>

Il server non ha restituito le dimensioni del file. BITS trasferisce solo contenuto statico e richiede al server HTTP di restituire l'intestazione Content-Length. La richiesta di trasferimento ha esito negativo se l'URL punta al contenuto dinamico.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG \_ E SUPPORTO HTTP INSUFFICIENTE \_ \_ \_ (0x80200012)
</dt> <dd>

Il server non supporta il protocollo HTTP/1.1.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG \_ E INSUFFICIENT RANGE SUPPORT \_ \_ \_ (0x80200013)
</dt> <dd>

Il server non supporta l'intestazione Content-Range. In genere, questo errore viene visualizzato quando si tenta di scaricare contenuto dinamico. È anche possibile ricevere questo errore se un proxy intermedio rimuove l'intestazione Content-Range o Content-Length.

</dd> <dt>

<span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E REMOTE NON SUPPORTATO \_ \_ \_ (0x80200014)
</dt> <dd>

L'uso remoto di BITS non è supportato. Per altre informazioni, vedere [Utenti e connessioni di rete.](users-and-network-connections.md)

</dd> <dt>

<span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ E NEW OWNER \_ \_ \_ DIFF MAPPING \_ (0x80200015)
</dt> <dd>

Il mapping dell'unità di rete per il file locale è diverso per il proprietario corrente rispetto al proprietario precedente.

</dd> <dt>

<span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E NUOVO PROPRIETARIO NO FILE ACCESS \_ \_ \_ \_ \_ (0x80200016)
</dt> <dd>

Il nuovo proprietario non dispone di autorizzazioni sufficienti per i file di processo temporanei.

</dd> <dt>

<span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>ELENCO DI PROXY BG \_ E \_ TROPPO GRANDE \_ \_ \_ (0x80200018)
</dt> <dd>

L'elenco di proxy HTTP è troppo lungo. L'elenco non deve superare i 32 KB.

</dd> <dt>

<span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG \_ E PROXY BYPASS LIST TOO LARGE \_ \_ \_ \_ \_ (0X80200019)
</dt> <dd>

L'elenco di bypass del proxy HTTP è troppo lungo. L'elenco non deve superare i 32 KB.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E TROPPI FILE \_ \_ \_ (0x8020001C)
</dt> <dd>

Non è possibile aggiungere più file a un processo di caricamento.

</dd> <dt>

<span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG \_ E FILE LOCALE MODIFICATO \_ \_ \_ (0x8020001D)
</dt> <dd>

Il contenuto del file locale è stato modificato dopo l'inizio del processo di trasferimento. Il contenuto del file locale non può cambiare dopo l'avvio del processo di trasferimento in un processo di caricamento o caricamento-risposta.

</dd> <dt>

<span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E TROPPO GRANDE \_ \_ (0x80200020)
</dt> <dd>

Le dimensioni del file di caricamento superano le dimensioni massime consentite per il caricamento specificate nel server.

</dd> <dt>

<span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG \_ E STRING TOO LONG \_ \_ \_ (0x80200021)
</dt> <dd>

La stringa specificata è troppo lunga.

</dd> <dt>

<span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG \_ E CLIENT SERVER PROTOCOL \_ \_ \_ \_ MISMATCH (0x80200022)
</dt> <dd>

Il client e il server non sono riusciti a negoziare un protocollo da usare per il processo di caricamento.

</dd> <dt>

<span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG \_ E SERVER EXECUTE ENABLED \_ \_ \_ (0x80200023)
</dt> <dd>

Le autorizzazioni di scripting o di esecuzione sono abilitate nella directory virtuale IIS associata al processo. Per caricare i file nella directory virtuale, disabilitare le autorizzazioni di scripting ed esecuzione per la directory virtuale.

</dd> <dt>

<span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>NOME \_ UTENTE BG E \_ \_ TROPPO GRANDE \_ (0x80200025)
</dt> <dd>

Il nome utente non può superare i 300 caratteri.

</dd> <dt>

<span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>PASSWORD \_ BG E \_ \_ TROPPO GRANDE \_ (0x80200026)
</dt> <dd>

La password non può superare i 65535 caratteri.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ INVALID \_ AUTH TARGET \_ (0x80200027)
</dt> <dd>

La destinazione di autenticazione specificata non è valida.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ INVALID \_ AUTH SCHEME \_ (0x80200028)
</dt> <dd>

Lo schema di autenticazione specificato non è valido.

</dd> <dt>

<span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG \_ E INVALID RANGE \_ \_ (0x8020002B)
</dt> <dd>

L'intervallo di byte specificato non è valido. L'intervallo di byte deve esistere all'interno del file remoto specificato.

</dd> <dt>

<span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>INTERVALLI SOVRAPPOSTI BG \_ E \_ \_ (0x8020002C)
</dt> <dd>

L'elenco di intervalli di byte contiene intervalli sovrapposti o duplicati, che non sono supportati.

</dd> <dt>

<span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E BLOCKED BY POLICY \_ \_ \_ (0x8020003E)
</dt> <dd>

Criteri di gruppo impostazioni impediscono l'esecuzione dei processi in background in questo momento. Per informazioni dettagliate, vedere il [criterio MaxInternetBandwidth.](group-policies.md)

</dd> <dt>

<span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG \_ E INFORMAZIONI PROXY NON VALIDE \_ \_ \_ (0x8020003F)
</dt> <dd>

Errore di run-time che indica che l'elenco proxy o l'elenco di bypass proxy specificato usando il metodo [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) non è valido.

</dd> <dt>

<span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E CREDENZIALI NON VALIDE \_ \_ (0x80200040)
</dt> <dd>

Il formato delle credenziali di sicurezza fornite non è valido.

</dd> <dt>

<span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG \_ E RECORD ELIMINATO \_ \_ (0x80200042)
</dt> <dd>

Il record della cache è stato eliminato. Il tentativo di aggiornamento è stato abbandonato.

</dd> <dt>

<span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>ERRORE \_ BG E \_ UPNP \_ (0x80200045)
</dt> <dd>

Si è verificato un errore UPnP (Universal Plug and Play). Controllare il dispositivo gateway Internet.

</dd> <dt>

<span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG \_ E \_ PEERCACHING \_ DISABILITATO (0x80200047)
</dt> <dd>

Il peer caching è disabilitato.

</dd> <dt>

<span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)
</dt> <dd>

Il record della cache è in uso e non può essere modificato o eliminato. Riprovare dopo alcuni secondi.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E TROPPI PROCESSI PER UTENTE \_ \_ \_ \_ \_ (0x80200049)
</dt> <dd>

Il numero di processi per l'utente ha superato il limite di processi per utente impostato dall'impostazione di Criteri di gruppo MaxJobsPerUser.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E TROPPI PROCESSI PER COMPUTER \_ \_ \_ \_ \_ (0x80200050)
</dt> <dd>

Il numero di processi per il computer ha superato il limite di processi per computer impostato dall'impostazione maxJobsPerMachine Criteri di gruppo.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E TROPPI FILE NEL PROCESSO \_ \_ \_ \_ \_ (0x80200051)
</dt> <dd>

Il numero di file per il processo ha superato il limite di file per processo impostato dall'impostazione maxFilesPerJob Criteri di gruppo.

</dd> <dt>

<span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E \_ TROPPI \_ \_ INTERVALLI NEL FILE \_ \_ (0X80200052)
</dt> <dd>

Il numero di intervalli per il file ha superato il limite di intervalli per file impostato dall'impostazione maxRangesPerFile Criteri di gruppo.

</dd> <dt>

<span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>CONVALIDA BG \_ E \_ NON RIUSCITA \_ (0x80200053)
</dt> <dd>

L'applicazione ha richiesto dati da un sito Web, ma la risposta non è valida. Per informazioni dettagliate, usare Visualizzatore eventi per visualizzare il log operativo di \\ Microsoft \\ Windows \\ Bits-client. \\

</dd> <dt>

<span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG \_ E \_ MAXDOWNLOAD \_ TIMEOUT (0x80200054)
</dt> <dd>

Timeout di BITS durante il download del processo. Il download non è stato completato entro il tempo di download massimo impostato per il processo o l'impostazione maxDownloadTime Criteri di gruppo.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG \_ E HTTP ERROR \_ \_ \_ 400 (0x80190190)
</dt> <dd>

Il server non è stato in grado di elaborare la richiesta di trasferimento perché la sintassi del nome file remoto non è valida.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG \_ E HTTP ERROR \_ \_ \_ 401 (0x80190191)
</dt> <dd>

L'utente non dispone dell'autorizzazione per accedere al file remoto. La risorsa richiesta prevede l'autenticazione degli utenti.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG \_ E HTTP ERROR \_ \_ \_ 404 (0x80190194)
</dt> <dd>

L'URL richiesto non esiste nel server.

In IIS 7 questo errore può indicare

-   I caricamenti BITS non sono abilitati nella directory virtuale (vdir) nel server.
-   Le dimensioni di caricamento superano il limite massimo di caricamento . Per informazioni dettagliate, vedere la proprietà dell'estensione IIS [**BITSMaximumUploadSize.**](bits-iis-extension-properties.md)

</dd> <dt>

<span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG \_ E HTTP ERROR \_ \_ \_ 407 (0x80190197)
</dt> <dd>

L'utente non dispone dell'autorizzazione per accedere al proxy. Il proxy richiede l'autenticazione utente.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG \_ E HTTP ERROR \_ \_ \_ 414 (0x8019019E)
</dt> <dd>

Il server non è in grado di elaborare la richiesta di trasferimento. Il Uniform Resource Identifier (URI) nel nome file remoto è più lungo di quanto il server possa interpretare.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG \_ E HTTP ERROR \_ \_ \_ 501 (0x801901F5)
</dt> <dd>

Il server non supporta la funzionalità necessaria per soddisfare la richiesta. In IIS 6 questo errore indica che i caricamenti BITS non sono abilitati nella directory virtuale (vdir) nel server.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG \_ E HTTP ERROR \_ \_ \_ 503 (0x801901F7)
</dt> <dd>

Il servizio è temporaneamente sovraccarico e non può elaborare la richiesta. Riprendere il processo in un secondo momento.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG \_ E HTTP ERROR \_ \_ \_ 504 (0x801901F8)
</dt> <dd>

Timeout della richiesta di trasferimento durante l'attesa di un gateway. Riprendere il processo in un secondo momento.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG \_ E HTTP ERROR \_ \_ \_ 505 (0x801901F9)
</dt> <dd>

Il server non supporta la versione del protocollo HTTP specificata nel nome file remoto.

</dd> </dl>

Il file di intestazione Bitsmsg.h contiene valori restituiti HTTP aggiuntivi non elencati in precedenza che BITS usa internamente. Per informazioni su questi e altri valori restituiti HTTP che è possibile ricevere, vedere la specifica RFC 2616 della Internet Engineering Task Force all'indirizzo [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .

 

 