---
title: Eventi Windows
description: Gli eventi vengono in genere utilizzati per la risoluzione dei problemi relativi al software di driver e applicazioni. Prima di Windows Vista, è possibile utilizzare Event Tracing for Windows (ETW) o la registrazione degli eventi per registrare gli eventi. In Windows Vista è stato introdotto un nuovo modello di eventi per unificare sia l'API Event Tracing for Windows (ETW) che l'API registro eventi di Windows. Windows 10 introduce TraceLogging che si basa su ETW e fornisce un modo semplificato per instrumentare il codice per gli sviluppatori nativi, .NET e WinRT.
ms.assetid: c10baa8d-50b9-4fda-89d0-d00b1d9f5404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3d22580c38e45d06f5362e99626642eebdfe20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046693"
---
# <a name="windows-events"></a>Eventi Windows

Gli eventi vengono in genere utilizzati per la risoluzione dei problemi relativi al software di driver e applicazioni.

-   Prima di Windows Vista, è possibile utilizzare [Event Tracing for Windows](/windows/desktop/ETW/event-tracing-portal) (ETW) o la [registrazione](/windows/desktop/EventLog/event-logging) degli eventi per registrare gli eventi.
-   In Windows Vista è stato introdotto un nuovo modello di eventi per unificare sia l'API [Event Tracing for Windows](/windows/desktop/ETW/event-tracing-portal) (ETW) che l'API [registro eventi di Windows](/windows/desktop/WES/windows-event-log) .
-   Windows 10 introduce [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) che si basa su ETW e fornisce un modo semplificato per instrumentare il codice per gli sviluppatori nativi, .NET e WinRT.

Il nuovo modello [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) consente di includere dati strutturati con eventi, correlare gli eventi e non richiede un file XML del manifesto di strumentazione separato.

Il modello di Windows Vista utilizza un manifesto XML per definire gli eventi che si desidera pubblicare. Gli eventi possono essere pubblicati in un canale o in una sessione ETW. È possibile pubblicare gli eventi nei seguenti tipi di canali: amministratore, operativo, analitico e debug. Se si utilizza solo ETW per abilitare il server di pubblicazione, non è necessario specificare i canali nel manifesto. Per informazioni dettagliate sulla scrittura di un manifesto, vedere [scrittura di un manifesto di strumentazione](/windows/desktop/WES/writing-an-instrumentation-manifest)e per informazioni sui canali, vedere Definizione di [canali](/windows/desktop/WES/defining-channels).

Per registrare l'autore di eventi e pubblicare gli eventi, usare l'API ETW. Per informazioni dettagliate, vedere [fornire eventi](/windows/desktop/ETW/providing-events) e [sviluppare un provider](/windows/desktop/WES/developing-a-provider). Se sono abilitati, l'autore dell'evento scriverà automaticamente gli eventi nei canali specificati nel manifesto.

Se si desidera controllare gli eventi pubblicati da un autore di eventi a un livello di granularità più preciso, utilizzare l'API ETW. Se, ad esempio, il manifesto definisce gli eventi di scrittura e di lettura, è possibile abilitare solo gli eventi di scrittura. Un evento può inoltre specificare un valore di livello, ad esempio avviso o errore, in modo che sia possibile limitare gli eventi scritti a quelli che specificano il livello di errore. Per informazioni dettagliate, vedere [controllo delle sessioni di traccia eventi](/windows/desktop/ETW/controlling-event-tracing-sessions). Gli eventi vengono scritti nel file di log della sessione.

Per l'utilizzo di eventi è necessario recuperare gli eventi da un canale di eventi, un file di log eventi (file con estensione evtx o evt), un file di traccia (file con estensione ETL) o una sessione ETW in tempo reale. Per utilizzare gli eventi da un file di traccia ETW o da una sessione ETW in tempo reale, utilizzare le funzioni TDH (Trace Data Helper) in ETW per utilizzare gli eventi. È anche possibile usare TDH per leggere i metadati dell'evento. Per informazioni dettagliate, vedere [utilizzo degli eventi](/windows/desktop/ETW/consuming-events). Per utilizzare gli eventi da un canale di eventi o da un file di log eventi, utilizzare le funzioni del registro eventi di Windows per eseguire query o sottoscrivere eventi. Per ulteriori informazioni, vedere [esecuzione di query per eventi](/windows/desktop/WES/querying-for-events) o [sottoscrizione di eventi](/windows/desktop/WES/subscribing-to-events).

Prima di Windows Vista, è necessario utilizzare [Event Tracing for Windows](/windows/desktop/ETW/event-tracing-portal) o la [registrazione degli eventi](/windows/desktop/EventLog/event-logging) per pubblicare e utilizzare gli eventi.

 

 