---
description: 'Altre informazioni su: Eventi di traccia di gestione della memoria'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Eventi di traccia di gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb395082d46ddd668cbb91ee396f211a4055472f49682ab75efc90cedca7ad5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809008"
---
# <a name="memory-management-tracing-events"></a>Eventi di traccia di gestione della memoria

In questa sezione vengono descritte informazioni dettagliate su specifici dettagli degli eventi di traccia della gestione della memoria.

La traccia di gestione della memoria è una funzionalità di risoluzione dei problemi che può essere abilitata nei file binari per la vendita al dettaglio per tracciare determinati eventi di gestione della memoria con un sovraccarico minimo. Questa funzionalità offre funzionalità di diagnostica migliori per gli sviluppatori e il supporto tecnico del prodotto. La traccia degli eventi di gestione della memoria supporta l'allocazione dell'heap di traccia, la riallocazione e le operazioni gratuite.

La traccia eventi di gestione della memoria usa Event Tracing for Windows (ETW), una funzionalità di traccia ad alta velocità per utilizzo generico fornita dal sistema operativo. ETW fornisce un meccanismo di traccia per gli eventi generati dalle applicazioni in modalità utente e dai driver di dispositivo in modalità kernel. ETW può abilitare e disabilitare la registrazione in modo dinamico, semplificando l'esecuzione di analisi dettagliate negli ambienti di produzione senza richiedere riavvii o riavvii dell'applicazione. La traccia degli eventi di gestione della memoria con ETW è supportata in Windows 7, Windows Server 2008 R2 e versioni successive. Per informazioni generali su ETW, vedere [Migliorare il debug e l'ottimizzazione delle prestazioni con ETW.](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

Nell'elenco seguente vengono fornite informazioni dettagliate per ogni evento di traccia di gestione della memoria. Per altre informazioni su qualsiasi evento, fare clic sul nome dell'evento.



| Nome evento                                                  | Descrizione                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**ALLOCAZIONE \_ DI EVENTI HEAP \_ \_ ETW**](etw-heap-event-alloc.md)     | Evento di traccia di gestione della memoria per un'operazione di allocazione heap.    |
| [**ETW \_ HEAP \_ EVENT \_ FREE**](etw-heap-event-free.md)       | Evento di traccia di gestione della memoria per un'operazione di memoria libera dell'heap.          |
| [**\_RIALLOCARE GLI EVENTI HEAP \_ \_ ETW**](etw-heap-event-realloc.md) | Evento di traccia di gestione della memoria per un'operazione di riallocazione dell'heap. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Migliorare il debug e la regolazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
