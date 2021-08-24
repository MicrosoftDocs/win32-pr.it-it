---
description: 'Questa è una panoramica di cosa aspettarsi per il percorso end-to-end di un evento per ognuna delle quattro tecnologie di traccia fornite da Microsoft: TraceLogging, basata su manifesto, WPP e MOF.'
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: Panoramica dei metadati degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931b8adbdb22cdbf2e0806e2d69c367e64ad92926390825a48a2fa51d50605ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755061"
---
# <a name="event-metadata-overview"></a>Panoramica dei metadati degli eventi

Questa è una panoramica di cosa aspettarsi per il percorso end-to-end di un evento per ognuna delle quattro tecnologie di traccia fornite da Microsoft: [TraceLogging,](../tracelogging/trace-logging-about.md) [basata](writing-manifest-based-events.md)su manifesto, [WPP](windows-software-trace-preprocessor.md)e [MOF.](tracing-events.md) Affronta il problema sia per quanto riguarda il payload di un singolo evento che i metadati associati che ne descrivono la struttura, rendendo possibile decodificare in un secondo momento l'evento in parti ragionevoli di dati. Comprendere il percorso di ogni parte di un evento è importante quando si sceglie la tecnologia di traccia appropriata per un progetto. Non esiste una soluzione unica per la traccia.

## <a name="event-payloads"></a>Payload degli eventi

Per qualsiasi tecnologia di traccia fornita da Microsoft, quando si chiama il comando Write (ad esempio [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) per basata su manifesto o [**TraceLoggingWrite**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) per TraceLogging), i dati forniti per l'evento in fase di esecuzione vengono ripiegati in un BLOB binario contiguo denominato payload dell'evento. Questo è separato dallo schema di eventi o dai metadati degli eventi (illustrati di seguito), che descrive il layout di questo BLOB binario per gli strumenti di decodifica. La modalità di generazione esatta del payload dell'evento varia a seconda della tecnologia di traccia usata e, in ultima analisi, se l'evento è classico (stile [**TraceEvent)**](/windows/win32/api/evntrace/nf-evntrace-traceevent) o moderno **(stile EventWrite).**

Per gli eventi classici, il flag in [**EVENT \_ TRACE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) viene passato a [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) che determina come si verifica questa situazione:

\- Se **si specifica WNODE FLAG USE \_ \_ \_ MOF \_ PTR,** una matrice di [**CAMPI MOF \_**](/windows/win32/api/evntrace/ns-evntrace-mof_field) segue l'INTESTAZIONE EVENT [**\_ TRACE \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) in memoria. Il runtime ETW concatena i dati dell'evento come specificato in questi campi per formare il payload dell'evento.

\- Se **WNODE \_ FLAG USE \_ \_ MOF \_ PTR** non viene specificato, il payload dell'evento viene costruito direttamente in memoria dall'utente dopo [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).

MoF e WPP sono provider classici. Tuttavia, l'implementazione WPP si occupa di tutto questo per conto dell'utente.

Per gli eventi non classici, in EventWrite vengono passati diversi [**\_ \_ DESCRITTORI**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) DI DATI [**EVENTI.**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) Il runtime ETW concatena i dati dell'evento come specificato in questi descrittori per formare il payload dell'evento.

Entrambe le tecnologie basate su manifesto e TraceLogging sono in genere provider moderni. Con il manifesto, se si mc.exe generare automaticamente il codice di registrazione (opzione um o km), la generazione del payload viene eseguita automaticamente. La generazione del payload viene sempre curata da TraceLogging.

Il risultato finale è che viene generato un payload per un evento in fase di esecuzione. Tutti i payload sono fondamentalmente simili in quanto sono BLOB binari di dati contenenti solo i dati di campo per quel particolare evento, indipendentemente dalla tecnologia di traccia usata e dai tipi di campo supportati da tale tecnologia di traccia. Senza i metadati dell'evento, il payload dell'evento non ha significato e non è incomprensibile.

Il runtime ETW deve quindi portare questo BLOB di eventi dal provider al consumer, dove viene nuovamente associato ai metadati e diventa decodificabile. Il runtime ETW aggiungerà alcuni metadati aggiuntivi che indicano le circostanze del payload, ad esempio elementi come il timestamp, l'ID thread e le parole chiave dell'evento. Queste informazioni sono rilevanti per il modo in cui l'evento è stato indirizzato tramite il runtime ed è anche utile per comprendere l'identità e il contesto dell'evento in fase di decodifica. Viene infine visualizzato come parte di [**EVENT \_ TRACE**](/windows/win32/api/evntrace/ns-evntrace-event_trace) o [**EVENT \_ RECORD**](/windows/win32/api/evntcons/ns-evntcons-event_record) per il consumer

