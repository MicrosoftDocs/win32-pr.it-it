---
description: 'Altre informazioni su: eventi di traccia di gestione della memoria'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Eventi di traccia di gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319452"
---
# <a name="memory-management-tracing-events"></a>Eventi di traccia di gestione della memoria

In questa sezione vengono descritte le informazioni dettagliate relative a specifici eventi di traccia della gestione della memoria.

La traccia di gestione della memoria è una funzionalità di risoluzione dei problemi che può essere abilitata nei file binari finali per tracciare determinati eventi di gestione della memoria con un sovraccarico minimo. Questa funzionalità consente di migliorare le funzionalità di diagnostica per gli sviluppatori e il supporto tecnico. Traccia eventi di gestione della memoria supporta la traccia dell'allocazione dell'heap, della riallocazione e delle operazioni gratuite

Traccia eventi di gestione della memoria usa Event Tracing for Windows (ETW), una funzionalità di traccia a utilizzo generale e ad alta velocità fornita dal sistema operativo. ETW fornisce un meccanismo di traccia per gli eventi generati da applicazioni in modalità utente e driver di dispositivo in modalità kernel. ETW può abilitare e disabilitare la registrazione in modo dinamico, semplificando l'esecuzione di analisi dettagliate negli ambienti di produzione senza richiedere riavvii o riavvii di applicazioni. La traccia eventi di gestione della memoria con ETW è supportata in Windows 7, Windows Server 2008 R2 e versioni successive. Per informazioni generali su ETW, vedere [migliorare il debug e l'ottimizzazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

Nell'elenco seguente vengono fornite informazioni dettagliate per ogni evento di traccia della gestione della memoria. Per ulteriori informazioni su qualsiasi evento, fare clic sul nome dell'evento.



| Nome evento                                                  | Descrizione                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**\_ \_ Alloc evento heap \_ ETW**](etw-heap-event-alloc.md)     | Evento di traccia di gestione della memoria per un'operazione di allocazione heap.    |
| [**\_evento heap \_ ETW \_ gratuito**](etw-heap-event-free.md)       | Evento di traccia della gestione della memoria per un'operazione di heap disponibile.          |
| [**\_evento heap \_ ETW \_ REALLOC**](etw-heap-event-realloc.md) | Evento di traccia della gestione della memoria per un'operazione di riallocazione dell'heap. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Migliorare il debug e la regolazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
