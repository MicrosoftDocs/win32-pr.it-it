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
# <a name="memory-management-tracing-events"></a><span data-ttu-id="7749c-103">Eventi di traccia di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="7749c-103">Memory Management Tracing Events</span></span>

<span data-ttu-id="7749c-104">In questa sezione vengono descritte le informazioni dettagliate relative a specifici eventi di traccia della gestione della memoria.</span><span class="sxs-lookup"><span data-stu-id="7749c-104">This section describes detailed information on specific Memory management tracing event details.</span></span>

<span data-ttu-id="7749c-105">La traccia di gestione della memoria è una funzionalità di risoluzione dei problemi che può essere abilitata nei file binari finali per tracciare determinati eventi di gestione della memoria con un sovraccarico minimo.</span><span class="sxs-lookup"><span data-stu-id="7749c-105">Memory management tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain memory management events with minimal overhead.</span></span> <span data-ttu-id="7749c-106">Questa funzionalità consente di migliorare le funzionalità di diagnostica per gli sviluppatori e il supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="7749c-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="7749c-107">Traccia eventi di gestione della memoria supporta la traccia dell'allocazione dell'heap, della riallocazione e delle operazioni gratuite</span><span class="sxs-lookup"><span data-stu-id="7749c-107">Memory management event tracing supports tracing heap allocation, reallocation, and free operations.</span></span>

<span data-ttu-id="7749c-108">Traccia eventi di gestione della memoria usa Event Tracing for Windows (ETW), una funzionalità di traccia a utilizzo generale e ad alta velocità fornita dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7749c-108">Memory management event tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="7749c-109">ETW fornisce un meccanismo di traccia per gli eventi generati da applicazioni in modalità utente e driver di dispositivo in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="7749c-109">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="7749c-110">ETW può abilitare e disabilitare la registrazione in modo dinamico, semplificando l'esecuzione di analisi dettagliate negli ambienti di produzione senza richiedere riavvii o riavvii di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="7749c-110">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="7749c-111">La traccia eventi di gestione della memoria con ETW è supportata in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7749c-111">Memory management event tracing using ETW is supported on Windows 7 , Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="7749c-112">Per informazioni generali su ETW, vedere [migliorare il debug e l'ottimizzazione delle prestazioni con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="7749c-112">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="7749c-113">Nell'elenco seguente vengono fornite informazioni dettagliate per ogni evento di traccia della gestione della memoria.</span><span class="sxs-lookup"><span data-stu-id="7749c-113">The following list provides detailed information for each memory management tracing event.</span></span> <span data-ttu-id="7749c-114">Per ulteriori informazioni su qualsiasi evento, fare clic sul nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7749c-114">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="7749c-115">Nome evento</span><span class="sxs-lookup"><span data-stu-id="7749c-115">Event Name</span></span>                                                  | <span data-ttu-id="7749c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7749c-116">Description</span></span>                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="7749c-117">**\_ \_ Alloc evento heap \_ ETW**</span><span class="sxs-lookup"><span data-stu-id="7749c-117">**ETW\_HEAP\_EVENT\_ALLOC**</span></span>](etw-heap-event-alloc.md)     | <span data-ttu-id="7749c-118">Evento di traccia di gestione della memoria per un'operazione di allocazione heap.</span><span class="sxs-lookup"><span data-stu-id="7749c-118">Memory management tracing event for a heap allocation operation.</span></span>    |
| [<span data-ttu-id="7749c-119">**\_evento heap \_ ETW \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="7749c-119">**ETW\_HEAP\_EVENT\_FREE**</span></span>](etw-heap-event-free.md)       | <span data-ttu-id="7749c-120">Evento di traccia della gestione della memoria per un'operazione di heap disponibile.</span><span class="sxs-lookup"><span data-stu-id="7749c-120">Memory management tracing event for a heap free operation.</span></span>          |
| [<span data-ttu-id="7749c-121">**\_evento heap \_ ETW \_ REALLOC**</span><span class="sxs-lookup"><span data-stu-id="7749c-121">**ETW\_HEAP\_EVENT\_REALLOC**</span></span>](etw-heap-event-realloc.md) | <span data-ttu-id="7749c-122">Evento di traccia della gestione della memoria per un'operazione di riallocazione dell'heap.</span><span class="sxs-lookup"><span data-stu-id="7749c-122">Memory management tracing event for a heap re-allocation operation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7749c-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7749c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7749c-124">Migliorare il debug e la regolazione delle prestazioni con ETW</span><span class="sxs-lookup"><span data-stu-id="7749c-124">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
