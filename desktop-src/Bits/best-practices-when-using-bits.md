---
title: Procedure consigliate per l'uso di BITS
description: Questa sezione contiene informazioni da prendere in considerazione quando si progetta un'applicazione che usa BITS.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: cbc11365cde74e092ae179c8b41562a16de9a6c36f0d85e51787a979c9332863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702091"
---
# <a name="best-practices-when-using-bits"></a>Procedure consigliate per l'uso di BITS

Questa sezione contiene informazioni da prendere in considerazione quando si progetta un'applicazione che usa BITS.

## <a name="user-context-or-service-context"></a>Contesto utente o contesto del servizio

BITS trasferisce i file solo quando il proprietario del processo è connesso al computer (l'utente deve aver eseguito l'accesso in modo interattivo). BITS non supporta il **comando RunAs.** Per altri dettagli, vedere [Utenti e connessioni di rete.](users-and-network-connections.md)

Se non è necessario il contesto di un utente per l'applicazione, prendere in considerazione la scrittura di un servizio in esecuzione come LocalSystem, LocalService o NetworkService. Questi account di sistema sono sempre connessi, quindi il trasferimento non è soggetto alla disconnessione di un utente. Tuttavia, se si rappresenta un utente quando si crea il processo, vengono applicate le regole di accesso interattivo. Per altri dettagli, vedere [Account del servizio e BITS.](service-accounts-and-bits.md)

## <a name="jobs-are-persistent"></a>I processi sono persistenti

