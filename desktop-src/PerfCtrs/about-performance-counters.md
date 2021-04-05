---
description: I contatori vengono utilizzati per fornire informazioni sulle prestazioni del sistema operativo o di un'applicazione, un servizio o un driver.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: Informazioni sui contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dec7c71e99ab614ee64e3d1e8c9620f0be78c14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881781"
---
# <a name="about-performance-counters"></a>Informazioni sui contatori delle prestazioni

I contatori delle prestazioni di Windows forniscono un livello di astrazione generale con un'interfaccia coerente per la raccolta di diversi tipi di dati di sistema, come CPU, memoria e statistiche di utilizzo del disco. Gli amministratori di sistema utilizzano i contatori delle prestazioni per monitorare i problemi di prestazioni o di comportamento. Gli sviluppatori di software utilizzano i contatori delle prestazioni per esaminare l'utilizzo delle risorse dei propri componenti.

> [!IMPORTANT]
> I contatori delle prestazioni di Windows sono ottimizzati per l'individuazione e la raccolta dei dati di amministrazione/diagnostica. Non sono appropriati per la raccolta di dati ad alta frequenza o per la profilatura dell'applicazione perché non sono progettati per essere raccolti più di una volta al secondo. Per un minor overhead di accesso alle informazioni di sistema, è possibile preferire API dirette, ad esempio [**Helper stato processo**](../psapi/process-status-helper.md), [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex), [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)o [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes). Per la profilatura, è possibile raccogliere i log ETW con i dati di profilatura di sistema utilizzando [**tracelog.exe**](/windows-hardware/drivers/devtest/tracelog) con le `-critsec` `-dpcisr` Opzioni,, o oppure `-eflag` `-ProfileSource` è possibile utilizzare la [**profilatura del contatore hardware**](/previous-versions/windows/desktop/hcp/hcp-reference).

> [!NOTE]
> Non confondere i contatori delle prestazioni di Windows con l'API [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) . I contatori delle prestazioni di Windows forniscono un'astrazione di alto livello per molti tipi di informazioni di sistema. La funzione QueryPerformanceCounter fornisce l'accesso ottimizzato a un timestamp ad alta precisione.

## <a name="getting-started"></a>Introduzione

- Utilizzare [gli strumenti del contatore delle prestazioni](performance-counters-tools.md) quando si desidera raccogliere o visualizzare i dati sulle prestazioni da un sistema.
- Utilizzare le [API di raccolta del contatore delle prestazioni](consuming-counter-data.md) quando si desidera scrivere uno script o un programma che raccoglie i dati sulle prestazioni dal sistema locale.
- Utilizzare [le classi del contatore delle prestazioni WMI](/windows/desktop/WmiSdk/monitoring-performance-data) quando si desidera raccogliere dati sulle prestazioni da un sistema locale o remoto utilizzando WMI.
- Utilizzare le [API del provider del contatore delle prestazioni](providing-counter-data.md) quando si desidera pubblicare dati sulle prestazioni dal componente software.

## <a name="concepts"></a>Concetti

Il sistema di contatori delle prestazioni di Windows è organizzato in **consumer**, **provider**, **CounterSet**, **contatori**, **istanze** e **valori dei** contatori.

Un **consumer** è un componente software che utilizza i dati sulle prestazioni. Windows include diversi [strumenti predefiniti](performance-counters-tools.md) che consentono di utilizzare i dati sulle prestazioni. Quali gestione attività, Monitoraggio risorse, performance monitor, typeperf.exe, logman.exe e relog.exe. Gli sviluppatori possono scrivere script e applicazioni che accedono ai contatori delle prestazioni tramite le [API del contatore delle prestazioni](consuming-counter-data.md).

Un **provider** è un componente software che [genera e pubblica i dati sulle prestazioni](providing-counter-data.md). Un provider pubblicherà i dati per uno o più *CounterSet*. È ad esempio possibile che un sistema di database si registri come provider di dati delle prestazioni.

