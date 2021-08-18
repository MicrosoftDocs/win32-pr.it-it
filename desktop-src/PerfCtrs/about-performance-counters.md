---
description: I contatori vengono usati per fornire informazioni sulle prestazioni del sistema operativo o di un'applicazione, un servizio o un driver.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: Informazioni sui contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 8a80ac907ef842e4564f0e67daa173fee165bc93d8fa568920df8ffc24b8c9a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978916"
---
# <a name="about-performance-counters"></a>Informazioni sui contatori delle prestazioni

Windows I contatori delle prestazioni forniscono un livello di astrazione di alto livello con un'interfaccia coerente per la raccolta di vari tipi di dati di sistema, ad esempio statistiche di utilizzo della CPU, della memoria e del disco. Gli amministratori di sistema usano i contatori delle prestazioni per monitorare i problemi di prestazioni o di comportamento. Gli sviluppatori di software usano i contatori delle prestazioni per controllare l'utilizzo delle risorse dei componenti.

> [!IMPORTANT]
> Windows I contatori delle prestazioni sono ottimizzati per l'individuazione e la raccolta di dati amministrativi/diagnostici. Non sono appropriati per la raccolta di dati ad alta frequenza o per la profilatura dell'applicazione perché non sono progettati per essere raccolti più di una volta al secondo. Per un accesso con sovraccarico inferiore alle informazioni di sistema, è possibile preferire API più dirette, ad esempio Process [**Status Helper,**](../psapi/process-status-helper.md) [**GlobalMemoryStatusEx,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)o [**GetProcessTimes.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes) Per la profilatura, è possibile raccogliere i log ETW con i dati di profilatura del sistema usando [**tracelog.exe**](/windows-hardware/drivers/devtest/tracelog) con le opzioni , , o oppure è possibile usare la profilatura dei `-critsec` `-dpcisr` `-eflag` `-ProfileSource` [**contatori hardware**](/previous-versions/windows/desktop/hcp/hcp-reference).

