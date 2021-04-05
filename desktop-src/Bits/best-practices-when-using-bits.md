---
title: Procedure consigliate per l'uso di BITS
description: Questa sezione contiene informazioni da tenere in considerazione quando si progetta un'applicazione che usa BITS.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: bbf69e75b99994eea3e8986d1be9920ff1a12bc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955239"
---
# <a name="best-practices-when-using-bits"></a>Procedure consigliate per l'uso di BITS

Questa sezione contiene informazioni da tenere in considerazione quando si progetta un'applicazione che usa BITS.

## <a name="user-context-or-service-context"></a>Contesto utente o contesto del servizio

BITS trasferisce i file solo quando il proprietario del processo è connesso al computer (l'utente deve avere eseguito l'accesso in modo interattivo). BITS non supporta il comando **RunAs** . Per ulteriori informazioni, vedere [utenti e connessioni di rete](users-and-network-connections.md).

Se non è necessario il contesto di un utente per l'applicazione, è consigliabile scrivere un servizio eseguito come LocalSystem, LocalService o NetworkService. Questi account di sistema sono sempre connessi, quindi il trasferimento non è soggetto a una disconnessione utente. Tuttavia, se si rappresenta un utente durante la creazione del processo, vengono applicate le regole di accesso interattivo. Per ulteriori informazioni, vedere [account del servizio e BITS](service-accounts-and-bits.md).

## <a name="jobs-are-persistent"></a>I processi sono persistenti

I processi rimangono nella coda fino a quando non viene chiamato il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . I file del processo non sono disponibili per l'utente fino a quando non viene chiamato il **completamento**. In genere, si chiama **completa** quando lo stato del processo è **il \_ processo \_ BG stato \_ trasferito** e si chiama **Annulla** quando il processo si trova nello stato di errore **\_ \_ \_ temporaneo dello stato del processo \_ BG** o in stato del **\_ processo \_ \_ BG** e non può più avanzare.