- Un **provider v1** è un componente software che pubblica i dati sulle prestazioni tramite una [dll di prestazioni](providing-counter-data-using-a-performance-dll.md) eseguita nel processo del consumer. Un provider v1 viene installato su un sistema tramite un `.ini` file. L'architettura del provider v1 è deprecata. I nuovi provider devono usare l'architettura del provider v2.
- Un **provider v2** è un componente software che pubblica i dati sulle prestazioni tramite le [API del provider del contatore delle prestazioni](providing-counter-data-using-version-2-0.md). Un provider v2 viene installato su un sistema tramite un `.man` file (manifesto XML).

Un **contatore** è un raggruppamento di dati sulle prestazioni all'interno di un provider. Un contatore ha un nome e uno o più *contatori*. La raccolta dei dati da un contatore restituisce un numero di *istanze*. In alcune API Windows, CounterSet sono denominati **oggetti prestazioni**. Un provider di dati sulle prestazioni di un sistema di database, ad esempio, potrebbe fornire un contatore per le statistiche per database.

Un **contatore** è la definizione di un singolo elemento di dati sulle prestazioni. Un contatore ha un nome e un tipo. Un contatore "statistiche per database", ad esempio, potrebbe contenere un contatore denominato "transazioni al secondo" con tipo `PERF_COUNTER_COUNTER` .

Un' **istanza** è un'entità per la quale vengono segnalati i dati sulle prestazioni. Un'istanza ha un nome (stringa) e uno o più *valori dei contatori*. Un contatore "statistiche per database", ad esempio, può contenere un'istanza per ogni database. Il nome dell'istanza sarà il nome del database e ogni istanza conterrebbe i valori dei contatori per i contatori "transazioni al secondo", "utilizzo memoria" e "utilizzo disco".

Un **valore del contatore** è il valore di un singolo elemento di dati del contatore delle prestazioni. Un valore del contatore è un Unsigned Integer, a 32 bit o a 64 bit, a seconda del tipo del contatore corrispondente. Quando si parla di un' *istanza*, un *valore del contatore* può talvolta essere chiamato *contatore* o *valore*.

> [!TIP]
> Potrebbe essere utile correlare i termini del contatore delle prestazioni a termini più comuni del foglio di calcolo. Un **contatore** è analogo a una tabella. Un **contatore** è analogo a una colonna. Un' **istanza** è simile a una riga. Un **valore del contatore** è analogo a una cella della tabella.

**CounterSet a istanza singola** contengono sempre i dati per una sola istanza. Si tratta di un problema comune per CounterSet che segnala le statistiche globali del sistema. Windows, ad esempio, dispone di un contatore incorporato a istanza singola denominato "Memory" che segnala l'utilizzo della memoria globale.

**CounterSet** a più istanze contengono dati per un numero variabile di istanze. Questa operazione è comune per CounterSet che segnalano le entità all'interno del sistema. Windows, ad esempio, dispone di un contatore incorporato a più istanze denominato "informazioni sul processore" che segnala un'istanza per ogni CPU installata.

I consumer raccoglieranno e registreranno periodicamente i dati da un contatore del provider. Ad esempio, il consumer potrebbe raccogliere dati una volta al secondo o una volta al minuto. I dati raccolti sono detti **esempi**. Un esempio è costituito da timestamp insieme ai dati per le istanze del contatore. I dati per ogni istanza includono il nome dell'istanza (stringa) e un set di valori dei contatori (Integer, un valore per ogni contatore nel set di contatori).

I nomi delle istanze devono essere in genere univoci all'interno di un campione, ovvero un provider non deve restituire due istanze con lo stesso nome come parte di un singolo campione. Alcuni provider meno recenti non seguono questa regola, quindi gli [utenti devono essere in grado di tollerare nomi di istanza non univoci](handling-duplicate-instance-names.md). Per i nomi di istanza non viene fatta distinzione tra maiuscole e minuscole, pertanto le istanze non devono avere nomi che differiscono solo nel caso.

> [!NOTE]
> Per motivi di compatibilità con le versioni precedenti, il contatore "processo" restituisce nomi di istanza non univoci in base al nome file EXE. Ciò può causare confusione nei risultati, soprattutto quando viene avviato o arrestato un processo con un nome non univoco, in quanto in genere si verificheranno glitch per i dati a causa di una corrispondenza errata dei nomi di istanza tra i campioni. I consumer di del contatore di "processo" devono essere in grado di tollerare questi nomi di istanza non univoci e le anomalie dei dati risultanti.

