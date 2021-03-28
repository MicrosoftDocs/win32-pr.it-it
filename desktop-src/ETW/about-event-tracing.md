---
description: Event Tracing for Windows (ETW) è una funzionalità di traccia a livello di kernel efficiente che consente di registrare gli eventi del kernel o definiti dall'applicazione in un file di log.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: Informazioni sulla traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2f13284cec1d9300c23241fafe154f277f72a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966837"
---
# <a name="about-event-tracing"></a>Informazioni sulla traccia eventi

Event Tracing for Windows (ETW) è una funzionalità di traccia a livello di kernel efficiente che consente di registrare gli eventi del kernel o definiti dall'applicazione in un file di log. È possibile utilizzare gli eventi in tempo reale o da un file di log e utilizzarli per eseguire il debug di un'applicazione o per determinare la posizione in cui si verificano problemi di prestazioni nell'applicazione.

ETW consente di abilitare o disabilitare la traccia eventi in modo dinamico, consentendo di eseguire analisi dettagliate in un ambiente di produzione senza richiedere il riavvio del computer o dell'applicazione.

L'API di traccia eventi è suddivisa in tre componenti distinti:

-   [Controller](#controllers), che avviano e arrestano una sessione di traccia eventi e abilitano i provider
-   [Provider](#providers), che forniscono gli eventi
-   [Consumer](#consumers), che utilizzano gli eventi

Il diagramma seguente illustra il modello di traccia eventi.

![modello di traccia eventi](images/etdiag2.png)

## <a name="controllers"></a>Controllers

I controller sono applicazioni che definiscono le dimensioni e la posizione del file di log, avviano e arrestano le [sessioni di traccia eventi](event-tracing-sessions.md), abilitano i provider in modo che possano registrare gli eventi nella sessione, gestire le dimensioni del pool di buffer e ottenere statistiche di esecuzione per le sessioni. Le statistiche della sessione includono il numero di buffer utilizzati, il numero di buffer recapitati e il numero di eventi e buffer persi. 

Per ulteriori informazioni, vedere [controllo delle sessioni di traccia eventi](controlling-event-tracing-sessions.md).

## <a name="providers"></a>Provider

I provider sono applicazioni che contengono la strumentazione di traccia eventi. Dopo la registrazione di un provider, un controller può quindi abilitare o disabilitare la traccia eventi nel provider. Il provider definisce l'interpretazione dell'abilitazione o disabilitazione. In genere, un provider abilitato genera eventi, mentre un provider disabilitato non lo consente. In questo modo è possibile aggiungere la traccia eventi all'applicazione senza che sia necessario generare eventi sempre. 

Anche se il modello ETW separa il controller e il provider in applicazioni separate, un'applicazione può includere entrambi i componenti.

Per ulteriori informazioni, vedere la pagina relativa alla [fornitura di eventi](providing-events.md).

### <a name="types-of-providers"></a>Tipi di provider

Sono disponibili quattro tipi principali di provider: i provider MOF (classico), i provider WPP, i provider basati su manifesto e i provider TraceLogging. Se si scrivono applicazioni per Windows Vista o versioni successive, è necessario utilizzare un provider basato su manifesto o un provider TraceLogging per cui non è necessario supportare i sistemi legacy.

#### <a name="mof-classic-providers"></a>Provider MOF (classico):

-   Usare le funzioni [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) e [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) per registrare e scrivere gli eventi.
-   Utilizzare le classi MOF per definire gli eventi in modo che i consumer sappiano come utilizzarli.
-   Può essere abilitato da una sola sessione di traccia alla volta.

#### <a name="wpp-providers"></a>Provider WPP:

-   Usare le funzioni [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) e [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) per registrare e scrivere gli eventi.
-   Sono stati associati i file MDF (compilati nel file PDB di un file binario) contenenti informazioni di decodifica derivate dall'analisi del preprocessore della strumentazione WPP nel codice sorgente.
-   Può essere abilitato da una sola sessione di traccia alla volta.

#### <a name="manifest-based-providers"></a>Provider basati su manifesto:

-   Usare [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) e [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) per registrare e scrivere gli eventi.
-   Utilizzare un manifesto per definire gli eventi in modo che i consumer sappiano come utilizzarli.
-   Può essere abilitato fino a otto sessioni di traccia simultaneamente.

#### <a name="tracelogging-providers"></a>Provider [TraceLogging](/windows/desktop/tracelogging/trace-logging-about) :

-   Usare [TraceLoggingRegister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) e [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) per registrare e scrivere gli eventi.
-   Usare gli eventi autodescrittivi in modo che gli eventi stessi contengano tutte le informazioni necessarie per l'utilizzo.
-   Può essere abilitato fino a otto sessioni di traccia simultaneamente.

Tutti i provider di eventi utilizzano fondamentalmente la famiglia di API di analisi degli eventi ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) per le tecnologie legacy e [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) per le versioni più recenti). I provider di eventi differiscono semplicemente per i tipi di campo archiviati nei payload dell'evento e dove archiviano le informazioni di decodifica degli eventi associati.

## <a name="consumers"></a>Consumer

I consumer sono applicazioni che selezionano una o più sessioni di traccia eventi come origine di eventi. Un consumer può richiedere eventi contemporaneamente da più sessioni di traccia eventi; il sistema recapita gli eventi in ordine cronologico. I consumer possono ricevere eventi archiviati nei file di log o da sessioni che inviano eventi in tempo reale. Quando si elaborano gli eventi, un consumer può specificare l'ora di inizio e di fine e verranno recapitati solo gli eventi che si verificano nell'intervallo di tempo specificato. 

Per ulteriori informazioni, vedere [utilizzo degli eventi](consuming-events.md).

## <a name="missing-events"></a>Eventi mancanti

PerfMon, diagnostica di sistema e altri strumenti di sistema possono segnalare eventi mancanti nel registro eventi e indicare che le impostazioni per Event Tracing for Windows (ETW) potrebbero non essere ottimali. Gli eventi possono essere persi per diversi motivi:

-   La dimensione totale dell'evento è maggiore di 64K. Sono incluse l'intestazione ETW e i dati o il payload. Un utente non ha alcun controllo sugli eventi mancanti, perché la dimensione dell'evento è configurata dall'applicazione.

-   Le dimensioni del buffer ETW sono inferiori alle dimensioni totali dell'evento. Un utente non ha alcun controllo sugli eventi mancanti poiché le dimensioni dell'evento sono configurate dall'applicazione per la registrazione degli eventi.

-   Per la registrazione in tempo reale, il consumer in tempo reale non utilizza gli eventi in modo sufficientemente rapido o non è presente nel suo complesso e quindi il file di supporto si riempie. Questo può verificarsi se il servizio Registro eventi viene arrestato e avviato quando si registrano gli eventi. Un utente non ha alcun controllo sugli eventi mancanti.

-   Quando si esegue la registrazione in un file, il disco è troppo lento per restare al passo con la frequenza di registrazione.

Per questi motivi, segnalare questi problemi al provider dell'applicazione o del servizio che genera gli eventi. Questi problemi possono essere corretti solo dallo sviluppatore dell'applicazione o dal servizio che registra gli eventi. Se gli eventi mancanti vengono segnalati nel servizio Registro eventi, questo potrebbe indicare un problema con la configurazione del servizio Registro eventi. L'utente può avere una certa capacità di aumentare lo spazio su disco massimo che può essere utilizzato dal servizio Registro eventi, in modo da ridurre il numero di eventi mancanti.

 

 
