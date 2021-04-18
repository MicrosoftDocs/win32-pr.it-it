---
description: 'Si tratta di una panoramica di cosa aspettarsi per il percorso end-to-end di un evento per ognuna delle quattro tecnologie di traccia fornite da Microsoft: TraceLogging, basato su manifesto, WPP e MOF.'
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: Cenni preliminari sui metadati degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c16853ef2639fd560f5b5da30447556119ec877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484364"
---
# <a name="event-metadata-overview"></a>Cenni preliminari sui metadati degli eventi

Si tratta di una panoramica di cosa aspettarsi per il percorso end-to-end di un evento per ognuna delle quattro tecnologie di traccia fornite da Microsoft: [TraceLogging](../tracelogging/trace-logging-about.md), [basato su manifesto](writing-manifest-based-events.md), [WPP](windows-software-trace-preprocessor.md)e [MOF](tracing-events.md). Si avvicina al problema rispetto al payload di un singolo evento e ai metadati associati che ne descrivono la struttura, rendendo possibile la decodifica successiva dell'evento in porzioni di dati sensibili. Comprendere il percorso di ogni evento è importante quando si sceglie quale tecnologia di traccia è appropriata per un progetto. Non esiste alcuna soluzione per la traccia di una dimensione.

## <a name="event-payloads"></a>Payload dell'evento

Per qualsiasi tecnologia di traccia fornita da Microsoft, quando si chiama il comando Write (ad esempio [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) per [**TraceLoggingWrite**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) basato su manifesto o per TraceLogging), i dati forniti per l'evento in fase di esecuzione vengono ridotti in un BLOB binario contiguo denominato payload dell'evento. Si tratta di un codice separato dallo schema di eventi o dai metadati dell'evento (illustrati di seguito), che descrive il layout di questo BLOB binario per la decodifica degli strumenti. Il modo in cui viene eseguita la generazione del payload dell'evento varia a seconda della tecnologia di traccia usata e infine se l'evento è classico (stile [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) ) o moderno (stile **EventWrite** ).

Per gli eventi classici, il flag [**nell' \_ \_ intestazione della traccia dell'evento**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) viene passato a [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) , che determina il modo in cui si verifica:

\- Se **il \_ flag WNODE \_ utilizza \_ MOF \_ ptr** viene specificato, una matrice [**di \_ campi MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) segue l' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) in memoria. Il runtime ETW concatenerà i dati dell'evento come specificato in questi campi per formare il payload dell'evento.

\- Se **il \_ flag WNODE \_ utilizza \_ MOF \_ ptr** non è specificato, il payload dell'evento viene costruito dall'utente direttamente in memoria dopo l' [**\_ \_ intestazione di traccia dell'evento**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).

Sia MOF che WPP sono provider classici. Tuttavia, l'implementazione di WPP si occupa automaticamente di tutti questi riconoscimenti.

Per gli eventi non classici, un numero di [**\_ \_ descrittori di dati evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) viene passato a [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite). Il runtime ETW concatenerà i dati dell'evento come specificato nei descrittori per formare il payload dell'evento.

Le tecnologie basate su manifesto e TraceLogging sono generalmente provider moderni. Con basato su manifesto, se si consente a mc.exe di generare automaticamente il codice di registrazione (switch um o km), la generazione del payload viene eseguita automaticamente. La generazione del payload viene sempre eseguita da TraceLogging.

Il risultato finale è che un payload per un evento viene generato in fase di esecuzione. Tutti i payload sono fondamentalmente simili in quanto si tratta di BLOB binari di dati contenenti solo i dati del campo per quel particolare evento, indipendentemente dalla tecnologia di traccia utilizzata e dai tipi di campo supportati da tale tecnologia di traccia. Senza i metadati dell'evento, il payload dell'evento non è significativo e incomprensibile.

Il compito del runtime ETW consiste quindi nell'eseguire questo BLOB di eventi dal provider al consumer, dove viene riassociato ai relativi metadati e diventa decodificabile. Tramite il runtime ETW vengono aggiunti alcuni metadati aggiuntivi che indicano le circostanze del payload, ad esempio le parole chiave timestamp, ID thread e l'evento. Queste informazioni sono rilevanti per il modo in cui l'evento è stato instradato tramite il runtime ed è utile anche per comprendere l'identità e il contesto dell'evento in fase di decodifica. Viene infine esposto come parte della [**\_ traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace) o del record dell' [**evento \_**](/windows/win32/api/evntcons/ns-evntcons-event_record) per il consumer

## <a name="event-metadata"></a>Metadati dell'evento