I nomi delle istanze devono essere stabili tra gli esempi, ovvero un provider deve usare lo stesso nome di istanza per la stessa entità ogni volta che viene raccolto il contatore.

Ogni contatore ha un tipo. Il tipo di contatore indica il tipo di valore non **elaborato** del contatore, ovvero un intero senza segno a 32 bit o un intero senza segno a 64 bit. Il tipo di contatore indica inoltre ciò che rappresenta il valore non elaborato del contatore, che determina la modalità di elaborazione del valore non elaborato per generare statistiche utili.

Anche se alcuni tipi di contatori sono semplici e hanno un valore non elaborato che è direttamente utile, molti tipi di contatori richiedono un' [elaborazione aggiuntiva](calculating-counter-values.md) per creare un **valore formattato** utile. Per produrre il valore formattato, alcuni tipi di contatori richiedono valori non elaborati di due campioni, alcuni tipi di contatori richiedono timestamp e alcuni tipi di contatori richiedono valori non elaborati da più contatori. Ad esempio:

- `PERF_COUNTER_LARGE_RAWCOUNT` è un valore non elaborato a 64 bit che non richiede l'elaborazione. È appropriato per i valori temporizzati, ad esempio "byte di memoria in uso".
- `PERF_COUNTER_RAWCOUNT_HEX` è un valore non elaborato a 32 bit che richiede che sia utile solo la formattazione esadecimale semplice. È appropriato per le informazioni di identificazione temporizzata o di identificazione, ad esempio "flag" o "indirizzo di base".
- `PERF_COUNTER_BULK_COUNT` è un valore non elaborato a 64 bit che indica un conteggio degli eventi e viene utilizzato per calcolare la velocità con cui si verificano gli eventi. Per essere utile, questo tipo di contatore richiede due esempi separati nel tempo. Il valore formattato è la frequenza dell'evento, ovvero il numero di volte in cui l'evento si è verificato al secondo nell'intervallo tra i due esempi. Dato due esempi `s0` e `s1` , il valore formattato (frequenza degli eventi) verrebbe calcolato come `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` .

Si prevede che i provider si comportino come se fossero senza stato, ovvero la raccolta di dati da un contatore non influisce in modo visibile sullo stato del provider. Un provider, ad esempio, non deve reimpostare i valori del contatore su 0 quando viene raccolto un contatore e non deve usare il timestamp di una raccolta precedente per modificare i valori nella raccolta corrente. Al contrario, deve fornire valori di contatori raw semplici con tipi accurati, in modo che il consumer possa calcolare statistiche utili in base ai valori non elaborati e ai relativi timestamp.

## <a name="performance-api-architecture"></a>Architettura API per le prestazioni

![Le applicazioni del contatore delle prestazioni richiamano le API Windows che chiamano i provider per ottenere i dati sulle prestazioni.](images/architecture.png)

I consumer dei contatori delle prestazioni includono:

- [Applicazioni fornite da Microsoft](performance-counters-tools.md) , ad esempio Gestione attività, monitoraggio risorse, Performance Monitor e typeperf.exe.
- Le aree API di alto livello fornite da Microsoft che espongono i dati dei contatori delle prestazioni, ad esempio [le classi di prestazioni WMI](/windows/desktop/WmiSdk/monitoring-performance-data).
- Le applicazioni o gli script che usano le [API di consumer del contatore delle prestazioni](consuming-counter-data.md).

La maggior parte degli utenti del contatore delle prestazioni usa le API di [PDH.dll](using-the-pdh-functions-to-consume-counter-data.md) per raccogliere dati sulle prestazioni. PDH gestisce molti aspetti complessi della raccolta dei contatori delle prestazioni, ad esempio l'analisi delle query, la corrispondenza di istanze tra più campioni e l'elaborazione di valori formattati dai dati del contatore non elaborati. L'implementazione di PDH usa le API del registro di sistema per l'utilizzo di dati da un provider v1 e usa le API di consumer V2 durante l'utilizzo di dati da un provider v2.

