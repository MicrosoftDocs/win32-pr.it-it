---
title: Traccia di rete nell'architettura di Windows 7
description: Nella figura seguente è illustrata l'architettura di base della traccia di rete in Windows 7.
ms.assetid: b3023469-0f98-451c-b39f-c3eae771eacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41221ebf434c05a8c9b7c8489e861128029b5320
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300370"
---
# <a name="network-tracing-in-windows-7-architecture"></a>Traccia di rete in Windows 7: architettura

Nella figura seguente è illustrata l'architettura di base della traccia di rete in Windows 7.

![diagramma dell'architettura di traccia di rete](images/ut1.png)

La traccia di rete utilizza il Framework di Event Tracing for Windows (ETW) disponibile in Windows. I componenti di rete (ad esempio Winsock, TCP/IP, NDIS, acquisizione pacchetti e così via) vengono registrati come provider di traccia ETW ed emettono eventi correlati all'attività di rete. Qualsiasi attività registrabile di significato può essere un evento registrato in ETW. La traccia per questi componenti di rete e le acquisizioni di pacchetti può essere abilitata usando il contesto di **traccia Netsh** che funge da controller ETW.

Le tracce generate vengono raccolte in un file di log di traccia eventi (ETL). Questi file ETL possono quindi essere analizzati utilizzando diversi strumenti, ad esempio Network Monitor 3,2 e versioni successive, Visualizzatore eventi, **netsh trace Convert** o Tracerpt.exe.

Ogni evento ETW dispone di un'intestazione comune in cui ETW archivia informazioni quali le proprietà, i timestamp e l'ID attività dell'evento. Per ulteriori informazioni sugli ID attività, vedere [scrittura di eventi correlati in uno scenario end-to-end](../etw/writing-related-events-in-an-end-to-end-scenario.md). L'ID attività viene utilizzato per correlare gli eventi. In modalità utente gli ID attività vengono archiviati nei thread e tutti gli eventi registrati in un thread verranno automaticamente contrassegnati con lo stesso ID attività. In modalità kernel, l'ID attività deve essere passato in modo esplicito quando viene registrato un evento. Per impostazione predefinita, i file ETL sono correlati a raggruppare gli eventi in ID attività specifici.

Per ulteriori informazioni sugli eventi di Windows e ETW, vedere [eventi di Windows](../events/windows-events.md).

## <a name="etw-components-in-network-tracing"></a>Componenti ETW nella traccia di rete

La traccia di rete usa ETW come meccanismo di traccia principale per fornire informazioni sulle attività dei sottosistemi di rete. In ETW sono presenti quattro componenti principali: sessioni di traccia eventi, provider di eventi, controller di eventi e consumer di eventi.

Il buffering e la registrazione avvengono nelle *sessioni di traccia eventi* che accettano eventi dai provider e creano file di traccia.

Un *provider di eventi* è un'entità logica che scrive eventi nelle sessioni ETW. Un provider di eventi può essere un'applicazione in modalità utente, un'applicazione gestita, un driver o qualsiasi altra entità software. I provider di eventi registrano con ETW e scrivono gli eventi da diversi punti del codice richiamando l'API di registrazione ETW. A causa della crescente strumentazione degli eventi in molti componenti del sistema operativo, anche un'applicazione o uno scenario semplice in Windows conterrà diversi componenti che sono provider di eventi.

Un *controller eventi* avvia e arresta le sessioni di traccia eventi e Abilita i provider. Quando un provider di eventi viene abilitato in modo dinamico dall'applicazione del controller eventi, il provider invia gli eventi a una sessione di traccia eventi specifica designata dal controller eventi. Ogni evento inviato dal provider di eventi alla sessione di traccia eventi è costituito da un'intestazione fissa, che include i metadati dell'evento e gli eventuali dati personalizzati aggiuntivi registrati dal provider.

Un *consumer di eventi* è un'applicazione che legge i file di log o che è in ascolto di una sessione di traccia eventi per gli eventi in tempo reale e li elabora. Un esempio di consumer di eventi è Microsoft Network Monitor 3,2, che include la possibilità di leggere e visualizzare i file di log prodotti dalla traccia di rete in Windows 7.

Gli eventi vengono recapitati ai consumer di eventi in ordine cronologico e sono presenti diverse applicazioni consumer di eventi che visualizzano gli eventi in formati specifici. Quando un evento viene registrato in una sessione, ETW aggiunge informazioni aggiuntive all'intestazione dell'evento, inclusi il timestamp, l'ID del processo e del thread, il numero del processore e i dati di utilizzo della CPU del thread di registrazione. Questi dati vengono quindi passati ai consumer di eventi, insieme ai dati personalizzati inclusi nel provider.

Si prevede che i provider che usano le nuove [API di registrazione eventi](/windows/win32/api/evntprov/nf-evntprov-eventwrite) forniscano un file XML denominato [manifesto dell'evento](../wes/eventschema-schema.md). Questo file fornisce i metadati per definire tutti i dati personalizzati e le informazioni sul layout per gli eventi scritti dal provider. Un'applicazione consumer per utilizzo generico usa quindi le API [Trace Data Helper (TDH)](/windows/win32/api/tdh/) per recuperare i metadati dell'evento, decodificare gli eventi e visualizzarli.

Grazie alla funzionalità di traccia di rete in Windows 7, il lato controller o consumer di eventi include il supporto per la traccia end-to-end, integrato con le esperienze di supporto e diagnostica di Windows generali. Uno scenario definisce una raccolta di provider di eventi che coinvolgono lo scenario. Il lato controller o consumer di eventi definisce gli scenari (contesti) in cui è possibile usare la traccia, inclusi i provider pertinenti per gli scenari specificati tra i componenti di rete. Il lato del provider di eventi include eventi di traccia di rete standardizzati di diversi componenti nello stack di rete, che possono essere correlati tramite ID attività ETW. I provider utilizzano uno schema di rete comune che standardizza l'utilizzo di concetti ETW quali parole chiave, livelli, attività e codici operativi. Lo schema definisce anche eventi comuni per molti componenti di rete, ad esempio eventi di errore, eventi di eliminazione di pacchetti, eventi dello schema ed eventi di transizione di stato.

 

 