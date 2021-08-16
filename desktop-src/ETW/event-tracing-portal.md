---
description: Questa documentazione è per le applicazioni in modalità utente che vogliono usare ETW. Per informazioni sulla strumentazione dei driver di dispositivo eseguiti in modalità kernel, vedere Traccia software WPP e Aggiunta di traccia eventi ai driver Kernel-Mode in Windows Driver Kit (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Event Tracing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908e935d48749d80e5b2cfe237efeed5413c839157e53b489f4857c0349b4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070221"
---
# <a name="event-tracing"></a>Event Tracing

## <a name="purpose"></a>Scopo

Traccia eventi per Windows (ETW) offre ai programmatori di applicazioni la possibilità di avviare e arrestare sessioni di traccia eventi, instrumentare un'applicazione per fornire eventi di traccia e utilizzare gli eventi di traccia. Gli eventi di traccia contengono un'intestazione di evento e dati definiti dal provider che descrivono lo stato corrente di un'applicazione o di un'operazione. È possibile usare gli eventi per eseguire il debug di un'applicazione ed eseguire l'analisi della capacità e delle prestazioni.

Questa documentazione è per le applicazioni in modalità utente che vogliono usare ETW. Per informazioni sulla strumentazione dei driver di dispositivo eseguiti in modalità kernel, vedere [Traccia software WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) e Aggiunta di traccia eventi ai driver [Kernel-Mode](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in Windows Driver Kit (WDK).

## <a name="where-applicable"></a>Se applicabile

Usare ETW quando si vuole instrumentare l'applicazione, registrare eventi utente o kernel in un file di log e utilizzare gli eventi da un file di log o in tempo reale.

## <a name="developer-audience"></a>Sviluppatori

ETW è progettato per sviluppatori C e C++ che scrivono applicazioni in modalità utente.

## <a name="run-time-requirements"></a>Requisiti di runtime

ETW è incluso in Microsoft Windows 2000 e versioni successive. Per informazioni sui sistemi operativi necessari per usare una funzione specifica, vedere la sezione Requisiti della documentazione relativa alla funzione.

## <a name="process-etw-traces-in-net-code"></a>Elaborare tracce ETW nel codice .NET

È possibile usare [l'API TraceProcessing .NET](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) per analizzare le tracce ETW per le applicazioni e altri componenti software. Questa API viene usata internamente in Microsoft per analizzare i dati ETW prodotti dal sistema di progettazione Windows e viene usata anche per alimentare diverse tabelle in [Windows analizzatore prestazioni](/windows-hardware/test/wpt/windows-performance-analyzer). Questa API è disponibile come pacchetto NuGet.

Per altre informazioni, vedi [questo articolo](/windows/apps/trace-processing/overview).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                     | Descrizione                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Novità della traccia eventi](what-s-new-in-event-tracing.md)<br/> | Nuove funzionalità aggiunte a Traccia eventi in ogni versione.<br/>          |
| [Informazioni sulla traccia eventi](about-event-tracing.md)<br/>                 | Informazioni generali sulla traccia eventi.<br/>                                |
| [Uso della traccia eventi](using-event-tracing.md)<br/>                 | Argomenti relativi alle attività che descrivono come usare l'API ETW.<br/>               |
| [Informazioni di riferimento sulla traccia eventi](event-tracing-reference.md)<br/>         | Descrizioni dettagliate delle funzioni ETW e di altri elementi di programmazione. <br/> |



 

 

 