Alcuni utenti del contatore delle prestazioni meno recenti usano le [API del registro di sistema](using-the-registry-functions-to-consume-counter-data.md) per raccogliere dati sulle prestazioni dalla chiave speciale `HKEY_PERFORMANCE_DATA` del registro di sistema. Questa operazione non è consigliata per il nuovo codice perché l'elaborazione dei dati dal registro di sistema è complessa e soggetta a errori. L'implementazione dell'API del registro di sistema supporta direttamente la raccolta dei dati dai provider v1. Supporta indirettamente la raccolta dei dati dai provider v2 tramite un livello di conversione che usa le API consumer V2.

Alcuni utenti del contatore delle prestazioni usano le [funzioni consumer Perflib V2](using-the-perflib-functions-to-consume-counter-data.md) per accedere direttamente ai dati dai provider v2. Si tratta di un approccio più complesso rispetto all'utilizzo di dati tramite le API PDH, ma questo approccio può essere utile se non è possibile utilizzare le API PDH a causa di problemi relativi alle prestazioni o alle dipendenze. L'implementazione di PerfLib V2 supporta direttamente la raccolta dei dati dai provider v2. Non supporta la raccolta dei dati dai provider v1.

> [!NOTE]
> Windows OneCore non include PDH.dll e non include il supporto per l'utilizzo di dati dei contatori delle prestazioni tramite le API del registro di sistema. I consumer in esecuzione su OneCore devono usare le funzioni consumer PerfLib V2.

I provider v1 vengono implementati come DLL del provider caricata nel processo del consumer. L'implementazione dell'API del registro di sistema gestisce il caricamento della DLL del provider, la chiamata alla DLL per raccogliere i dati sulle prestazioni e lo scaricamento della DLL nel modo appropriato. La DLL del provider è responsabile della [raccolta dei dati sulle prestazioni in base alle esigenze](communicating-with-your-application.md), ad esempio tramite API Windows normali, RPC, named pipe, Shared Memory o altri meccanismi di comunicazione interprocesso.

I provider v2 vengono implementati come programma in modalità utente (spesso un servizio Windows) o come driver in modalità kernel. In genere, il codice del provider di dati sulle prestazioni è integrato direttamente in un componente esistente (ovvero il driver o il servizio sta segnalando le statistiche relative a se stesso). L'implementazione di PerfLib V2 gestisce le richieste e le risposte tramite il PCW.sys estensione del kernel, in modo che il provider non debba in genere implementare alcuna comunicazione interprocesso per fornire i dati sulle prestazioni.

> [!NOTE]
> Gli strumenti e le API dei contatori delle prestazioni di Windows includono supporto limitato per l'accesso ai contatori delle prestazioni da altri computer tramite registro di sistema remoto (per i provider v1) e RPC (per i provider v2). Questo supporto è spesso difficile da usare in termini di controlli di autenticazione (gli strumenti e le API possono autenticarsi solo come utente corrente), oltre che in termini di [configurazione del sistema](accessing-remote-counter-data.md) (gli endpoint e i servizi necessari sono disabilitati per impostazione predefinita). In molti casi, è preferibile accedere ai contatori delle prestazioni dei sistemi remoti tramite [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) anziché tramite il supporto predefinito di accesso remoto.

## <a name="developer-audience"></a>Sviluppatori

I contatori delle prestazioni vengono spesso utilizzati dagli amministratori per identificare i problemi di prestazioni o il comportamento anomalo dei sistemi, dagli sviluppatori per studiare l'utilizzo delle risorse dei componenti software e dai singoli utenti per comprendere come si comportano i programmi nel proprio sistema. L'utilizzo può essere eseguito tramite strumenti GUI come gestione attività o performance monitor, strumenti da riga di comando come typeperf.exe o logman.exe, tramite scripting tramite WMI e PowerShell oppure tramite le API C/C++ e .NET.

I provider dei contatori delle prestazioni vengono in genere implementati come driver in modalità kernel o in modalità utente. I provider del contatore delle prestazioni vengono in genere scritti in C o C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.

Per la cronologia delle versioni [, vedere Novità](performance-counters-what-s-new.md).

## <a name="see-also"></a>Vedi anche

[Utilizzo dei contatori delle prestazioni](using-performance-counters.md)

[Riferimento ai contatori delle prestazioni](performance-counters-reference.md)