## <a name="event-metadata"></a>Metadati degli eventi

Il percorso per i metadati degli eventi è diverso a seconda della tecnologia di traccia usata ed è una delle considerazioni più importanti quando si confronta ogni tecnologia.

### <a name="mof"></a>MOF

I metadati dell'evento vengono creati manualmente dal creatore dell'evento sotto forma di uno schema MOF speciale in un file mof. Lo schema creato deve corrispondere al payload registrato per consentire la decodifica corretta dell'evento da parte dei consumer. I decodificatori di eventi richiedono che il file mof sia registrato nel sistema [ usandomofcomp.exe](../wmisdk/mofcomp.md). Per altre informazioni sulla pubblicazione di schemi MOF, vedere [Pubblicazione dello schema di eventi per un provider classico](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>Wpp

I metadati degli eventi vengono generati e archiviati automaticamente nel file con estensione pdb del file tracewpp.exe durante il processo di compilazione. Questi metadati possono essere estratti in un secondo momento sotto forma di file con estensione tmf autonomo tracepdb.exe. I decodificatori di eventi richiedono in genere il file con estensione pdb o tmf. Per altre informazioni sui tracepdb.exe, vedere Panoramica di [Tracepdb](/windows-hardware/drivers/devtest/tracepdb-overview)e per altre informazioni sull'tracewpp.exe, vedere [Attività TraceWPP](/windows-hardware/drivers/devtest/tracewpp-task).

### <a name="manifest-based"></a>Basata su manifesto

Le definizioni degli eventi vengono scritte in un file con estensione man. I manifesti degli eventi vengono eseguiti tramite il compilatore manifesto ([mc.exe](../wes/message-compiler--mc-exe-.md)), generando le intestazioni necessarie per la compilazione dell'origine e diversi file di risorse binari con estensione bin. Questi file di risorse devono quindi essere compilati come risorse in un file binario e il file binario risultante inserito nel sistema che intende decodificare gli eventi da tale provider basato su manifesto. Inoltre, il manifesto deve essere installato nel sistema usando [wevtutil.exe](../wes/windows-event-log-tools.md) Soprattutto, gli attributi **resourceFileName** e **messageFileName** nell'elemento XML del provider nel manifesto dell'evento installato devono identificare correttamente il percorso assoluto completo del file binario in cui sono stati inseriti i file di risorse. Si noti che questi percorsi possono essere sovrascritti in fase di installazione del manifesto usando le wevtutil.exe /rf e /mf. Un sistema che non ha eseguito correttamente e completamente questi passaggi non sarà in grado di decodificare gli eventi da questo provider. I decodificatori di eventi richiedono quindi un manifesto installato e il file binario con le risorse associate installate nel percorso specificato dai percorsi dei file di risorse e messaggi. Per altre informazioni sulla pubblicazione di schemi basati su manifesto, vedere [Pubblicazione dello schema di eventi per un provider basato su manifesto](publishing-your-event-schema-for-a-manifest-base-provider.md).

### <a name="tracelogging"></a>TraceLogging

Tutti gli eventi TraceLogging sono autodescritti. I metadati dell'evento necessari per decodificare l'evento vengono generati e trasmessi automaticamente insieme al payload in un formato binario compatto. I decodificatori di eventi necessitano solo dell'evento TraceLogging e di una conoscenza del formato dei metadati TraceLogging.

## <a name="configuring-tdh-for-decoding"></a>Configurazione di TDH per la decodifica

Sono disponibili molti strumenti di decodifica. È tuttavia consigliabile usare TDH laddove possibile, perché decodifica tutte le tecnologie di traccia con un'API unificata. A seconda del tipo di traccia interessata alla decodifica, TDH può richiedere una configurazione esplicita.

### <a name="mof"></a>MOF

TDH usa i dati di decodifica MOF registrati nel sistema usando mofcomp.exe. Per altre informazioni, vedere [Pubblicazione dello schema di eventi per un provider classico.](publishing-your-event-schema-for-a-classic-provider.md)

### <a name="wpp"></a>Wpp

TDH deve essere puntato al file con estensione pdb o al file con estensione tmf associato per il provider WPP che si sta tentando di decodificare. Questa operazione può essere eseguita chiamando [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter). In caso contrario, il motore di decodifica eseguire il fall back sulla variabile di ambiente TRACE \_ FORMAT \_ SEARCH \_ PATH.

### <a name="manifest-based"></a>Basata su manifesto

TDH usa tutti i provider basati su manifesto registrati nel sistema usando wevtutil.exe.

### <a name="tracelogging"></a>TraceLogging

Le versioni più recenti di TDH rilevano e decodificano automaticamente gli eventi TraceLogging senza passaggi aggiuntivi.

 

 