> [!NOTE]
> Non confondere Windows contatori delle prestazioni con [**l'API QueryPerformanceCounter.**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) Windows I contatori delle prestazioni forniscono un'astrazione di alto livello per molti tipi di informazioni di sistema. La funzione QueryPerformanceCounter fornisce l'accesso ottimizzato a un timestamp ad alta precisione.

## <a name="getting-started"></a>Introduzione

- Utilizzare [gli strumenti contatore delle](performance-counters-tools.md) prestazioni quando si desidera raccogliere o visualizzare i dati sulle prestazioni da un sistema.
- Usare [le API di raccolta dei contatori delle](consuming-counter-data.md) prestazioni quando si vuole scrivere uno script o un programma che raccoglie dati sulle prestazioni dal sistema locale.
- Utilizzare [le classi dei contatori delle](/windows/desktop/WmiSdk/monitoring-performance-data) prestazioni WMI quando si desidera raccogliere dati sulle prestazioni da un sistema locale o remoto tramite WMI.
- Usare [le API del provider dei contatori delle](providing-counter-data.md) prestazioni quando si vogliono pubblicare dati sulle prestazioni dal componente software.

## <a name="concepts"></a>Concetti

Il Windows del contatore delle prestazioni è organizzato in consumer **,** provider **,** **contatori** **,** contatori **,** contatori , istanze e valori **dei contatori**.

Un **consumer** è un componente software che usa i dati sulle prestazioni. Windows include diversi [strumenti predefiniti che](performance-counters-tools.md) usano i dati sulle prestazioni. tra cui Gestione attività, Monitoraggio risorse, Monitor prestazioni, typeperf.exe, logman.exe e relog.exe. Gli sviluppatori possono scrivere script e applicazioni che accedono ai contatori delle prestazioni tramite [le API dei contatori delle prestazioni](consuming-counter-data.md).

Un **provider** è un componente software che [genera e pubblica dati sulle prestazioni.](providing-counter-data.md) Un provider pubblicherà i dati per uno o più *insiemi di contatori*. Ad esempio, un sistema di database potrebbe registrarsi come provider di dati per le prestazioni.

- Un **provider V1** è un componente software che pubblica i dati sulle prestazioni tramite una [DLL](providing-counter-data-using-a-performance-dll.md) delle prestazioni eseguita nel processo del consumer. Un provider V1 viene installato in un sistema tramite un `.ini` file. L'architettura del provider V1 è deprecata. I nuovi provider devono usare l'architettura del provider V2.
- Un **provider V2 è** un componente software che pubblica i dati sulle prestazioni tramite le API del provider del [contatore delle prestazioni](providing-counter-data-using-version-2-0.md). Un provider V2 viene installato in un sistema tramite `.man` un file (manifesto XML).

Un **insieme di contatori** è un raggruppamento di dati sulle prestazioni all'interno di un provider. Un insieme di contatori ha un nome e uno o più *contatori*. La raccolta dei dati da un insieme di contatori restituisce un numero di *istanze* di . In alcune API Windows, i contatori sono denominati oggetti **prestazioni**. Ad esempio, un provider di dati sulle prestazioni per un sistema di database potrebbe fornire un contatore per le statistiche per database.

Un **contatore** è la definizione di singoli dati sulle prestazioni. Un contatore ha un nome e un tipo. Ad esempio, un insieme di contatori "statistiche per database" potrebbe contenere un contatore denominato "transazioni al secondo" con tipo `PERF_COUNTER_COUNTER` .

**Un'istanza** è un'entità sulla quale vengono segnalati i dati sulle prestazioni. Un'istanza ha un nome (stringa) e uno o più valori *del contatore*. Ad esempio, un insieme di contatori "statistiche per database" potrebbe contenere un'istanza per ogni database. Il nome dell'istanza sarà il nome del database e ogni istanza conterrà i valori dei contatori per i contatori "transazioni al secondo", "utilizzo della memoria" e "utilizzo del disco".

Un **valore del contatore** è il valore di un singolo dato del contatore delle prestazioni. Un valore del contatore è un intero senza segno, a 32 bit o a 64 bit a seconda del tipo del contatore corrispondente. Quando si parla di *un'istanza* di , un *valore del contatore* può talvolta essere chiamato *contatore* o *valore*.

> [!TIP]
> Potrebbe essere utile correlare i termini dei contatori delle prestazioni a termini del foglio di calcolo più familiari. Un **insieme di contatori** è simile a una tabella. Un **contatore** è simile a una colonna. **Un'istanza** è simile a una riga. Un **valore del** contatore è simile a una cella nella tabella.

**I contatori a istanza singola** contengono sempre dati relativi esattamente a un'istanza. Questo è comune per i contatori che segnalano statistiche globali del sistema. Ad esempio, Windows ha un insieme di contatori a istanza singola incorporato denominato "Memory" che segnala l'utilizzo della memoria globale.

**I contatori a istanze multiple** contengono dati per un numero variabile di istanze. Questo è comune per i contatori che segnalano le entità all'interno del sistema. Ad esempio, Windows ha un insieme di contatori a istanze multipla incorporato denominato "Informazioni processore" che segnala un'istanza per ogni CPU installata.

I consumer raccoglieranno e registreranno periodicamente i dati dall'insieme di contatori di un provider. Ad esempio, il consumer potrebbe raccogliere i dati una volta al secondo o una volta al minuto. I dati raccolti sono denominati **campione.** Un esempio è costituito da timestamp insieme ai dati per le istanze dell'insieme di contatori. I dati per ogni istanza includono il nome dell'istanza (stringa) e un set di valori del contatore (numeri interi, un valore per ogni contatore nell'insieme di contatori).

I nomi delle istanze devono in genere essere univoci all'interno di un campione, ad esempio un provider non deve restituire due istanze con lo stesso nome come parte di un singolo esempio. Alcuni provider meno recenti non seguono questa regola, pertanto i consumer devono essere in grado di [tollerare nomi di istanza non univoci](handling-duplicate-instance-names.md). I nomi delle istanze non distinguono tra maiuscole e minuscole, pertanto le istanze non devono avere nomi che differiscono solo per la distinzione tra maiuscole e minuscole.

> [!NOTE]
> Per motivi di compatibilità con le versioni precedenti, il counterset "Process" restituisce nomi di istanza non univoci in base al nome file EXE. Ciò può causare risultati confusi, soprattutto quando un processo con un nome non univoco viene avviato o arrestato, in quanto in genere si verificano problemi di dati a causa di una corrispondenza non corretta dei nomi di istanza tra i campioni. I consumer dell'insieme di contatori "Process" devono essere in grado di tollerare questi nomi di istanza non univoci e gli anomalie dei dati risultanti.

