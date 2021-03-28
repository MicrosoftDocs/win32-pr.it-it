---
description: Questa documentazione è destinata alle applicazioni in modalità utente che desiderano utilizzare ETW. Per informazioni sulla strumentazione dei driver di dispositivo eseguiti in modalità kernel, vedere la pagina relativa alla traccia del software WPP e aggiunta della traccia eventi ai driver Kernel-Mode in Windows Driver Kit (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Event Tracing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349326"
---
# <a name="event-tracing"></a>Event Tracing

## <a name="purpose"></a>Scopo

Event Tracing for Windows (ETW) fornisce ai programmatori di applicazioni la possibilità di avviare e arrestare le sessioni di traccia eventi, instrumentare un'applicazione per fornire eventi di traccia e utilizzare gli eventi di traccia. Gli eventi di traccia contengono un'intestazione di evento e dati definiti dal provider che descrivono lo stato corrente di un'applicazione o di un'operazione. È possibile utilizzare gli eventi per eseguire il debug di un'applicazione ed eseguire l'analisi delle prestazioni e della capacità.

Questa documentazione è destinata alle applicazioni in modalità utente che desiderano utilizzare ETW. Per informazioni sulla strumentazione dei driver di dispositivo eseguiti in modalità kernel, vedere la pagina relativa alla [traccia del software WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) e [aggiunta della traccia eventi ai driver Kernel-Mode](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in Windows Driver Kit (WDK).

## <a name="where-applicable"></a>Se applicabile

Utilizzare ETW quando si desidera instrumentare l'applicazione, registrare eventi utente o kernel in un file di log e utilizzare eventi da un file di log o in tempo reale.

## <a name="developer-audience"></a>Sviluppatori

ETW è progettato per gli sviluppatori C e C++ che scrivono applicazioni in modalità utente.

## <a name="run-time-requirements"></a>Requisiti di runtime

ETW è incluso in Microsoft Windows 2000 e versioni successive. Per informazioni sui sistemi operativi necessari per usare una funzione specifica, vedere la sezione requisiti della documentazione relativa alla funzione.

## <a name="process-etw-traces-in-net-code"></a>Elaborare tracce ETW nel codice .NET

È possibile usare l' [API .NET TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) per analizzare le tracce ETW per le applicazioni e altri componenti software. Questa API viene utilizzata internamente in Microsoft per analizzare i dati ETW prodotti dal sistema ingegneristico Windows e viene inoltre utilizzata per potenziare diverse tabelle in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer). Questa API è disponibile come pacchetto NuGet.

Per altre informazioni, vedi [questo articolo](/windows/apps/trace-processing/overview).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                     | Descrizione                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Novità della traccia eventi](what-s-new-in-event-tracing.md)<br/> | Nuove funzionalità aggiunte alla traccia eventi in ogni versione.<br/>          |
| [Informazioni sulla traccia eventi](about-event-tracing.md)<br/>                 | Informazioni generali sull'analisi degli eventi.<br/>                                |
| [Utilizzo di traccia eventi](using-event-tracing.md)<br/>                 | Argomenti correlati alle attività che descrivono come usare l'API ETW.<br/>               |
| [Riferimento traccia eventi](event-tracing-reference.md)<br/>         | Descrizione dettagliata delle funzioni ETW e di altri elementi di programmazione. <br/> |



 

 

 