Se non si chiama il metodo [**complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o il metodo [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) entro 90 giorni ( [JobInactivityTimeout](group-policies.md) predefinito criteri di gruppo), il servizio annulla il processo. È sempre necessario chiamare il metodo **complete** o **Cancel** e non basarsi sul criterio JobInactivityTimeout per la pulizia dei processi. I processi rimasti nella coda possono impedire agli utenti di creare altri processi se viene raggiunto il limite dei criteri MaxJobsPerUser o MaxJobsPerMachine.

## <a name="when-to-use-foreground-or-background-priority"></a>Quando usare la priorità in primo piano o in background

A meno che il processo non sia critico all'ora o l'utente sia attivamente in attesa, è consigliabile utilizzare sempre una priorità in background. Tuttavia, in alcuni casi può essere necessario passare dalla priorità in background alla priorità in primo piano, ad esempio quando il proxy o il server non supporta l'intestazione Content-Range oppure il software antivirus nel client rimuove la richiesta di intestazione di intervallo. Il passare alla priorità in primo piano funziona solo per i file le cui dimensioni del file sono inferiori a 2 GB. Per un esempio, vedere l'implementazione per il metodo [**IBackgroundCopyCallback:: JobError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) . Si noti inoltre che se il processo in primo piano viene interrotto a causa di una disconnessione della rete o quando l'utente si disconnette, il processo avrà esito negativo perché BITS invierà una richiesta di intervallo per tentare di riavviare il trasferimento dal punto in cui è stata interrotta.

A partire da Windows 8, è consigliabile configurare i processi di download con il **\_ \_ \_ \_ contenuto dinamico della proprietà processo BITS** e il **\_ \_ \_ primo piano priorità processo BG** quando si fa riferimento a server che non soddisfano i [requisiti http per i download BITS](http-requirements-for-bits-downloads.md). Tenere presente che questa operazione comporterà la necessità di riavviare il download dall'inizio se viene interrotto, ad esempio a causa di problemi di connettività o di riavvio del sistema.

Per informazioni sulle priorità disponibili e sul modo in cui BITS usa il livello di priorità per pianificare i processi, vedere [**\_ \_ priorità del processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Errori temporanei ed irreversibili

Alcuni errori sono reversibili e altri no. Ad esempio, l'errore "server non disponibile" è un errore reversibile e l'errore "accesso negato" è un errore irreversibile. BITS inserisce errori reversibili in uno stato di errore temporaneo e ritenta il processo dopo un intervallo specificato. Se il processo non è in grado di eseguire lo stato di avanzamento, BITS sposta il processo in uno stato di errore irreversibile. Usare i metodi [**Metodo ibackgroundcopyjob:: SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) e [**Metodo ibackgroundcopyjob:: SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) per controllare il modo in cui bits elabora gli errori temporanei.

Per i processi in primo piano, è necessario limitare la quantità di tempo in cui un processo rimane nello stato di errore temporaneo e provare a eseguire il ripristino. Usare il metodo [**SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) per limitare la quantità di tempo per cui un processo rimane nello stato di errore temporaneo o per forzare il processo nello stato di errore irreversibile. Se si lascia che il processo tenti il ripristino, è consigliabile usare il metodo [**SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) per impostare il ritardo minimo dei tentativi su 60 secondi oppure chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per attivare nuovamente il processo.

Per ulteriori informazioni, vedere [**\_ \_ lo stato del processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [il ciclo di vita di un processo BITS e la](life-cycle-of-a-bits-job.md) [gestione degli errori](handling-errors.md).

## <a name="measuring-network-bandwidth-usage"></a>Misurazione dell'utilizzo della larghezza di banda di rete

BITS potrebbe usare la scheda di rete del client per stimare la larghezza di banda di rete disponibile. Poiché BITS non è in grado di misurare la larghezza di banda oltre il client, BITS potrebbe congestionere il collegamento WAN. Per ridurre la congestione sul collegamento WAN, è possibile utilizzare i criteri di gruppo **MaxInternetBandwidth** per limitare la quantità di larghezza di banda utilizzata dal client. Per altre informazioni, vedere [larghezza di banda di rete](network-bandwidth.md) e [criteri di gruppo](group-policies.md).

Se si sta scrivendo un'applicazione che molti client utilizzeranno per scaricare i file da un determinato server, è necessario prendere in considerazione uno schema che Sfalsa le richieste di download in modo da non sovraccaricare il server con le richieste.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Impostazione delle credenziali per l'autenticazione del server e del proxy

Se si prevede che il proxy o il server richieda le credenziali utente, è necessario fornire le credenziali a BITS. Per specificare le credenziali, chiamare il metodo [**IBackgroundCopyJob2:: Secredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) . BITS supporta gli schemi di autenticazione di base, digest, Negotiate, NTLM e Passport.

Per informazioni dettagliate sull'autenticazione, vedere [autenticazione](authentication.md).

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Specifica delle impostazioni proxy per gli account utente e gli account del servizio

Per impostazione predefinita, BITS usa le impostazioni proxy di Internet Explorer dell'utente. Per eseguire l'override delle impostazioni proxy di Internet Explorer dell'utente, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) .

Le impostazioni proxy di Internet Explorer non sono valide per gli account di sistema, pertanto il comportamento predefinito del proxy (**\_ \_ \_ \_ preconfigurazione utilizzo proxy processo BG**) funzionerà correttamente nelle distribuzioni WPAD (Web Proxy Auto-Discovery Protocol), a meno che non vengano eseguiti passaggi di configurazione aggiuntivi. Se l'applicazione è un servizio in esecuzione come LocalSystem, LocalService o NetworkService, prendere in considerazione la configurazione di un token helper nei processi BITS oppure impostare in modo esplicito le impostazioni del proxy corrette chiamando [**Metodo ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **\_ \_ \_ \_ l'override di utilizzo del proxy del processo BG**. In alternativa, è possibile usare le opzioni **/util/SetIEProxy** di BitsAdmin.exe per impostare le impostazioni proxy di Internet Explorer per l'account di sistema LocalSystem, LocalService o NetworkService. Per informazioni dettagliate, vedere [lo strumento Bitsadmin](bitsadmin-tool.md).

BITS non riconosce le impostazioni proxy impostate utilizzando il file di Proxycfg.exe.

A partire da Windows 10 ottobre 2018 aggiornamento (10,0; Build 17763), BITS usa lo stesso ordine del proxy usato da WinHttp con AUTOMATIC_PROXY. BITS usa questo ordinamento più compatibile quando si specifica BG_JOB_PROXY_USAGE_PRECONFIG. BG_JOB_PROXY_USAGE_PRECONFIG è il valore predefinito per specificare il proxy HTTP.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Specifica delle impostazioni specifiche dell'utente per l'autenticazione dei proxy

Se si utilizzano BITS in un ambiente che richiede l'autenticazione proxy mentre è in esecuzione come account senza credenziali NTLM o Kerberos utilizzabili nel dominio di rete del computer, è necessario eseguire passaggi aggiuntivi per l'autenticazione corretta utilizzando le credenziali di un altro account utente che dispone di credenziali nel dominio. Si tratta di uno scenario tipico quando il codice BITS è in esecuzione come servizio di sistema, ad esempio LocalService, NetworkService o LocalSystem, in quanto questi account non dispongono di credenziali NTLM o Kerberos utilizzabili.

Per informazioni dettagliate sul funzionamento dell'autenticazione in questo scenario, vedere [Authentication.](authentication.md)

## <a name="scalability"></a>Scalabilità

Se nella coda sono presenti più di 100 processi, le prestazioni possono iniziare a diminuire a seconda della composizione del processo. BITS usa l'impostazione dei criteri [MaxJobsPerMachine](group-policies.md) per imporre un limite rigido al numero di processi nella coda. Le applicazioni devono limitare il numero di processi a circa 10, in modo che più applicazioni abbiano la possibilità di superare le linee guida per 100 processi. In genere, un'applicazione con un numero elevato di processi da inviare Invia prima di tutto 10 processi, quindi ne invia uno alla volta al termine di ogni processo.

Anche il numero di file nel processo deve essere limitato a un massimo di 10 file. Se si desidera trasferire un numero elevato di file per un processo, provare a creare un file CAB che contenga tutti i file.

## <a name="http-headers-can-be-in-any-case"></a>Le intestazioni HTTP possono essere in qualsiasi caso

Gli standard HTTP hanno sempre detto che le intestazioni HTTP devono essere considerate senza distinzione tra maiuscole e minuscole (RFC 7230 sezione 3,2). Lo standard HTTP più recente, RFC 7540, va oltre e dice che il traffico HTTP/2 deve confrontare le intestazioni senza distinzione tra maiuscole e minuscole e deve presentare intestazioni in lettere minuscole (RFC 6540, sezione 8.1.2). Anche quando il traffico viene inviato con intestazioni non minuscole, i proxy possono scegliere di forzare le intestazioni in lettere minuscole.

## <a name="avoiding-personally-identifiable-information-pii"></a>Evitare informazioni personali (PII)

I processi BITS, inclusi il nome visualizzato e la descrizione e i nomi dei file, sono visibili a tutti gli utenti con privilegi di amministratore. Possono anche essere aggiunti ai dati di telemetria di Windows. È consigliabile evitare di inserire dati sensibili, ad esempio il nome dell'utente, nei dettagli del processo.