I nomi delle istanze devono essere stabili tra gli esempi, ad esempio un provider deve usare lo stesso nome di istanza per la stessa entità ogni volta che viene raccolto il counterset.

Ogni contatore ha un tipo . Il tipo di contatore indica il tipo del valore non elaborato del contatore **(intero** senza segno a 32 bit o intero senza segno a 64 bit). Il tipo di contatore indica anche il valore non elaborato del contatore, che determina come deve essere elaborato il valore non elaborato per generare statistiche utili.

Anche se alcuni tipi di contatore sono semplici e hanno [](calculating-counter-values.md) un valore non elaborato che è direttamente utile, molti tipi di contatore richiedono un'elaborazione aggiuntiva per creare un **valore formattato utile.** Per produrre il valore formattato, alcuni tipi di contatore richiedono valori non elaborati da due campioni, alcuni tipi di contatore richiedono timestamp e alcuni tipi di contatore richiedono valori non elaborati da più contatori. Esempio:

- `PERF_COUNTER_LARGE_RAWCOUNT` è un valore non elaborato a 64 bit che non richiede alcuna elaborazione per essere utile. È appropriato per i valori tempormente, ad esempio "Byte di memoria in uso".
- `PERF_COUNTER_RAWCOUNT_HEX` è un valore non elaborato a 32 bit che richiede che sia utile solo la formattazione esadecimale semplice. È appropriato per informazioni tempormente specifiche o di identificazione, ad esempio "Flag" o "Indirizzo di base".
- `PERF_COUNTER_BULK_COUNT` è un valore non elaborato a 64 bit che indica un conteggio degli eventi e viene usato per calcolare la frequenza con cui si verificano gli eventi. Per essere utile, questo tipo di contatore richiede due campioni separati nel tempo. Il valore formattato è la frequenza degli eventi, ad esempio il numero di volte in cui l'evento si è verificato al secondo nell'intervallo tra i due campioni. Dati due campioni `s0` e , il valore `s1` formattato (frequenza eventi) verrà calcolato come `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` .

Si prevede che i provider si comportino come se fossero senza stato, ad esempio la raccolta di dati da un contatore non dovrebbe influire in modo visibile sullo stato del provider. Ad esempio, un provider non deve reimpostare i valori del contatore su 0 quando viene raccolto un insieme di contatori e non deve usare il timestamp di una raccolta precedente per modificare i valori nella raccolta corrente. Deve invece fornire valori del contatore non elaborati semplici con tipi accurati in modo che il consumer possa calcolare statistiche utili in base ai valori non elaborati e ai relativi timestamp.

## <a name="performance-api-architecture"></a>Architettura dell'API prestazioni

![Le applicazioni dei contatori delle Windows richiamano API che e chiamano nei provider per ottenere i dati sulle prestazioni.](images/architecture.png)

I consumer dei contatori delle prestazioni includono:

- [Applicazioni fornite da Microsoft,](performance-counters-tools.md) ad esempio Gestione attività, Monitoraggio risorse, Monitor prestazioni e typeperf.exe.
- Superfici API di alto livello fornite da Microsoft che espongono i dati dei contatori delle prestazioni, ad esempio [le classi di prestazioni WMI.](/windows/desktop/WmiSdk/monitoring-performance-data)
- Applicazioni o script che usano api consumer del [contatore delle prestazioni](consuming-counter-data.md).

La maggior parte dei consumer dei contatori delle prestazioni usa api [PDH.dll](using-the-pdh-functions-to-consume-counter-data.md) per raccogliere dati sulle prestazioni. PDH gestisce molti aspetti complessi della raccolta dei contatori delle prestazioni, ad esempio l'analisi delle query, la corrispondenza di istanze tra più campioni e il calcolo di valori formattati dai dati dei contatori non elaborati. L'implementazione PDH usa le API del Registro di sistema quando si utilizzano i dati da un provider V1 e usa le API consumer V2 quando si utilizzano i dati da un provider V2.