Il percorso dei metadati degli eventi è diverso a seconda della tecnologia di traccia utilizzata ed è una delle considerazioni più importanti per il confronto di ogni tecnologia.

### <a name="mof"></a>MOF

I metadati dell'evento vengono creati manualmente dal creatore dell'evento sotto forma di uno schema MOF speciale in un file MOF. Lo schema creato deve corrispondere al payload che viene registrato per consentire la decodifica corretta dell'evento da parte dei consumer. Per i decodificatori di eventi è necessario che il file con estensione MOF sia registrato nel sistema utilizzando [mofcomp.exe](../wmisdk/mofcomp.md). Per ulteriori informazioni sulla pubblicazione di schemi MOF, vedere la pagina relativa alla [pubblicazione dello schema di eventi per un provider classico](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>WPP

I metadati degli eventi vengono generati e archiviati automaticamente nel file PDB del file binario da tracewpp.exe durante il processo di compilazione. Questi metadati possono essere estratti in un secondo momento sotto forma di file con estensione MDF autonomo tramite tracepdb.exe. I decodificatori di eventi richiedono in genere il file con estensione PDB o MDF. Per ulteriori informazioni su tracepdb.exe, vedere [Panoramica di TracePdb](/windows-hardware/drivers/devtest/tracepdb-overview)e per altre informazioni sui tracewpp.exe, vedere [attività TraceWPP](/windows-hardware/drivers/devtest/tracewpp-task).

### <a name="manifest-based"></a>Basata su manifesto

Le definizioni degli eventi vengono create in un file con estensione Man. I manifesti dell'evento vengono eseguiti tramite il compilatore del manifesto ([mc.exe](../wes/message-compiler--mc-exe-.md)), generando le intestazioni necessarie per la compilazione dell'origine, oltre a diversi file di risorse binari. bin. Questi file di risorse devono quindi essere compilati come risorse in un file binario e il file binario risultante sul sistema che intende decodificare gli eventi del provider basato su manifesto. Inoltre, il manifesto deve essere installato nel sistema utilizzando [wevtutil.exe](../wes/windows-event-log-tools.md) più importante, gli attributi **resourceFileName** e **messageFileName** nell'elemento XML del provider nel manifesto dell'evento installato devono identificare correttamente il percorso assoluto completo del file binario in cui sono stati inseriti i file di risorse. Si noti che questi percorsi possono essere sovrascritti al momento dell'installazione del manifesto usando le opzioni wevtutil.exe/RF e/MF. Un sistema che non è in grado di eseguire correttamente questa procedura non sarà in grado di decodificare gli eventi di questo provider. I decodificatori di eventi richiedono quindi un manifesto installato e il file binario con le risorse associate installate nel percorso specificato dai percorsi dei file di risorse e messaggi. Per ulteriori informazioni sulla pubblicazione di schemi basati su manifesto, vedere la pagina relativa alla [pubblicazione dello schema di eventi per un provider basato su manifesto](publishing-your-event-schema-for-a-manifest-base-provider.md).

### <a name="tracelogging"></a>TraceLogging

Tutti gli eventi TraceLogging sono autodescrittivi. I metadati dell'evento necessari per decodificare l'evento vengono generati automaticamente e trasmessi insieme al payload in un formato binario compatto. I decodificatori di evento necessitano solo dell'evento TraceLogging e comprendono il formato dei metadati TraceLogging.

## <a name="configuring-tdh-for-decoding"></a>Configurazione di TDH per la decodifica

Sono disponibili molti strumenti di decodifica. Tuttavia, si consiglia di usare TDH, laddove possibile, perché decodifica tutte le tecnologie di traccia con un'API unificata. A seconda del tipo di traccia di cui si è interessati per la decodifica, TDH potrebbe richiedere una configurazione esplicita.

### <a name="mof"></a>MOF

TDH utilizza i dati di decodifica MOF registrati nel sistema utilizzando mofcomp.exe. Per ulteriori informazioni, vedere la pagina relativa alla [pubblicazione dello schema di eventi per un provider classico](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>WPP

TDH deve puntare al file con estensione PDB o all'MDF associato per il provider WPP che si sta tentando di decodificare. Questa operazione può essere eseguita chiamando [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter). In caso contrario, il motore di decodifica eseguirà il fallback sul percorso di ricerca del formato di traccia della variabile di ambiente \_ \_ \_ .

### <a name="manifest-based"></a>Basata su manifesto

TDH utilizza tutti i provider basati su manifesto registrati nel sistema utilizzando wevtutil.exe.

### <a name="tracelogging"></a>TraceLogging

Le versioni più recenti di TDH rilevano e decodificano automaticamente gli eventi TraceLogging senza ulteriori passaggi.

 

 