I processi rimangono nella coda fino a quando non si chiama [**il metodo IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o [**IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) I file nel processo non sono disponibili per l'utente fino a quando non si chiama **Complete**. In genere, si chiama **Complete** quando lo stato del processo è **BG \_ JOB STATE \_ \_ TRANSFERRED** e si chiama **Cancel** quando il processo si trova nello stato BG JOB TRANSIENT **\_ \_ \_ \_ ERROR** o **BG JOB STATE \_ \_ \_ ERROR** e non può più essere in corso.

Se non si chiama il [**metodo Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o il metodo [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) entro 90 giorni (impostazione predefinita [JobInactivityTimeout](group-policies.md) Criteri di gruppo), il servizio annulla il processo. È sempre necessario chiamare il **metodo Complete** o **Cancel** e non basarsi sui criteri JobInactivityTimeout per la pulizia dei processi. I processi rimasti nella coda potrebbero impedire agli utenti di creare altri processi se viene raggiunto il limite dei criteri MaxJobsPerUser o MaxJobsPerMachine.

## <a name="when-to-use-foreground-or-background-priority"></a>Quando usare la priorità di primo piano o di sfondo

A meno che il processo non sia critico per il tempo o l'utente sia attivamente in attesa, è consigliabile usare sempre una priorità in background. In alcuni casi, tuttavia, può essere necessario passare dalla priorità in background alla priorità in primo piano, ad esempio quando il proxy o il server non supporta l'intestazione Content-Range o il software antivirus nel client rimuove la richiesta di intestazione dell'intervallo. Il passaggio alla priorità di primo piano funziona solo per i file la cui dimensione è inferiore a 2 GB. Per un esempio, vedere l'implementazione per [**il metodo IBackgroundCopyCallback::JobError.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) Si noti anche che se il processo in primo piano viene interrotto a causa di una disconnessione di rete o della disconnessione dell'utente, il processo avrà esito negativo perché BITS invierà una richiesta di intervallo per provare a riavviare il trasferimento dal punto in cui è stato interrotto.

A partire da Windows 8, è consigliabile configurare i processi di download con CONTENUTO DINAMICO PROPRIETÀ PROCESSO BITS e **BG \_ JOB PRIORITY \_ \_ FOREGROUND** quando la destinazione è server che non soddisfano i requisiti HTTP per i download [BITS](http-requirements-for-bits-downloads.md). **\_ \_ \_ \_** Tenere presente che ciò comporta che BITS deve riavviare il download dall'inizio in caso di interruzione, ad esempio a causa di problemi di connettività o riavvio del sistema.

Per informazioni sulle priorità disponibili e su come BITS usa il livello di priorità per pianificare i processi, vedere [**BG \_ JOB \_ PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Errori temporanei e irreversibili

Alcuni errori sono recuperabili e altri no. Ad esempio, l'errore "Server non disponibile" è reversibile e l'errore "Accesso negato" è un errore irreversibile. BITS inserisce gli errori ripristinabili in uno stato di errore temporaneo e tenta di nuovo il processo dopo un intervallo specificato. Se il processo non è in grado di avanzamento, BITS sposta il processo in uno stato di errore irreversibile. Usare i [**metodi IBackgroundCopyJob::SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) e [**IBackgroundCopyJob::SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) per controllare il modo in cui BITS elabora gli errori temporanei.

Per i processi in primo piano, è necessario limitare la quantità di tempo per cui un processo rimane nello stato di errore temporaneo e si tenta di eseguire il ripristino. Usare il [**metodo SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) per limitare la quantità di tempo per cui un processo rimane nello stato di errore temporaneo o per forzare il processo allo stato di errore irreversibile. Se si consente al processo di provare a eseguire il ripristino, è necessario usare il metodo [**SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) per impostare il ritardo minimo tra i tentativi su 60 secondi oppure chiamare il metodo [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per attivare nuovamente il processo.

Per altre informazioni, vedere [**BG \_ JOB \_ STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [Ciclo di vita di un processo BITS](life-cycle-of-a-bits-job.md)e Gestione degli [errori.](handling-errors.md)

## <a name="measuring-network-bandwidth-usage"></a>Misurazione dell'utilizzo della larghezza di banda di rete

BITS potrebbe usare la scheda di rete del client per stimare la larghezza di banda di rete disponibile. Poiché BITS non è in grado di misurare la larghezza di banda oltre il client, BITS può inserire il collegamento WAN. Per ridurre la congestione sul collegamento WAN, è possibile usare i criteri di gruppo **MaxInternetBandwidth** per limitare la quantità di larghezza di banda utilizzata dal client. Per altre informazioni, vedere Larghezza [di banda di rete](network-bandwidth.md) e Criteri di [gruppo.](group-policies.md)

Se si scrive un'applicazione che molti client useranno per scaricare file da un determinato server, è consigliabile prendere in considerazione uno schema che sfalsa le richieste di download in modo da non sovraccaricare il server con le richieste.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Impostazione delle credenziali per l'autenticazione proxy e server

Se si prevede che il proxy o il server richieda le credenziali utente, è necessario fornire le credenziali a BITS. Per specificare le credenziali, chiamare il [**metodo IBackgroundCopyJob2::SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) BITS supporta gli schemi di autenticazione Basic, Digest, Negotiate, NTLM e Passport.

Per informazioni dettagliate sull'autenticazione, vedere [Autenticazione.](authentication.md)

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Specifica delle impostazioni proxy per gli account utente e gli account del servizio

Per impostazione predefinita, BITS usa le impostazioni proxy Internet Explorer'utente. Per eseguire l'override delle impostazioni proxy Internet Explorer dell'utente, chiamare il [**metodo IBackgroundCopyJob::SetProxySettings.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)

Le impostazioni proxy Internet Explorer non si applicano agli account di sistema, pertanto il comportamento predefinito del proxy (**BG \_ JOB PROXY \_ USAGE \_ \_ PRECONFIG**) funzionerà correttamente solo nelle distribuzioni WPAD (Web Proxy Auto-Discovery Protocol), a meno che non vengano emersi passaggi di configurazione aggiuntivi. Se l'applicazione è un servizio in esecuzione come LocalSystem, LocalService o NetworkService, è consigliabile configurare un token helper nei processi BITS o impostare in modo esplicito le impostazioni proxy corrette chiamando [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG \_ JOB PROXY USAGE \_ \_ \_ OVERRIDE**. In alternativa, è possibile usare le opzioni **/Util /SetIEProxy** di BitsAdmin.exe per impostare le impostazioni proxy Internet Explorer per l'account di sistema LocalSystem, LocalService o NetworkService. Per informazioni dettagliate, vedere [Strumento BitsAdmin.](bitsadmin-tool.md)

BITS non riconosce le impostazioni proxy impostate usando il Proxycfg.exe file.

A partire dal Aggiornamento di Windows 10 (ottobre 2018) (10.0; Build 17763), BITS usa lo stesso ordine proxy che WinHttp usa con AUTOMATIC_PROXY. BITS usa questo ordinamento più compatibile quando BG_JOB_PROXY_USAGE_PRECONFIG specificato. BG_JOB_PROXY_USAGE_PRECONFIG è il valore predefinito per specificare il proxy HTTP.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Specifica delle impostazioni specifiche dell'utente per l'autenticazione dei proxy

Se si usa BITS in un ambiente che richiede l'autenticazione proxy durante l'esecuzione come account senza credenziali NTLM o Kerberos utilizzabili nel dominio di rete del computer, è necessario eseguire passaggi aggiuntivi per eseguire correttamente l'autenticazione usando le credenziali di un altro account utente che dispone di credenziali nel dominio. Si tratta di uno scenario tipico quando il codice BITS viene eseguito come servizio di sistema, ad esempio LocalService, NetworkService o LocalSystem, perché tali account non dispongono di credenziali NTLM o Kerberos utilizzabili.

Per informazioni dettagliate sul funzionamento dell'autenticazione in questo scenario, vedere [Autenticazione.](authentication.md)

## <a name="scalability"></a>Scalabilità

Se nella coda sono presenti più di 100 processi, le prestazioni potrebbero iniziare a diminuire a seconda della composizione del processo. BITS usa [l'impostazione dei criteri MaxJobsPerMachine](group-policies.md) per imporre un limite rigido al numero di processi nella coda. Le applicazioni devono limitare il numero dei processi a circa 10, in modo che più applicazioni avranno meno probabilità di superare le linee guida dei 100 processi. In genere, un'applicazione con un numero elevato di processi da inviare invia prima 10 processi e quindi ne invia uno alla volta al termine di ogni processo.

Anche il numero di file nel processo deve essere limitato a un massimo di 10 file. Se si desidera trasferire un numero elevato di file per un processo, è consigliabile creare un file CAB contenente tutti i file.

## <a name="http-headers-can-be-in-any-case"></a>Le intestazioni HTTP possono essere in qualsiasi caso

Gli standard HTTP hanno sempre detto che le intestazioni HTTP devono essere considerate senza distinzione tra maiuscole e minuscole (RFC 7230 sezione 3.2). Lo standard HTTP più recente, RFC 7540, va oltre e afferma che il traffico HTTP/2 deve confrontare le intestazioni senza distinzione tra maiuscole e minuscole e deve presentare intestazioni in lettere minuscole (RFC 6540, sezione 8.1.2). Anche quando il traffico viene inviato con intestazioni non minuscole, i proxy possono scegliere di forzare le intestazioni in lettere minuscole.

## <a name="avoiding-personally-identifiable-information-pii"></a>Evitare informazioni personali

I processi BITS, inclusi il nome visualizzato del processo, la descrizione e i nomi file, sono visibili a tutti gli utenti con privilegi di amministratore. Possono anche essere aggiunti alla telemetria Windows dati di telemetria. È consigliabile evitare di inserire dati sensibili, ad esempio il nome dell'utente, nei dettagli del processo.