Alcuni consumer di contatori delle prestazioni meno recenti usano [le API del Registro di sistema per](using-the-registry-functions-to-consume-counter-data.md) raccogliere dati sulle prestazioni dalla chiave speciale del Registro di `HKEY_PERFORMANCE_DATA` sistema. Questa operazione non è consigliata per il nuovo codice perché l'elaborazione dei dati dal Registro di sistema è complessa e erta. L'implementazione dell'API del Registro di sistema supporta direttamente la raccolta di dati dai provider V1. Supporta indirettamente la raccolta di dati dai provider V2 tramite un livello di traduzione che usa le API consumer V2.

Alcuni consumer di contatori delle prestazioni usano [le funzioni consumer PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md) per accedere direttamente ai dati dai provider V2. Questo approccio è più complesso rispetto all'uso dei dati usando le API PDH, ma questo approccio può essere utile se le API PDH non possono essere usate a causa di problemi di prestazioni o dipendenze. L'implementazione di PerfLib V2 supporta direttamente la raccolta di dati dai provider V2. Non supporta la raccolta di dati dai provider V1.

> [!NOTE]
> Windows OneCore non include il PDH.dll e non include il supporto per l'utilizzo dei dati dei contatori delle prestazioni tramite le API del Registro di sistema. I consumer in OneCore devono usare le funzioni PerfLib V2 Consumer.

I provider V1 vengono implementati come DLL del provider che viene caricata nel processo consumer. L'implementazione dell'API del Registro di sistema gestisce il caricamento della DLL del provider, la chiamata alla DLL per raccogliere i dati sulle prestazioni e lo scaricamento della DLL in base alle esigenze. La DLL del [](communicating-with-your-application.md)provider è responsabile della raccolta dei dati sulle prestazioni nel modo appropriato, ad esempio usando normali API Windows, RPC, named pipe, memoria condivisa o altri meccanismi di comunicazione interprocesso.

I provider V2 vengono implementati come programma in modalità utente (spesso Windows servizio) o come driver in modalità kernel. In genere il codice del provider di dati sulle prestazioni è integrato direttamente in un componente esistente, ad esempio il driver o il servizio segnala statistiche su se stesso. L'implementazione di PerfLib V2 gestisce le richieste e le risposte tramite l'estensione del kernel PCW.sys, quindi il provider in genere non deve implementare alcuna comunicazione interprocesso per fornire i dati sulle prestazioni.

> [!NOTE]
> Windows Gli strumenti e le API dei contatori delle prestazioni includono un supporto limitato per l'accesso ai contatori delle prestazioni da altri computer tramite Registro di sistema remoto (per i provider V1) e RPC (per i provider V2). Questo supporto è spesso difficile da usare in termini di controlli di autenticazione (gli strumenti e le API possono eseguire l'autenticazione solo come utente corrente) e in termini di configurazione del sistema [(gli](accessing-remote-counter-data.md) endpoint e i servizi necessari sono disabilitati per impostazione predefinita). In molti casi, è meglio accedere ai contatori delle prestazioni dei sistemi remoti tramite [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) anziché tramite il supporto di accesso remoto incorporato.

## <a name="developer-audience"></a>Sviluppatori

I contatori delle prestazioni vengono spesso utilizzati dagli amministratori per identificare problemi di prestazioni o comportamenti anomali dei sistemi, dagli sviluppatori per studiare l'utilizzo delle risorse dei componenti software e dai singoli utenti per comprendere il comportamento dei programmi nel sistema. L'utilizzo può verificarsi tramite strumenti gui come Gestione attività o Monitor prestazioni, strumenti da riga di comando come typeperf.exe o logman.exe, tramite script tramite WMI e PowerShell o tramite API C/C++ e .NET.

I provider di contatori delle prestazioni vengono in genere implementati come driver in modalità kernel o servizi in modalità utente. I provider di contatori delle prestazioni vengono in genere scritti in C o C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della pagina di riferimento per tale elemento.

Per la cronologia delle versioni, [vedere Novità](performance-counters-what-s-new.md)di .

## <a name="see-also"></a>Vedi anche

[Utilizzo dei contatori delle prestazioni](using-performance-counters.md)

[Informazioni di riferimento per i contatori delle prestazioni](performance-counters-reference.md)
