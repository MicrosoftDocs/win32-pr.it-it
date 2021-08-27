---
description: Event Tracing for Windows (ETW) è un'efficiente funzionalità di traccia a livello di kernel che consente di registrare eventi definiti dall'applicazione o kernel in un file di log.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: Informazioni su Event Tracing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5004ada6d0d11d9c232a6fda1553ea24de5a59fb1d03e46728084f84f0e79de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086431"
---
# <a name="about-event-tracing"></a>Informazioni su Event Tracing

Event Tracing for Windows (ETW) è un'efficiente funzionalità di traccia a livello di kernel che consente di registrare eventi definiti dall'applicazione o kernel in un file di log. È possibile utilizzare gli eventi in tempo reale o da un file di log e usarli per eseguire il debug di un'applicazione o per determinare dove si verificano problemi di prestazioni nell'applicazione.

ETW consente di abilitare o disabilitare la traccia eventi in modo dinamico, consentendo di eseguire la traccia dettagliata in un ambiente di produzione senza richiedere il riavvio del computer o dell'applicazione.

L'API Event Tracing è suddivisa in tre componenti distinti:

-   [Controller](#controllers), che avviano e arrestano una sessione di traccia eventi e abilitano i provider
-   [Provider](#providers), che forniscono gli eventi
-   [Consumer](#consumers), che utilizzano gli eventi

Il diagramma seguente illustra il modello di traccia eventi.

![modello di traccia eventi](images/etdiag2.png)

## <a name="controllers"></a>Controllers

I controller sono applicazioni che definiscono le dimensioni e il percorso del file di log, avviano e arrestano le sessioni di traccia [eventi,](event-tracing-sessions.md)abilitano i provider in modo che possano registrare eventi nella sessione, gestire le dimensioni del pool di buffer e ottenere statistiche di esecuzione per le sessioni. Le statistiche di sessione includono il numero di buffer utilizzati, il numero di buffer recapitati e il numero di eventi e buffer persi. 

Per altre informazioni, vedere [Controllo delle sessioni di traccia eventi.](controlling-event-tracing-sessions.md)

## <a name="providers"></a>Provider

I provider sono applicazioni che contengono la strumentazione di traccia eventi. Dopo la registrazione di un provider, un controller può quindi abilitare o disabilitare la traccia eventi nel provider. Il provider definisce l'interpretazione di essere abilitato o disabilitato. In genere, un provider abilitato genera eventi, mentre un provider disabilitato non lo genera. In questo modo è possibile aggiungere la traccia eventi all'applicazione senza richiedere che generi sempre eventi. 

Anche se il modello ETW separa il controller e il provider in applicazioni separate, un'applicazione può includere entrambi i componenti.

Per altre informazioni, vedere [Specifica di eventi.](providing-events.md)

### <a name="types-of-providers"></a>Tipi di provider

Esistono quattro tipi principali di provider: provider MOF (versione classica), provider WPP, provider basati su manifesto e provider TraceLogging. È consigliabile usare un provider basato su manifesto o un provider TraceLogging se si scrivono applicazioni per Windows Vista o versioni successive che non devono supportare sistemi legacy.

#### <a name="mof-classic-providers"></a>Provider MOF (versione classica):

-   Usare le [funzioni RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) [e TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) per registrare e scrivere eventi.
-   Usare le classi MOF per definire gli eventi in modo che i consumer sappiano come utilizzarli.
-   Può essere abilitato da una sola sessione di traccia alla volta.

#### <a name="wpp-providers"></a>Provider WPP:

-   Usare le [funzioni RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) [e TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) per registrare e scrivere eventi.
-   Avere file TMF associati (compilati in un file PDB di un file binario) contenenti informazioni di decodifica dedotto dall'analisi del preprocessore della strumentazione WPP nel codice sorgente.
-   Può essere abilitato da una sola sessione di traccia alla volta.

#### <a name="manifest-based-providers"></a>Provider basati su manifesto:

-   Usare [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) ed [EventWrite per](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) registrare e scrivere eventi.
-   Usare un manifesto per definire gli eventi in modo che i consumer sappiano come utilizzarli.
-   Può essere abilitato da un massimo di otto sessioni di traccia contemporaneamente.

#### <a name="tracelogging-providers"></a>[Provider TraceLogging:](/windows/desktop/tracelogging/trace-logging-about)

-   Usare [TraceLoggingRegister e](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) per registrare e scrivere eventi.
-   Usare eventi autodescritti in modo che gli eventi stessi contengano tutte le informazioni necessarie per utilizzarli.
-   Può essere abilitato da un massimo di otto sessioni di traccia contemporaneamente.

Tutti i provider di eventi usano fondamentalmente la famiglia di API Event Tracing ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) per le tecnologie legacy e [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) per quelle più recenti). I provider di eventi si differenziano semplicemente per i tipi di campo archiviati nei payload degli eventi e per la posizione in cui archiviano le informazioni di decodifica degli eventi associate.

## <a name="consumers"></a>Consumer

I consumer sono applicazioni che selezionano una o più sessioni di traccia eventi come origine degli eventi. Un consumer può richiedere eventi da più sessioni di traccia eventi contemporaneamente. il sistema recapita gli eventi in ordine cronologico. I consumer possono ricevere eventi archiviati in file di log o da sessioni che recapitare eventi in tempo reale. Durante l'elaborazione degli eventi, un consumer può specificare l'ora di inizio e di fine e verranno recapitati solo gli eventi che si verificano nell'intervallo di tempo specificato. 

Per altre informazioni, vedere [Utilizzo di eventi.](consuming-events.md)

## <a name="missing-events"></a>Eventi mancanti

Perfmon, Diagnostica di sistema e altri strumenti di sistema possono segnalare eventi mancanti nel registro eventi e indicare che le impostazioni per Event Tracing for Windows (ETW) potrebbero non essere ottimali. Gli eventi possono essere persi per diversi motivi:

-   La dimensione totale dell'evento è maggiore di 64 KB. Sono inclusi l'intestazione ETW e i dati o il payload. Un utente non ha alcun controllo su questi eventi mancanti perché le dimensioni dell'evento sono configurate dall'applicazione.

-   Le dimensioni del buffer ETW sono inferiori alle dimensioni totali dell'evento. Un utente non ha alcun controllo su questi eventi mancanti perché le dimensioni dell'evento sono configurate dall'applicazione che gli ha registrati.

-   Per la registrazione in tempo reale, il consumer in tempo reale non sta utilizzando gli eventi abbastanza rapidamente o non è completamente presente e quindi il file di backup si sta riempiendo. Ciò può verificarsi se il servizio Registro eventi viene arrestato e avviato quando vengono registrati gli eventi. Un utente non ha alcun controllo su questi eventi mancanti.

-   Quando si esegue la registrazione in un file, il disco è troppo lento per rimanere al passo con la velocità di registrazione.

Per uno di questi motivi, segnalare questi problemi al provider dell'applicazione o del servizio che genera gli eventi. Questi problemi possono essere risolti solo dallo sviluppatore dell'applicazione o dal servizio che registrazione gli eventi. Se gli eventi mancanti vengono segnalati nel servizio Registro eventi, è possibile che si sia verificato un problema con la configurazione del servizio Registro eventi. L'utente potrebbe avere una capacità limitata di aumentare lo spazio massimo su disco che deve essere usato dal servizio Registro eventi, riducendo il numero di eventi mancanti.

 

 
